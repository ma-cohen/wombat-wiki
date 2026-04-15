Turn the following brain-dump into a short, organized markdown note in this wiki.

Brain-dump: $ARGUMENTS

## Steps

1. **Understand** what the thought is about
2. **Choose or create a category** — short, lowercase noun folder (e.g. `dev`, `ideas`, `books`, `cooking`, `health`); prefer an existing folder over creating a new one
3. **Check for duplicates** — read existing files in the target folder; if one covers the same topic, update it instead of creating a new file
4. **Write or update** the file at `<category>/<slug>.md`

## File Format

```markdown
---
title: "Short, clear title"
summary: "One sentence. What this is and why it matters."
tags: [tag1, tag2]
date: YYYY-MM-DD
updated: YYYY-MM-DD
---

<one-paragraph distillation of the brain-dump — raw thought, lightly edited>

## Key Points

- Most important idea
- Second idea
- Third idea (keep to 3–5 bullets max)

## Notes

Optional: links, follow-up questions, or context that didn't fit above. Omit if empty.
```

## Rules

- Short and scannable — a good note takes 30 seconds to read
- Strip filler; prefer bullets; one idea per bullet
- One idea per file — split if the dump covers multiple distinct topics
- Never delete existing notes — update or merge
- Preserve the user's raw thought as the opening paragraph, lightly cleaned up
- `date` = when first created; `updated` = today when modifying an existing note
