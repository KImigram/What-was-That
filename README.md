# What Was That?

**Understand as you go.**

A lightweight AI Agent Skill that automatically identifies and explains unfamiliar English technical terms, acronyms, domain-specific concepts, and specialized expressions during conversations.

No more interrupting your learning flow to look up unfamiliar terms and expressions.

## Why?

When learning something new with AI, conversations often contain unfamiliar words and expressions:

- Acronyms like RAG, LoRA, DDIM and BER.
- Technical concepts like Embedding, Quantization and Inference.
- Specialized expressions like Trade-off, Bottleneck and Under the Hood.
- Domain-specific terminology from different fields.

Sometimes, understanding just one unfamiliar expression makes the whole explanation much easier to follow.

What Was That? helps you understand these terms naturally, right when they appear.

## Features

- **Smart Detection** — Identifies potentially unfamiliar terms and expressions based on context, instead of translating every English word.
- **Inline Explanation** — Provides translations and, when useful, concise explanations inside parentheses immediately after the original term.
- **Adaptive Language** — Follows the language of your conversation.
- **Session-level Deduplication** — Avoids repeating explanations for terms already explained in the current conversation.
- **Familiarity Awareness** — Respects terms you explicitly mark as already understood.
- **Optional Persistence** — Can use a user-provided or host-supported vocabulary file when available; otherwise, it falls back to session-level behavior.

## Example

### Without What Was That?

RAG can improve an AI agent by retrieving external knowledge.

### With What Was That?

RAG（Retrieval-Augmented Generation，检索增强生成：先检索外部资料，再让大模型结合资料生成回答）can improve an AI agent by retrieving external knowledge.

A little explanation, right when you need it.

## Installation

What Was That? follows the [Agent Skills](https://agentskills.io/) format.

1. Clone or download this repository.
2. Place the `what-was-that` folder in a directory supported by your AI agent's Skill system.
3. Reload or restart the agent if required.
4. Enable the Skill or configure automatic loading according to your agent's documentation.

Installation paths and automatic activation behavior depend on the host platform.

## Usage

Once loaded, simply talk to your AI assistant normally.

You can also explicitly invoke the Skill in supported agents.

For example, in Codex:

```text
$what-was-that
Explain how RAG and Reranking work together.
```

You can provide feedback through natural language:

- "我已经熟悉 RAG，以后不用解释了。"
- "重新解释一下 Embedding。"
- "这个概念我还不太懂。"
- "暂时关闭术语解释。"
- "恢复术语解释。"

## Design Philosophy

What Was That? is not a general-purpose translator or dictionary.

Its goal is to identify potentially unfamiliar terms and expressions, explain them when useful, and preserve the natural flow of conversation.

**Explain less, understand more.**

## Project Structure

```text
what-was-that/
├── SKILL.md
├── README.md
└── tests/
    └── test-cases.md
```

## Limitations

- Automatic activation depends on the host agent and its Skill loading mechanism.
- Session-level deduplication relies on the current conversation context.
- Cross-conversation familiarity requires optional persistent storage supported by the host environment.
- Terminology recognition and explanations depend on the underlying language model and its understanding of context.

## Roadmap

- [x] Core terminology explanation rules
- [x] Context-aware term detection
- [x] Adaptive language behavior
- [x] Inline explanations
- [x] Session-level deduplication
- [x] Basic familiarity management
- [ ] Persistent personal vocabulary
- [ ] More platform-specific installation guides
- [ ] Further multilingual improvements

## Contributing

Suggestions, bug reports and contributions are welcome!

Try it, find cases where it explains too much or too little, and help improve the experience.

## License

This project is licensed under the [MIT License](LICENSE).