# Hermes Official Profile / Kanban Usage Summary

日期：2026-05-16

## 这份文档解决什么问题

本次讨论的问题是：

> 如果要把 Hermes 用成一个能自主运营的小型 AI 公司，应该怎么设计 profile、board 和 Kanban？

结论：

> 第一版不要做复杂公司。最适合的是一个 5 人 AI 工作室，用一个 Kanban board 跑生产任务，用 Markdown 保存战略、路线图和制度。

## 官方文档里的关键理解

Hermes 官方文档里的核心关系可以简单理解为：

```text
profile = 员工
board = 一个项目或业务线的工作队列
kanban task = 具体工作单
comment / metadata = 交接记录和审计记录
gateway dispatcher = 自动派工的人
```

官方 Kanban 不是普通待办清单，而是多个 Hermes profiles 共享的耐久任务板。

每个任务会分配给一个 profile。dispatcher 会把对应 profile 拉起来工作。worker 做完以后，通过 Kanban 工具写入完成结果、阻塞原因、评论和交接信息。

官方资料：

- Hermes Kanban: https://hermes-agent.nousresearch.com/docs/user-guide/features/kanban
- Hermes Profiles: https://hermes-agent.nousresearch.com/docs/user-guide/profiles/
- Kanban Tutorial: https://hermes-agent.nousresearch.com/docs/user-guide/features/kanban-tutorial
- Kanban Orchestrator: https://hermes-agent.nousresearch.com/docs/zh-Hans/user-guide/skills/bundled/devops/devops-kanban-orchestrator

## 社区经验里的提醒

社区和 GitHub issue 里反复出现几个实际问题：

1. 不要给不存在的 profile 派任务。

   Hermes 不会自动猜测 assignee。任务分给不存在的 profile，容易卡在队列里。

2. worker profile 要有正确工具权限。

   有用户反馈，新建 profile 如果只有 `hermes-cli`，没有 `web`、`browser`、`terminal`、`file` 等工具，worker 会做不出真正结果，甚至静默失败。

3. 不要一次放太多 ready 任务。

   如果自托管模型或机器资源有限，太多 ready 任务会让 dispatcher 同时拉起太多 worker，打满资源。

4. 第一版不要拆太多 board。

   board 是硬隔离。多个 board 意味着不同数据库、workspace 和 logs。早期拆太多，会增加心智负担和调度混乱。

相关资料：

- GitHub issue: Kanban worker profile toolsets: https://github.com/NousResearch/hermes-agent/issues/22924
- GitHub issue: Kanban board ownership: https://github.com/NousResearch/hermes-agent/issues/21877
- Reddit community megathread: https://www.reddit.com/r/hermesagent/comments/1t5cjlm/megathread_multiagent_workflows_kanban_delegation/

## 最适合当前项目的第一版结构

当前项目是 Indiesite：面向中国出口工厂的英文独立站改造和内容承接公司。

现在最适合的结构是：

```text
board:
  indiesite

profiles:
  indiesite-operator
  indiesite-mira
  indiesite-design
  indiesite-dex
  indiesite-nora
```

第一版只用一个 `indiesite` board。

原因：

- 当前还在产品制作阶段，不是多客户交付阶段。
- 主要目标是做展示资产、样板站、案例和模板。
- 一个 board 足够承载当前所有生产任务。
- 过早拆 `board-office`、`client-a`、`client-b` 会让系统变重。

以后满足这些条件，再考虑拆 board：

- 同时跑多个真实客户项目。
- 展示资产生产和客户交付互相干扰。
- 需要严格隔离客户资料。
- 需要独立的组织审计或董事会办公室。

## 每个 profile 做什么

### indiesite-operator

角色：

> 总经理 / 调度员 / Chief of Staff

负责：

- 听懂创始人目标。
- 判断下一步先做什么。
- 把目标拆成 Kanban 任务。
- 分配给 Mira、Design、Dex、Nora。
- 看任务有没有卡住。
- 处理阻塞。
- 判断什么时候需要创始人拍板。
- 汇总最终结果。

不负责：

- 不亲自包办所有文案、设计和代码。
- 不替 Nora 做最终验收。
- 不把战略文件写成一堆没人执行的任务。

### indiesite-mira

角色：

> 市场、内容、买家视角负责人

负责：

- 行业研究。
- 海外买家关心点。
- 网站 brief。
- 页面结构。
- 英文内容方向。
- 案例叙事。
- 避免空话和 AI 味英文。

典型任务：

```text
为阀门工厂 demo 写行业 brief
为旧站改造案例写 before/after 叙事
整理海外买家在产品页需要看到的信息
```

### indiesite-design

角色：

> 设计负责人 / 视觉方向负责人

负责：

- 找优秀参考网站。
- 判断行业适合什么视觉风格。
- 写 `design.md`。
- 给 Dex 明确视觉边界。
- 看桌面和手机截图。
- 判断视觉是否过关。
- 给出返工建议。

典型任务：

```text
为阀门 demo 找 8 个工业网站参考
输出 design.md 和视觉禁止项
评审 Dex 首页截图是否有工业可信度
```

### indiesite-dex

角色：

> 制作和工程负责人

负责：

- 根据 Mira 的 brief 和 Design 的 design.md 做原型。
- 使用 Kimi 做快速草稿。
- 使用 Codex 工程化。
- 修响应式。
- 加 SEO metadata。
- 检查链接、图片、按钮、表单。
- 保证资产能打开、能展示、能维护。

典型任务：

```text
根据 design.md 做阀门 demo 首页原型
把原型工程化成完整静态网站
修复移动端首屏和询盘路径问题
```

### indiesite-nora

角色：

> QA Gate / 商业展示风控

负责：

- 判断资产能不能对外展示。
- 检查是否像假案例。
- 检查英文是否自然。
- 检查内容是否具体。
- 检查是否有夸大宣传。
- 检查询盘路径是否清楚。
- 输出 Pass / Conditional Pass / Fail。

典型任务：

```text
评审阀门 demo 是否能进入展示资产库
列出 P0/P1/P2 问题
判断是否需要创始人拍板接受风险
```

## Kanban 放什么

Kanban 只放真正进入执行的工作。

适合上 Kanban 的任务：

- 有明确负责人。
- 有明确产出。
- 需要交接。
- 需要验收。
- 会阻塞别人。
- 需要保留审计记录。
- 需要跨 profile 协作。

例子：

```text
Mira 完成阀门行业 brief
Design 完成视觉参考和 design.md
Dex 完成首页原型
Design 完成桌面/手机截图评审
Dex 完成全站工程版本
Nora 完成商业 QA
Operator 汇总是否进入展示资产库
```

## Kanban 不放什么

不适合上 Kanban 的内容：

- 公司愿景。
- 长期战略方向。
- 创始人口味。
- 角色说明。
- 权限制度。
- 还没决定执行的灵感。
- 不需要别人行动的笔记。

这些应该放 Markdown，例如：

```text
vision.md
roadmap.md
taste-memory.md
roles.md
operating-principles.md
```

## CEO 的阶段计划怎么处理

CEO / 创始人可能会有这样的阶段计划：

```text
阶段 1：做阀门 demo
阶段 2：沉淀成模板
阶段 3：复制 3 个行业
阶段 4：开始找客户
```

这些阶段本身更适合放在 `roadmap.md`，不要全部塞进 Kanban。

Kanban 只放当前阶段真正要执行的任务。

例如当前阶段是：

```text
阶段 1：做阀门 demo
```

那么 Kanban 应该放：

```text
Mira: 完成阀门行业 brief
Design: 完成视觉参考和 design.md
Dex: 完成首页原型
Design: 评审桌面/手机截图
Dex: 完成全站工程版本
Nora: 完成商业 QA
Operator: 汇总阶段结果
```

如果需要追踪阶段完成情况，可以放一张收口卡：

```text
任务：判断阀门 demo 是否完成阶段 1
负责人：indiesite-operator
依赖：Mira / Design / Dex / Nora 的任务全部完成
产出：阶段总结、剩余问题、是否进入展示资产库
```

这样比做一个很大的战略卡更清楚。

## 推荐 Kanban 使用规则

第一版规则：

```text
1. 一个任务只给一个负责人。
2. 一个任务必须有明确产出。
3. 一个任务必须写清楚完成标准。
4. 需要别人接着做，就写交接结果。
5. 卡住就 block，不要假装 done。
6. 小任务直接做，不要为了流程上 Kanban。
7. 重要、长期、跨角色、要验收的任务才上 Kanban。
```

推荐状态：

```text
triage
todo
ready
running
blocked
done
archived
```

简单理解：

```text
triage = 粗想法，还没讲清楚
todo = 已决定要做，但还没准备好开工
ready = 可以派工
running = 正在做
blocked = 卡住，需要输入或处理
done = 完成
archived = 归档
```

## 推荐任务模板

```text
Title:

Owner:

Goal:

Required output:

Acceptance:

Inputs:

Blocked by:

Needs review by:

Evidence links:

Notes:
```

## 最终建议

当前最适合的落地方式：

```text
不要先建复杂公司。
先建 1 个 board + 5 个 profiles。
Kanban 只管正在发生的生产工作。
Markdown 管战略、路线图、制度和记忆。
等真实复杂度出现，再拆更多 board 和角色。
```

一句话：

> Hermes 第一版应该像一个带任务白板的 5 人 AI 工作室，而不是一开始就像一个多部门集团公司。
