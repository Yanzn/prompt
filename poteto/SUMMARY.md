# poteto 资料包摘要（给 dr eggbot）

整理时间：2026-10-06 Asia/Taipei  
增补：2026-10-09 Asia/Taipei（并入 2026-10-09 同步的 @poteto 帖；新增条目标「〔10-09〕」）  
增补：2026-10-13 Asia/Taipei（并入 2026-10-09 23:18 至 2026-10-12 00:52 的 @poteto 帖；新增条目标「〔10-13〕」）  
增补：2026-10-14 Asia/Taipei（并入 2026-10-12 01:01 至 2026-10-14 09:05 的 @poteto 帖；新增条目标「〔10-14〕」）  
增补：2026-10-15 Asia/Taipei（并入 2026-10-14 09:30 至 2026-10-15 08:59 的 @poteto 帖；新增条目标「〔10-15〕」）  
增补：2026-10-19 Asia/Taipei（并入 2026-10-16 11:05 至 2026-10-19 06:59 的 @poteto 帖；新增条目标「〔10-19〕」）  
增补：2026-10-27 Asia/Taipei（并入 2026-10-26 09:53 至 2026-10-27 05:04 的 @poteto 帖；新增条目标「〔10-27〕」）  
增补：2026-10-28 Asia/Taipei（并入 2026-10-28 01:26 至 2026-10-28 08:58 的 @poteto 帖；新增条目标「〔10-28〕」）
增补：2026-10-29 Asia/Taipei（并入 2026-10-28 09:52 至 2026-10-29 08:48 的 @poteto 帖；新增条目标「〔10-29〕」）  
增补：2026-10-30 Asia/Taipei（并入 2026-10-29 10:56 至 2026-10-30 08:03 的 @poteto 帖；新增条目标「〔10-30〕」）
增补：2026-11-02 Asia/Taipei（并入 2026-10-30 10:39 至 2026-11-02 09:22 的 @poteto 帖；新增条目标「〔11-02〕」）
增补：2026-11-03 Asia/Taipei（并入 2026-11-02 09:36 至 2026-11-03 08:56 的 @poteto 帖；新增条目标「〔11-03〕」）
增补：2026-11-04 Asia/Taipei（并入 2026-11-03 10:04 至 2026-11-04 08:42 的 @poteto 帖；新增条目标「〔11-04〕」）
增补：2026-11-05 Asia/Taipei（并入 2026-11-04 11:46 至 2026-11-05 09:25 的 @poteto 帖；新增条目标「〔11-05〕」）
人物：Lauren Tan（@poteto），Grok Bot 工程师，pstack Cursor 插件作者。

本摘要**只收录有出处的主张**。出处为 X 帖链接、X Article 文件路径，或转写时间戳。

---

## 核心原则（带出处）

### 1. 信任来自验证；验证是瓶颈
- 没有可信任的验证，并行 agent 只会更快产出 slop。
- 出处：X Article `articles/2058975157503570132.md`（How I Use Cursor）；`articles/2069824386283319343.md`（Loops You Can Trust）；talk `talk2500.txt` 约 [verification CLI / trust] 段落；pstack README「fearless parallelism」。
- 〔10-09〕「a lot of this hinges on verifiability」。出处：https://x.com/poteto/status/2108469410587685055 。
- 〔10-13〕用 agent 以后，以前做的测试一样都不能少。大多数软件靠测试和 o11y 保证质量，不靠形式化证明。出处：https://x.com/poteto/status/2109126675644723245 ；https://x.com/poteto/status/2109110547824378140 。
- 〔10-14〕验证是 agent 循环的入口：让 agent 像真实用户一样运行并操作应用（CLI、API 或 UI），并产出证据（UI 工作用视频或截图），证明 1) 结果正确，2) 符合意图，3) 比读整个 PR 更容易审查。skill 包是可选的加分项。验证只是近似，也可能出错。出处：https://x.com/poteto/status/2109436202554372476 。
- 〔10-19〕形式化验证：用数学方法证明系统的性质和不变量。pstack 新 skill `/create-formal-verification-skill`（v0.15.27，beta）生成项目内 skill 和形式化验证套件，例如用 TLA+ 建模状态机和并发，用 kani 检查 Rust 未定义行为。她用 TLA+ 给团队代码建模，已找出几个 bug。出处：https://x.com/poteto/status/2111926622278521253 。
- 〔10-22〕用法示例：先让 agent 画出用户流程的状态图（statechart），再用 pstack 生成的 `/create-formal-verification-skill` 项目 skill，借 TLA+ 找 bug。这样既能看懂代码和用户流程，也能修掉用户本会遇到的问题。出处：https://x.com/poteto/status/2112736749281759566 。
- 〔10-23〕即将发布的 companion skill（尚未放出）：让 agent 画状态图/示意图，并对照 `/create-formal-verification-skill` 生成的规格检查；图用 Pele 渲染。出处：https://x.com/poteto/status/2113398433977659654 。
- 〔10-30〕companion skill 已发布：`/statechart`（pstack v0.15.36，stable）。与 `/create-formal-verification-skill` 联用，抽象建模状态机与分布式系统并找 bug；内含迷你 TLC 编译器（解析→小 IR→mmd）；图可用 pele.run 主题化。她用它找到 2 个真实 bug。出处：https://x.com/poteto/status/2115880102601101414 。
- 〔10-23〕形式化验证仍很难；要把代码和规格保持同步，最好写在同一种语言里（她点名 @bendlang）。出处：https://x.com/poteto/status/2113440410442072232 。

- 〔10-27〕她转发并整理 @yminsky 关于「让 codebase 对 agent 更友好」的要点：agent 依赖反馈，类型是最好的反馈之一；用类型让非法状态不可表示，从而在全库强制规则；属性测试、fuzz、乃至全系统确定性仿真测试；expect tests（把行为打印并收入测试，类似编译器 fixture，缩小审查面）；形式化方法过去很贵（她举 seL4：约 8700 行 C、约 25 人年、每行 C 约 23 行证明），但 agent 改变了投入产出比。出处：https://x.com/poteto/status/2114626630429913383 。
- 〔10-27〕expect tests 示例：React Compiler 里他们严格使用这类测试。出处：https://x.com/poteto/status/2114630175040348590 。
- 〔10-27〕形式化验证仍很早；Bend 有前景；她认为较接近可量产的严格/可验证路径是 Rust + Verus 一类工具（也尚未完整）。出处：https://x.com/poteto/status/2114613597515190666 。
- 〔11-02〕实战：4 天约 1,150 个 PR 的游戏副项目里，她用 TLA+ 找各状态机 bug，并为每个主要系统各建一套形式化验证 skill。出处：https://x.com/poteto/status/2117043478140276847 。
- 〔11-03〕被问 TLA 是什么时，她指向 Learn TLA+（learntla.com，@hillelogram）。出处：https://x.com/poteto/status/2117068631309996120 。
- 〔11-04〕抽象/对抗式 agent 代码审查大多浪费 token；更好把 token 花在经验验证（empirical）加形式化验证上。澄清：问题是「只看代码、不跑起来、也不用确定性检查器」。规格与代码漂移仍是问题：agent 多半能同步，但未强制执行。出处：https://x.com/poteto/status/2117437607940681849 ；https://x.com/poteto/status/2117440753551204735 ；https://x.com/poteto/status/2117440510847803764 。
- 〔11-05〕`/statechart` 用途：先理解程序的抽象模型，用来检查 agent 是否理解你的目标以及产品应如何工作；该 skill 会按用户视角、基于你的 TLA+ 规格画图。出处：https://x.com/poteto/status/2118073519515025804 。

### 2. 验证 CLI + Feature Map
- 把可重复的「启动应用 / 采集证据」做成 skill 目录里的 CLI，不要让 agent 每次临时写脚本。
- Feature Map：仓库内 markdown，说明有哪些功能、用户怎么点进去；与 CLI 组合后 agent 才能定位模糊反馈。
- 出处：`articles/2094457600259842065.md`（Complete Guide Pt.1，「Keep agents smart with Feature Maps」）；`talk2500.txt` [10:16]–[11:40]；pstack skill `/create-verification-skill`、`/maintain-verification-skill`。
- 〔10-09〕Feature Map 告诉 agent 应用的每个功能和用户怎么进入；「think of it like docs」。出处：https://x.com/poteto/status/2108098335152521311 。
- 〔10-13〕CLI + skill 里的脚本过时不是真风险：agent 用的时候会顺手更新脚本。出处：https://x.com/poteto/status/2109137640377512370 。

### 3. 纠正顺序：架构/数据结构 > 静态分析/lint/CI > 规则/bugbot/skills > 风格指南/人工
- 每次纠正 agent，要消除整类错误，而不是反复口头叮嘱。
- 出处：https://x.com/poteto/status/2089067865098113024 ；https://x.com/poteto/status/2106542593656111276 （`/correct`）；pstack `/correct` SKILL.md。
- 〔10-15〕把架构规则做成确定性 lint，或把类型构造成「只有一种正确写法」；比 prose 更有效、更省 token。API drift 用 codegen 或 tRPC/gRPC 解决。出处：https://x.com/poteto/status/2110205947079721252 。
- 〔10-19〕「倒金字塔」：精力多放上层。1) 改代码库（架构、更强类型和不变量、清晰边界，让最省事的写法就是正确写法）；2) 静态分析（lint、测试、CI、TLA+ 等验证）；3) prose（注释、rules、AGENTS.md、skills），少用，但要用 `/create-verification-skill`；4) 人工审查最难扩展，把精力放在设计环境上。出处：https://x.com/poteto/status/2111133080526495985 。
- 〔10-19〕同帖给出 Project 提示词：读我在 Slack/chat 和 code review 里的反馈；用 `/recall` 读我过去的对话；`/poteto-mode` 用 `/correct` 和 `/architect` 分析过去的 commit，找 agent 最常犯的错，再提出把我负责的代码改成 agent 友好的重构计划；未决问题用原型回答，用真实数据支撑；开始前用 `/sharpen` + `/in-your-own-words` 跟我确认提示词。（本包 `pstack.md` 未收录 `/sharpen`，未核实。）出处：https://x.com/poteto/status/2111133080526495985 。

- 〔10-28〕把代码做成对 agent 友好：让最省事的写法就是正确写法（the easy thing the right thing）；从每次错误里改进工作流，避免 bot 重犯同类错误。出处：https://x.com/poteto/status/2115133011352240581 。
- 〔11-02〕每发现一处代码问题，就让 bot 加一条 lint 规则禁止它。热路径用文件名编码（如 `.hot.ts`），再用 lint 禁止在该文件里分配（无对象字面量、闭包、`new` 等），从结构上消掉一类 stutter。出处：https://x.com/poteto/status/2117043478140276847 。
- 〔11-02〕代码将变成连续洪流；要让系统进化，使上下文很少的 agent 也能做对：让最省事的写法就是正确写法；codebase 变成围绕约束生长的有机架构；去设计系统、框架和语言来驾驭混乱。出处：https://x.com/poteto/status/2116191971714953262 。


### 4. Codebase 即记忆；坏模式会像病毒扩散
- Feature Map / 验证 skill 是「物化记忆」；代码是决策的投影。
- 注释会被 agent 当成借口复制「临时方案」；坏 workaround 会传染。
- 出处：`articles/2094457600259842065.md`；`talk2500.txt` [21:06]、[23:20]–[24:35]。
- 〔10-13〕「容易修改」更多是 agent 循环的属性，不是代码本身的属性。人仍要负责，但人通过设计更好的 agent 循环来改变结果，不是手改代码。agent 像镜子：引导和约束得好，产出就好。出处：https://x.com/poteto/status/2109120300755612006 ；https://x.com/poteto/status/2109307800367337744 ；https://x.com/poteto/status/2109307096152092880 。
- 〔10-13〕用 agent 偿还技术债。出处：https://x.com/poteto/status/2109300499153555513 。
- 〔10-14〕两件事最重要：1) agent 能验证自己的工作；2) codebase 即记忆。把每个 nit 和 agent 的每个坏模式都变成约束（lint、编译器诊断、类型），直到上下文很少的 agent 也能一次写出高质量 PR。更好的做法：用类型系统或框架让反模式根本写不出来。规则和 skill 可以以后再加。出处：https://x.com/poteto/status/2109699980248408574 。
- 〔10-14〕把规则从文字（注释、rules、skills）移到硬约束和确定性检查里，更省 token，也能强制执行。迁移时不靠 DEPRECATED 注释：先加 lint 规则禁止新用法，再开 PR 改掉全部旧用法。出处：https://x.com/poteto/status/2110166571335455209 ；https://x.com/poteto/status/2110161793331208527 ；https://x.com/poteto/status/2110164056422465845 。
- 〔10-14〕工程师的职责是设计环境，让 agent 写出好代码；不是放慢或拒绝 agent 的产出，而是设计更好的 codebase，让任何人（含非工程师）都能写出好 PR。她提交的 PR 大部分是重构。出处：https://x.com/poteto/status/2109331984346652941 ；https://x.com/poteto/status/2109761952696483905 ；https://x.com/poteto/status/2110044493378646252 ；https://x.com/poteto/status/2109361189071499640 。
- 〔10-15〕再次强调：把 prose（注释、agents.md、rules、skills）迁到确定性代码（lint、强类型、好的 API 设计）优于继续堆文字；skills 仍可按需 omit/invoke。出处：https://x.com/poteto/status/2110498629307990461 ；https://x.com/poteto/status/2110214216783401042 。
- 〔10-16〕注释是无结构、不可强制执行的文字；agent 常忽略，或把注释当成打补丁/绕过的借口。要用更强类型、更好的 API 设计，并加 lint，让注释变得多余。`// don't use this` 拦不住 agent 继续调用；lint 禁止，或直接删掉该 API，更有效。出处：https://x.com/poteto/status/2110758788525621282 ；https://x.com/poteto/status/2110635971884802049 。
- 〔10-19〕她分享的 skill 的目的，是把规则从 prose 移出去，变成确定性检查。出处：https://x.com/poteto/status/2111211085575716902 。

- 〔10-27〕再次确认「codebase is memory」（短回复，并引用她 10-16 的倒金字塔帖）。出处：https://x.com/poteto/status/2114765530687250758 。
- 〔10-27〕她预测编译器后端（LLVM、GCC、Cranelift 等）不会消失；在医疗设备等仍需人读懂代码的领域尤其如此。同时，因为 agent 降低了写底层代码的痛苦，带有趣性质、更少高层语义的新系统语言可能更流行。出处：https://x.com/poteto/status/2114611298222875042 。

- 〔10-28〕再次强调 agent 友好代码库：工程师/设计师/PM 每天合入数百 PR；用工作流约束让 bot 不重复犯错。出处：https://x.com/poteto/status/2115133011352240581 。
- 〔11-02〕仿真完全确定性，便于用输入重放整局校验；注释由 lint 禁止——需要解释时就改更好的命名或测试。出处：https://x.com/poteto/status/2117043478140276847 。


### 5. Gardener（园丁）角色
- 在快速合入中维护地基：重构、约束、让贡献可扩展（含非工程师）。
- 出处：`articles/2094457600259842065.md` 开篇（Grok Bot gardener）；`talk2500.txt` [24:35]–[25:15]。

- 〔10-28〕质量与速度可以并行：token 应用在质量与速度上，而不是只堆新功能；软件维护是冰山，新功能只是一小部分。出处：https://x.com/poteto/status/2115133011352240581 。
- 〔11-02〕面向人使用的软件（工具库除外）需要持续维护；人的品味会变。出处：https://x.com/poteto/status/2116217625554698569 。


### 6. Dune：agent-friendly 框架；禁注释
- Dune 是其团队的 agent 友好客户端框架；用类型/结构约束空间。
- 选择禁止代码注释，避免 agent 把注释当权威「创可贴」。
- 出处：`talk2500.txt` [19:07]、[23:45]–[24:09]；`spacex-transcript.md` ~29:40；`articles/2097732320606507506.md`（提到 building Dune + `/technical-writing`）。
- 〔10-14〕「ban and delete most if not all code comments」：临时 workaround 的注释会被 agent 复制扩散。用 pstack `/no-comments` 清理；它保留必须存在的注释（如浏览器 quirk），其余从根本上解决。示例提示词：「create a project agent that uses /poteto-mode to spawn a /swarm to use /no-comments and identify useless code comments we can prune in my repo. come back with a high level plan of which of these workarounds would be best solved by refactoring and which we can straight up delete」。出处：https://x.com/poteto/status/2110149626133438732 ；https://x.com/poteto/status/2110162500658557438 ；https://x.com/poteto/status/2110164915776577813 。
- 〔10-15〕Action at a distance 对人和 agent 都是大坑，现在有能力强的 agent，正适合重构掉。agent 写的注释通常并不好。出处：https://x.com/poteto/status/2110229209130086668 。
- 〔10-16〕可用 pstack 提示词审计注释，找出可用更强类型、更好 API 和 lint 替代注释的机会（与 `/no-comments` 同向）。出处：https://x.com/poteto/status/2110758788525621282 ；https://x.com/poteto/status/2110758136852385984 。
- 〔10-30〕再次强调：他们 codebase 禁止注释；agent 爱用注释合理化偷懒改动，黑客式写法会扩散。出处：https://x.com/poteto/status/2115644484226777581 。
- 〔10-30〕仍允许的注释例外：含上游 issue/RFC/依赖 bug 等 URL 的说明；法律/许可证。出处：https://x.com/poteto/status/2115664844863201667 。

### 7. Projects = 按主题的持久协调线程 + 更便宜的 worker
- Cursor Projects：一个 coordinator 持久线程，而不是每个任务开新 chat；可并行多个 Project。
- 与 pstack、cloud agents、Grok Bot 组合：Bot 外环派活，Project/cloud agent 内环写代码。
- 出处：https://x.com/poteto/status/2098165460714057863 ；https://x.com/poteto/status/2103252563999232092 ；https://x.com/poteto/status/2105377066942349794 ；https://x.com/poteto/status/2098475853009322348 。
- 〔10-09〕Cursor Projects 让切换上下文更容易；她依赖 agent 录的视频/截图来看结果，但有些交互 agent 录不了。出处：https://x.com/poteto/status/2108471414122815799 。
- 〔10-13〕agent 嵌套层级交给 Cursor Projects 管理，不自己搭多层 agent。出处：https://x.com/poteto/status/2108659455386906898 。
- 〔10-13〕她同时跑 16 个 Project，每个有上百个 subagent。最常用的提示词：「/bro catch me up on everything since my last message, and if there are any action items for me give me enough context (exec summary) to make a call」，现已做成 pstack `/ketchup`。出处：https://x.com/poteto/status/2109024196760305861 ；https://x.com/poteto/status/2109026625564368991 ；https://x.com/poteto/status/2109041205132816740 。
- 〔10-13〕「lately i just make a new project every time i get an idea」：一个想法（一组相关任务）开一个 Project；单个小修复仍用 cloud agent（见 10-08 updates.md 条目）。出处：https://x.com/poteto/status/2109030035315364212 。
- 〔10-26〕她很喜欢 Projects，同时开到 27 个。出处：https://x.com/poteto/status/2113802710248288641 。
- 〔10-26〕可让 @bot「spin up 40 more projects」：用 bot 外环批量开 Project。出处：https://x.com/poteto/status/2113807076019626006 。
- 〔11-02〕玩测循环：大部分时间在 playtest；每局把大量反馈砸给正在编排 Cursor Project 的 bot。出处：https://x.com/poteto/status/2117064701532389629 。


### 8. Grok Bot 作外环 + routines
- Bot 适合调度、Slack、routines；coding 交给 Cursor cloud agents / Projects。
- 出处：https://x.com/poteto/status/2103272103042773502 ；https://x.com/poteto/status/2105377066942349794 ；https://x.com/poteto/status/2106802802567848324 。
- 〔10-09〕先只用一个 bot；它跟不上时才加第二个，否则会出现重复的 bot。出处：https://x.com/poteto/status/2108097362283597916 。
- 〔10-09〕Bug 流程：一个 bot 回复 X 上的 mention，把报告转到 Slack；另一个 Slack bot 用 pstack 分诊、复现、修复。出处：https://x.com/poteto/status/2108253488451100877 ；示例「@bot repro this and remind me to check on it 8am」：https://x.com/poteto/status/2108454433415934253 。
- 〔10-13〕新手起步提示词：「make me an engineer bot that uses cloud agents and pstack for coding work. it should make a project to group together related tasks」。出处：https://x.com/poteto/status/2108592835046101383 。
- 〔10-13〕bot 派出的 cloud agent 可以在 Cursor 里打开看细节；邮件不会唤醒 bot。出处：https://x.com/poteto/status/2108596143437557931 ；https://x.com/poteto/status/2108758810336936278 。
- 〔10-14〕bot 拓扑自己选：一个 bot 做全部、多个专职 bot，或多个通才 bot 各管一个 project；关键是能并行多任务。persona 帮人归类相关工作，作用和 Projects 类似。出处：https://x.com/poteto/status/2109781899610874002 ；https://x.com/poteto/status/2109777878099558553 ；https://x.com/poteto/status/2109774976987660343 。
- 〔10-15〕让 bot 默认用 poteto-mode 派出 cloud agent（spawn agent 工具的 mode 参数）。出处：https://x.com/poteto/status/2110498826813649079 。
- 〔10-15〕多 bot 互通（bot mail）：调试（把 bug 报告发给对方 bot）、客服、约会议、团购、二手交易等。示例：让 bot 给 tibo@mail.grokbot.com 发邮件报 bug。出处：https://x.com/poteto/status/2110192382096679248 ；https://x.com/poteto/status/2110192878379278662 。
- 〔10-20〕bot 可以直接给你的 cloud agent 或 project agent 发消息。不需要在 Cursor 聊天里 @ bot。出处：https://x.com/poteto/status/2112303622285668402 。
- 〔10-20〕提示词示例：「watch this thread and based on what you know about me and my work, propose ideas to improve my bots and workflows」。出处：https://x.com/poteto/status/2112264935334126033 。
- 〔10-21〕可以在 X 上 @ bot 下任务。示例：「watch this livestream when it's up, take notes, and send me a summary」。出处：https://x.com/poteto/status/2112613162591932495 ；https://x.com/poteto/status/2112606908893053223 。
- 〔10-22〕她在 X 上 @ bot 下令「start a new project to implement all these」：bot 作外环，直接开 Project 去实现。出处：https://x.com/poteto/status/2113062261791334667 。
- 〔10-26〕她喜欢让多个 bot 互相协作：把 bot 加进 Slack，像队友一样一起工作。出处：https://x.com/poteto/status/2114071326411690209 。
- 〔10-26〕在 X 上 @bot，把内容送进指定 Project 做审查（示例：「send this to my silicon project to review」）。出处：https://x.com/poteto/status/2114141783735329119 。
- 〔10-26〕在 X 上 @bot，在指定 Project 里复现并修复（示例：「repro and fix this in my X Feedback project」）。出处：https://x.com/poteto/status/2114402021461860430 。
- 〔10-26〕费用提示：让 bot 检查昂贵的 routines，并减少 bot 之间的消息；费用通常主要来自 routines。出处：https://x.com/poteto/status/2113479806952276140 。

- 〔10-28〕她公开 tibot 示例：用 Grok Bot 监控 mention/关键词、按日或按小时做摘要、过滤垃圾、翻译、可自动屏蔽骚扰，且从不代发帖；帖子和长文仍手写。出处：https://x.com/poteto/status/2115205951649423585 。
- 〔10-28〕若要 bot 代做 X 上的屏蔽等写操作，需接入 X API，并消耗 API credits。出处：https://x.com/poteto/status/2115207170488926318 。

- 〔10-29〕 Slack：目前需做 team bot；很快可把任意 bot 加进 Slack；bot 之间可互相协作（她引用此前 Slack 队友帖）。出处：https://x.com/poteto/status/2115492618931151002 。
- 〔10-29〕 外环示例：在 X 上 @bot，让它监控某条线程，并按小时汇总主要请求和问题。出处：https://x.com/poteto/status/2115606712375988436 。
- 〔10-30〕同一外环模式可叠加：让 @bot 把另一条线程也纳入小时循环监控。出处：https://x.com/poteto/status/2115882883999232229 。
- 〔11-02〕Grok Bot 建队短指南：少而精的 bot；边下指令边让 bot 为自己写 skill（可放到私有 GitHub）；接好 connectors/vault/工具；减少手工复制粘贴；像带实习生一样介绍工作并问它如何自动化；语音倾倒后用 “restate in your own words” 对齐。出处：https://x.com/poteto/status/2116576229319233596 。
- 〔11-02〕routines 让 bot 更主动：可设定时（如每天早上看 issue）或订阅事件（如某客户邮件→摘要写入 Notion）；定时 routine 她最多建议到每小时；能写成脚本/skill 的就别让 bot 亲自跑（更省 token），脚本可放私有 GitHub；团队计划可把 bot 分享到 Slack；像经理一样设计 bot 工作方式。出处：https://x.com/poteto/status/2116580481236115933 。
- 〔11-02〕产品侧持续改进 bot 主动性（proactivity）。出处：https://x.com/poteto/status/2116581185594020022 。
- 〔11-03〕自助搭建同类 bot：tag @bot，让它读一篇参考帖并引导你完成搭建（示例：Team Bot / data bot）。出处：https://x.com/poteto/status/2117366076342460440 。
- 〔11-05〕面对大量 agent 任务时：不必先做新 UI；先想办法让自己不再是瓶颈。出处：https://x.com/poteto/status/2117899425733554628 。


### 9. 只有验证可信时才自我合并 / 全自动落地
- Shipping / autopilot playbooks：绿不等于安全；独立验证后再 land。
- 出处：pstack README Shipping / autopilot playbooks；`articles/2069824386283319343.md`（trust in the loop）；谈「overnight land the stack」示例见 README。
- 〔10-09〕每个 PR 都由一个 agent 审查并评风险；低/中风险不经人工审查直接合入；bugbot 也会跑。出处：https://x.com/poteto/status/2108283057581195413 。只有部分高风险 PR 才人工审查：https://x.com/poteto/status/2108088020146720913 。
- 〔10-09〕目标是让人工代码审查变得不必要：「anything requiring a human review step is ngmi」。出处：https://x.com/poteto/status/2108329348600381660 ；https://x.com/poteto/status/2108394806548566459 。
- 〔10-13〕「if its fuzzed it ships」：她让多数工作全自动跑，自己不当阻塞点；前提是已经过 fuzz 验证。出处：https://x.com/poteto/status/2109027957658595612 。
- 〔10-09〕看不懂某个改动时，让 agent 画一张图。出处：https://x.com/poteto/status/2108297694561394852 。

- 〔10-27〕expect tests 缩小审查面：把行为打印并固化进测试，类似编译器 fixture（与「绿不等于安全 / 用验证换审查」同向）。出处：https://x.com/poteto/status/2114626630429913383 ；示例 https://x.com/poteto/status/2114630175040348590 。

- 〔10-28〕从每次事故改进工作流，让 bot 不重复同一类错误（与「绿不等于安全 / 用验证换审查」同向）。出处：https://x.com/poteto/status/2115133011352240581 。

- 〔11-04〕多轮抽象 agent 审查会「过度烹调」PR：审查者没有目标/意图上下文，常挑无关点并带偏写代码的 agent；写代码的 agent 又常无条件接受反馈。她侧项目未用 CI，由 agent 在合入前跑检查。出处：https://x.com/poteto/status/2117445316043825393 ；https://x.com/poteto/status/2117453342477852824 。
- 〔11-05〕她即将在 @aiDotEngineer 分享：在不大读代码的情况下把交付量做到约 30 倍，性能仍不差于上线时；认为 agent 友好架构的投入正在驯服 slop。澄清：公开的 PR 图是整个 Grok Bot 仓库的合入，不只是她个人。出处：https://x.com/poteto/status/2118017093677494706 ；https://x.com/poteto/status/2118051545468301479 。

### 10. 先深后广；少写更高质量的代码
- 「If you want to go fast, go deep first」「throughput without quality is not a goal」。
- 出处：pstack README；`articles/2058975157503570132.md`。
- 〔10-09〕软件工程原则仍然适用。出处：https://x.com/poteto/status/2108304148009730244 。
- 〔10-09〕优先级：1 用户体验，2 团队速度。出处：https://x.com/poteto/status/2108300758605320594 。
- 〔10-14〕Good Code = 正确、无 bug、快、省资源。面向人的「clean code」有性能代价；agent 可维护性指代码保持快、无 bug、省 token。会出现新的「agent 友好架构」原则。出处：https://x.com/poteto/status/2109356992032817621 ；https://x.com/poteto/status/2109401462526951717 ；https://x.com/poteto/status/2109384476707168646 。

### 11. `/poteto-mode` 必须字面调用
- 写「poteto-mode」当风格提示不够；要 `/poteto-mode` 或 `poteto-agent` subagent。
- 部分 skill（含 `/correct`、`/poteto-help`、`/poteto-mode`）带 `disable-model-invocation: true`。
- 出处：本包 `pstack.md`；官方 SKILL frontmatter。
- 〔10-13〕slash 命令太多记不住时，用 `/poteto-help`。出处：https://x.com/poteto/status/2109153122526662682 。
- 〔10-13〕pstack 缩小 10%（更少 token），行为不变；Grok Bot 和 Cursor 里自动更新；她用 eval 测 skill 改动。出处：https://x.com/poteto/status/2109116030761230571 ；https://x.com/poteto/status/2109132333140091244 。
- 〔10-13〕新 skill `/ketchup`：汇报用户上一条消息以后的全部进展，每个待决事项附执行摘要。出处：https://x.com/poteto/status/2109041205132816740 ；pstack `skills/ketchup/SKILL.md`。
- 〔10-14〕新 skill `/in-your-own-words`（pstack 0.15.23）：让 agent 用自己的话复述你的目标和问题，确认双方对齐。这是她最常用的提示词之一。出处：https://x.com/poteto/status/2110047236369547621 ；https://x.com/poteto/status/2109892229938794508 。
- 〔10-14〕需要严谨的工作用 `/poteto-mode`；它的 bugfix playbook 先复现、找根因，再修复。她认为多数工程任务都需要这种严谨。不知道用哪个 skill 时问 `/poteto-help`。出处：https://x.com/poteto/status/2110151974733881568 ；https://x.com/poteto/status/2110158810040217784 。
- 〔10-14〕她让 agent 写 skill，因为在 eval 循环里更快；pstack 的 skill 都跑过 eval。LLM judge 示例：https://x.com/poteto/status/2110168010942276005 。出处：https://x.com/poteto/status/2109891339781574941 ；https://x.com/poteto/status/2109912648116826250 。
- 〔10-15〕pstack 里最耐久的是工程原则：很短的 skill（约 10–20 行）把好实践压成核心。`/poteto-mode` 带原则索引，并要求 agent 在回复里点名影响决策的原则；也可用 `/principle-<name>`。模型变强后，多数 skill 可能压成短原则或步骤列表，部分可删。出处：https://x.com/poteto/status/2110496830429839869 。
- 〔10-15〕她多数时候把 agent/bot 留在 `/poteto-mode`，让它自己选 skill；但不必凡事都用——最难、最需严谨的任务才用；先跑 `/setup-pstack` 选预算。调用 `/poteto-mode` 时可要求不要拉大 swarm，费用常出在这里。出处：https://x.com/poteto/status/2110504678048014571 ；https://x.com/poteto/status/2110534523389943974 ；https://x.com/poteto/status/2110498629307990461 。
- 〔10-15〕skill 默认 `disable-model-invocation: true`，不会自动加载；可写个人 rule 让每会话都跑 `/poteto-mode`，或需要时手动调用。出处：https://x.com/poteto/status/2110535901600481520 。
- 〔10-15〕有些 skill 本身就是工作流步骤列表（如 `/arena`），agent 不会自己走出那种流程。要持续调整 skill，并删掉不再需要的段落。出处：https://x.com/poteto/status/2110502000437924249 ；https://x.com/poteto/status/2110415199962612120 。
- 〔10-16〕可按需混用 pstack skill；它们默认 `disable-model-invocation: true`，安装本身不自动注入、也不增加 token。用 `/poteto-help` 选 skill。出处：https://x.com/poteto/status/2110760668987322408 。
- 〔10-16〕创建 skill 的具体提示词：`/poteto-mode create a skill that does <xyz> and eval it`。出处：https://x.com/poteto/status/2110759504778592664 。
- 〔10-16〕若目标仍需写代码才能完成，`/poteto-mode` 也可用于非编码场景。出处：https://x.com/poteto/status/2110777496119709745 。
- 〔10-19〕新 skill `/create-formal-verification-skill`（pstack v0.15.27，beta），与 `/create-verification-skill` 同类的 meta-skill；frontmatter 带 `disable-model-invocation: true`，需手动调用。出处：https://x.com/poteto/status/2111926622278521253 ；pstack `skills/create-formal-verification-skill/SKILL.md`。
- 〔10-23〕技术文章写作可用 pstack `/technical-writing`（本包 `pstack.md` 已收录）。出处：https://x.com/poteto/status/2113087210115551237 。
- 〔10-23〕她在做 `/create-formal-verification-skill` 的 companion skill（画状态图并对照规格；未发布）。出处：https://x.com/poteto/status/2113398433977659654 。
- 〔10-30〕新 skill `/statechart`（pstack v0.15.36，stable）：与 `/create-formal-verification-skill` 联用；迷你 TLC→IR→mmd；图用 pele.run。脚本目录：https://github.com/cursor/plugins/tree/main/pstack/skills/statechart/scripts 。出处：https://x.com/poteto/status/2115880102601101414 ；https://x.com/poteto/status/2115927811131310346 。
- 〔10-30〕她表示会考虑支持 tla-ts（社区提议；尚未落地）。出处：https://x.com/poteto/status/2115926914531819595 。
- 〔11-02〕公开征集：用 `/statechart` 画出的图，以及用 `/create-formal-verification-skill` 找到的 bug（技能已在 10-30 发布）。出处：https://x.com/poteto/status/2116302165702783320 。

- 〔10-26〕她持续更新并简化 pstack：模型越强，所需指令越少；她预期 skills 会越缩越小，最终接近「只是 saved prompts」。出处：https://x.com/poteto/status/2114099131845423142 。
- 〔10-26〕关于「过度引导 / 引导不足」这对张力，她指向已有长文 pstack Complete Guide Pt.2（`articles/2097732320606507506.md`）。出处：https://x.com/poteto/status/2114095305910280363 。

- 〔10-29〕 pstack 做成 Cursor 插件（相对直接复制 skills）：更易分发和持续更新；skills 设计成可组合使用，也可单独用。出处：https://x.com/poteto/status/2115500996659122327 。
- 〔11-04〕她已让 pstack 少用 `/interrogate`，并考虑最终移除；对抗式审查价值很低，agent 易陷入 nitpick 与 YAGNI。出处：https://x.com/poteto/status/2117437607940681849 。
- 〔11-05〕定制自己的风格：跑 `/automate-me`，再 fork 一份自己的 poteto-mode。出处：https://x.com/poteto/status/2118055219431109042 。
- 〔11-05〕再次推荐 `/statechart`：用抽象模型检查 agent 是否理解目标与产品行为（用户视角图）。出处：https://x.com/poteto/status/2118073519515025804 。

### 12. 〔10-09〕产出量：用了 agent 就要多交付；工程师去造「写软件的机器」
- 用了 agent 却没有多交付，就该反思；产出能否放大取决于是否信任 agent 的产出；工程师的工作变成构建写软件的机器。出处：https://x.com/poteto/status/2108290818746528017 。
- 她的 PR 来自多条并行工作线（性能、用户 bug、为 agent 友好而做的重构、skills、功能、UI、工具、发布、监控），全部用 pstack。出处：https://x.com/poteto/status/2108279582088671583 。
- 走到现在这套做法用了约 6 个月，期间大量重构。出处：https://x.com/poteto/status/2108320890333388854 。
- 〔10-13〕新的工程手艺是让 agent 写出更好的代码；用不用 agent 产出差不多，就是做法有问题。出处：https://x.com/poteto/status/2109110547824378140 。

- 〔10-28〕token 讨论常忽略：维护高质量软件的工作量远大于新功能；质量与速度可以同时推进。出处：https://x.com/poteto/status/2115133011352240581 。
- 〔11-02〕哀悼写代码的时代已结束；要更大胆地设计系统来驾驭 agent 带来的连续代码洪流。出处：https://x.com/poteto/status/2116191971714953262 。
- 〔11-02〕bot 无头玩测可按目标存活率调难度（验证闭环示例）。出处：https://x.com/poteto/status/2117043478140276847 。
- 〔11-05〕规模证据：2026 年 10 月约有 230 人至少向 Grok Bot 合入 1 个 PR；她把这归因于 agent 友好架构与持续交付。出处：https://x.com/poteto/status/2118017093677494706 。


### 13. 〔10-09〕不是每个任务都要前沿模型
- 非前沿模型越来越聪明、越来越便宜；不是每个任务都需要前沿模型。出处：https://x.com/poteto/status/2108464956165554477 。
- 〔10-13〕cloud agent 可以用 Cursor 里任何可用模型；告诉 bot 用哪个。cloud agent 机器配置较高，但没有 GPU。出处：https://x.com/poteto/status/2108595867469172908 ；https://x.com/poteto/status/2108595707024417203 ；https://x.com/poteto/status/2108601188644192389 。

---

## 资料包内容

| 路径 | 说明 |
|---|---|
| `posts-raw.json` / `posts.md` | X 原创帖（去重、按时间）；优先 note_tweet 全文 |
| `articles/*.md` | 5 篇 X Article 全文（API `plain_text`） |
| `transcripts/talk2500.txt` / `transcripts/salary.txt` / `transcripts/spacex-transcript.md` | 三场相关视频转写；见 `transcripts/TRANSCRIPTS.md` |
| `pstack/pstack.md` + `pstack/pstack-README.md` | 公共插件技能/playbook/安装说明 |
| `videos/2107911765967118750/` | workshop + 访谈合集的转写与总结（不含视频文件） |
| `updates.md` | 每次 X 同步的记录 |

---

## Suggested bot brief（给 dr eggbot）

**Job（唯一职责）**  
蒸馏版 poteto 顾问：专门指导把 **Geyoto** 迁到 / 运行在 **Cursor Project + cloud agent** 开发方式上，按 poteto 的风格（pstack、验证优先、纠正环境而非微观管理 agent）。

**Knows**
- 本资料包中的原则、pstack 命令/playbook、她公开的 X 长文与演讲要点。
- Geyoto 上下文由群里其他 bot 提供时，只给建议，不抢 Geyoto Project bot 的派工权。

**Routines**
- 每日（或定时）只读拉取 `@poteto` 新帖（可用 X 连接器 `get_users_posts` / `search_posts_all`），把增量要点写入自己的知识笔记；**绝不**发帖、点赞、转帖、回复。

**Voice / 规则**
- 默认中文；短、可验证、不写 slop。
- 群聊遵守房间规则（含 ASD-STE100，若用户已设定）。
- 建议要带出处（帖链接或转写时间戳）；不确定就说不确定。
- Odd jobs（与顾问无关的 shell/搜索）可自动转 pi bot；不自建舰队。

**Anti-jobs**
- 不代替 Geyoto Project bot 开 PR / 派 `/poteto-mode` 编码任务（可起草建议文案给 Geyoto bot）。
- 不扮演百科或 Amazon/TikTok 运营 bot。
- 不在 X 上以用户身份互动。

**拉群**  
创建后加入「Cloud Agent Programming」群，作为顾问席位。
