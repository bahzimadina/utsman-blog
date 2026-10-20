---
title: "Teach Your AI Assistant by Example, Not by Long Commands"
date: 2026-10-21
slug: teaching-ai-assistant-by-example
lang: en
pair: ngalatih-asisten-ku-conto
excerpt: "Long instructions often confuse AI assistants. Give two or three well-chosen examples, and you get faster, more accurate results."
tags: [ai, prompting, productivity, technology]
draft: false
---

## Long Commands Do Not Guarantee Better Output

Many people assume that the longer the prompt, the smarter the AI assistant's answer. That is not how large language models work. When you feed them a wall of text packed with elaborate rules and branching logic, they often lose track and produce inconsistent results. These models do not reason like humans; they detect patterns in the text you provide. A complex prompt creates a complex, unpredictable pattern.

## Examples Work Better

A simpler and more reliable method is *few-shot prompting*. Instead of describing what you want in paragraphs, you give two or three clear input-output examples. Suppose you want meeting notes turned into a summary. Rather than explaining the desired format at length, just paste raw notes alongside a good summary you have already written.

Another simple case is sorting email. Instead of writing "Determine whether this email is a request, a report, or a promotion. If unsure, respond with 'none of the above'.", you get better results by showing examples like these:

- "Please send the monthly report tomorrow morning." → request
- "I sent the October report yesterday." → report
- "50% off the premium plan, today only!" → promotion

The assistant picks up the pattern immediately without reading a long rulebook.

## When Is This Approach Most Effective?

Few-shot prompting shines whenever you need a specific output format: tables, JSON, or a particular writing tone. If you run a customer support channel, showing examples of polite replies versus direct replies will guide the assistant's voice. A 2024 LangChain benchmark on tool calling showed the gap plainly: one model was right only 16% of the time with no examples, then reached 52% once given three examples similar to the question at hand.

## Best Practices

- Choose examples that are correct, not approximate.
- Aim for 2–3 examples; more is not always better.
- Make sure the examples cover different cases: positive, negative, and slightly tricky ones.
- If the assistant still gets it wrong, change the examples rather than adding more rules.

## Wrapping Up

Teaching an AI assistant is a lot like teaching a person: a solid example beats a long speech every time. 🎯
