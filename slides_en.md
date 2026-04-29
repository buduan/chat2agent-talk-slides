---
theme: default
highlighter: shiki
lineNumbers: false
info: |
  ## From Chatbot to Co-worker: Building and Using AI Agents
drawings:
  persist: false
transition: slide-left
title: From Chatbot to Co-worker
mdc: true
# Import custom styles
css: unocss
style: "@import './styles/style.css'; @import './styles/theme.css';"
layout: cover
---

# <span class="font-bold text-6xl leading-tight"> From Chatbot <br /> <span class="text-sky-500"> to Co-worker </span> </span>

## <span class="font-semibold text-xl">Agent Introduction and Practice</span>

<div class="pt-4 text-sm text-sky-500 font-semibold tracking-widest uppercase">
  Let AI become your true collaborator
</div>

---
layout: two-cols
---

# **Agenda**

<Timeline>

- **Part 01**: What is an AI Agent?
- **Part 02**: Evolution Path from Prompt to Agent
- **Part 03**: How to Use Agents Effectively?
- **Part 04**: Security Awareness

</Timeline>

::right::

<div class="pl-8">

<v-clicks>

**You will learn**

- What is an AI Agent
- From asking questions to letting AI do work
- Agent usage techniques
- How to build your own Agent

</v-clicks>

</div>

---
layout: part-title
part: 1
partTitle: What is an AI Agent?
partSubtitle: Understanding AI Agents
partDescription: From conversational AI to autonomous task-executing agents
totalParts: 4
---

---
layout: quote
class: text-center
quote: "Have you ever used AI tools?"
---

# **Have you ever used AI tools?**

---
layout: iframe
url: https://www.mentimeter.com/app/presentation/aly6gnke2jvdm3uf9kmmz1f7tn4bssbu/embed
---

---
layout: two-cols-header
---

# **Conversational AI vs AI Agent**

::left::

<div class="text-center pt-8">

<v-clicks>

### 🗣️ Conversational AI (Chat AI)

**Q&A Mode**

You ask a question

It gives an answer

Then you execute it yourself

</v-clicks>

</div>

::right::

<div class="text-center pt-8">

<v-clicks>

### 🤖 AI Agent

**Agent Mode**

You state a goal

It plans itself

It executes itself

It provides feedback

</v-clicks>

</div>

---

# **What is an AI Agent?**

<div class="pt-8">

Three core capabilities of an AI Agent:

<div class="grid grid-cols-3 gap-6 mt-8">

<div class="text-center p-4 rounded-lg bg-blue-500 bg-opacity-10">

<div class="text-4xl mb-2">👁️</div>

### **Perception**

Read external information like files, emails, webpages, calendars

</div>

<div class="text-center p-4 rounded-lg bg-sky-100 bg-opacity-50">

<div class="text-4xl mb-2">🧠</div>

### **Planning**

Break down large goals into multi-step tasks

</div>

<div class="text-center p-4 rounded-lg bg-sky-200 bg-opacity-40">

<div class="text-4xl mb-2">🦾</div>

### **Execution**

Operate tools—send emails, run code, control browsers

</div>

</div>

<div class="mt-12 p-6 bg-sky-50 bg-opacity-70 rounded-lg">

**AI Agent = LLM Brain + Tool Limbs + Memory System**

</div>

</div>

---

# **Agent's Three-Layer Architecture**

| Layer | English Name | Core Responsibility | Typical Capabilities |
|------|--------|----------|----------|
| Channel | Channel Layer | Receive and standardize external inputs | Parse message sources, extract context, route requests |
| Brain | Brain / Agent Loop | Understand goals and create execution plans | Task breakdown, step planning, tool selection, result evaluation |
| Execution | Body / Tools | Call tools and perform specific actions | File Read/Write, code execution, browser control, message sending |

---

# **Coding Agent and Agentic AI**

<div class="pt-8 grid grid-cols-2 gap-8">

<div class="p-6 rounded-lg bg-blue-500 bg-opacity-10">

### **💻 Coding Agent**

<div class="text-left mt-4 opacity-80">
Focusing on software development scenarios
- Read code
- Write code
- Run tests
- Submit PRs
</div>

<div class="mt-4 text-sm">
Representatives: Claude Code, Cursor, Devin, GitHub Copilot Agent
</div>

</div>

<div class="p-6 rounded-lg bg-sky-100 bg-opacity-50">

### **🌐 Agentic AI**

<div class="text-left mt-4 opacity-80">
Targeting broader business and life scenarios

- Research
- Book flights
- Make reports
- Send emails
</div>

<div class="mt-4 text-sm">
Representatives: ChatGPT Agent, Manus, Claude Cowork, OpenClaw
</div>

</div>

</div>

<div class="text-center mt-4 text-xl opacity-80">

**Common point: From "answering questions" to "completing tasks"**

</div>

---
layout: part-title
part: 2
partTitle: Evolution Path from Prompt to Agent
partSubtitle: Evolution Path
partDescription: Master the mindset shift from asking questions to getting AI to work for you
totalParts: 4
---

---

# **Four Stages**

<div class="pt-8">

<div class="grid grid-cols-4 gap-4 text-center">

<div class="p-4 rounded-lg bg-blue-500 bg-opacity-10">

### **Stage 1**

**Questioner**

Single-turn dialogue

</div>

<div class="p-4 rounded-lg bg-sky-100 bg-opacity-50">

### **Stage 2**

**Instructor**

Multi-round + Prompt design

</div>

<div class="p-4 rounded-lg bg-sky-50 bg-opacity-60">

### **Stage 3**

**Tool user**

LLM + Tools

</div>

<div class="p-4 rounded-lg bg-sky-200 bg-opacity-40">

### **Stage 4**

**Agent user**

Autonomous planning

</div>

</div>

</div>

---

# **Comparison of the Four Stages**

<div class="pt-8">

| Stage | Mode | What You Do | What AI Does |
|------|------|----------|-----------|
| **Stage 1** | Single-turn dialogue | Ask questions | Give answers |
| **Stage 2** | Multi-round + Prompt design | Write clear requirements, give context | Generate content, provide suggestions |
| **Stage 3** | LLM + Tools | Describe target, choose tools | Call tools, process results |
| **Stage 4** | Autonomous planning + Multi-step execution | Give goals and constraints | Autonomously break down, execute, provide feedback |

</div>

---

# **Core Transitions of Each Stage**

<div class="pt-6 flex flex-col gap-4 max-w-2xl">

<div class="p-5 rounded-xl border border-violet-300 bg-violet-50 bg-opacity-60">
  <div class="text-lg font-bold text-violet-600 mb-1">Stage 1 → 2</div>
  <div class="text-base font-semibold text-gray-800 mb-0.5">From "Asking randomly" to "Knowing how to ask"</div>
  <div class="text-sm font-normal text-gray-500">Learn to give AI enough context and constraints</div>
</div>

<div class="p-5 rounded-xl border border-sky-300 bg-sky-50 bg-opacity-60">
  <div class="text-lg font-bold text-sky-600 mb-1">Stage 2 → 3</div>
  <div class="text-base font-semibold text-gray-800 mb-0.5">From "Chatting" to "Working"</div>
  <div class="text-sm font-normal text-gray-500">Connect AI to real tools, not just text generation</div>
</div>

<div class="p-5 rounded-xl border border-emerald-300 bg-emerald-50 bg-opacity-60">
  <div class="text-lg font-bold text-emerald-600 mb-1">Stage 3 → 4</div>
  <div class="text-base font-semibold text-gray-800 mb-0.5">From "Single-step execution" to "Autonomous completion"</div>
  <div class="text-sm font-normal text-gray-500">Hand the goal over to the Agent, instead of monitoring every step</div>
</div>

</div>

---
layout: center
class: text-center
---

# **Which stage are you in now?**

<div class="pt-8 text-2xl opacity-80">

Most people are stuck between Stage 1~2

</div>

<div class="mt-12 p-8 bg-yellow-100 bg-opacity-30 rounded-lg max-w-4xl mx-auto">

What really unleashes the value of Agent is mastering the thinking mode of **Stage 3 and Stage 4**

</div>

<div class="mt-8 text-xl opacity-60">

It's not about letting AI write for you, but letting AI work for you

</div>

---
layout: part-title
part: 3
partTitle: How to Use Agents Effectively?
partSubtitle: Best Practices
partDescription: Assigning tasks, providing tools, setting rules
totalParts: 4
---

---
layout: center
---

# **Tip 1: Assign "Tasks", not "Questions"**

<div class="pt-8">

Most people are used to asking AI questions

But what an Agent needs is:

<div class="grid grid-cols-4 gap-4 mt-8">

<div class="p-4 rounded-lg bg-blue-500 bg-opacity-10 text-center">

### **🎯 Target**

</div>

<div class="p-4 rounded-lg bg-sky-100 bg-opacity-50 text-center">

### **📋 Context**

</div>

<div class="p-4 rounded-lg bg-sky-50 bg-opacity-60 text-center">

### **🔧 Constraints**

</div>

</div>

</div>

---

# **Inefficient Commands vs Efficient Commands**

<div class="pt-4">

| Inefficient Command | Efficient Command |
|---------|---------|
| "Help me write an email" | "Send an email to Teacher Zhang on my behalf, explaining my thesis defense is next Wednesday, ask him for feedback by 3pm Tuesday, with a formal yet friendly tone" |
| "Look up some info" | "Search for the top 3 domestic AI news of this week, summarize into a 200-word brief, and send it to my WeChat" |
| "Manage my schedule" | "Send me a daily schedule reminder at 8 AM every morning, if there are more than 3 tasks, help me rank them by importance" |

</div>

---

# **GTCA Command Structure**

<div class="pt-8">

<div class="grid grid-cols-4 gap-6">

<div class="text-center">

<span class="text-7xl text-blue-500 font-bold">G</span>

<div class="text-2xl text-blue-500 font-bold mt-4">Goal</div>

**What is the goal**

</div>

<div class="text-center">

<span class="text-7xl text-sky-500 font-bold">T</span>

<div class="text-2xl text-sky-500 font-bold mt-4">Tools</div>

**What tools can be used**

</div>

<div class="text-center">

<span class="text-7xl text-sky-400 font-bold">C</span>

<div class="text-2xl text-sky-400 font-bold mt-4">Context</div>

**Background information**


</div>

<div class="text-center">

<span class="text-7xl text-sky-300 font-bold">A</span>

<div class="text-2xl text-sky-300 font-bold mt-4">Action</div>

**Expected output format**

</div>

</div>

</div>

---

# **Tip 2: Let AI learn to use tools**

<div class="pt-8">

<div class="grid grid-cols-2 gap-8">

<div class="p-6 rounded-lg bg-blue-500 bg-opacity-10">

### **🔌 MCP Tools**

<div class="text-left mt-4">
- Open standards
- Connect external tools and data sources
- GitHub, Notion, Slack...
</div>

</div>

<div class="p-6 rounded-lg bg-sky-100 bg-opacity-50">

### **📦 Skills**

<div class="text-left mt-4">
- Reusable capability packages
- Encapsulate workflow methodologies
- PPT generation, financial report analysis...
</div>

</div>

</div>

</div>

---

# **MCP: Model Context Protocol**

<div class="pt-8">

<div class="max-w-4xl mx-auto">

<div class="p-8 bg-blue-500 bg-opacity-10 rounded-lg">

**MCP is to AI what USB-C is to hardware**

</div>

<div class="mt-8 grid grid-cols-2 gap-8">

<div>

### **Core Features**

- **Unified interface**: One protocol connects everything
- **Plug and play**: No need to write integration logic
- **Open standard**: Proposed by Anthropic

</div>

<div>

### **Common MCP Servers**

- GitHub
- Notion
- Slack
- Linear
- Figma
- Database
- File System

</div>

</div>

</div>

</div>

---

# **Skills: Reusable Capability Packages**

<div class="pt-8">

<div class="max-w-4xl mx-auto">

<div class="p-6 bg-sky-100 bg-opacity-50 rounded-lg mb-6">

A Skill = Documentation (SKILL.md) + Optional scripts/templates/reference materials

</div>

<div class="grid grid-cols-2 gap-6">

<div>

### **Characteristics**

- Loaded on-demand, does not occupy main context
- Composable, shareable, versionable
- Encapsulates professional knowledge

</div>

<div>

### **Typical Examples**

- PPT generation
- PDF processing
- Financial report analysis
- Brand style writing
- Data visualization

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

**Channel for connecting external tools**

<div class="mt-4 text-left">
- Connect real systems
- Call external APIs
- Access data sources
</div>

</div>

<div class="p-8 rounded-lg bg-sky-100 bg-opacity-50">

### **📦 Skills**

**Encapsulated practical methodologies**

<div class="mt-4 text-left">
- Knowledge and process
- Best practices
- Working patterns
</div>

</div>

</div>

</div>

---

# **How to use Skills well**

<div class="pt-8">

<div class="grid grid-cols-2 gap-6">

<div class="p-4 rounded-lg bg-blue-500 bg-opacity-10">

### **🎯 Focus on single scenario**

A Skill solves only one type of problem

</div>

<div class="p-4 rounded-lg bg-sky-100 bg-opacity-50">

### **📝 Write clear trigger conditions**

Clarify "when to use it"

</div>

<div class="p-4 rounded-lg bg-sky-50 bg-opacity-60">

### **🔗 Make good use of combination**

String them together to complete complex tasks

</div>

<div class="p-4 rounded-lg bg-sky-200 bg-opacity-40">

### **📦 Start with templates**

Reuse official or community Skills

</div>

</div>

</div>

---

# **Make Your Own Skills**

<div class="pt-8">

<div class="p-6 bg-sky-50 bg-opacity-70 rounded-lg max-w-4xl mx-auto mb-8">

**The greatest value of Skills is not using what others have written, but encoding your own workflow into it**

</div>

<div class="text-left max-w-3xl mx-auto">

```
my-skill/
├── SKILL.md          ← Required: Trigger conditions + Operational steps + Output formats
├── template.md       ← Optional: Output template
└── example.txt       ← Optional: Reference examples
```

</div>

</div>

---

# **SKILL.md Four-Part Writing Method**

<div class="pt-4">

<div class="grid grid-cols-2 gap-8">

<div class="text-left">

```markdown {all|1-2|4-5|7-10|12-13|all}
## When to use
Trigger this Skill when the user needs to write a weekly work report.

## Goal
Generate a well-structured, focus-highlighted weekly report, suitable for sending to the direct supervisor.

## Steps
1. Ask what tasks were completed this week
2. Ask about next week's plans and current blockers
3. Organize into three parts: "Achievements / Next Week / Support Needed"
4. Formal tone, no more than 3 items per section, start with verbs

## Output format
Markdown, with heading levels, total words under 300
```

</div>

<div class="text-left relative" style="min-height: 220px;">

<div v-click="1" v-click-hide="2" class="absolute inset-0 p-4 rounded-lg bg-blue-500 bg-opacity-10">

### **📌 When to use**

**Tell the Agent when to use this Skill**

- Clear trigger scenarios
- Prevent false triggers
- Ensure load in the appropriate context

</div>

<div v-click="2" v-click-hide="3" class="absolute inset-0 p-4 rounded-lg bg-sky-100 bg-opacity-50">

### **🎯 Goal**

**Define what goal this Skill wants to achieve**

- Clear expected results
- Evaluation criteria
- Alignment with user intent

</div>

<div v-click="3" v-click-hide="4" class="absolute inset-0 p-4 rounded-lg bg-sky-50 bg-opacity-60">

### **📋 Steps**

**Give specific operational steps and processes**

- Executable sequence of steps
- Key decision points
- Best practice experiences

</div>

<div v-click="4" class="absolute inset-0 p-4 rounded-lg bg-sky-200 bg-opacity-40">

### **📤 Output format**

**Define the format and specification of the output**

- Output structure requirements
- Format constraints
- Quality standards

</div>

</div>

</div>

</div>

---

# **Three-Step Start Method**

<div class="pt-8">

<div class="grid grid-cols-3 gap-8">

<div class="text-center">

**<span class="text-6xl text-blue-500 font-bold">Step 1</span>**

<div class="text-3xl text-blue-500 font-bold mt-4">Identify recurring tasks</div>

<div class="mt-4 opacity-70">
Find something you repeat every week
</div>

<div class="opacity-60 mt-2">
Writing reports, organizing meeting notes, sending follow-up emails...
</div>

</div>

<div class="text-center">

**<span class="text-6xl text-sky-500 font-bold">Step 2</span>**

<div class="text-3xl text-sky-500 font-bold mt-4">Deconstruct Prompt</div>

<div class="mt-4 opacity-70">
Paste the Prompt you normally use
</div>

<div class="opacity-60 mt-2">
Break it into "Trigger conditions + Steps + Output formats"
</div>

</div>

<div class="text-center">

**<span class="text-6xl text-sky-400 font-bold">Step 3</span>**

<div class="text-3xl text-sky-400 font-bold mt-4">Test and iterate</div>

<div class="mt-4 opacity-70">
Save as SKILL.md
</div>

<div class="opacity-60 mt-2">
Load in Claude, run it once, modify according to output
</div>

</div>

</div>

</div>

---

# **Skill Scenarios Suitable for Customization**

<div class="pt-8">

| Scenario | Skill Name | Core Value |
|------|-----------|---------|
| Weekly Report | weekly-report | Unified style, eliminate formatting adjustments |
| Meeting Notes | meeting-notes | Automatically extract Action Items |
| Email Drafting | email-drafter | Maintain usual tone and signature style |
| Competitor Analysis | competitor-research | Fixed analytical framework, output is comparable |
| Book/Article Summary | article-summary | Unified summary structure, easy to archive |

</div>

---

# **Tip 3: Instruction / Rule**

<div class="pt-8">

<div class="max-w-4xl mx-auto">


If Skills are "an operations manual to the Agent"

Then Instruction / Rule is **"setting the rules for the Agent"**

For Claude Code / Cowork, it's `CLAUDE.md`

For OpenClaw, it's `CONFIG.md`

For Codex, it's `AGENT.md`

<div class="grid grid-cols-2 gap-6">

<div class="p-4 rounded-lg bg-blue-400 bg-opacity-10">

### **Instruction**

<div class="text-left mt-2">
Tell Agent who it is, what the goal is
</div>

Biased towards identity and role setting

</div>

<div class="p-4 rounded-lg bg-sky-100 bg-opacity-50">

### **Rule**

<div class="text-left mt-2">
Constrain the behavioral boundary of the Agent
</div>

Biased towards "what can/cannot be done"

</div>

</div>

</div>

</div>

---

# **Five Types of Common Rules**

<div class="pt-8">

| Type | Example |
|------|------|
| **Identity Setting** | "You are my personal work assistant named Xiaobai, familiar with my working habits" |
| **Language Style** | "Keep all replies in English, professional terms should stick to their original words, keep an objective and concise tone" |
| **Output format** | "Always put conclusion first in suggestions, followed by reasons, up to 3 points, numbered" |
| **Behavior Boundary** | "Don't initiate sending out any external messages, you must confirm the operation details with me before executing" |
| **Priority Logic** | "If I say 'Urgent', skip background analysis, supply executable plan straight away" |

</div>

---

# **Complete Instruction Example**

<div class="pt-4 text-left max-w-4xl mx-auto">

```
You are my personal efficiency assistant, named Xiaobai.

[Role]
You know my work background (Product Manager for a B2B SaaS product),
familiar with my daily workflow, including writing PRDs, doing competitor analysis, preparing weekly reports.

[Style]
- Reply in English, brief and direct, don't use openers like "Sure" "No problem"
- Technical terms retain English abbreviations (e.g. API, DAU, MRR)
- Keep each reply under 200 words unless I ask for details

[Behavior Boundary]
- Involves sending emails, submitting documents and other external operations, must list operation content for me to confirm first
- Do not actively recommend paid tools or services

[Priority]
- When I say "Urgent", give the plan right away, skip analysis
- When I say "Detailed", expand on all details and evidence
```

</div>

---

# **Four Principles of Writing Good Rules**

<div class="pt-8">

<div class="grid grid-cols-2 gap-6">

<div class="p-6 rounded-lg bg-blue-500 bg-opacity-10">

### **1️⃣ Specific Over Abstract**

"Short reply" is worse than "Reply no more than 150 words"

</div>

<div class="p-6 rounded-lg bg-sky-100 bg-opacity-50">

### **2️⃣ Positive Descriptions**

Saying "Only do X" is more effective than "Don't do Y"

</div>

<div class="p-6 rounded-lg bg-sky-50 bg-opacity-60">

### **3️⃣ Don't Get Greedy**

5 precise rules > 20 vague requirements

</div>

<div class="p-6 rounded-lg bg-sky-200 bg-opacity-40">

### **4️⃣ Constant Iteration**

Update and iterate along with changing habits

</div>

</div>

</div>

---
layout: part-title
part: 4
partTitle: Security Awareness
partSubtitle: Security & Safety
partDescription: Minimum privilege principle, low risk first, periodic review
totalParts: 4
---

---

# **Three Security Principles**

<div class="pt-8">

<div class="space-y-4">

<div class="p-4 rounded-lg bg-sky-400 bg-opacity-20">

### **🔐 Principle of Least Privilege**

<div class="text-xl mt-2">
Only give the Agent the permissions it truly needs
</div>

</div>

<div class="p-4 rounded-lg bg-sky-50 bg-opacity-60">

### **🧪 Test Low-Risk First**

<div class="text-xl mt-2">
Test with non-sensitive tasks first before granting higher privileges
</div>

</div>

<div class="p-4 rounded-lg bg-blue-500 bg-opacity-10">

### **🔍 Periodic Review**

<div class="text-xl mt-2">
Check what the Agent is doing rather than completely letting go
</div>

</div>

</div>

</div>

---
layout: center
class: text-center
---

# **Summary**

<div class="pt-8">

<div class="max-w-6xl mx-auto grid grid-cols-3 gap-6">

<div class="text-left p-4 rounded-lg bg-blue-500 bg-opacity-10 h-full">

### **Core of AI Agent**

**LLM Brain + Tool Limbs + Memory System**

From "Answering Questions" to "Completing Tasks"

</div>

<div class="text-left p-4 rounded-lg bg-sky-100 bg-opacity-50 h-full">

### **Key to Using Agent**

**Assign tasks + Provide tools + Set rules**

It's not about having AI write for you, but having AI work for you

</div>

<div class="text-left p-4 rounded-lg bg-sky-50 bg-opacity-60 h-full">

### **Security First**

**Least privilege + Low-risk testing + Periodic review**

</div>

</div>

</div>

---
layout: center
class: text-center
---

# <span class="text-6xl font-bold text-blue-500"> THAT IS ALL! </span>

<div class="text-xl opacity-80">

Starting today, let AI be your true collaborator

</div>
