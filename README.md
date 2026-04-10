# multilingual-translator

> 🇰🇷 [한국어 README](./README.ko.md)

**Multilingual translation for structured .md documents with structure-matching QC.**

## Prerequisites

- **Obsidian Vault** — QC validation script counts wikilinks (`[[...]]`) and embeds (`![[...]]`) for structure preservation
- **Claude Cowork or Claude Code** environment

## Goal

multilingual-translator automates multi-language publishing: establishes English as baseline, translates in parallel, validates structure preservation across callouts, tables, wikilinks, and HTML divs.

## When & How to Use

Trigger when you have a structured .md document to translate. Always translates to English first (baseline), then other languages in parallel. Validates structural parity after every translation.

## Use Cases

| Scenario | Prompt | What Happens |
|---|---|---|
| Translate to 3 languages | `"Translate README to Spanish, French, German"` | EN baseline→parallel ES/FR/DE→QC: verify structure match→3 translated files |
| Multi-language API docs | `"Translate API docs to 5 languages, code blocks untouched"` | EN version→preserve code fences→5 languages→structure validation |
| Batch translation | `"Translate 10 docs to Japanese, Korean, Chinese"` | Sub-agent parallelization→validate each independently→coverage report |

## Key Features

- English-first baseline for canonical version
- Parallel translation to N languages simultaneously
- Structure-matching QC: callouts, tables, wikilinks, HTML divs, code blocks preserved
- Sub-agent management for parallel document handling
- Validation report with structure match percentage

## Works With

- **[deliverable-engine](https://github.com/jasonnamii/deliverable-engine)** — structured docs ideal for translation
- **[obsidian-markdown](https://github.com/jasonnamii/obsidian-markdown)** — translates Obsidian markdown with wikilinks intact

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

This is one of 25+ custom skills. See the full catalog: [github.com/jasonnamii/cowork-skills](https://github.com/jasonnamii/cowork-skills)

## License

MIT License — feel free to use, modify, and share.
