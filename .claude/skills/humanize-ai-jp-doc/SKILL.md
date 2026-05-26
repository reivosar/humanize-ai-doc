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

   **Step B — Sentence length scan**
   Find every sentence over 40 characters. Split or add a comma.

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
- [ ] Each sentence is 40 characters or fewer (split or add a comma if over)
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

### Boilerplate removal
- [ ] 本ドキュメントでは〜説明します → deleted
- [ ] ご不明な点があれば〜 → deleted
