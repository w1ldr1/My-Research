# Repository Guidelines

## Project Structure & Module Organization
This repository is a small research workspace, not an application codebase. Root-level files hold individual research deliverables such as `cell-service-research.md`, `payment-gateways-sole-proprietor-llc.md`, and `military_tax_prep_research.txt`. Keep new research files at the repository root unless a topic grows large enough to justify its own folder. The `.claude/` directory contains local assistant settings and should remain tooling-only.

## Build, Test, and Development Commands
There is no build system or automated test suite in this repository today.

- `ls -la` to inspect the current document set
- `rg "keyword" .` to search across notes quickly
- `git status` to review pending edits once this folder is initialized as a Git repo

If you add scripts later, document them here and keep them narrowly scoped to content validation or export tasks.

## Coding Style & Naming Conventions
Use Markdown for research notes unless plain text is more appropriate. Prefer short sections, descriptive headings, and compact bullet lists. Name files in lowercase with hyphens and topic-oriented terms, for example `vendor-comparison-2026.md`. Include a year or version only when it materially improves clarity. Avoid spaces in filenames.

For prose:
- keep paragraphs brief
- use consistent heading levels
- prefer factual, source-backed wording over draft notes left inline

## Testing Guidelines
Quality control here is manual. Before committing:

- verify headings render correctly in Markdown
- check links, dates, and quoted figures
- confirm filenames match the topic and format
- remove temporary notes, placeholders, and duplicated sections

If a document depends on external sources, include enough context in the file for another contributor to verify the claims.

## Commit & Pull Request Guidelines
This folder is not currently a Git repository, so there is no established local commit history to follow yet. When version control is added, use concise imperative commit messages such as `Add payment gateway comparison` or `Revise Indianapolis destinations notes`.

Pull requests should include a short summary, list affected files, and note any facts that still need verification. For substantial rewrites, include the reason for the update and any source changes that drove it.
