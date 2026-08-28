# Contributing

Contributions are welcome.

The goal of this repository is simple: explain complex LLM concepts in **10 words or less** without losing the core technical meaning.

## What you can contribute

- Add a missing LLM concept
- Improve an existing explanation
- Fix technical inaccuracies
- Fix wording, grammar, or consistency
- Suggest a better category or organization

## Writing guidelines

Each explanation should:

- Be **10 words or fewer**
- Capture the core idea, not every implementation detail
- Prefer plain English over jargon
- Use technical terms when necessary for accuracy
- Avoid filler words
- Avoid marketing language
- Be understandable without already knowing the definition

Prefer:

> **Continuous batching:** Add new requests as existing requests finish

Avoid:

> **Continuous batching:** An advanced inference optimization technique that improves GPU utilization

The first explains the mechanism. The second mostly describes why it is useful.

## Accuracy over simplicity

The 10-word limit should not make an explanation misleading.

If a concept cannot be explained accurately within 10 words, narrow the definition rather than removing an important distinction.

## Style

Follow this format:

- **Concept:** Explanation in 10 words or less

Use sentence case for concept names unless the standard name uses different capitalization.

Keep explanations concise and neutral.

## Adding a concept

Add the concept under the most relevant section in `README.md`.

If no suitable section exists, propose a new one.

Before adding a concept:

1. Check that it is not already covered.
2. Confirm the explanation is technically accurate.
3. Count the words.
4. Keep the wording as simple as possible.

## Pull requests

Keep pull requests focused.

For significant or potentially ambiguous definitions, briefly explain the reasoning or link to a primary source such as a paper or official documentation.

Small wording improvements do not need extensive justification.
