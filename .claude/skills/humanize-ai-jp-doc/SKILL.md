---
name: humanize-ai-jp-doc
description: Use this skill when the user asks to humanize AI-generated Japanese documentation, make Japanese docs more human-friendly, remove AI writing patterns in Japanese, or rewrite Japanese documents for readability.
version: 2.0.0
---

You are an expert at rewriting AI-generated Japanese text into natural, readable Japanese.

The definition of readable Japanese and all conversion rules are in `READABLE_JAPANESE.md` in this skill directory. Read it first.

## Process

1. Read `READABLE_JAPANESE.md`
2. Read the target file or text
3. Rewrite following the rules in `READABLE_JAPANESE.md`
4. If a file was provided, save it
5. Before finalizing, run this 3-step scan on your output:

   **Step A — List scan (most common miss)**
   Read each prose paragraph. If it contains 3+ sentences that each describe one
   discrete item (no causal link, no explanation between them), convert to bullet list.

   **Step B — Line break scan**
   Count characters. When you hit character 40, break. No exceptions, no judgment.
   Then check paragraph boundaries, headings, and list blocks for blank line rules.

   **Step C — Checklist**
   — (merged into Step D below)

   **Step C — Checklist**
   Go through the checklist below item by item. Rewrite anything that fails.

## Post-rewrite verification checklist

### Conclusion first
- [ ] Each section/paragraph opens with the conclusion; details follow

### Specificity (人間らしさ)
- [ ] No vague/generic expressions — write "when", "what", "what for" concretely

### Headings
- [ ] `#` used only for the document title (one per document)
- [ ] Body text follows every heading — no consecutive headings
- [ ] Only `##` and `###` used (never `####` or deeper)
- [ ] Every heading ends with a noun (体言止め)

### Lists vs prose
- [ ] Procedural steps → numbered list
- [ ] 3 or more parallel items → bullet list
- [ ] 2 or fewer items / explanations / reasons / causal relationships → prose

### Indentation
- [ ] Supplementary notes and cautions inside steps → indented
- [ ] Body paragraphs and standalone notes → not indented
- [ ] Indent depth is 1 level max

### Sentence quality
- [ ] One piece of information per sentence
- [ ] Prose: every 読点 is followed by a newline — no exceptions
- [ ] Prose: every line is 40 characters or fewer — break at character 40 if no 読点
- [ ] List items: one line each, no mid-item breaks, ≤40 characters
- [ ] Deeply nested modifiers extracted into a separate sentence
- [ ] Trimming did not erase meaning — if it did, reword instead of delete
- [ ] No sentences ending with abstract nouns (効率化・品質向上 etc.) — follow with "what" and "how it changes"

### Word choice
- [ ] Demonstratives (これ・その・ここ etc.) replaced with concrete nouns
- [ ] No consecutive また / さらに / なお — keep one or delete
- [ ] 〜することができます → 〜できます
- [ ] 〜を行います → 〜します
- [ ] 〜が提供されています → 〜を使えます
- [ ] Unnecessary katakana loanwords replaced with Japanese equivalents

### Line breaks
- [ ] Prose: every line is exactly ≤40 characters — break at character 40, no exceptions
- [ ] List items: never break mid-item — rewrite to fit on one line (≤40 chars)
- [ ] One blank line between paragraphs
- [ ] One blank line before every heading
- [ ] No blank line immediately after a heading — body text follows directly
- [ ] No blank lines between list items
- [ ] One blank line before and after a list block
- [ ] No 読点 (、) at the end of a sentence — close with 。

### Boilerplate removal
- [ ] 本ドキュメントでは〜説明します → deleted
- [ ] ご不明な点があれば〜 → deleted
