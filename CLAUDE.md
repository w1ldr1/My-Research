# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

A personal research workspace — not an application codebase. Root-level files are individual research deliverables (`.md`, `.txt`, `.docx`). There is no build system, test suite, or runtime.

## Useful commands

```bash
ls -la              # inspect current document set
rg "keyword" .      # search across notes
git status          # review pending edits
```

## File conventions

- Format: Markdown unless plain text is more appropriate
- Naming: lowercase with hyphens, topic-first (e.g. `vendor-comparison-2026.md`); include a year only when it adds clarity; no spaces
- New files go at the repository root unless a topic grows large enough to justify its own folder
- The `.claude/` directory is tooling-only — don't add research content there

## Prose style

- Short paragraphs, descriptive headings, compact bullet lists
- Factual, source-backed wording — remove draft placeholders before committing
- Consistent heading levels within a document

## Before committing

- Verify headings render correctly in Markdown
- Check links, dates, and quoted figures
- Confirm filenames match the topic and format
- Remove temporary notes, placeholders, and duplicated sections
- If a document cites external sources, include enough context for another reader to verify the claims

## Commit messages

Concise imperative style: `Add payment gateway comparison`, `Revise Indianapolis destinations notes`.
