# quiz-notes · 考研笔记与学习管理

单文件 HTML PWA 应用，为考研复习提供笔记、刷题、专注计时与可视化数据管理。整个应用是一个独立的 `.html` 文件（约 405KB，9300+ 行），浏览器直接打开即可运行，无需任何构建步骤。

## 项目结构

```
quiz-notes/
├── quiz_v4-2(1).html   # 整个应用（HTML + CSS + JS 内联，约 405KB）
└── README.md           # 本说明文件
```

## 文件内部分区（按行号）

| 行号区间 | 内容 |
|----------|------|
| 1–67 | `<head>` 与 CSS 变量基础定义（颜色、圆角、间距、字体） |
| 55–85 | 三套主题变量：学院蓝（默认）/ Obsidian 蓝灰 / Modern 橄榄绿 |
| 86–1253 | 通用组件样式：按钮、卡片、Toast、底栏、编辑器、模态框等 |
| 1254–3183 | 刷题模块（Quiz）专属样式：Obsidian 浅色美学、题卡、地图、树视图 |
| 2593–3123 | `<body>` 主体：5 个主面板（main-panel）+ 编辑器 overlay |
| 3125–3160 | 笔记编辑器 overlay（全屏覆盖层） |
| 3162–3179 | 底部导航栏（5 个 Tab） |
| 3181–3183 | Toast 容器、城市模态框容器 |
| 3184 | 引入 `marked.min.js`（CDN，用于 Markdown 渲染） |
| 3185–末尾 | 主 `<script>` 块（全部业务逻辑） |

## 顶层 DOM 结构

```
<body>
├── .main-panel#panel-notes       笔记面板
├── .main-panel#panel-timer       计时面板
├── .main-panel#panel-dashboard   仪表盘面板（默认 active）
├── .main-panel#panel-quiz        刷题面板
├── .main-panel#panel-settings    设置面板
├── .editor-overlay#editorOverlay 笔记编辑器（全屏覆盖层）
├── .bottom-nav                   底部导航（5 个 Tab）
├── .toast-container              Toast 消息容器
└── #cityModalContainer           城市建筑详情模态框
```

## 五大功能模块

### 1. 📒 笔记（notes）
- 卡片式笔记列表，全屏编辑器 overlay
- Markdown 实时预览（marked.js）
- 工具栏快捷插入：粗体、斜体、代码、H3、列表、链接、单词组
- 自动统计字数、时间戳

### 2. ⏱ 计时（timer）
- 专注计时器（开始/暂停/停止），按学科归类
- 今日建设指令（基于考研倒计时阶段）
- 各任务时长占比饼图（Canvas 绘制）
- 学习城市 · 时长生长（Canvas 建筑可视化）
- 城市成就地图（点击建筑查看详情）

### 3. 📊 仪表盘（dashboard，默认 Tab）
- 今日作战室：考研倒计时 + 当日任务
- 333 四城区建设进度（教育学原理/中教史/外教史/教心）
- 每日签到 + 连续天数
- 角色等级系统（学徒→初学者→进阶者→高手→大师）
- 今日概览统计
- 物理章节 / 教育综合 / 英语学习 / 知识闯关卡片

### 4. 📝 刷题（quiz）
- 题库地图（按学科分组、网格/树状视图切换）
- 题目卡片（单选/多选/填空/简答），支持题干高亮、下划线标记
- 答题反馈、错题管理、收藏夹（双击题目收藏）
- 标签系统（重点/易错/高频/待复习 + 自定义）
- 题库管理：粘贴生成、JSON 导入、合并、删除
- AI 反馈解析（parseAIFeedback）
- 沉浸式模式（移动端滚动聚焦）

### 5. ⚙ 设置（settings）
- 界面调节：字号、密度、主题、玻璃效果、PC 布局
- 功能开关：背景音乐、音效、电脑版
- 数据留存：导出/导入整包 JSON、安装 PWA
- 题库管理（折叠卡）：列表、合并、删除、标签编辑
- 云端同步（折叠卡）：GitHub / Gitee 双通道、自动推送

## JavaScript 架构

### 数据持久化
- **存储 key**：`localStorage['kaoyan_farm_v6']`
- **数据结构** `DEF()` (line 3586)：
  ```
  {
    notes[], focusSessions[], totalFocusSec,
    physicsChapters[], eduDaily{}, momoDays{}, readingDays{},
    totalReading, score, scoreLog[], signDays{}, signStreak,
    streakMomo, lastMomoDate,
    quizBanks[], quizProgress{},
    favoriteQuestions[], favoriteTags[],
    examPlan{ targetDate, mainSubject, cityMode, dailyBuild },
    wordGroups[],
    syncCfg{ ghToken, ghRepo, ghPath, geeToken, geeRepo, geePath, autoSync },
    settings{ fontSize, density, customSubjects[], glass, music, sfx, lastExportAt, theme }
  }
  ```
- **存储保护**：`save()` 检测超过 4MB 时调用 `trimOldData()` 自动清理一年前数据
- **全局状态变量**：`A`（应用数据对象），通过 `load()`/`save()` 读写

### 关键常量
| 常量 | 行号 | 说明 |
|------|------|------|
| `K` | 3585 | localStorage 主 key |
| `EXAM_TARGET_DATE` | 3870 | 考研目标日期（2026-12-20） |
| `PLAN_DISTRICTS` | 3872 | 333 四城区配置（学科/建筑/颜色/话题） |
| `PLAN_PHASES` | 3882 | 4 个复习阶段（地基/一轮/二轮/冲刺） |
| `LEVELS` | 4194 | 角色等级配置（5 级，分数阈值） |
| `CITY_COLORS` | 7073 | 城市建筑配色表 |
| `SUBJECT_COLORS` | 7465 | 学科配色表 |
| `LVL_LABEL/LVL_STAR` | 7562/7563 | 建筑等级名称（地基/简装/标准/高级/地标） |
| `CHAR_CFG` | 8189 | 角色形象绘制配置 |
| `SUBJECT_CONFIG` | 8606 | 333 四学科配置（含关键词检测） |
| `EXTRA_SUBJECT_CONFIG` | 8630 | 额外学科（物理/英语）配置 |

### 核心函数分组（按行号）

**数据层（3585–3625）**
`load` / `save` / `trimOldData` / `T` / `TS` / `FMT` / `FMTM` / `ID`

**工具函数（3633–3685）**
`toast` / `esc` / `jse` / `jsArg` / `textVal` / `firstText`

**题干高亮（3636–3684）**
`renderStemWithHighlights` / `applyStemHighlight` / `removeStemHighlight` / `findQuestionById` / `refreshCurrentCardStem`

**题目规范化（3688–3733）**
`normalizeQuizQuestion` / `normalizeQuizBank` / `normalizeAllQuizBanks`

**题目渲染与解析（3841–3889）**
`analysisHtml` / `answerFeedbackHtml` / `getQuizFieldLine` / `getQuizFieldSection`

**考研规划（3889–3997）**
`ensureExamPlan` / `daysUntilExam` / `getPlanPhase` / `dateIndex` / `getTodayDistrict` / `getDistrictBySubject` / `getTodayTopic` / `getTodayFocusSeconds` / `getTodayQuizStats` / `getWrongQuestionCount` / `getWeeklyActiveCount` / `getDailyMissions` / `getTodayBuildPct` / `getDistrictStats` / `markTodayBuild`

**时间与存储（3997–4007）**
`formatDateTime` / `dataSizeText` / `updateRetentionStatus`

**积分与等级（4195–4208）**
`addScore` / `getLevel` / `nextLevel`

**题目解析与渲染（4214–4923）**
`parseQuestions` / `renderQuizCard` / `refreshCardFooter` / `getProgress` / `recordQuizAttempt` / `recalcBankStats`

**收藏与标签（4923–5655）**
`isQuestionFavorited` / `toggleFavoriteByDblClick` / `showTagSelectorForCard` / `toggleFavorite` / `showTagSelector` / `renderFavoriteList` / `renderFavoriteTags`

**刷题进度与沉浸模式（5655–5818）**
`restoreQuizProgress` / `scrollToAndFocus` / `bindFocusMode` / `isMobileQuizViewport` / `setQuizImmersive` / `setupQuizImmersiveObserver`

**题库管理（5818–6165）**
`updateBankSelect` / `showExportModal` / `parseAIFeedback` / `doCopy` / `fallbackCopy` / `promptCopy` / `renderQuizBanks` / `getAllExistingTags` / `updateBankTagEditor` / `buildTagTree` / `countBanksInTree` / `getQuizBankStats`

**刷题地图与轨道（6351–6718）**
`getMainQuest` / `renderQuizTrack` / `renderQuizMap` / `renderBankSelect` / `renderMergeSelects` / `saveQuizProgress`

**笔记编辑器（6796–6929）**
`openNote` / `updateWordCount` / `renderPreview` / `renderNoteList` / `onChipClick` / `onChipDelete` / `updateSubjectUI`

**布局与计时器（7003–7086）**
`applyPCLayout` / `updateTimerUI` / `resetTimerUI` / `updateTimerPanel`

**Canvas 可视化（7086–7880）**
`drawCityMap` / `drawRefinedBuilding` / `lightenColor` / `roundRect` / `showBuildingModal` / `closeBuildingModal` / `getSubjectData` / `getCityData` / `renderPieChart` / `getBuildingLevel` / `renderCityChart` / `drawBuilding`

**同步与仪表盘渲染（7880–8318）**
`loadSyncConfig` / `updateSyncStatus` / `renderCommandCenter` / `renderTimerMission` / `setTimerSubject` / `updateTopBar` / `renderSignGrid` / `renderPhysics` / `updateEdu` / `updateEnglish` / `drawCharacter` / `updateCharacterCard` / `updateDashboard` / `applyZoom` / `applyDensity`

**学科检测与分组（8606–末尾）**
`detectSubjectId` / `getSubjectConfig` / `groupBanksBySubject` / `aggregateStats`

## 技术栈

- **HTML / CSS / JavaScript**：单文件内联，无构建工具、无框架
- **PWA**：Service Worker 离线缓存（缓存 key `kynotes-v2`）
- **localStorage 持久化**：单 key `kaoyan_farm_v6`，上限 4MB，自动清理
- **marked.js**（CDN）：Markdown 渲染
- **Canvas 2D**：城市建筑、饼图、角色形象手绘
- **CSS 变量主题系统**：3 套主题（学院蓝 / Obsidian 蓝灰 / Modern 橄榄绿）
- **同步后端**：GitHub / Gitee（通过个人 Token 推送 JSON 文件）

## Claude 访问方式

仓库为 Public，可直接通过以下方式访问：

- **仓库主页**：https://github.com/gangshangka/quiz-notes
- **HTML 源文件 raw**：https://raw.githubusercontent.com/gangshangka/quiz-notes/main/quiz_v4-2(1).html
  （注：URL 含括号 `(1)`，部分客户端需编码为 `%28%29`）
- **文件树 API**：https://api.github.com/repos/gangshangka/quiz-notes/git/trees/main?recursive=1
- **README raw**：https://raw.githubusercontent.com/gangshangka/quiz-notes/main/README.md

在 Claude.ai 中贴仓库主页链接即可，Claude 会自动读取文件树与 README 理解项目结构。

## 本地运行

浏览器直接打开 `quiz_v4-2(1).html`。推荐 Chrome / Edge / Safari 以支持 PWA 与 Service Worker。
