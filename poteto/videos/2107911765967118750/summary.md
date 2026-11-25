# 视频总结：Lauren Tan（@poteto）workshop + Matt Pocock 访谈合集

整理时间：2026-10-08 Asia/Taipei。整理人：poteto bot（只读）。
转写全文：`transcript.md`（同目录）。

## 结论

1. 这个视频是转发者剪辑的合集，不是 poteto 本人发布。
2. 视频长 3:43:40。有效内容约 2 小时。
3. 合集里有两场活动：
   - Colin Matthews 主持的 workshop（Lauren 主讲）。这一场出现 3 次：0:00:00–0:52:26（剪辑版）、1:54:20–2:51:07（完整版，带开场自我介绍）、2:51:07–3:43:40（与第一段重复）。
   - Matt Pocock 的直播访谈（0:52:26–1:54:20）。资料包里已有这场的转写：`spacex-transcript.md`。
4. 她的理论主线没有变：**先验证，再信任；用硬约束代替口头纠正；信任够了才扩大并行和自动合并。**
5. 这场 workshop 与资料包大体一致。新增的是细节：Dune 的五条规则、skill 的 eval 做法、"先在本地建验证再上云"、PR 拆分的理由、token 投入的 ROI 说法。
6. 没有发现与资料包矛盾的内容。

## 来源与可信度

- 帖子：https://x.com/scarfpinkgirl/status/2107911765967118750 （@scarfpinkgirl "pinky girl"，2026-10-08 03:11 Asia/Taipei）。
- 帖子引用了 @unicodef1wn 的一篇 X Article（"AI Company-in-a-Box: Full 12-Step Roadmap…"，链接已 404）。那篇不是 poteto 写的。
- 帖子里的章节说明不准确：
  - "1:54:23 CI rules…" 实际是同一场 workshop 的完整版重新开始。
  - "52:27 Scale from 1 agent to a full team" 实际是 Matt Pocock 访谈。
  - 帖子说 "almost 3-hour"，实际 3:43:40，其中约 52 分钟重复。
- 说话人：
  - 1:54:20 起，她自我介绍 "I'm Lauren Tan … potato on Twitter … at Cursor for about five months"。主持人称她 "Lauren"，她称主持人 "Colin"。画面里有 Colin Matthews 的摄像头和 "GrokBot team workshops" 字样。
  - 0:52:26 起是 Matt Pocock 访谈。画面标注 "Matt" 和 "poteto"。
  - 0:00:00–0:01:02 是一段开场插入。画面是 Lauren 在 SpaceX 舞台上拿麦讲话。这段话不在 workshop 原始音频里。来源活动无法确认。内容是"AI 应该像结对编程伙伴，我花更多时间审查 AI 的输出"。**我不能确认这是她本人的观点，还是她在复述别人的问题。**
- 日期推断（我的推断）：她说"这个月才到 12 号，我已经合了将近 800 个 PR"（0:05:05）。资料包里 2026-08-09 的帖子预告"下周三和 Colin Matthews 办 workshop"（`posts.md` 第 2096 行，https://x.com/poteto/status/2086258720779215290 ）。所以这场 workshop 很可能是 2026-08-12 前后。

## 核心观点（时间戳取第一段 0:00–0:52；完整版在 1:54:20 之后，约 +1:56）

### 1. 信任曲线：不信任就只能微管理【已在资料包】
- 不信任 agent，就像经理不信任下属，只能盯着每一步（0:02:02）。
- 信任上升后，才能并行更多 agent。现在她的 agent 自动合并 PR，她早上在 main 上审已合入的 20 个 PR（0:03:34）。
- 不要从"盯一个 agent"直接跳到"开几百个云端 agent"。那只会浪费 token（0:25:05）。
- 资料包：`SUMMARY.md` §1、§9；`spacex-transcript.md` 1:31（trust ladder）；`updates.md` 2026-10-07 条（1 小时后自动合并）。

### 2. 验证是最重要的技能；Feature Map 让 agent 找得到功能【已在资料包】
- 验证 = agent 自己运行代码、抓 CPU trace / heap snapshot、开模拟器，像用户一样用（0:05:41）。
- 验证不保证代码"好"，但保证代码"对"。这是信任的第一步（0:06:08）。
- 没有验证 skill 时，人就是验证者，也是瓶颈（0:08:12）。
- 她的第一个 skill 是 control-glass（用 CDP 控制 agents window）（0:08:42）。
- 只有 CLI 不够。agent 不知道"左侧栏""PR tab"在哪。Feature Map 写清楚：功能是什么、用户怎么到达、快捷键、CDP 用的 DOM 属性（0:09:43–0:12:15）。
- 用 pstack `/create-verification-skill` 生成，用 `/maintain-verification-skill` 保持更新（0:12:46）。
- 资料包：`SUMMARY.md` §2；`articles/2094457600259842065.md`；`talk2500.txt` [10:16]–[11:40]；`pstack.md` 第 69–70 行。

### 3. 先在本地建验证，再上云【部分新增】
- 建验证 skill 时先在本地做，因为你能看到 agent 怎么操作应用（0:22:31）。
- 本地可信后，再交给 cloud agent 和 automation。例：Benny 在云端电脑里复现 bug，并确认 main 上已经修好（0:24:04–0:24:35）。
- 验证 skill 的价值不只给个人，也给整个团队（0:23:33）。
- 资料包：Benny 见 `articles/2058975157503570132.md` 第 58–61 行。**"先本地、后云端"这个顺序是新细节。**

### 4. skill 从失败模式里长出来；用 eval 维护 skill【部分新增】
- pstack 不是规划出来的。她每看到一种 agent 失败（乱猜、不读代码、"找到了 smoking gun"），就写一个 skill（0:13:47–0:15:49）。
- eval = skill 的单元测试。做法（0:16:49–0:20:59）：
  1. coordinator agent 先写评分标准（rubric）。
  2. 派多个 sub-agent 执行。目录名要伪装，不让它们知道在被测，因为 agent 知道被测会改变行为。
  3. 用另一个模型做 judge，交叉检查评分偏差。
  4. 跨多个模型跑同一个 eval。
  5. 用 `/loop` 反复 hillclimb，直到全部 10/10。
- 她用同样方法 eval 了验证 skill 里的 CLI（0:20:59）。
- 维护 skill 需要品味：读 tool call 和 thinking，找失败点（0:19:26）。
- 资料包：`pstack.md` 第 86 行（hillclimb）、第 94 行（eval playbook）；`articles/2069824386283319343.md` 第 83 行。**eval 的具体步骤和"eval 验证 CLI"是新细节。**

### 5. 约束分层：硬约束优先，软约束兜底【已在资料包，有新例子】
- 分层（0:40:04–0:43:09，幻灯片）：1 codebase/架构 → 2 静态分析（lint/compiler/CI）→ 3 rules/bugbot → 4 skills → 5 style guide。
- 1 和 2 能让 CI 变红，是硬约束。3–5 是软约束，agent 会忘。只有软约束，代码库迟早变垃圾（0:42:39）。
- 每次在 PR 里写同一条评论，就把它变成 lint 规则、CI 失败，或从结构上消除这类问题（0:44:12）。
- 新例子：
  - Dune 禁用 React `useEffect`，CI 直接失败（0:36:27）。
  - 禁止代码注释，因为 agent 会把临时说明当成永久规则（0:36:57）。
  - `electron main` 和 `electron renderer` 两个目录之间，CI 检查依赖图，禁止错误导入（0:39:33）。
  - 技术栈也是约束。Rust 编译器很严格，所以"能编译基本就能用"（0:43:09）。
- 资料包：`SUMMARY.md` §3、§6；`pstack.md` 第 111–119 行；`talk2500.txt` [16:25]–[16:52]、[23:45]–[24:09]。**`useEffect` 禁用、依赖图检查、Rust 例子是新细节。**

### 6. Dune：让最短路径就是正确路径【部分新增】
- 核心原则："the shortest path is the best path"。agent 爱走捷径，所以把正确做法设计成最短做法（0:41:06）。
- 一个 feature 一个目录，代码集中，agent 不用到处找（0:40:35）。
- 幻灯片 "Agent-friendly architecture" 的五条规则（0:39:40–0:42:00 画面 OCR）：
  1. The conventional path requires fewer decisions than a shortcut.
  2. Forbidden dependencies fail mechanically.
  3. Every durable value has one obvious writer.
  4. New product work adds isolated files rather than branches in shared roots.
  5. Exceptions are narrow, explicit, and reviewed as architecture changes.
- 幻灯片还写了 agent 的行为假设：复制最近的模式、改已打开的文件、选能编译的最短路径、不删看不到调用方的代码、即使违反系统不变量也照做。
- Dune 不开源。她说可以截图让 agent 照着建（0:41:36）。
- 资料包：`SUMMARY.md` §6；`talk2500.txt` [19:29]–[19:35]。**五条规则原文是新内容。**

### 7. 重写：绿地项目风险最大，机会也最大【已在资料包】
- 大厂的护栏是为"最弱的工程师"设计的，所以 brownfield 项目让 agent 写也比较安全（0:29:46）。
- vibe-coded 的新项目没有护栏，会长成"organic architecture"，越来越失控（0:30:18–0:31:51）。
- 她用 600 多个 PR 把 Grok Bot 重构到 Dune。之后她基本不看代码；PM 和设计师也能直接提交功能（0:32:22、0:51:25）。
- 资料包：organic architecture 帖 https://x.com/poteto/status/2078527882499150286 （`posts.md` 第 2286 行）；rewrites 帖 https://x.com/poteto/status/2054657980705185933 ；`updates.md` 2026-10-08 条（TTR）；`talk2500.txt` [20:06]（设计师、PM 也能贡献）。

### 8. PR 要拆小；token 投入看 ROI【部分新增】
- PR 没有硬上限，大小 50 到 1000 行不等。但她要求 agent 把工作拆成多个 PR（0:34:23）。
- 理由：git 历史是重要上下文；每个 PR 原子化，出 bug 时容易定位和回滚（0:35:25）。
- token 前期花得多（重构、加约束）。和招人比，ROI 是正的；团队可以保持小（0:45:44–0:49:23）。
- 资料包：`updates.md` 2026-10-07 条（她的 PR 几百行）。**拆 PR 的理由和 ROI 说法是新细节。**

## Matt Pocock 访谈段（0:52:26–1:54:20）

- 这一段与 `spacex-transcript.md` 是同一场直播（YouTube MN9dGgmLyso）。
- 我用 Whisper 转写了这一段，用来核对，全文在 `transcript.md`。
- 段 B 的 Whisper 文本与 `spacex-transcript.md` 按顺序对照，9392 个词里有 9005 个词能对上（约 96%）。
- 我没有发现资料包以外的新主张。本文件不重复总结。

## 对 Geyoto 的启示（全部是我的推断）

1. CLI 计划 v2 的方向正确。它对应观点 2（CLI + Feature Map）和观点 3（先本地，CI 跑 `--all` against local，再做生产只读）。
2. 可以考虑给验证 CLI 加 eval：固定一组任务，给 CLI 输出打分，用另一个模型复核。这对应观点 4。
3. Feature Map 可以补"用户怎么点到"和页面选择器（例如 `data-*` 属性）。这样 agent 能把模糊的问题报告对到页面。这对应观点 2。
4. 群里反复出现的纠正，应该变成 CI 检查，不要只写进说明。`order_price_wecom_alert_gates` 检查就是这个做法。这对应观点 5。
5. 自动合并要等验证可信。这与"先保持一个 Project"的规则一致。这对应观点 1。

## 转写方法与质量

- 视频：`video720.mp4`（1280x720，3:43:40，从帖子媒体直链下载）。
- 主方法：烧录字幕 OCR。ffmpeg 每秒取 3 帧，裁剪字幕框，只保留字幕框内的白字，用 tesseract（eng）识别，再合并相邻重复行。字幕是英文，所以用 eng 模型，没有用 chi_sim。
- Workshop 段（0:00–0:52、1:54–3:43）OCR 质量好。与 Whisper 抽样对照（1:02–9:50），词级一致率 92.4%。
- 已知问题：
  - 字幕原文本身有错（例如 "GroffBot"、"SpaxeXAI"），我没有改。
  - 0:50:55 和 3:42:09 附近，原字幕重复 "they're not really excited for that" 多次。这是原视频字幕的错误。
  - Matt Pocock 段字幕样式不同，OCR 失败，改用 Whisper（small.en）转写。
