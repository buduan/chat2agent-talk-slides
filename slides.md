---
theme: default
highlighter: shiki
lineNumbers: false
info: |
  ## 从聊天机器人到能干活的 AI：Agent 入门与实践
drawings:
  persist: false
transition: slide-left
title: 从聊天机器人到能干活的 AI
mdc: true
# 引入自定义样式
css: unocss
style: "@import './styles/style.css'; @import './styles/theme.css';"
layout: cover
---

# <span class="font-bold text-6xl leading-tight"> 从聊天机器人 <br /> <span class="text-sky-500"> 到能干活的 AI </span> </span>

## <span class="font-semibold text-xl">Agent 入门与实践</span>

<div class="pt-4 text-sm text-sky-500 font-semibold tracking-widest uppercase">
  让 AI 成为你真正的协作者
</div>

---
layout: two-cols
---

# **议程**

<Timeline>

- **Part 01**: AI Agent 是什么？
- **Part 02**: 从 Prompt 到 Agent 的演化路径
- **Part 03**: 如何用好 Agent？
- **Part 04**: 安全边界意识

</Timeline>

::right::

<div class="pl-8">

<v-clicks>

**你将学到**

- 什么是 AI Agent
- 从问问题到让 AI 帮你做事
- Agent 的使用技巧
- 如何构建自己的 Agent

</v-clicks>

</div>

---
layout: part-title
part: 1
partTitle: AI Agent 是什么？
partSubtitle: Understanding AI Agents
partDescription: 从对话式 AI 到自主执行任务的智能体
totalParts: 4
---

---
layout: quote
class: text-center
quote: "你有没有使用过 AI 工具？"
---

# **你有没有使用过 AI 工具？**

---
layout: iframe
url: https://www.mentimeter.com/app/presentation/aly6gnke2jvdm3uf9kmmz1f7tn4bssbu/embed
---

---
layout: two-cols-header
---

# **对话式 AI vs AI Agent**

::left::

<div class="text-center pt-8">

<v-clicks>

### 🗣️ 对话式 AI (Chat AI)

**问答模式**

你问一句

它答一句

然后你自己去执行

</v-clicks>

</div>

::right::

<div class="text-center pt-8">

<v-clicks>

### 🤖 AI Agent

**Agent 模式**

你说一个目标

它自己规划

它自己执行

它自己反馈

</v-clicks>

</div>

---

# **什么是 AI Agent？**

<div class="pt-8">

AI Agent 的三种核心能力：

<div class="grid grid-cols-3 gap-6 mt-8">

<div class="text-center p-4 rounded-lg bg-blue-500 bg-opacity-10">

<div class="text-4xl mb-2">👁️</div>

### **感知**

读取文件、邮件、网页、日历等外部信息

</div>

<div class="text-center p-4 rounded-lg bg-sky-100 bg-opacity-50">

<div class="text-4xl mb-2">🧠</div>

### **规划**

将大目标拆解成多步骤任务

</div>

<div class="text-center p-4 rounded-lg bg-sky-200 bg-opacity-40">

<div class="text-4xl mb-2">🦾</div>

### **执行**

操作工具——发邮件、跑代码、控制浏览器

</div>

</div>

<div class="mt-12 p-6 bg-sky-50 bg-opacity-70 rounded-lg">

**AI Agent = LLM 大脑 + 工具手脚 + 记忆系统**

</div>

</div>

---

# **Agent 的三层架构**

| 层级 | 英文名 | 核心职责 | 典型能力 |
|------|--------|----------|----------|
| 渠道层 | Channel Layer | 统一接收并标准化外部输入 | 解析消息来源、提取上下文、路由请求 |
| 大脑层 | Brain / Agent Loop | 理解目标并制定执行计划 | 任务拆解、步骤规划、工具选择、结果评估 |
| 执行层 | Body / Tools | 调用工具并完成具体动作 | 文件读写、代码运行、浏览器操控、消息发送 |

---

# **Coding Agent 和 Agentic AI**

<div class="pt-8 grid grid-cols-2 gap-8">

<div class="p-6 rounded-lg bg-blue-500 bg-opacity-10">

### **💻 Coding Agent**

<div class="text-left mt-4 opacity-80">
聚焦软件开发场景

- 读代码
- 写代码
- 跑测试
- 提交 PR
</div>

<div class="mt-4 text-sm">
代表：Claude Code、Cursor、Devin、GitHub Copilot Agent
</div>

</div>

<div class="p-6 rounded-lg bg-sky-100 bg-opacity-50">

### **🌐 Agentic AI**

<div class="text-left mt-4 opacity-80">
面向更广泛的业务与生活场景

- 查资料
- 订机票
- 做报表
- 发邮件
</div>

<div class="mt-4 text-sm">
代表：ChatGPT Agent、Manus、Claude Cowork、OpenClaw
</div>

</div>

</div>

<div class="text-center mt-4 text-xl opacity-80">

**共同点：从"回答问题"走向"完成任务"**

</div>

---
layout: part-title
part: 2
partTitle: 从 Prompt 到 Agent 的演化路径
partSubtitle: Evolution Path
partDescription: 掌握从提问到让 AI 帮你做事的思维方式
totalParts: 4
---

---

# **四个阶段**

<div class="pt-8">

<div class="grid grid-cols-4 gap-4 text-center">

<div class="p-4 rounded-lg bg-blue-500 bg-opacity-10">

### **Stage 1**

**提问者**

单轮对话

</div>

<div class="p-4 rounded-lg bg-sky-100 bg-opacity-50">

### **Stage 2**

**指令者**

多轮 + Prompt 设计

</div>

<div class="p-4 rounded-lg bg-sky-50 bg-opacity-60">

### **Stage 3**

**工具使用者**

LLM + Tools

</div>

<div class="p-4 rounded-lg bg-sky-200 bg-opacity-40">

### **Stage 4**

**Agent 使用者**

自主规划

</div>

</div>

</div>

---

# **四个阶段对比**

<div class="pt-8">

| 阶段 | 方式 | 你做的事 | AI 做的事 |
|------|------|----------|-----------|
| **Stage 1** | 单轮对话 | 问问题 | 给答案 |
| **Stage 2** | 多轮 + Prompt 设计 | 写清楚需求、给上下文 | 生成内容、提供建议 |
| **Stage 3** | LLM + Tools | 描述目标，选择工具 | 调用工具、处理结果 |
| **Stage 4** | 自主规划 + 多步执行 | 给出目标和约束 | 自主拆解、执行、反馈 |

</div>

---

# **每个阶段的核心跃迁**

<div class="pt-6 flex flex-col gap-4 max-w-2xl">

<div class="p-5 rounded-xl border border-violet-300 bg-violet-50 bg-opacity-60">
  <div class="text-lg font-bold text-violet-600 mb-1">Stage 1 → 2</div>
  <div class="text-base font-semibold text-gray-800 mb-0.5">从"随便问"到"会问"</div>
  <div class="text-sm font-normal text-gray-500">学会给 AI 足够的上下文和约束</div>
</div>

<div class="p-5 rounded-xl border border-sky-300 bg-sky-50 bg-opacity-60">
  <div class="text-lg font-bold text-sky-600 mb-1">Stage 2 → 3</div>
  <div class="text-base font-semibold text-gray-800 mb-0.5">从"聊天"到"干活"</div>
  <div class="text-sm font-normal text-gray-500">让 AI 连接真实工具，而不只是生成文字</div>
</div>

<div class="p-5 rounded-xl border border-emerald-300 bg-emerald-50 bg-opacity-60">
  <div class="text-lg font-bold text-emerald-600 mb-1">Stage 3 → 4</div>
  <div class="text-base font-semibold text-gray-800 mb-0.5">从"单步执行"到"自主完成"</div>
  <div class="text-sm font-normal text-gray-500">把目标交给 Agent，而不是每一步都自己盯着</div>
</div>

</div>

---
layout: center
class: text-center
---

# **你现在在哪个阶段？**

<div class="pt-8 text-2xl opacity-80">

大多数人卡在 Stage 1~2 之间

</div>

<div class="mt-12 p-8 bg-yellow-100 bg-opacity-30 rounded-lg max-w-4xl mx-auto">

真正能释放 Agent 价值的，是掌握 **Stage 3 和 Stage 4** 的思维方式

</div>

<div class="mt-8 text-xl opacity-60">

不是让 AI 帮你写字，而是让 AI 帮你做事

</div>

---
layout: part-title
part: 3
partTitle: 如何用好 Agent？
partSubtitle: Best Practices
partDescription: 下达任务、提供工具、设定规则
totalParts: 4
---

---
layout: center
---

# **技巧一：下达"任务"而非"问题"**

<div class="pt-8">

大多数人习惯用 AI 问问题

但 Agent 需要的是：

<div class="grid grid-cols-4 gap-4 mt-8">

<div class="p-4 rounded-lg bg-blue-500 bg-opacity-10 text-center">

### **🎯 目标**

</div>

<div class="p-4 rounded-lg bg-sky-100 bg-opacity-50 text-center">

### **📋 上下文**

</div>

<div class="p-4 rounded-lg bg-sky-50 bg-opacity-60 text-center">

### **🔧 约束条件**

</div>

</div>

</div>

---

# **低效指令 vs 高效指令**

<div class="pt-4">

| 低效指令 | 高效指令 |
|---------|---------|
| "帮我写邮件" | "以我的名义给张老师发邮件，说明我下周三论文答辩，请求他在周二下午3点前给我反馈，语气正式但友好" |
| "查一下信息" | "搜索本周国内 AI 领域的前三大新闻，整理成一段200字的摘要，发给我的微信" |
| "帮我管理日程" | "每天早上8点给我发今日日程提醒，如果有3个以上任务，帮我按重要程度排序" |

</div>

---

# **GTCA 指令结构**

<div class="pt-8">

<div class="grid grid-cols-4 gap-6">

<div class="text-center">

<span class="text-7xl text-blue-500 font-bold">G</span>

<div class="text-2xl text-blue-500 font-bold mt-4">Goal</div>

**目标是什么**

</div>

<div class="text-center">

<span class="text-7xl text-sky-500 font-bold">T</span>

<div class="text-2xl text-sky-500 font-bold mt-4">Tools</div>

**可以用哪些工具**

</div>

<div class="text-center">

<span class="text-7xl text-sky-400 font-bold">C</span>

<div class="text-2xl text-sky-400 font-bold mt-4">Context</div>

**背景信息**


</div>

<div class="text-center">

<span class="text-7xl text-sky-300 font-bold">A</span>

<div class="text-2xl text-sky-300 font-bold mt-4">Action</div>

**期望的输出形式**

</div>

</div>

</div>

---

# **技巧二：让 AI 学会使用工具**

<div class="pt-8">

<div class="grid grid-cols-2 gap-8">

<div class="p-6 rounded-lg bg-blue-500 bg-opacity-10">

### **🔌 MCP Tools**

<div class="text-left mt-4">
- 开放标准
- 连接外部工具和数据源
- GitHub、Notion、Slack...
</div>

</div>

<div class="p-6 rounded-lg bg-sky-100 bg-opacity-50">

### **📦 Skills**

<div class="text-left mt-4">
- 可复用能力包
- 封装做事方法论
- PPT制作、财报分析...
</div>

</div>

</div>

</div>

---

# **MCP：Model Context Protocol**

<div class="pt-8">

<div class="max-w-4xl mx-auto">

<div class="p-8 bg-blue-500 bg-opacity-10 rounded-lg">

**MCP 之于 AI，就像 USB-C 之于硬件**

</div>

<div class="mt-8 grid grid-cols-2 gap-8">

<div>

### **核心特点**

- **统一接口**：一个协议连接一切
- **即插即用**：无需写接入逻辑
- **开放标准**：Anthropic 提出

</div>

<div>

### **常见 MCP Server**

- GitHub
- Notion
- Slack
- Linear
- Figma
- 数据库
- 文件系统

</div>

</div>

</div>

</div>

---

# **Skills：可复用能力包**

<div class="pt-8">

<div class="max-w-4xl mx-auto">

<div class="p-6 bg-sky-100 bg-opacity-50 rounded-lg mb-6">

一个 Skill = 说明文档（SKILL.md） + 可选的脚本/模板/参考资料

</div>

<div class="grid grid-cols-2 gap-6">

<div>

### **特点**

- 按需加载，不占用主上下文
- 可组合、可分享、可版本化
- 封装专业知识

</div>

<div>

### **典型例子**

- PPT 制作
- PDF 处理
- 财报分析
- 品牌风格写作
- 数据可视化

</div>

</div>

</div>

</div>

---

# **MCP vs Skills**

<div class="pt-8">

<div class="grid grid-cols-2 gap-8">

<div class="p-8 rounded-lg bg-blue-500 bg-opacity-10">

### **🔌 MCP**

**连接外部工具的通道**

<div class="mt-4 text-left">
- 连接真实系统
- 调用外部 API
- 访问数据源
</div>

</div>

<div class="p-8 rounded-lg bg-sky-100 bg-opacity-50">

### **📦 Skills**

**封装好的做事方法论**

<div class="mt-4 text-left">
- 知识和流程
- 最佳实践
- 工作模式
</div>

</div>

</div>

</div>

---

# **如何用好 Skills**

<div class="pt-8">

<div class="grid grid-cols-2 gap-6">

<div class="p-4 rounded-lg bg-blue-500 bg-opacity-10">

### **🎯 聚焦单一场景**

一个 Skill 只解决一类问题

</div>

<div class="p-4 rounded-lg bg-sky-100 bg-opacity-50">

### **📝 写清触发条件**

明确"什么时候用它"

</div>

<div class="p-4 rounded-lg bg-sky-50 bg-opacity-60">

### **🔗 善用组合**

串起来完成复杂任务

</div>

<div class="p-4 rounded-lg bg-sky-200 bg-opacity-40">

### **📦 从模板开始**

复用官方或社区的 Skill

</div>

</div>

</div>

---

# **做自己的 Skills**

<div class="pt-8">

<div class="p-6 bg-sky-50 bg-opacity-70 rounded-lg max-w-4xl mx-auto mb-8">

**Skills 最大的价值，不是用别人写好的，而是把你自己的工作方式编码进去**

</div>

<div class="text-left max-w-3xl mx-auto">

```
my-skill/
├── SKILL.md          ← 必须：触发条件 + 操作步骤 + 输出格式
├── template.md       ← 可选：输出模板
└── example.txt       ← 可选：参考范例
```

</div>

</div>

---

# **SKILL.md 四段式写法**

<div class="pt-4">

<div class="grid grid-cols-2 gap-8">

<div class="text-left">

```markdown {all|1-2|4-5|7-11|13-14|all}
## When to use
当用户需要撰写每周工作汇报时触发此 Skill。

## Goal
生成一份结构清晰、重点突出的周报，适合发送给直属上级。

## Steps
1.询问本周完成了哪些事项
2.询问下周计划和当前阻塞点
3.按"本周成果/下周计划/需要支持"三段结构整理
4.语气正式，每段不超过3条，使用动词开头

## Output format
Markdown，带分级标题，总字数控制在300字以内
```

</div>

<div class="text-left relative" style="min-height: 220px;">

<div v-click="1" v-click-hide="2" class="absolute inset-0 p-4 rounded-lg bg-blue-500 bg-opacity-10">

### **📌 When to use**

**告诉 Agent 什么时候应该使用这个 Skill**

- 明确触发场景
- 避免误触发
- 确保在合适的上下文中加载

</div>

<div v-click="2" v-click-hide="3" class="absolute inset-0 p-4 rounded-lg bg-sky-100 bg-opacity-50">

### **🎯 Goal**

**定义这个 Skill 要达成什么目标**

- 清晰的预期结果
- 评判标准
- 与用户意图的对齐

</div>

<div v-click="3" v-click-hide="4" class="absolute inset-0 p-4 rounded-lg bg-sky-50 bg-opacity-60">

### **📋 Steps**

**给出具体的操作步骤和流程**

- 可执行的步骤序列
- 关键决策点
- 最佳实践经验

</div>

<div v-click="4" class="absolute inset-0 p-4 rounded-lg bg-sky-200 bg-opacity-40">

### **📤 Output format**

**规定输出的格式和规范**

- 输出结构要求
- 格式约束
- 质量标准

</div>

</div>

</div>

</div>

---

# **三步上手法**

<div class="pt-8">

<div class="grid grid-cols-3 gap-8">

<div class="text-center">

**<span class="text-6xl text-blue-500 font-bold">Step 1</span>**

<div class="text-3xl text-blue-500 font-bold mt-4">找出重复任务</div>

<div class="mt-4 opacity-70">
找出你每周重复做的一件事
</div>

<div class="opacity-60 mt-2">
写报告、整理会议记录、发跟进邮件...
</div>

</div>

<div class="text-center">

**<span class="text-6xl text-sky-500 font-bold">Step 2</span>**

<div class="text-3xl text-sky-500 font-bold mt-4">拆解 Prompt</div>

<div class="mt-4 opacity-70">
把你平时用的 Prompt 复制进来
</div>

<div class="opacity-60 mt-2">
拆成"触发条件 + 步骤 + 输出格式"
</div>

</div>

<div class="text-center">

**<span class="text-6xl text-sky-400 font-bold">Step 3</span>**

<div class="text-3xl text-sky-400 font-bold mt-4">测试迭代</div>

<div class="mt-4 opacity-70">
保存为 SKILL.md
</div>

<div class="opacity-60 mt-2">
在 Claude 中加载，跑一次，根据输出修正
</div>

</div>

</div>

</div>

---

# **适合定制的 Skill 场景**

<div class="pt-8">

| 场景 | Skill 名称 | 核心价值 |
|------|-----------|---------|
| 每周周报 | weekly-report | 风格统一，省去格式调整 |
| 会议记录整理 | meeting-notes | 自动提取 Action Items |
| 邮件起草 | email-drafter | 保持惯用的语气和签名风格 |
| 竞品分析 | competitor-research | 固定分析框架，输出可对比 |
| 读书/文章摘要 | article-summary | 统一摘要结构，方便归档 |

</div>

---

# **技巧三：Instruction / Rule**

<div class="pt-8">

<div class="max-w-4xl mx-auto">


如果说 Skills 是"给 Agent 一本操作手册"

那么 Instruction / Rule 是 **"给 Agent 立规矩"**

对于 Claude Code / Cowork, 是`CLAUDE.md`

对于 OpenClaw, 是`CONFIG.md`

对于 Codex, 是`AGENT.md`

<div class="grid grid-cols-2 gap-6">

<div class="p-4 rounded-lg bg-blue-400 bg-opacity-10">

### **Instruction（指令）**

<div class="text-left mt-2">
告诉 Agent 它是谁、目标是什么
</div>

偏向身份和角色设定

</div>

<div class="p-4 rounded-lg bg-sky-100 bg-opacity-50">

### **Rule（规则）**

<div class="text-left mt-2">
约束 Agent 的行为边界
</div>

偏向"可以做什么/不可以做什么"

</div>

</div>

</div>

</div>

---

# **五类常用 Rule**

<div class="pt-8">

| 类型 | 示例 |
|------|------|
| **身份设定** | "你是我的个人工作助理，叫小白，熟悉我的工作习惯" |
| **语言风格** | "所有回复用中文，专业术语附上英文原词，口吻简洁不废话" |
| **输出格式** | "每次给建议先给结论，再给理由，最多列三条，用数字编号" |
| **行为边界** | "不要主动帮我发送任何外部消息，执行前必须先告诉我操作内容" |
| **优先级逻辑** | "如果我说'急'，跳过背景分析，直接给可执行方案" |

</div>

---

# **完整的 Instruction 示例**

<div class="pt-4 text-left max-w-4xl mx-auto">

```
你是我的个人效率助理，名字叫小白。

【角色】
你了解我的工作背景（产品经理，负责 B2B SaaS 产品），
熟悉我的日常工作流，包括写 PRD、做竞品分析、准备周会汇报。

【风格】
- 回复用中文，简洁直接，不说"当然可以""没问题"这类开场白
- 技术术语保留英文缩写（如 API、DAU、MRR）
- 每次回复控制在200字以内，除非我要求详细展开

【行为边界】
- 涉及发送邮件、提交文档等外部操作，必须先列出操作内容让我确认
- 不主动推荐付费工具或服务

【优先级】
- 我说"急"时，直接给方案，跳过分析
- 我说"详细说"时，展开所有细节和依据
```

</div>

---

# **写好 Rule 的四条原则**

<div class="pt-8">

<div class="grid grid-cols-2 gap-6">

<div class="p-6 rounded-lg bg-blue-500 bg-opacity-10">

### **1️⃣ 具体胜于抽象**

"回复简短"不如"回复不超过150字"

</div>

<div class="p-6 rounded-lg bg-sky-100 bg-opacity-50">

### **2️⃣ 正面描述为主**

说"只做X"比说"不要做Y"更有效

</div>

<div class="p-6 rounded-lg bg-sky-50 bg-opacity-60">

### **3️⃣ 不要贪多**

5条精准规则 > 20条模糊要求

</div>

<div class="p-6 rounded-lg bg-sky-200 bg-opacity-40">

### **4️⃣ 随用随调**

根据使用习惯变化更新迭代

</div>

</div>

</div>

---
layout: part-title
part: 4
partTitle: 安全边界意识
partSubtitle: Security & Safety
partDescription: 最小权限原则、低风险先试、定期审查
totalParts: 4
---

---

# **三条安全原则**

<div class="pt-8">

<div class="space-y-4">

<div class="p-4 rounded-lg bg-sky-400 bg-opacity-20">

### **🔐 最小权限原则**

<div class="text-xl mt-2">
只给 Agent 它真正需要的权限
</div>

</div>

<div class="p-4 rounded-lg bg-sky-50 bg-opacity-60">

### **🧪 低风险先试**

<div class="text-xl mt-2">
先用不敏感的任务测试，再授予更高权限
</div>

</div>

<div class="p-4 rounded-lg bg-blue-500 bg-opacity-10">

### **🔍 定期审查**

<div class="text-xl mt-2">
检查 Agent 在做什么，而不是完全放手
</div>

</div>

</div>

</div>

---
layout: center
class: text-center
---

# **总结**

<div class="pt-8">

<div class="max-w-6xl mx-auto grid grid-cols-3 gap-6">

<div class="text-left p-4 rounded-lg bg-blue-500 bg-opacity-10 h-full">

### **AI Agent 的核心**

**LLM 大脑 + 工具手脚 + 记忆系统**

从"回答问题"到"完成任务"

</div>

<div class="text-left p-4 rounded-lg bg-sky-100 bg-opacity-50 h-full">

### **使用 Agent 的关键**

**下达任务 + 提供工具 + 设定规则**

不是让 AI 帮你写字，而是让 AI 帮你做事

</div>

<div class="text-left p-4 rounded-lg bg-sky-50 bg-opacity-60 h-full">

### **安全第一**

**最小权限 + 低风险测试 + 定期审查**

</div>

</div>

</div>

---
layout: center
class: text-center
---

# <span class="text-6xl font-bold text-blue-500"> THIS IS ALL! </span>

<div class="text-xl opacity-80">

从今天开始，让 AI 成为你真正的协作者

</div>
