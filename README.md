# humanize-ai-doc

A Claude Code skill that rewrites AI-generated documentation into clear, human-friendly text.

## What it does

- Removes verbose AI preambles
- Converts excessive bullet lists into prose
- Shortens sentences
- Reduces passive voice
- Preserves all original meaning

## Installation

```bash
mkdir -p ~/.claude/skills/humanize-ai-doc
ln -s "$(pwd)/skills/humanize-ai-doc/SKILL.md" ~/.claude/skills/humanize-ai-doc/SKILL.md
```

## Usage

Ask Claude to humanize a document:

```
Humanize this document: path/to/doc.md
```

Claude will automatically apply this skill.
