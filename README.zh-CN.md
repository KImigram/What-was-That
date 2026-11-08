# What Was That?
[English](README.md) | [简体中文](README.zh-CN.md)

**边聊边懂，理解每一个新概念。**

What Was That? 是一个轻量级 AI Agent Skill，能够在日常对话中自动识别并解释用户可能不熟悉的英文专业术语、缩写、领域概念及特殊表达。

无需频繁中断对话、手动查询陌生词汇，让理解新知识的过程更加自然流畅。

## 它能干什么？

当我们通过 AI 学习新知识时，经常会遇到一些陌生的英文术语和表达，例如：

- **专业缩写**：RAG、LoRA、DDIM、BER 等。
- **技术概念**：Embedding、Quantization、Inference 等。
- **特殊表达**：Trade-off、Bottleneck、Under the Hood 等。
- **领域术语**：来自计算机科学、金融、医学等不同专业领域的词汇。

有时候，只需要理解其中一个陌生词汇，就能读懂整段解释。

What Was That? 希望解决的正是这个问题：**让 AI 在正常回答问题的同时，自然地解释那些可能妨碍你理解的术语和表达。**

## 功能特性

- **智能识别（Smart Detection）** — 结合对话上下文判断哪些术语值得解释，而不是机械翻译所有英文单词。
- **行内注释（Inline Explanation）** — 在术语首次出现时，直接在其后添加括号注释，提供中文翻译及必要的简短解释。
- **语言自适应（Adaptive Language）** — 根据当前对话语言自动调整解释语言，中文对话使用中文解释，英文对话使用英文解释。
- **会话内去重（Session-level Deduplication）** — 同一对话中已经解释过的术语不再重复注释，避免影响阅读体验。
- **熟悉度感知（Familiarity Awareness）** — 尊重用户明确表示已经掌握的术语，不再主动重复解释。
- **可选持久化（Optional Persistence）** — 在运行环境支持且提供相应存储时，可以使用个人词汇表记录已掌握术语；否则正常使用会话内管理机制。

## 效果示例

### 未使用 What Was That?

RAG 可以通过检索外部知识，提升 AI Agent 的回答质量。

### 使用 What Was That?

RAG（Retrieval-Augmented Generation，检索增强生成：先检索外部资料，再让大模型结合资料生成回答）可以通过检索外部知识，提升 AI Agent 的回答质量。

只需要一点恰到好处的解释，就能让陌生概念变得更容易理解。

## 安装方法

What Was That? 遵循 [Agent Skills](https://agentskills.io/) 规范。

1. 下载或克隆本仓库。
2. 将 `what-was-that` Skill 文件夹放入所使用 AI Agent 支持的 Skills 目录中。
3. 根据需要重新加载或重启 Agent。
4. 按照对应平台的说明启用 Skill，或配置自动加载。

不同 AI Agent 的安装路径和自动触发机制可能有所区别。

### Codex 安装示例

对于 Windows 用户，可以将 Skill 安装到：

```text
C:\Users\<用户名>\.agents\skills\what-was-that\
```

确保该目录下存在 `SKILL.md` 文件。

安装完成后，可以在 Codex 中尝试显式调用：

```text
$what-was-that
解释一下 RAG 和 Reranking 的区别。
```

也可以直接进行普通对话，测试 Codex 是否能够自动识别并加载 Skill。

请注意：自动触发取决于 Agent 的 Skill 加载机制，并不保证每次对话都会自动启用。

## 使用方法

Skill 加载后，你可以像平时一样与 AI 交流，无需额外操作。

你还可以通过自然语言调整解释行为：

- 「我已经熟悉 RAG，以后不用解释了。」
- 「重新解释一下 Embedding。」
- 「这个概念我还不太懂。」
- 「暂时关闭术语解释。」
- 「恢复术语解释。」

What Was That? 会根据你的反馈调整当前对话中的注释行为。

## 设计理念

What Was That? 不是一个普通的翻译器，也不是一个需要主动查询的专业词典。

它希望在不改变原本对话内容、结构和风格的前提下，自动识别可能妨碍用户理解的术语，并提供适量解释。

我们的目标不是解释每一个英文单词，而是**恰好解释那些值得解释的内容**。

**Explain less, understand more.**

少一点无关注释，多一点自然理解。

## 项目结构

```text
what-was-that/
├── SKILL.md
├── README.md
├── README.zh-CN.md
└── tests/
    └── test-cases.md
```

## 当前限制

- **自动触发**：是否能够自动加载 Skill，取决于宿主 Agent 的运行机制。
- **会话内去重**：依赖当前对话上下文，无法保证在上下文被截断后仍能完整识别所有已解释术语。
- **跨对话记忆**：需要运行环境支持额外的持久化存储，目前尚未提供完整的自动词汇库管理功能。
- **解释准确性**：术语识别和解释质量取决于底层语言模型的上下文理解能力。


## 参与贡献

欢迎提交 Issue、Pull Request 或其他建议！

如果你在使用过程中发现：

- 某些术语应该解释却没有解释；
- 某些常见词汇被过度注释；
- 同一个术语反复出现解释；
- 注释影响了原本的阅读体验；

欢迎反馈，帮助 What Was That? 变得更好用。

## 开源协议

本项目采用 [MIT License](LICENSE) 开源协议。