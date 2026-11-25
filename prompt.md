# 1 提示词合集

## 1.1 目录

- [1.2 澄清需求](#12-澄清需求)
  - [1.2.1 找出需求里没说清的业务规则](#121-找出需求里没说清的业务规则)
  - [1.2.2 用你自己的话复述我的目标和我要解决的问题](#122-用你自己的话复述我的目标和我要解决的问题)
- [1.3 制定计划](#13-制定计划)
  - [1.3.1 先设计接口，用原型验证疑问](#131-先设计接口用原型验证疑问)
  - [1.3.2 把迁移拆成可以验证的小步](#132-把迁移拆成可以验证的小步)
- [1.4 查找与整理资料](#14-查找与整理资料)
  - [1.4.1 了解现有功能是怎么实现的](#141-了解现有功能是怎么实现的)
- [1.5 编写与调试代码](#15-编写与调试代码)
  - [1.5.1 理解遗留代码里的设计假设](#151-理解遗留代码里的设计假设)
  - [1.5.2 调查后台任务超时](#152-调查后台任务超时)
  - [1.5.3 先迁移一个，再写工具处理其余的](#153-先迁移一个再写工具处理其余的)
  - [1.5.4 从历史提交查找反复出现的错误](#154-从历史提交查找反复出现的错误)
- [1.6 界面与交互](#16-界面与交互)
  - [1.6.1 审查整个项目的用户体验](#161-审查整个项目的用户体验)
  - [1.6.2 按状态变化检查动效](#162-按状态变化检查动效)
- [1.7 写作与修改](#17-写作与修改)
  - [1.7.1 用通俗的话重述上一条回答](#171-用通俗的话重述上一条回答)
- [1.8 检查与验收](#18-检查与验收)
  - [1.8.1 检查架构中的过度抽象](#181-检查架构中的过度抽象)
  - [1.8.2 检查改动会影响哪些地方](#182-检查改动会影响哪些地方)
  - [1.8.3 复现故障并用录像验证修复](#183-复现故障并用录像验证修复)

引用块保留来源中的原句或原命令。以斜杠开头的 Poteto 示例使用 pstack。

## 1.2 澄清需求

### 1.2.1 找出需求里没说清的业务规则

> 运用 **Michael Polanyi（迈克尔·波兰尼）** 的认知理论审视这份需求文档。识别出我默认存在但未明说的隐性前提（默会维度），列出开发过程中最容易出现理解偏差的 5 个边界条件。

来源：你提供的 Gemini 对话。

### 1.2.2 用你自己的话复述我的目标和我要解决的问题

> restate in your own words what you think my goals are and what the problem i'm trying to solve is

[Poteto 原帖](https://x.com/poteto/status/2104744961904394699)

## 1.3 制定计划

### 1.3.1 先设计接口，用原型验证疑问

> /poteto-mode we need to add rate limiting for external webhooks. /architect this first, and answer any open questions with prototypes. let me review before proceeding.

[Poteto 原文](poteto/articles/2097732320606507506.md)

### 1.3.2 把迁移拆成可以验证的小步

> /poteto-mode create a plan to migrate our entire UI library to StyleX. break the migration into small, verifiable PRs. each PR must have its visual regression tests and live verification steps. i want the final result to be 100% identical compared to the original - bugs included

[Poteto 原文](poteto/articles/2097732320606507506.md)

## 1.4 查找与整理资料

### 1.4.1 了解现有功能是怎么实现的

> /how is virtualization implemented?

[Poteto 原文](poteto/articles/2097732320606507506.md)

## 1.5 编写与调试代码

### 1.5.1 理解遗留代码里的设计假设

> 基于 **Michael Polanyi** 的知识结构理论分析 `@legacy-module.ts`。剥离表面的语法逻辑，还原原开发者隐藏在代码结构、命名和异常处理中的设计直觉与领域假设。

来源：你提供的 Gemini 对话。

### 1.5.2 调查后台任务超时

> /poteto-mode investigate why background workers periodically fail with timeout errors. give me a breakdown of what we know, what data you used, and your best hypotheses.

[Poteto 原文](poteto/articles/2097732320606507506.md)

### 1.5.3 先迁移一个，再写工具处理其余的

> Do the first unit by hand to learn the recipe, then have the agent write a codemod for the mechanical parts and a checker that proves the output.

Poteto 在文章中给出的做法。[Poteto 原文](poteto/articles/2069824386283319343.md)

### 1.5.4 从历史提交查找反复出现的错误

> /poteto-mode use /correct and /architect on past commits to find the most common pitfalls agents fall into, then propose a plan to rearchitect the code i own so it's more agent friendly. answer open questions with prototyping rather than defer to me, and back the plan with real data.

[Poteto 原帖](https://x.com/poteto/status/2111133080526495985)

## 1.6 界面与交互

### 1.6.1 审查整个项目的用户体验

[数字生命卡兹克原文，第 1 条](https://aihot.news/items/jb7ohptrc5ctyx9maoimz2hn0#:~:text=复杂应该留给我们系统)

### 1.6.2 按状态变化检查动效

[数字生命卡兹克原文，第 2 条](https://aihot.news/items/jb7ohptrc5ctyx9maoimz2hn0#:~:text=把项目的动效整体做到苹果那种细腻)

## 1.7 写作与修改

### 1.7.1 用通俗的话重述上一条回答

> /bro

pstack 原命令，需安装 pstack。[Poteto 原文](poteto/pstack/pstack-README.md)

## 1.8 检查与验收

### 1.8.1 检查架构中的过度抽象

> 遵循 **Michael Polanyi** 反对机械还原论的哲学立场，评估当前系统架构。指出哪些地方存在脱离实际业务语境的过度抽象，给出最贴合当前团队开发直觉的简化方案。

来源：你提供的 Gemini 对话。

### 1.8.2 检查改动会影响哪些地方

> /blast-radius

pstack 原命令，需安装 pstack。[Poteto 原文](poteto/pstack/pstack-README.md)

### 1.8.3 复现故障并用录像验证修复

> /poteto-mode repro this with /control-app. if it repros on main, fix it and show me a video as proof

[Poteto 原文](poteto/articles/2097732320606507506.md)
