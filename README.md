
# What was That
**Understand as you go.**

An AI Agent Skill that automatically explains unfamiliar
technical terms and acronyms during conversations.

No more interrupting your learning flow to look up
every unfamiliar technical term.

## Why?

When learning something new with AI, conversations often
contain unfamiliar technical terminology:

- Acronyms like RAG, LoRA, DDIM and BER.
- Concepts like Embedding, Quantization and Inference.
- Domain-specific expressions and technical jargon.

Term Companion helps you understand them naturally,
right when they appear.

## Features

- **Smart Detection** — Identifies relevant technical
  terms instead of translating every English word.
- **Inline Explanation** — Provides translations and
  concise explanations at first occurrence.
- **Adaptive Language** — Follows the language of
  your conversation.
- **Session-level Deduplication** — Avoids explaining
  the same term repeatedly.
- **Familiarity Awareness** — Respects terms you
  explicitly mark as already understood.
- **Optional Persistence** — Supports a personal
  known-term list when the host environment allows it.

## Example

Without Term Companion:

"RAG can improve an AI agent by retrieving
external knowledge."

With Term Companion:

"RAG (Retrieval-Augmented Generation，检索增强生成)
can improve an AI agent by retrieving external knowledge."

A little explanation, right when you need it.

## Installation

Term Companion follows the Agent Skills format.

1. Download or clone this repository.
2. Place the `term-companion` folder in a directory
   supported by your AI agent's Skill system.
3. Reload or restart the agent if required.
4. Enable the Skill or configure automatic loading
   according to your agent's documentation.

Installation paths and automatic activation behavior
depend on the host platform.

## Usage

Once loaded, simply talk to your AI assistant normally.

You can also provide feedback:

- "我已经熟悉 RAG，以后不用解释了。"
- "重新解释一下 Embedding。"
- "这个概念我还不太懂。"
- "暂时关闭术语解释。"

## Design Philosophy

Term Companion is not a general-purpose translator.

Its goal is to explain only the terms that matter,
without changing the natural flow of conversation.

**Explain less, understand more.**

## Project Structure

```text
term-companion/
├── SKILL.md
├── README.md
├── references/
│   └── term-guidelines.md
└── tests/
    └── test-cases.md
```

## Limitations

- Automatic activation depends on the host agent.
- Session-level deduplication relies on conversation context.
- Cross-conversation familiarity requires optional
  persistent storage supported by the host.
- Terminology recognition and explanations depend
  on the underlying language model.

## Roadmap

- [x] Core terminology explanation rules
- [x] Adaptive language behavior
- [x] Session-level deduplication
- [x] Basic familiarity management
- [ ] Persistent personal vocabulary
- [ ] More platform-specific installation guides
- [ ] Multilingual improvements

## Contributing

Suggestions, bug reports and contributions are welcome!

Try it, find cases where it explains too much or too little,
and help improve the experience.

## License

To be determined.
