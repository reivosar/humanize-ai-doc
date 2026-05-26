# humanize-ai-jp-doc

AIが生成した日本語文書を、読みやすい日本語に書き直すClaude Codeスキル。

## できること

- AIの文章を結論から始まる構造に変換する
- こそあど言葉を具体的な名詞に置き換える
- 冗長な動詞を短縮する（「〜することができます」→「〜できます」）
- 抽象名詞で終わる文を具体的な内容に言い直す
- 見出し・箇条書き・インデントを整理する

「読みやすい日本語」の定義は `.claude/skills/humanize-ai-jp-doc/READABLE_JAPANESE.md` に記載している。

## インストール

```bash
mkdir -p ~/.claude/skills/humanize-ai-jp-doc
ln -s "$(pwd)/.claude/skills/humanize-ai-jp-doc/SKILL.md" ~/.claude/skills/humanize-ai-jp-doc/SKILL.md
ln -s "$(pwd)/.claude/skills/humanize-ai-jp-doc/READABLE_JAPANESE.md" ~/.claude/skills/humanize-ai-jp-doc/READABLE_JAPANESE.md
```

## 使い方

```
/humanize-ai-jp-doc path/to/doc.md
```

テキストを直接渡すこともできる：

```
/humanize-ai-jp-doc 本ドキュメントでは〜
```
