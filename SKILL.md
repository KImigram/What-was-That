
---
name: what-was-that
description: >
  Automatically identify and explain unfamiliar English
  technical terms, acronyms, domain-specific concepts,
  and specialized expressions during conversations.
  Help users understand unfamiliar terminology and expressions
  without interrupting the natural flow of conversation.
---

# What was That

Help users understand unfamiliar or critical terminology naturally
during conversations.

The goal is not to translate every English word, but to
explain terms that may prevent the user from understanding
the current topic.

## 1. Term Detection

Identify terms worth explaining based on context.

Prioritize:
- Technical terms and domain-specific concepts.
- Acronyms and abbreviations.
- Names of algorithms, architectures, protocols and metrics.
- Specialized expressions that are important to the current topic
  or may be unfamiliar to the user.

Do not normally explain:
- Everyday English words.
- Common programming languages and basic technical vocabulary.
- Product names, file names, variable names and code identifiers.
- Terms that are irrelevant to understanding the current answer.

Do not rely on a fixed blacklist. A familiar term may still
need explanation when it is central to a new topic.

## 2. Explanation Rules

When a relevant term appears for the first time:

- Preserve its original English spelling.
- For acronyms, provide the full English name when known.
- Provide a translation in the language of the conversation.
- Add one short, plain-language explanation only when it
  helps clarify the term or improve understanding.
- Keep both the translation and any additional explanation
  inside the same parentheses immediately after the term.


Examples:

RAG (Retrieval-Augmented Generation，
检索增强生成：先检索外部资料，再让大模型结合资料生成回答。)


Embedding (嵌入表示：
将文本或其他数据转换成能够表达其特征的向量。)

Keep explanations accurate, concise and easy to understand.

Never invent the full name of an acronym. If its meaning
is ambiguous, use the surrounding context to determine
the intended meaning.

## 3. Language Adaptation

Follow the language the user is communicating in.

- Chinese conversation: translate and explain in Chinese.
- English conversation: explain in English.
- Other languages: use the conversation language when possible.

Always preserve the original technical term.

## 4. First-occurrence Management

Maintain a lightweight record of terms already explained
in the current conversation.

- Explain a term only on its first relevant occurrence.
- Do not repeat explanations unnecessarily.
- If the same abbreviation has a different meaning
  in another context, explain the new meaning.
- If the user asks for an explanation again, explain it.

Being explained does not mean the user has mastered
the term.

## 5. Familiarity Management

Respect explicit user feedback.

Examples:
- "I already know RAG."
- "以后不用解释 LoRA 了。"
- "这个词我还不太懂。"

When the user explicitly marks a term as familiar,
treat it as a known term and avoid explaining it
in future conversations when that information is available.

Persistent storage is optional.

If a user-provided or platform-supported vocabulary file
is available and writable, it may be used to maintain
known terms across conversations.

Never claim that a term has been permanently saved
when persistent storage is unavailable.

## 6. Formatting and Readability

- Prefer inline explanations immediately after the term.
- Keep annotations short and natural.
- Prioritize unfamiliar terms and expressions rather than annotating 
  everything, keeping their annotations concise and within parentheses. 
- When many unfamiliar terms appear together, prioritize
  the terms most important to understanding the answer.
- Do not create a separate glossary unless requested.

Never modify code blocks, commands, file paths,
variable names or quoted source material.

## 7. User Control

Respect requests to:
- Explain a particular term in more detail.
- Mark a term as already understood.
- Temporarily disable terminology explanations.
- Resume terminology explanations.

These rules should complement the assistant's normal
response behavior, not replace it.

Do not let terminology explanations interrupt the
original answer's structure, tone or reasoning.
