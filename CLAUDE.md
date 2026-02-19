# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repository Is

Claude Code Plugin for UI/UX design guidance targeting Japanese SaaS / web application development. Pure documentation (Markdown only) — no build, test, or lint steps exist. All content is in Japanese.

## Architecture

```
.claude-plugin/plugin.json   — Plugin manifest (name, version, author)
commands/ui-review.md        — /ui-review command definition
skills/
  {skill-name}/
    SKILL.md                 — Main skill file (YAML frontmatter + guidance)
    references/*.md          — Detailed reference documents
```

### Three Skills

| Skill | Purpose | References |
|-------|---------|------------|
| `ui-best-practices` | Visual design, component states, UX patterns, anti-patterns | 4 files |
| `shig` | Sociomedia HIG — 100 design principles (OOUI, interaction, forms, mobile, a11y) | 6 files |
| `ux-writing` | Japanese UI writing — text patterns, idiomatic usage, error messages | 4 files |

### One Command

`/ui-review` — Reviews code for UX pattern completeness, visual consistency, and anti-patterns. Complementary to RAMS plugin (which handles accessibility/WCAG).

## Skill File Conventions

**SKILL.md frontmatter**:
```yaml
---
name: lowercase-hyphenated    # Must match directory name
description: >-               # When this skill should activate
  ...
---
```

**SKILL.md body structure**: H1 title → citation block → themed action guidelines → checklist → reference file links.

**Reference files**: No frontmatter. Start with H1, then citation block, then guideline item table, then independent "実装への適用ノート" sections.

## Citation Model (Copyright Law Article 32 Compliance)

External sources (SHIG, SmartHR Design System) are cited following Japanese fair use requirements:

1. **SKILL.md**: Full citation block with copyright holder, work title, URL, © notice
2. **Each reference file**: Citation block after intro + table headers marked with `（出典: {source}）`
3. **Scope of quotation**: Only guideline item names (titles) and URLs — never quote original body text
4. **主従関係**: Original "実装への適用ノート" content is the primary work; quoted item names are supplementary

When adding new skills based on external sources, always follow this pattern.
