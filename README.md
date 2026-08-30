<div align="center">

# 🏇 Awesome Harness Engineering 中文版

**驾驭工程 — 当代码不再由人类手写，工程师的核心能力是什么？**

[![Awesome](https://img.shields.io/badge/Awesome-🏇_Harness-ff6d00?style=for-the-badge)](https://github.com/whobot-ai/awesome-harness-engineering-zh)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=for-the-badge)](https://github.com/whobot-ai/awesome-harness-engineering-zh/pulls)

---

*Prompt Engineering 教我们如何说话，Context Engineering 教我们该看什么，*
*Harness Engineering 教我们如何建造一个世界，让 AI 在其中不会迷路。*

</div>

> **一句话理解 Harness Engineering：** 不是写更好的提示词，不是喂更多的上下文，而是**建造一个环境**——让 AI 智能体在其中只能做对的事。就像铁轨之于火车：火车的动力再强，没有铁轨它哪儿也去不了。

---

## 📖 目录

- [核心洞察：为什么 Harness Engineering 是必然](#-核心洞察为什么-harness-engineering-是必然)
- [概念演进：三个时代](#-概念演进三个时代)
- [术语表](#-术语表)
- [奠基之作](#-奠基之作)
- [官方深度文章](#-官方深度文章)
- [名人观点与 X 热议](#-名人观点与-x-热议)
- [五大核心支柱](#-五大核心支柱)
- [核心原则](#-核心原则)
- [行业 Harness 实践对比](#-行业-harness-实践对比)
- [Context 管理：Harness 的核心战场](#-context-管理harness-的核心战场)
- [高价值开源项目](#-高价值开源项目)
- [深度文章与分析](#-深度文章与分析)
- [中文社区资源](#-中文社区资源)
- [论文与学术研究](#-论文与学术研究)
- [工具链与实践框架](#-工具链与实践框架)
- [Harness Engineer 技能图谱](#-harness-engineer-技能图谱)
- [The Bitter Lesson：保持轻量，准备重构](#-the-bitter-lesson保持轻量准备重构)

---

## 🧠 核心洞察：为什么 Harness Engineering 是必然

传统软件工程的核心假设是：**代码由人类编写，由机器执行。** 整个工程体系——代码审查、设计模式、架构原则——都围绕这个假设构建。

Harness Engineering 诞生于一个根本性的范式转移：**代码由 AI 编写，由人类审查，由机器执行。** 当"编写者"从人类变为 AI 智能体时，工程师的角色从"建造者"变为"建筑师+质检员"——你不再砌砖，你设计蓝图并确保每块砖都砌对了地方。

这不是一个渐进式的效率提升，这是软件工程的**相变**。

### 类比理解

| 领域 | 类比 |
|------|------|
| **赛马** | 骑师不替马跑步，但决定方向、节奏和策略。Harness（马具）让马的力量为骑师所用 |
| **铁路** | 蒸汽机的发明不够，还需要铁轨、信号系统、调度中心。Harness 就是 AI 的铁路基础设施 |
| **交通规则** | 汽车越强大，交通规则越重要。AI 越聪明，Harness 越关键 |

> *"The model is the engine. The harness is the road, the guardrails, and the GPS."*
> — 社区共识

---

## 📐 概念演进：三个时代

```
2023 ─── Prompt Engineering ──→ "怎么跟 AI 说话"
              │
              │  我们发现：说什么不够，AI 需要看到正确的东西
              ▼
2025 ─── Context Engineering ──→ "给 AI 看什么信息"
              │
              │  我们发现：看到正确的东西也不够，AI 需要在正确的环境中工作
              ▼
2026 ─── Harness Engineering ──→ "构建什么环境让 AI 可靠地工作"
```

| 维度 | Prompt Engineering | Context Engineering | Harness Engineering |
|------|-------------------|--------------------|--------------------|
| **核心问题** | 怎么措辞 | 怎么组织信息 | 怎么设计系统 |
| **作用对象** | 单次对话 | 单次任务 | 持续运行的工作流 |
| **产出物** | 提示词模板 | RAG 管道、上下文窗口策略 | AGENTS.md、CI 规则、多智能体架构、反馈回路 |
| **失败模式** | AI 理解错了意图 | AI 缺少关键信息 | AI 在无约束环境中漂移 |
| **工程师角色** | 翻译官 | 信息架构师 | 系统架构师 |
| **类比** | 写信 | 整理档案 | 建造城市 |

> **关键洞察：** 这三个阶段不是替代关系，而是包含关系。Harness Engineering 包含了 Context Engineering，而 Context Engineering 包含了 Prompt Engineering。每一层都是前一层的超集。

---

## 📖 术语表

> 理解这些术语是进入 Harness Engineering 领域的第一步。

| 术语 | 英文 | 定义 |
|------|------|------|
| **Harness** | Agent Harness | 包裹 AI 模型的完整基础设施 — 工具、护栏、反馈循环、可观测层 |
| **上下文退化** | Context Degradation | 模型在长任务中随 context 填满而失去连贯性的现象 |
| **上下文焦虑** | Context Anxiety | 模型感知到 context 即将耗尽时过早结束工作的倾向 |
| **压缩** | Context Compaction | 智能摘要 context 以防止溢出的技术 |
| **护栏** | Guardrails | 限制 Agent 行为的确定性规则层 |
| **反馈循环** | Feedback Loop | Agent 检查自身输出并自我纠错的循环机制 |
| **人在回路** | Human-in-the-Loop (HITL) | 在关键决策点由人类提供监督的模式 |
| **文件交接** | File-based Handoff | Agent 间通过文件（而非对话）传递信息的通信模式 |
| **初始化 Agent** | Initializer Agent | 在第一个 session 中建立环境和上下文的专门 Agent |
| **生成-评估模式** | Generator-Evaluator Pattern | 受 GAN 启发，将生成和评估分离的多 Agent 架构模式 |
| **冲刺合约** | Sprint Contract | Generator 和 Evaluator 之间协商的、可测试的实现合约 |
| **Ralph 循环** | Ralph Loop | 拦截 Agent 退出尝试，在干净 context 中重新注入 prompt 的模式 |
| **渐进式发现** | Progressive Disclosure | 选择性加载工具而非一次全部加载的 context 管理策略 |
| **熵管理** | Entropy Management | 主动对抗系统随时间退化（文档不一致、架构违规）的维护机制 |
| **Hooks** | Lifecycle Hooks | 在 Agent 生命周期关键点执行自定义脚本的机制 |
| **沙箱** | Sandboxed Environment | 隔离的执行环境，提供安全性和可扩展性 |
| **苦涩教训** | The Bitter Lesson | Rich Sutton 的观点 — 利用计算的通用方法最终胜过人工设计；在 Harness 中意味着保持轻量、准备随模型进步而重构 |

**核心公式：**

```
Agent = Model + Harness
```

> 一个裸模型不是 Agent。当 Harness 赋予它状态管理、工具执行、反馈循环和可执行约束后，它才变成 Agent。

**计算机架构类比：**

| Harness 概念 | 计算机类比 |
|-------------|-----------|
| Model | CPU（算力） |
| Context Window | RAM（工作内存） |
| Agent Harness | 操作系统（调度与管理） |
| Agent | 应用程序 |

---

## 🏛️ 奠基之作

### Mitchell Hashimoto — 概念命名者

**[My AI Adoption Journey](https://mitchellh.com/writing/my-ai-adoption-journey)** — 2026年2月5日

> *"Every time you discover an agent has made a mistake, you take the time to engineer a solution so that it can never make that mistake again."*

Mitchell Hashimoto，HashiCorp 联合创始人、Terraform 创造者。他在这篇文章中首次明确命名了 "Harness Engineering" 这个概念。

**核心洞察：**

- 智能体犯的每一个错误，都应该转化为一条永久性的约束规则
- 不是修复 bug，而是**修复环境**——让这类 bug 在结构上不可能再次发生
- 好的 Harness 是一部"组织智慧的活文档"，它把团队的隐性知识显性化

**为什么这篇文章重要：** 它把散落在各个团队中的实践，统一为一个有名字的工程学科。命名即存在——一旦一种实践有了名字，它就能被教授、被讨论、被系统化。

---

## 📚 官方深度文章

### Anthropic（2 篇）

#### 1. Effective Harnesses for Long-Running Agents

**[原文链接](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)** — Justin Young · 2025年11月

**提出：Initializer Agent + Coding Agent 双代理架构**

```
┌──────────────────┐     claude-progress.txt     ┌──────────────────┐
│  Initializer     │ ──────────────────────────→ │  Coding Agent    │
│  Agent           │                              │                  │
│  · 分析仓库结构    │     git history 作为        │  · 执行具体编码    │
│  · 制定计划       │     跨 session 状态层        │  · 增量提交       │
│  · 写入进度文件    │ ←────────────────────────── │  · 更新进度       │
└──────────────────┘                              └──────────────────┘
```

**核心创新：**
- `claude-progress.txt` 文件作为智能体间的通信协议
- Git history 作为天然的状态持久层，智能体崩溃后可从最近的 commit 恢复
- 将一个不可靠的长任务，拆解为多个可靠的短任务

**哲学意义：** 这篇文章回答了一个根本性问题——**AI 智能体如何拥有"记忆"？** 答案不是更大的上下文窗口，而是把记忆外化为文件系统和 Git 历史。这与人类文明的发展惊人地相似：我们也是通过文字和书籍，把知识从大脑中外化出来。

---

#### 2. Harness Design for Long-Running Application Development

**[原文链接](https://www.anthropic.com/engineering/harness-design-long-running-apps)** — Prithvi Rajasekaran · 2026年3月

**提出：Planner-Generator-Evaluator 三代理架构（受 GAN 启发）**

```
        ┌─────────────┐
        │   Planner   │   制定 Sprint Contract
        └──────┬──────┘
               │
        ┌──────▼──────┐
        │  Generator  │   执行编码
        └──────┬──────┘
               │
        ┌──────▼──────┐
        │  Evaluator  │   验证 + 反馈
        └──────┬──────┘
               │
               └──→ 不满足？回到 Generator
```

**实验数据：**

| 架构 | 耗时 | 成本 | 结果 |
|------|------|------|------|
| 单代理 | 20 分钟 | $9 | 功能不可用，严重漂移 |
| 三代理 | 6 小时 | $200 | 功能完善的全栈应用 |

**核心创新：Sprint Contracts（冲刺合约）** — 借鉴 Scrum 的 Sprint 概念，把模糊的大目标拆解为有明确验收标准的小合约。每个合约都是可验证的。

**哲学意义：** 这篇文章证明了一个反直觉的观点——**更多的约束产生更好的结果。** 单代理拥有完全的自由，反而漂移失败；三代理互相约束，反而产出优秀。这与人类社会的治理逻辑完全一致：三权分立比独裁更稳定。

---

### OpenAI（2 篇）

#### 1. Harness Engineering: Leveraging Codex in an Agent-First World

**[原文链接](https://openai.com/index/harness-engineering/)**

**震撼数据：**
- 5 个月内，3 名工程师用 Codex 生成了约 **100 万行代码**
- 零手写代码
- 平均每人每天 3.5 个 PR，共合并约 1500 个 PR
- 效率提升约 **10 倍**

**哲学意义：** 这不仅是效率数据，这是对"软件工程师"这个职业的重新定义。当 3 个人可以产出 30 个人的代码量时，剩余的 27 个人该做什么？答案是：**他们应该成为 Harness Engineer——设计、维护和优化 AI 工作的环境。**

---

#### 2. Unlocking the Codex Harness: How We Built the App Server

**[原文链接](https://openai.com/index/unlocking-the-codex-harness/)**

OpenAI 内部实践的深度复盘：如何用 Codex 构建 Codex 自身的 App Server。一个精彩的"自举"（bootstrap）案例——用 AI 编码工具来构建 AI 编码工具本身。

---

### Google / DeepMind

#### Conductor — Context-Driven Development for Gemini CLI

**[原文链接](https://developers.googleblog.com/conductor-introducing-context-driven-development-for-gemini-cli/)**

Google 没有直接使用 "Harness Engineering" 这个术语，但通过 **Conductor** 项目实践了完全相同的理念：

```
Context（理解）→ Spec & Plan（规划）→ Implement（执行）
```

- 使用 Markdown 文件作为状态持久层
- 支持跨 session 恢复
- 严格的工作流约束：不理解就不规划，不规划就不动手

---

## 🗣️ 名人观点与 X 热议

### 行业领袖

| 人物 | 身份 | 核心观点 |
|------|------|----------|
| **Mitchell Hashimoto** | HashiCorp 联合创始人、Terraform 创造者 | 命名者。"每次智能体犯错，都应该被工程化为一条永久约束" |
| **Sam Altman** | OpenAI CEO | 称 Codex 桌面端是 "the most loved internal product we've ever had" |
| **Greg Brockman** | OpenAI 联合创始人 | 建议每个团队指定一名 "Agents Captain" 负责设计智能体工作流 |
| **Andrej Karpathy** | 前 OpenAI 联合创始人 | 提出 "Agentic Engineering" 术语，强调 **"模型不如 harness 重要"** |
| **Martin Fowler** | 软件工程泰斗 | 将 Harness Engineering 解构为三部分：Context Engineering + Architecture Constraints + Entropy Management |

### Andrej Karpathy 的深刻洞察

> *"The most important skill in AI engineering is not prompt writing. It's building the right harness — the constraints, the feedback loops, the recovery mechanisms."*

Karpathy 的观点代表了一个重要转折：当连 AI 研究的顶尖人物都说"模型不如环境重要"时，说明 Harness Engineering 不是营销概念，而是**工程现实**。

### Martin Fowler 的理论框架

**[Harness Engineering](https://martinfowler.com/articles/exploring-gen-ai/harness-engineering.html)** — Martin Fowler & Birgitta Böckeler

Fowler 将 Harness Engineering 解构为三个正交维度：

```
Harness Engineering
├── Context Engineering    — 给 AI 正确的信息
├── Architecture Constraints — 让 AI 只能做正确的事
└── Entropy Management     — 持续对抗系统退化
```

**哲学意义：** Fowler 引入了"熵管理"（Entropy Management）的概念——AI 生成的代码会自然趋向混乱，就像热力学第二定律。Harness Engineer 的职责之一，就是**持续对抗这种熵增**。这让 Harness Engineering 从一个工程实践上升为一种**信息论视角**。

---

## 🏗️ 五大核心支柱

> 综合 Anthropic、LangChain、NxCode 等来源，Harness Engineering 可归纳为五大支柱。

### 支柱一：工具编排（Tool Orchestration）

明确定义 Agent 可以访问哪些工具、如何调用、需要什么权限。

```
工具注册 → 权限边界 → 调用协议 → 结果处理
```

### 支柱二：护栏与安全约束（Guardrails）

多层级的确定性规则：

| 层级 | 示例 |
|------|------|
| **权限边界** | 限制文件/命令访问 |
| **验证检查** | 使用 linter 和测试套件 |
| **架构约束** | 强制结构性规则 |
| **速率限制** | 防止无限循环 |

> 反直觉发现：**更多约束往往产生更高可靠性，而非更低。**

### 支柱三：错误恢复与反馈循环（Feedback Loops）

- 自动重试逻辑（带递增策略）
- 自我验证循环（Agent 检查自己的工作）
- 回滚机制（恢复到之前的状态）
- 循环检测（识别卡住的模式）

> **LangChain 实证：仅通过 Harness 变更（非模型变更），将编码 Agent 的性能从 52.8% 提升到 66.5%。** 这个数据证明了 Harness 的独立价值 — 即使模型不变，更好的 Harness 也能带来显著提升。

### 支柱四：可观测性（Observability）

- 每个 Agent 动作和工具调用的日志
- Token 使用量和成本追踪
- 决策点和异常监控
- 跨 session 的进度追踪

### 支柱五：人机协作检查点（Human-in-the-Loop）

在关键时刻由人类提供监督的战略性决策点 — 从显式审批门到高风险时刻的定期进度审查。不是所有决策都需要人类参与，但**高风险决策必须有人类把关**。

---

## ⚖️ 核心原则

> 以下八大原则综合自 Mitchell Hashimoto、Anthropic、OpenAI 的实践，以及社区共识。

### 1. 人类掌舵，智能体执行

工程师定义方向、审查结果、设计环境。智能体在环境中执行。不是取代人类，而是**重新分工**。

### 2. 仓库即唯一事实来源

智能体无法参加站会，无法阅读 Slack，无法理解口头约定。**仓库中没有的知识，对智能体来说就不存在。** 因此，所有隐性知识必须被显性化为代码、文档或配置。

### 3. AGENTS.md 是目录，不是百科全书

不要试图在一个文件里塞入所有知识。AGENTS.md 应该像图书馆的索引——指向深层的真相源（架构文档、测试策略、API 规范），而不是复制它们。

### 4. 用机械手段执行架构约束

不要指望智能体"理解"你的架构风格。用 linter、类型检查、结构测试、CI 检查来**机械化地**执行约束。如果一个规则可以被自动检查，就不应该只写在文档里。

### 5. 智能体可读性优先于人类可读性

传统的"代码可读性"是为人类优化的。Harness Engineering 要求**同时为智能体优化可读性**——清晰的文件命名、一致的代码结构、显式的依赖关系。

### 6. 更少但更强表达力的工具

不要给智能体 100 个弱工具，给它 10 个强工具。每个工具都应该有明确的输入输出契约和错误处理。**渐进式发现胜过工具爆炸。**

### 7. 像智能体一样思考

观察你的智能体在哪里挣扎、在哪里犯错、在哪里停顿。这些挣扎点就是你的 harness 需要改进的地方。**每一次智能体的失败，都是 harness 的 bug。**

### 8. 纠正成本低，等待成本高

不要设置过重的审查门控。AI 生成的代码修复成本很低（让 AI 重新生成即可），但等待人类逐行审查的时间成本很高。**Fix-forward 优于 Block-and-wait。**

---

## 🔬 行业 Harness 实践对比

> 各家对 Harness 的实现路径不同，但核心理念一致：**约束即可靠性**。

| 产品 | 核心 Harness 机制 | 设计哲学 |
|------|-------------------|----------|
| **Claude Code** | 默认只读 → 显式用户审批；自动快照使所有编辑可逆；Hooks 系统在生命周期关键点执行自定义脚本；CLAUDE.md 提供持久项目上下文 | 安全第一，渐进信任 |
| **OpenAI Codex** | AGENTS.md 作为机器可读指令；可复现的隔离 worktree 环境；CI 强制的机械不变量维护架构边界 | 隔离执行，机械约束 |
| **Cursor** | `.cursor/rules` 文件包含持久 Markdown 指令；版本控制的、按文件模式匹配的规则 | 规则即代码，精准匹配 |
| **Vercel** | 删除了 80% 的 Agent 工具，减少步骤和 token 消耗 | **少即是多** |

### Claude Code 本身就是一个 Harness

这是一个重要的元认知：Claude Code 不只是一个编码工具，它是 Claude 模型之上的 **agentic harness 典范实现**：

| Claude Code 组件 | Harness 角色 |
|-----------------|-------------|
| Read / Write / Edit / Bash | 工具编排层 |
| 默认只读 + 用户审批 | 护栏与安全层 |
| Hooks 系统 | 生命周期管理 |
| CLAUDE.md | 持久化上下文 |
| Sub-agent 架构 | 多智能体编排 |
| 自动快照 | 错误恢复机制 |
| Context 自动压缩 | 熵管理 |

> 当你使用 Claude Code 时，你已经在使用 Harness Engineering 的产物。**理解这一点，是从"使用者"进化为"设计者"的第一步。**

---

## 🧩 Context 管理：Harness 的核心战场

> 长期运行的 Agent 面临的最大挑战是跨 context window 的连续性。这是 Harness Engineer 需要解决的最核心技术问题。

### 文件系统作为持久化层

| 机制 | 说明 |
|------|------|
| **Progress Files** | `claude-progress.txt` 记录工作历史，新 session 启动时读取 |
| **Feature Lists** | JSON 格式的功能规格带 pass/fail 状态 |
| **Git Commits** | 描述性提交消息维护代码状态历史 |
| **File-based Handoff** | Agent 间通过文件通信，避免对话长度爆炸 |

### Context 压缩与管理策略

| 策略 | 说明 | 适用场景 |
|------|------|----------|
| **Compaction** | 智能摘要 context 防止溢出 | 长对话 |
| **Tool Output Offloading** | 将完整输出存储到文件系统以减少噪音 | 大量工具调用 |
| **Progressive Disclosure** | 选择性加载工具而非一次全部加载 | 工具数量多 |
| **Ralph Loop** | 拦截退出尝试，在干净 context 中重新注入 prompt | Agent 过早放弃 |

### Session 启动标准流程

每个新 session 的启动序列 — 这是 Harness 最基础的"仪式"：

```
1. 检查工作目录状态
2. 审查 git log 和 progress 文件
3. 选择下一个未完成功能
4. 运行基础功能测试确认环境正常
5. 开始编码
```

> **哲学意义：** 这个流程让每个 session 都是"无状态"的——任何一个 session 崩溃，下一个 session 都能从上一个 commit 无缝恢复。这与微服务的无状态设计原则完全一致。

---

## 🔥 高价值开源项目

### 知识与学习

| 名称 | 说明 | Stars |
|------|------|-------|
| [**awesome-agent-harness**](https://github.com/AutoJunjie/awesome-agent-harness) | 最全面的 Harness Engineering 资源列表，11 个分类、50+ 工具 | ![Stars](https://img.shields.io/github/stars/AutoJunjie/awesome-agent-harness?style=flat-square&logo=github) |
| [**learn-claude-code**](https://github.com/shareAI-lab/learn-claude-code) | 中文学习资源，12 节课从零学 harness engineering | ![Stars](https://img.shields.io/github/stars/shareAI-lab/learn-claude-code?style=flat-square&logo=github) |
| [**harness-engineering**](https://github.com/deusyu/harness-engineering) | 中文学习指南，概念理解到实践 | ![Stars](https://img.shields.io/github/stars/deusyu/harness-engineering?style=flat-square&logo=github) |
| [**claude-code-best-practices**](https://github.com/anthropics/anthropic-cookbook) | Anthropic 官方 Cookbook，含 Harness 设计最佳实践 | ![Stars](https://img.shields.io/github/stars/anthropics/anthropic-cookbook?style=flat-square&logo=github) |

### Harness 框架与工具

| 名称 | 说明 | Stars |
|------|------|-------|
| [**claude-code-harness**](https://github.com/Chachamaru127/claude-code-harness) | Claude Code 专用开发 harness — Plan → Work → Review 自动循环 | ![Stars](https://img.shields.io/github/stars/Chachamaru127/claude-code-harness?style=flat-square&logo=github) |
| [**Conductor**](https://github.com/google-gemini/conductor) | Google 官方 Gemini CLI 扩展 — Context-Driven Development 工作流 | ![Stars](https://img.shields.io/github/stars/google-gemini/conductor?style=flat-square&logo=github) |
| [**planning-with-files**](https://github.com/OthmanAdi/planning-with-files) | Manus 风格持久化 Markdown 规划技能 — 跨 session 状态管理 | ![Stars](https://img.shields.io/github/stars/OthmanAdi/planning-with-files?style=flat-square&logo=github) |
| [**context-mode**](https://github.com/mksglu/context-mode) | 上下文虚拟化层 — 智能体运行时的上下文管理 | ![Stars](https://img.shields.io/github/stars/mksglu/context-mode?style=flat-square&logo=github) |
| [**SandBase Harness**](https://github.com/sandbaseai/sandbase-harness) | 本地优先的 Agent 运行时 — 持久化会话、MCP 工具治理、审批、审计回放与可替换沙箱后端 | ![Stars](https://img.shields.io/github/stars/sandbaseai/sandbase-harness?style=flat-square&logo=github) |
| [**lossless-claw**](https://github.com/Martian-Engineering/lossless-claw) | 无损上下文管理 — 防止长对话中的信息丢失 | ![Stars](https://img.shields.io/github/stars/Martian-Engineering/lossless-claw?style=flat-square&logo=github) |

### 记忆与状态持久化

| 名称 | 说明 | Stars |
|------|------|-------|
| [**memU**](https://github.com/NevaMind-AI/memU) | 面向 24/7 主动 Agent 的记忆系统 — Harness 的核心基础设施 | ![Stars](https://img.shields.io/github/stars/NevaMind-AI/memU?style=flat-square&logo=github) |
| [**OpenViking**](https://github.com/volcengine/OpenViking) | 火山引擎开源 AI Agent 上下文数据库 | ![Stars](https://img.shields.io/github/stars/volcengine/OpenViking?style=flat-square&logo=github) |
| [**MemOS**](https://github.com/MemTensor/MemOS) | AI 记忆操作系统 — 为智能体提供结构化记忆能力 | ![Stars](https://img.shields.io/github/stars/MemTensor/MemOS?style=flat-square&logo=github) |
| [**EverMemOS**](https://github.com/EverMind-AI/EverMemOS) | Agent 记忆操作系统 — 长期记忆与经验积累 | ![Stars](https://img.shields.io/github/stars/EverMind-AI/EverMemOS?style=flat-square&logo=github) |

### 多智能体编排

| 名称 | 说明 | Stars |
|------|------|-------|
| [**openfang**](https://github.com/RightNow-AI/openfang) | 开源 Agent 操作系统 — 多智能体协作基础设施 | ![Stars](https://img.shields.io/github/stars/RightNow-AI/openfang?style=flat-square&logo=github) |
| [**mission-control**](https://github.com/builderz-labs/mission-control) | AI Agent 编排仪表盘 — 可视化管理多智能体工作流 | ![Stars](https://img.shields.io/github/stars/builderz-labs/mission-control?style=flat-square&logo=github) |
| [**manifest**](https://github.com/mnfst/manifest) | 智能 LLM 路由 — 最高降本 70%，多模型协同的关键基础设施 | ![Stars](https://img.shields.io/github/stars/mnfst/manifest?style=flat-square&logo=github) |

### 安全与质量保障

| 名称 | 说明 | Stars |
|------|------|-------|
| [**AI-Infra-Guard**](https://github.com/Tencent/AI-Infra-Guard) | 腾讯 AI 红队平台 — 智能体安全扫描 | ![Stars](https://img.shields.io/github/stars/Tencent/AI-Infra-Guard?style=flat-square&logo=github) |
| [**clawsec**](https://github.com/prompt-security/clawsec) | Agent 安全技能套件 — Harness 的安全层 | ![Stars](https://img.shields.io/github/stars/prompt-security/clawsec?style=flat-square&logo=github) |
| [**moltis**](https://github.com/moltis-org/moltis) | Rust 原生智能体运行时 — 沙箱化、安全、可审计 | ![Stars](https://img.shields.io/github/stars/moltis-org/moltis?style=flat-square&logo=github) |

---

## 📖 深度文章与分析

### 必读（Tier 1）

| 文章 | 作者 | 核心贡献 |
|------|------|----------|
| [**My AI Adoption Journey**](https://mitchellh.com/writing/my-ai-adoption-journey) | Mitchell Hashimoto | 概念命名，提出"每次错误 → 永久约束"的核心范式 |
| [**Effective Harnesses for Long-Running Agents**](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents) | Anthropic / Justin Young | 双代理架构 + Git 作为状态层 |
| [**Harness Design for Long-Running Apps**](https://www.anthropic.com/engineering/harness-design-long-running-apps) | Anthropic / Prithvi Rajasekaran | 三代理架构（GAN 启发）+ Sprint Contracts |
| [**Harness Engineering (OpenAI)**](https://openai.com/index/harness-engineering/) | OpenAI | 3 人 5 个月 100 万行代码，10 倍效率提升的工程实证 |
| [**Harness Engineering**](https://martinfowler.com/articles/exploring-gen-ai/harness-engineering.html) | Martin Fowler & Birgitta Böckeler | 理论框架：Context + Constraints + Entropy Management |

### 深度分析（Tier 2）

| 文章 | 来源 | 核心贡献 |
|------|------|----------|
| [**Unlocking the Codex Harness**](https://openai.com/index/unlocking-the-codex-harness/) | OpenAI | 用 Codex 构建 Codex 自身的"自举"案例 |
| [**Conductor: Context-Driven Development**](https://developers.googleblog.com/conductor-introducing-context-driven-development-for-gemini-cli/) | Google | Gemini CLI 的 Harness 实践 |
| [**The Anatomy of an Agent Harness**](https://blog.langchain.com/the-anatomy-of-an-agent-harness/) | LangChain / Vivek Trivedy | Harness 的解剖学 — 拆解每个组件的职责与交互 |
| [**The Importance of Agent Harness in 2026**](https://www.philschmid.de/agent-harness-2026) | Philipp Schmid | 从 Hugging Face 视角看 Harness 的重要性 |
| [**Is Harness Engineering Real?**](https://www.latent.space/p/ainews-is-harness-engineering-real) | Latent.Space | "Big Model vs Big Harness" 辩论 — 模型能力和环境设计哪个更重要？ |
| [**Skill Issue: Harness Engineering for Coding Agents**](https://www.humanlayer.dev/blog/skill-issue-harness-engineering-for-coding-agents) | HumanLayer | 落地实践指南，从理论到可操作的步骤 |
| [**Anthropic's Harness Design Philosophy**](https://www.working-ref.com/en/reference/anthropic-harness-design-philosophy-evolution) | Working Ref | Anthropic 从多 Agent 到单 Agent 的设计哲学演进 |

### 思辨与行业洞察（Tier 3）

| 文章 | 来源 | 核心贡献 |
|------|------|----------|
| [**2025 Was Agents. 2026 Is Agent Harnesses.**](https://aakashgupta.medium.com/2025-was-agents-2026-is-agent-harnesses-heres-why-that-changes-everything-073e9877655e) | Aakash Gupta | 产品视角解读 — 为什么 Harness 改变一切 |
| [**The Rise of AI Harness Engineering**](https://cobusgreyling.medium.com/the-rise-of-ai-harness-engineering-5f5220de393e) | Cobus Greyling | 从对话式 AI 到 Harness 的演进趋势 |
| [**What Is Harness Engineering? Complete Guide**](https://www.nxcode.io/resources/news/what-is-harness-engineering-complete-guide-2026) | NxCode | 2026 年最全面的入门指南 |
| [**Agent Harnesses: From DIY to Product**](https://paddo.dev/blog/agent-harnesses-from-diy-to-product/) | Paddo.dev | 从手工作坊到产品化的演进路径 |
| [**Harness Engineering 实践指南**](https://www.phodal.com/blog/harness-engineering/) | Phodal（黄峰达） | 中文实践指南，三大落地原则 |
| [**从上下文工程到驾驭工程**](https://blog.csdn.net/shadowcz007/article/details/159111359) | CSDN | 中文深度分析，概念演进的完整脉络 |
| [**Harness Engineering 深度解析**](https://zhuanlan.zhihu.com/p/2014014859164026634) | 知乎 | 中文技术社区的深度讨论 |

---

## 🇨🇳 中文社区资源

| 资源 | 来源 | 说明 |
|------|------|------|
| [**宝玉 @dotey**](https://x.com/dotey) | X / Twitter | 中文社区最早的推广者之一，将其译为"驾驭工程" |
| [**Phodal 实践指南**](https://www.phodal.com/blog/harness-engineering/) | 博客 | 落地导向的中文实践指南 |
| [**learn-claude-code**](https://github.com/shareAI-lab/learn-claude-code) | GitHub | 12 节课中文系统教程 |
| [**CSDN 深度分析**](https://blog.csdn.net/shadowcz007/article/details/159111359) | CSDN | 概念演进的完整中文梳理 |
| [**知乎深度解析**](https://zhuanlan.zhihu.com/p/2014014859164026634) | 知乎 | 社区讨论与案例分析 |

---

## 📄 论文与学术研究

Harness Engineering 作为一个新兴领域，学术研究正在快速追赶工业实践。以下是与核心概念最相关的研究方向：

| 方向 | 关联 | 代表性工作 |
|------|------|-----------|
| **多智能体系统** | Harness 的核心架构模式之一 | Multi-Agent Software Development、MetaGPT |
| **LLM 可靠性与对齐** | Harness 存在的根本原因 | Constitutional AI、RLHF |
| **自主软件工程** | Harness Engineering 的应用领域 | SWE-bench、SWE-agent |
| **人机协作** | Harness 的交互设计层 | Human-AI Collaboration in SE |

---

## 🛠️ 工具链与实践框架

### AGENTS.md / CLAUDE.md 设计

这是 Harness 最基础也最重要的组件。一个好的 AGENTS.md 应该：

```markdown
# AGENTS.md 设计原则

1. 是目录，不是百科全书（指向深层文档，不复制内容）
2. 包含"为什么"，不只是"是什么"（智能体需要理解约束背后的理由）
3. 用具体示例，不用抽象描述（智能体从示例中学习比从规则中学习更可靠）
4. 定期演进（随着智能体失败模式的发现不断更新）
```

### CI/CD 作为 Harness 层

```
传统 CI/CD：             Harness-Enhanced CI/CD：

代码 → 构建 → 测试       AI 生成代码
                              ↓
                         自动 lint + 类型检查 ← 架构约束层
                              ↓
                         自动测试 ← 行为验证层
                              ↓
                         AI 自动修复 ← 反馈回路
                              ↓
                         人类审查 ← 终极把关
```

### 状态管理选型

| 方案 | 适用场景 | 复杂度 |
|------|---------|--------|
| `progress.txt` + Git | 单智能体，简单任务 | 低 |
| Markdown 文件 + 文件系统 | 多步骤，跨 session | 中 |
| 专用记忆系统（MemOS 等） | 24/7 运行，复杂工作流 | 高 |

---

## 🔮 编者洞察：Harness Engineering 的哲学意义

### 软件工程的"第二次工业革命"

第一次工业革命（19世纪）：机器取代了人类的**体力劳动**，但人类获得了新角色——机器的设计者和操作者。

AI 时代的"第二次工业革命"：AI 取代了人类的**编码劳动**，但人类获得了新角色——AI 工作环境的架构师。

Harness Engineering 就是这个新角色的**工程学科**。

### "Big Model vs Big Harness" 之争

当前 AI 界存在两种哲学：

1. **Big Model 派：** 模型越强大，需要的 harness 越少。最终模型会强到不需要任何约束。
2. **Big Harness 派：** 模型越强大，harness 越重要。因为更强的能力意味着更大的破坏力，需要更精确的约束。

**我们的判断：** Big Harness 派是对的。正如核能越强大，安全壳越重要。自动驾驶能力越强，交通法规越不能缺失。**能力和约束必须共同进化。**

### 写给工程师的话

如果你是一名软件工程师，Harness Engineering 不是你的威胁，而是你的**进化方向**。

你过去积累的一切——对代码质量的直觉、对架构设计的理解、对失败模式的经验——这些都不会过时。它们只是换了一个应用场景：从"自己写好代码"变成"设计一个环境让 AI 写好代码"。

**你是驯者，不是马。**

---

## 🧭 Harness Engineer 技能图谱

> 如果你想成为一名 Harness Engineer，这是你需要掌握的技能矩阵。

| 技能领域 | 具体要求 | 传统软件工程中的对应 |
|----------|----------|---------------------|
| **Prompt & Context Engineering** | 设计系统 prompt、管理 context 窗口 | 需求文档编写 |
| **API 设计** | 为可靠的工具接口设计 API | 接口设计 |
| **分布式系统** | 管理多 Agent 协调和状态同步 | 微服务架构 |
| **可观测性** | 日志、监控、追踪体系 | DevOps / SRE |
| **错误处理** | 重试、回滚、降级模式 | 容错设计 |
| **安全与权限** | 沙箱、权限边界、凭证管理 | 安全工程 |

> **范式转变：** 工程团队从「写代码」转向「设计环境、指定意图、构建反馈循环以使 Agent 可靠工作」。你过去积累的所有工程经验不会过时 — 它们只是换了一个应用场景。

---

## 🪞 The Bitter Lesson：保持轻量，准备重构

> Rich Sutton 的 "苦涩教训" — 利用计算的通用方法最终胜过人工设计。在 Harness Engineering 中，这意味着什么？

### 行业案例

- **Manus**：在几个月内多次重构 Harness
- **LangChain**：每年多次重新架构 Agent
- **Vercel**：删除 80% 的 Agent 工具，减少步骤和 token

### 三条核心建议

**1. Start Simple（从简单开始）**

> "找到最简单的可能解决方案，只在需要时增加复杂度。" — Anthropic

避免复杂控制流，提供原子工具，实现护栏。

**2. Build to Delete（为删除而构建）**

设计模块化架构，准备好随时替换。**Harness 中的每个组件都编码了对模型能力的假设** — 这些假设会随模型进步而过时。今天精心设计的多步骤工作流，明天可能被模型的原生能力完全替代。

**3. Harness as Dataset（Harness 即数据集）**

竞争优势在于捕获的**轨迹数据**，而非 prompt。Agent 的每次执行、每次失败、每次人类纠正，都是宝贵的训练数据。**失败不是浪费，失败是数据。**

> **哲学意义：** Harness Engineering 的终极悖论 — 你必须全力构建一个你知道终将被淘汰的系统。就像脚手架之于建筑：它在施工期间不可或缺，但建筑完工后必须拆除。优秀的 Harness Engineer 不执着于自己的 Harness，而是执着于**让 Agent 成功的使命**。

---

<div align="center">

*由 [WhoBot AI](https://www.whobot.com) 团队整理维护*

*欢迎 PR 贡献高价值内容 — 我们追求深度，不追求数量*

</div>
