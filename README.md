# quiz-notes · 考研笔记

单文件 HTML PWA 应用，用于考研复习的笔记、刷题、计时与数据管理。浏览器直接打开即可运行，无需构建。

## 项目结构

```
quiz-notes/
├── quiz_v4-2(1).html   # 整个应用（HTML+CSS+JS 内联，约 405KB）
└── README.md
```

## 功能（底部 5 个 Tab）

| Tab | 功能 |
|-----|------|
| 📒 笔记 | 笔记记录，支持 Markdown |
| ⏱ 计时 | 学习计时与时长统计 |
| 📊 仪表盘 | 数据可视化 |
| 📝 刷题 | 题库练习、错题管理 |
| ⚙ 设置 | 主题切换、同步配置 |

## 技术栈

- 纯前端单文件，无构建工具
- PWA + Service Worker 离线缓存
- localStorage 持久化（key: `kaoyan_farm_v6`）
- marked.js（CDN）渲染 Markdown
- 3 套主题：学院蓝 / Obsidian 蓝灰 / Modern 橄榄绿

## Claude 访问方式

仓库公开，可直接访问：

- 仓库：https://github.com/gangshangka/quiz-notes
- HTML 源文件：https://raw.githubusercontent.com/gangshangka/quiz-notes/main/quiz_v4-2(1).html

## 本地运行

浏览器打开 `quiz_v4-2(1).html` 即可。
