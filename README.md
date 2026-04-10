# Multilingual Translator

**Translation with structure-matching QC.**

Translates structured `.md` while preserving callouts, tables, wikilinks, HTML divs. Source → English first → others parallel. QC verifies structural parity.

### Example Prompts

```
"Translate to English, Chinese, Japanese" → EN baseline→CN+JP parallel→structure QC→fix
```

## Installation

```bash
git clone https://github.com/jasonnamii/multilingual-translator.git ~/.claude/skills/multilingual-translator
```

## Update

```bash
cd ~/.claude/skills/multilingual-translator && git pull
```

Skills placed in `~/.claude/skills/` are automatically available in Claude Code and Cowork sessions.

## Part of Cowork Skills

This is one of 25 custom skills. See the full catalog: [https://github.com/jasonnamii/cowork-skills](https://github.com/jasonnamii/cowork-skills)

## License

MIT License — feel free to use, modify, and share.
