# wombat-wiki Scaffold Design

**Date:** 2026-04-15  
**Status:** Approved

## What We're Building

An initial commit for the `wombat-wiki` GitHub repo that makes it a working
agent-driven knowledge base template — immediately usable and pushable to
`https://github.com/ma-cohen/wombat-wiki`.

## Files to Create

### `AGENT.md`
Instructions loaded automatically by any AI agent (Claude Code, Cursor, etc.)
at session start. Defines:
- The brain-dump workflow (user pastes thought → agent writes markdown)
- Dynamic category creation (no predefined list — infer from content)
- Frontmatter format for every note
- Deduplication rule: read the category folder before writing, merge if overlap found

### `README.md`
Human-readable explanation of the project:
- What it is and how it works
- How to create a new KB from this template (`gh repo create`)
- How to use it day-to-day (open in agent, dump thoughts, browse in Obsidian)

## What Is NOT Included
- No predefined category folders — the AI creates them from content
- No example notes — clean slate on first use
- No scripts, no LLM API keys, no external dependencies

## Repo Setup
- `git init` in the current directory
- Remote set to `https://github.com/ma-cohen/wombat-wiki`
- Initial commit with all files, then push to `main`

## Success Criteria
- Repo pushed to GitHub with a clean initial commit
- Any AI agent opening the repo can immediately start processing brain-dumps
  without further setup
- README is clear enough that someone unfamiliar can understand the workflow
  in under 2 minutes
