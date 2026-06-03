---
name: humanize-ai-jp-doc
description: Use this skill when the user asks to humanize AI-generated Japanese documentation, make Japanese docs more human-friendly, remove AI writing patterns in Japanese, or rewrite Japanese documents for readability.
version: 2.0.0
---

You are an expert at rewriting AI-generated Japanese text into natural, readable Japanese.

The definition of readable Japanese and all conversion rules are in `.claude/rules/language-settings.md`. Read it first.

## Process

1. Read `.claude/rules/language-settings.md`
2. Read the target file or text
3. Rewrite following the rules in `.claude/rules/language-settings.md`
4. If a file was provided, save it
5. Before finalizing, run this 3-step scan on your output:

   **Step A — List scan (most common miss)**
   Read each prose paragraph. If it contains 3+ sentences that each describe one
   discrete item (no causal link, no explanation between them), convert to bullet list.

   **Step B — Spacing scan**
   Check paragraph boundaries, headings, and list blocks for blank line rules.
   Check list items are not broken mid-item.

   **Step C — Checklist**
   Go through the checklist below item by item. Rewrite anything that fails.

## Post-rewrite verification checklist

### Conclusion first
- [ ] Check language-settings.md — Conclusion first

### Specificity
- [ ] Check language-settings.md — Specificity, Comparison, Numbers

### Headings
- [ ] `#` used only for the document title (one per document)
- [ ] Body text follows every heading — no consecutive headings
- [ ] Only `##` and `###` used (never `####` or deeper)
- [ ] Headings end with a noun-stop form in principle; verb endings allowed when flow demands it

### Lists vs prose
- [ ] Procedural steps → numbered list
- [ ] 3 or more parallel items → bullet list
- [ ] 2 or fewer items / explanations / reasons / causal relationships → prose

### Indentation
- [ ] Supplementary notes and cautions inside steps → indented
- [ ] Body paragraphs and standalone notes → not indented
- [ ] Indent depth is 1 level max

### Sentence quality
- [ ] One sentence per line — never run two sentences on the same line
- [ ] Blank line at every change of idea or topic
- [ ] Each paragraph covers exactly one topic — no unrelated sentences mixed in
- [ ] One piece of information per sentence
- [ ] Sentences are short and clear — split long sentences
- [ ] List items: one line each, no mid-item breaks — rewrite to shorten if needed
- [ ] Trimming did not erase meaning — if it did, reword instead of delete
- [ ] Check language-settings.md — Subject/predicate, Negative form, Nested modifiers, Abstract nouns

### Word choice
- [ ] Check language-settings.md — Demonstratives, Conjunctions, Conversion rules, Reader level
- [ ] When multiple points exist, count announced upfront (e.g., "There are 3 reasons")

### Line breaks
- [ ] Each sentence on its own line
- [ ] Blank line at every change of idea
- [ ] List items: never break mid-item — rewrite to shorten
- [ ] One blank line before every heading
- [ ] No blank line immediately after a heading — body text follows directly
- [ ] No blank lines between list items
- [ ] One blank line before and after a list block
- [ ] No comma at the end of a sentence — close with a period

### Repetition
- [ ] Check language-settings.md — Repetition
