# wombat-wiki — Claude Code Instructions

This repo is a personal knowledge base. Your job is to turn brain-dumps into
clean, organized, deduplicated markdown notes.

**When the user sends you any free-form text (a brain-dump), act immediately —
do not ask for clarification. Follow the steps below.**

## Your Role

When the user gives you a brain-dump (any free-form text), you:

1. **Understand** what the thought is about
2. **Choose or create a category** that fits (see below)
3. **Check for duplicates** before writing — read existing files in the target folder
4. **Write or update** a markdown file

## Categories

There are no predefined categories. Infer the right category from the content
and create the folder if it doesn't exist yet.

- Use short, lowercase, singular or plural noun folder names (e.g. `dev`, `ideas`, `books`, `cooking`, `health`)
- When a new dump could fit an existing category, prefer the existing one
- Only create a new category when the content clearly doesn't belong anywhere existing
- Cross-category content goes in the most specific category; add tags for the rest

## Before Writing — Check for Duplicates

Before creating a new file, read all existing files in the target category folder.
If an existing note covers the same topic:
- **Update it** — add the new information, re-summarize if needed
- Do NOT create a second file for the same idea

## File Format

Every note lives at: `<category>/<slug>.md`

Filename: short kebab-case slug derived from the title (e.g. `react-hooks-mental-model.md`)

```markdown
---
title: "Clear, concise title"
summary: "One or two sentences. What is this about and why does it matter."
tags: [tag1, tag2]
date: YYYY-MM-DD
updated: YYYY-MM-DD
---

<original brain-dump or cleaned-up version>

## Key Points

- Bullet points distilling the most important ideas

## Notes

Any additional context, links, or follow-up questions.
```

## Rules

- **Summaries are mandatory** — always write a clear `summary` in the frontmatter
- **One idea per file** — if a dump contains multiple distinct ideas, split them into separate files
- **Never delete notes** — update or merge, never remove existing content
- **Keep the original** — preserve the user's raw thought below the frontmatter, lightly cleaned up
- **Date** is when the note was first created; **updated** is today's date when you modify an existing note
- **Act on brain-dumps immediately** — do not ask the user what to do with dropped text; process it
