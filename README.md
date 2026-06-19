# quiz-notes 路 鑰冪爺绗旇涓庡涔犵鐞?
鍗曟枃浠?HTML PWA 搴旂敤锛屼负鑰冪爺澶嶄範鎻愪緵涓€浣撳寲瀛︿範绠＄悊銆傛暣涓簲鐢ㄦ槸涓€涓嫭绔嬬殑 `.html` 鏂囦欢锛堢害 405KB锛?300+ 琛岋級锛孒TML+CSS+JS 鍏ㄩ儴鍐呰仈锛屾祻瑙堝櫒鐩存帴鎵撳紑鍗冲彲杩愯锛屾棤闇€浠讳綍鏋勫缓姝ラ銆?
> 鏈?README 浠?*鍔熻兘瑙掑害**鎾板啓锛岀敤浜庤 AI 鍔╂墜锛堝 Claude锛夌悊瑙ｅ綋鍓嶅姛鑳藉叏璨岋紝鍙備笌鏋舵瀯閲嶆瀯銆佸姛鑳借璁℃垨鍒犲噺鍐崇瓥銆傚綋鍓嶅疄鐜颁负鍗曟枃浠跺師鍨嬶紝瀛樺湪鑱岃矗娣锋潅銆佺姸鎬佺鐞嗘暎涔便€佸彲缁存姢鎬у樊绛夐棶棰橈紝娆㈣繋鎻愬嚭閲嶆瀯鏂规銆?
## 椤圭洰缁撴瀯

```
quiz-notes/
鈹溾攢鈹€ quiz_v4-2(1).html   # 鏁翠釜搴旂敤锛圚TML+CSS+JS 鍐呰仈锛岀害 405KB锛?鈹斺攢鈹€ README.md
```

## 搴旂敤瀹氫綅

闈㈠悜鑰冪爺瀛︾敓锛堢洰鏍?333 鏁欒偛缁煎悎 + 鐗╃悊 + 鑻辫锛夌殑涓汉瀛︿範绠＄悊宸ュ叿锛屾妸**绗旇 / 涓撴敞璁℃椂 / 鍒烽 / 鏁版嵁鍙鍖?/ 娓告垙鍖栨縺鍔?*鏁村悎鍦ㄤ竴涓?PWA 閲岋紝鏀寔绂荤嚎浣跨敤銆佸璁惧鍚屾銆?
## 椤跺眰鏋舵瀯锛堢幇鐘讹級

- **褰㈡€?*锛氬崟鏂囦欢 PWA锛屾棤妗嗘灦銆佹棤鏋勫缓銆佹棤鍚庣
- **鐘舵€?*锛氬叏灞€鍙橀噺 `A`锛堝簲鐢ㄦ暟鎹璞★級锛岄€氳繃 `load()`/`save()` 璇诲啓 localStorage
- **瀛樺偍 key**锛歚localStorage['kaoyan_farm_v6']`锛堝崟 key 瀛樺叏閲?JSON锛?MB 涓婇檺鑷姩娓呯悊锛?- **璺敱**锛? 涓?`<div class="main-panel">` 閫氳繃 `switchMainTab(name)` 鍒囨崲鏄鹃殣锛屾棤 URL 璺敱
- **娓叉煋**锛氱洿鎺ユ搷浣?DOM锛坕nnerHTML / createElement锛夛紝鏃犺櫄鎷?DOM銆佹棤鍝嶅簲寮忕郴缁?- **鍚屾**锛氶€氳繃 GitHub / Gitee Contents API 鎶婃暣涓?JSON 鎺ㄩ€佸埌浠撳簱鏂囦欢锛坆ase64 缂栫爜锛?
## 鍔熻兘妯″潡鍏ㄦ櫙

搴曢儴瀵艰埅 5 涓?Tab锛屽鍔犲叏灞€缂栬緫鍣?overlay 涓庡涓ā鎬佹銆?
### 1. 馃搾 绗旇锛坣otes锛?
**鏍稿績鍔熻兘**
- 绗旇鍒楄〃锛堝崱鐗囧紡锛屾寜鏃堕棿鍊掑簭锛?- 鍏ㄥ睆缂栬緫鍣?overlay锛堣鐩栨暣涓〉闈級
- Markdown 瀹炴椂棰勮锛坢arked.js锛孋DN 鍔犺浇锛?- 宸ュ叿鏍忓揩鎹锋彃鍏ワ細绮椾綋 / 鏂滀綋 / 浠ｇ爜 / H3 / 鏃犲簭/鏈夊簭鍒楄〃 / 閾炬帴 / 鍗曡瘝缁?- 鑷姩缁熻瀛楁暟銆佹椂闂存埑
- 鎸夊绉戝垎绫伙紙chip 鏍囩锛?
**鏁版嵁**锛歚A.notes[]`锛屾瘡鏉″惈 id / title / content / subject / timestamp / wordCount

**鏋舵瀯闂**
- 缂栬緫鍣ㄦ槸鍏ㄥ眬 overlay锛屼笌绗旇鍒楄〃鑰﹀悎
- Markdown 娓叉煋渚濊禆 CDN锛岀绾垮満鏅け璐?- 鏃犲叏鏂囨悳绱€佹棤鏍囩绛涢€夈€佹棤鐩綍鏍?
### 2. 鈴?璁℃椂锛坱imer锛?
**鏍稿績鍔熻兘**
- 涓撴敞璁℃椂鍣紙寮€濮?鏆傚仠/鍋滄锛夛紝鎸夊绉戝綊绫昏褰?- 浠婃棩寤鸿鎸囦护锛堝熀浜庤€冪爺鍊掕鏃堕樁娈佃嚜鍔ㄧ敓鎴愶級
- 鍚勪换鍔℃椂闀垮崰姣旈ゼ鍥撅紙Canvas 鎵嬬粯锛?- **瀛︿範鍩庡競 路 鏃堕暱鐢熼暱**锛氭妸瀛︿範鏃堕暱鍙鍖栨垚鍩庡競寤虹瓚锛圕anvas锛夛紝寤虹瓚绛夌骇 = 鏃堕暱
- 鍩庡競鎴愬氨鍦板浘锛堢偣鍑诲缓绛戞煡鐪嬭鎯呮ā鎬佹锛?
**鏁版嵁**锛歚A.focusSessions[]`銆乣A.totalFocusSec`銆乣A.examPlan.dailyBuild{}`

**寤虹瓚绛夌骇鏄犲皠**锛坄LVL_LABEL`锛夛細鍦板熀 鈫?绠€瑁?鈫?鏍囧噯 鈫?楂樼骇 鈫?鍦版爣锛? 绾э級

**鏋舵瀯闂**
- Canvas 缁樺埗浠ｇ爜鍐楅暱锛?00+ 琛岋級锛屾湭鎶借薄
- 鍩庡競鍙鍖栦笌璁℃椂鍣ㄩ€昏緫娣峰湪涓€璧?- "浠婃棩寤鸿鎸囦护"绠楁硶纭紪鐮佸湪 `renderTimerMission()`

### 3. 馃搳 浠〃鐩橈紙dashboard锛岄粯璁?Tab锛?
**鏍稿績鍔熻兘**
- **浠婃棩浣滄垬瀹?*锛氳€冪爺鍊掕鏃?+ 褰撴棩浠诲姟 + 璧勬枡閿氱偣鎻愮ず
- **333 鍥涘煄鍖哄缓璁?*锛氭妸 333 鏁欒偛缁煎悎鍥涢棬瀛︾锛堟暀鑲插鍘熺悊/涓暀鍙?澶栨暀鍙?鏁欏績锛夋槧灏勬垚鍥涗釜鍩庡尯锛屾寜棰樺簱鍚嶅叧閿瘝鑷姩褰掔被
- **姣忔棩绛惧埌**锛氳繛缁鍒板ぉ鏁?+ 绉垎濂栧姳
- **瑙掕壊绛夌骇绯荤粺**锛氱Н鍒?鈫?绛夌骇锛堝寰掆啋鍒濆鑰呪啋杩涢樁鑰呪啋楂樻墜鈫掑ぇ甯堬紝5 绾э級锛孋anvas 缁樺埗澶村儚
- **浠婃棩姒傝**锛氫粖鏃ヤ笓娉ㄥ垎閽?/ 绉垎 / 鐗╃悊杩涘害 / 鏁欒偛缁煎悎 / 澧ㄥⅷ鍗曡瘝
- **瀛︾鍗＄墖**锛氱墿鐞嗙珷鑺?/ 鏁欒偛缁煎悎 / 鑻辫瀛︿範 / 鐭ヨ瘑闂叧

**澶嶄範闃舵瑙勫垝**锛坄PLAN_PHASES`锛屾寜璺濊€冭瘯澶╂暟鍒掑垎锛夛細
- 0鈥?5 澶╋細鍐插埡灏侀《锛堢湡棰樺鍗枫€侀敊棰樹慨澶嶃€佺瓟棰樻ā鏉匡級
- 36鈥?0 澶╋細浜岃疆鍔犲浐锛堥珮棰戣€冪偣銆佺畝绛旀鏋躲€侀敊棰樺洖鐐夛級
- 81鈥?50 澶╋細涓€杞缓璁撅紙鏁欐潗绔犺妭銆佽€冪翰瑕嗙洊銆佸熀纭€棰樺簱锛?- 150+ 澶╋細鍦板熀閾鸿锛堝缓绔嬬煡璇嗗湴鍥惧拰姣忔棩鑺傚锛?
**鏁版嵁**锛歚A.score` / `A.scoreLog[]` / `A.signDays{}` / `A.signStreak` / `A.examPlan`

**鏋舵瀯闂**
- 浠〃鐩樻壙鎷呬簡杩囧鑱岃矗锛堜綔鎴樺 + 绛惧埌 + 瑙掕壊 + 姒傝 + 瀛︾鍗＄墖锛?- "鍥涘煄鍖?姒傚康鑰﹀悎浜嗗绉戦厤缃€佸缓绛戝彲瑙嗗寲鍜岃繘搴︾粺璁?- 瑙掕壊绛夌骇銆佺鍒般€佺Н鍒嗘暎钀藉湪澶氫釜鍑芥暟涓?
### 4. 馃摑 鍒烽锛坬uiz锛?
**鏍稿績鍔熻兘**
- **棰樺簱鍦板浘**锛氭寜瀛︾鍒嗙粍锛岀綉鏍?鏍戠姸瑙嗗浘鍒囨崲锛屾樉绀鸿繘搴︽潯涓庣姸鎬侊紙宸叉帉鎻?瀛︿範涓級
- **棰樼洰鍗＄墖**锛氭敮鎸佸崟閫?澶氶€?濉┖/绠€绛?鍒ゆ柇棰?- **棰樺共楂樹寒**锛氶€変腑棰樺共鏂囧瓧鍙爣璁颁负楂樹寒鎴栦笅鍒掔嚎锛屾寔涔呭寲
- **绛旈鍙嶉**锛氬閿欏垽鏂€佺瓟妗堟樉绀恒€佽В鏋愬睍绀?- **绠€绛旈鍏抽敭璇嶅尮閰?*锛氭寜鍏抽敭璇嶅尮閰嶅害缁欏垎锛坄matchPct`锛?- **閿欓绠＄悊**锛氳嚜鍔ㄨ褰曢敊棰橈紝鍙噸鏂扮粌涔?- **鏀惰棌澶?*锛氬弻鍑婚鐩敹钘忥紝鍙墦鏍囩锛堥噸鐐?鏄撻敊/楂橀/寰呭涔?+ 鑷畾涔夛級
- **棰樺簱绠＄悊**锛?  - 绮樿创鏂囨湰鑷姩瑙ｆ瀽鐢熸垚棰樺簱锛坄parseQuestions`锛屾敮鎸?`銆愰鍨嬨€慲 + 绛旀/瑙ｆ瀽/鍏抽敭璇?鐭ヨ瘑鐐?闅惧害/鏉ユ簮 鍒嗚妭锛?  - JSON 鏂囦欢瀵煎叆
  - 棰樺簱鍚堝苟銆佸垹闄ゃ€佹爣绛剧紪杈?- **AI 鍙嶉瑙ｆ瀽**锛歚parseAIFeedback` 瑙ｆ瀽 AI 杩斿洖鐨勮瘎鍒嗕笌鍙嶉
- **娌夋蹈寮忔ā寮?*锛氱Щ鍔ㄧ婊氬姩鏃惰嚜鍔ㄨ仛鐒﹀綋鍓嶉鐩?
**棰樼洰鏁版嵁缁撴瀯**锛堣鑼冨寲鍚庯級锛?```
question = {
  id, type ('single'|'multiple'|'fill'|'short'|'judge'),
  stem, options[{label,text}], answer, analysis,
  keywords, knowledgePoint, difficulty, source
}
```

**杩涘害鏁版嵁**锛歚A.quizProgress[bankId][qid] = { status, answer, ts, notes, aiFeedback, aiScore, matchPct, highlights[] }`

**鏋舵瀯闂**
- 棰樼洰瑙ｆ瀽鍣?`parseQuestions` 鏄竴涓ぇ鍑芥暟锛?00+ 琛岋級锛岀‖缂栫爜鏍煎紡
- 鏀惰棌绯荤粺涓庢爣绛剧郴缁熻€﹀悎锛坄toggleFavoriteByDblClick` 瑙﹀彂 `showTagSelectorForCard`锛?- 绛旈銆佺Н鍒嗐€佽繘搴︺€佹覆鏌撲簰鐩歌皟鐢紝渚濊禆鍏崇郴娣蜂贡
- AI 鍙嶉瑙ｆ瀽锛坄parseAIFeedback`锛夎€﹀悎鍦?UI 灞?
### 5. 鈿?璁剧疆锛坰ettings锛?
**鏍稿績鍔熻兘**
- **鐣岄潰璋冭妭**锛氬瓧鍙凤紙灏?鏍囧噯/澶э級銆佸瘑搴︼紙绱у噾/鏍囧噯/瀹芥澗锛夈€佷富棰樺垏鎹€佺幓鐠冩晥鏋溿€丳C 甯冨眬
- **涓婚绯荤粺**锛? 濂楅璁撅紙瀛﹂櫌钃?claude / Obsidian 钃濈伆 / Modern 姗勬缁匡級锛岄€氳繃 CSS 鍙橀噺鍒囨崲
- **鍔熻兘寮€鍏?*锛氳儗鏅煶涔愩€侀煶鏁堛€佺數鑴戠増甯冨眬
- **鏁版嵁鐣欏瓨**锛氬鍑烘暣鍖?JSON / 瀵煎叆鏁村寘 JSON / 瀹夎 PWA 鍒颁富灞?- **棰樺簱绠＄悊**锛堟姌鍙犲崱锛夛細鍒楄〃銆佸悎骞躲€佸垹闄ゃ€佹爣绛剧紪杈戙€丣SON 瀵煎叆
- **浜戠鍚屾**锛堟姌鍙犲崱锛夛細
  - GitHub 鍚屾锛圱oken + 浠撳簱鍚?+ 鏂囦欢璺緞锛?  - Gitee 鍚屾锛圱oken + 浠撳簱鍚?+ 鏂囦欢璺緞锛?  - 鑷姩鎺ㄩ€佸紑鍏筹紙淇濆瓨鍚庤嚜鍔?push锛?  - 鎵嬪姩鎺ㄩ€?/ 鎷夊彇

**鍚屾瀹炵幇**锛氶€氳繃 GitHub/Gitee Contents API锛屾妸鏁翠釜 `A` 瀵硅薄 base64 缂栫爜鍚庡啓鍏ユ寚瀹氫粨搴撴枃浠讹紝鎷夊彇鏃跺弽鍚戣В鐮併€傚啿绐佸鐞嗙畝鍗曡鐩栥€?
**鏋舵瀯闂**
- 璁剧疆闈㈡澘鎵挎媴浜嗘暟鎹鐞嗐€侀搴撶鐞嗐€佸悓姝ラ厤缃笁绫讳笉鐩稿叧鑱岃矗
- 鍚屾閫昏緫锛坧ush/pull锛変笌 UI 鐘舵€併€侀敊璇鐞嗚€﹀悎
- 鏃犲啿绐佽В鍐虫満鍒讹紝澶氳澶囧悓姝ュ彲鑳戒涪鏁版嵁

## 璺ㄦā鍧楀叡浜満鍒?
### 绉垎绯荤粺
- `addScore(amt, reason)`锛氱粺涓€鍏ュ彛锛岃褰曞埌 `A.scoreLog[]`
- 瑙﹀彂鐐癸細绛旈姝ｇ‘锛?3锛夈€佺畝绛斿叧閿瘝鍖归厤锛堟寜鐧惧垎姣旓級銆佺鍒般€佹瘡鏃ュ缓璁?- 绛夌骇闃堝€硷細`LEVELS = [{lv:1,瀛﹀緬,0}, {lv:2,鍒濆鑰?100}, {lv:3,杩涢樁鑰?300}, {lv:4,楂樻墜,600}, {lv:5,澶у笀,1000}]`

### 鑰冪爺瑙勫垝绯荤粺
- 鐩爣鏃ユ湡锛歚2026-12-20`锛堢‖缂栫爜甯搁噺 `EXAM_TARGET_DATE`锛?- 鍥涘煄鍖洪厤缃細`PLAN_DISTRICTS`锛坕d / name / subject / icon / building / color / topics[]锛?- 瀛︾閰嶇疆锛歚SUBJECT_CONFIG`锛?33 鍥涢棬锛? `EXTRA_SUBJECT_CONFIG`锛堢墿鐞?/ 鑻辫锛?- 瀛︾鑷姩妫€娴嬶細`detectSubjectId(bankName)` 鎸夊叧閿瘝鍖归厤棰樺簱鍚嶅綊鍏ュ绉?
### 鏁版嵁鍚屾瑙﹀彂鐐?- `save()` 鍚庤嫢 `syncCfg.autoSync` 涓?true锛岃嚜鍔ㄨ皟鐢?`syncPush()`
- 鏀惰棌棰樼洰銆佺瓟棰樺畬鎴愮瓑鍏抽敭鍔ㄤ綔浼氭樉寮忚Е鍙戝悓姝?
### PWA
- Service Worker 缂撳瓨锛坘ey `kynotes-v2`锛?- 鍙畨瑁呭埌涓诲睆锛坄installPWA()`锛?
## 鏁版嵁妯″瀷鎬昏锛坄DEF()`锛?
```
A = {
  // 绗旇
  notes[],
  // 璁℃椂
  focusSessions[], totalFocusSec,
  // 瀛︾杩涘害锛堟寜鏃ユ湡閿級
  physicsChapters[], eduDaily{}, momoDays{}, readingDays{}, totalReading,
  // 娓告垙鍖?  score, scoreLog[], signDays{}, signStreak, streakMomo, lastMomoDate,
  // 鍒烽
  quizBanks[], quizProgress{},
  favoriteQuestions[], favoriteTags[],
  // 瑙勫垝
  examPlan{ targetDate, mainSubject, cityMode, dailyBuild{} },
  // 鍗曡瘝缁?  wordGroups[],
  // 鍚屾閰嶇疆
  syncCfg{ ghToken, ghRepo, ghPath, geeToken, geeRepo, geePath, autoSync },
  // 璁剧疆
  settings{ fontSize, density, customSubjects[], glass, music, sfx, lastExportAt, theme }
}
```

## 宸茬煡鏋舵瀯鐥涚偣锛堜緵閲嶆瀯鍙傝€冿級

1. **鍗曟枃浠?9300+ 琛?*锛欳SS / HTML / JS 鍏ㄩ儴鍐呰仈锛屾棤妯″潡杈圭晫锛岄毦浠ョ淮鎶や笌鍗忎綔
2. **鍏ㄥ眬鍙橀噺 `A` + 鐩存帴 DOM 鎿嶄綔**锛氭棤鍝嶅簲寮忕郴缁燂紝UI 涓庢暟鎹槗鑴辫妭
3. **鍑芥暟鑱岃矗娣锋潅**锛氫竴涓嚱鏁板彲鑳藉悓鏃跺仛鏁版嵁淇敼銆丏OM 娓叉煋銆佸壇浣滅敤瑙﹀彂锛堝 `recordQuizAttempt` 璋冪敤浜?`addScore` / `recalcBankStats` / `markTodayBuild` / `renderCommandCenter` / `save`锛?4. **鏃犺矾鐢?*锛歍ab 鍒囨崲涓嶆敼鍙?URL锛屾棤娉曟繁閾炬帴銆佹棤娉曡繑鍥?5. **绂荤嚎渚濊禆 CDN**锛歮arked.js 浠?CDN 鍔犺浇锛岀绾挎椂绗旇棰勮澶辨晥
6. **鍚屾鏃犲啿绐佽В鍐?*锛氬璁惧骞跺彂鍐欎細涓㈡暟鎹?7. **娓告垙鍖栭€昏緫鏁ｈ惤**锛氱Н鍒嗐€佺瓑绾с€佺鍒般€佸煄甯傚缓璁惧垎甯冨湪涓嶅悓鍖哄煙
8. **Canvas 浠ｇ爜鍐楅暱**锛氬煄甯傚缓绛戠粯鍒?700+ 琛屾湭鎶借薄
9. **棰樺簱瑙ｆ瀽纭紪鐮?*锛氬彧鏀寔鐗瑰畾鏍煎紡锛屾墿灞曢鍨嬮渶鏀硅В鏋愬櫒
10. **璁剧疆闈㈡澘鑱岃矗杩囪浇**锛歎I 璁剧疆 / 鏁版嵁绠＄悊 / 棰樺簱绠＄悊 / 鍚屾閰嶇疆娣峰湪涓€澶?
## 鎶€鏈爤

- HTML / CSS / JavaScript锛堝崟鏂囦欢鍐呰仈锛屾棤妗嗘灦锛?- PWA + Service Worker 绂荤嚎缂撳瓨
- localStorage 鎸佷箙鍖栵紙鍗?key锛?MB 涓婇檺鑷姩娓呯悊锛?- marked.js锛圕DN锛夋覆鏌?Markdown
- Canvas 2D 鎵嬬粯鍩庡競寤虹瓚銆侀ゼ鍥俱€佽鑹插ご鍍?- CSS 鍙橀噺涓婚绯荤粺锛? 濂楅璁撅級
- GitHub / Gitee Contents API 鍚屾

## Claude 璁块棶鏂瑰紡

浠撳簱 Public锛屽彲鐩存帴璁块棶锛?
- **浠撳簱涓婚〉**锛堟帹鑽愶紝Claude 浼氳嚜鍔ㄨ鍙栨枃浠舵爲涓?README锛夛細https://github.com/gangshangka/quiz-notes
- **HTML 婧愭枃浠?raw**锛歨ttps://raw.githubusercontent.com/gangshangka/quiz-notes/main/quiz_v4-2(1).html
  锛圲RL 鍚嫭鍙?`(1)`锛岄儴鍒嗗鎴风闇€缂栫爜涓?`%28%29`锛?- **鏂囦欢鏍?API**锛歨ttps://api.github.com/repos/gangshangka/quiz-notes/git/trees/main?recursive=1
- **README raw**锛歨ttps://raw.githubusercontent.com/gangshangka/quiz-notes/main/README.md

## 鏈湴杩愯

娴忚鍣ㄧ洿鎺ユ墦寮€ `quiz_v4-2(1).html`銆傛帹鑽?Chrome / Edge / Safari 浠ユ敮鎸?PWA 涓?Service Worker銆?