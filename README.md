# wombat-wiki

A personal knowledge base powered by any AI agent. Brain-dump your thoughts
— the AI organizes, summarizes, and deduplicates them into a clean markdown
vault you can browse in Obsidian.

## How It Works

```
You type a thought in your AI agent
    → Agent reads existing notes in the right category
    → Categorizes, summarizes, checks for duplicates
    → Writes or updates a markdown file in this repo
    → You browse in Obsidian (or any markdown reader)
```

No scripts. No API keys. No subscriptions. Just a repo and an AI agent.

## Getting Started

### 1. Create your own knowledge base from this template

Using GitHub CLI:
```bash
gh repo create my-kb-name --template ma-cohen/wombat-wiki --clone
cd my-kb-name
```

Or click **"Use this template"** on GitHub and clone the result.

### 2. Open the repo in your AI agent

Works with any agent that can read and write files:
- [Claude Code](https://claude.ai/code)
- [Cursor](https://cursor.sh)
- GitHub Copilot (Workspace mode)
- ChatGPT (with file tools)

The agent automatically reads `AGENT.md` for instructions.

### 3. Brain-dump

Just talk to your agent:

> "I just learned that React's useEffect cleanup function runs before the
> next effect, not after the component unmounts."

> "Idea: a browser extension that summarizes the current page into bullet
> points and saves it here."

> "Finished Atomic Habits. Main takeaway: habits are about identity, not
> outcomes."

The agent handles categorization, summaries, and deduplication.

### 4. Browse in Obsidian

Open this repo folder as an Obsidian vault. You get:
- File tree organized by category
- Full-text search across all notes
- Graph view showing connections
- Beautiful markdown rendering

## Structure

```
/
├── AGENT.md          ← Instructions for the AI agent (don't delete)
├── README.md         ← This file
├── dev/              ← Created by the agent as needed
│   └── *.md
├── ideas/
│   └── *.md
└── ...               ← More categories as your KB grows
```

## Multiple Knowledge Bases

Create as many as you need:

```bash
gh repo create cooking-wiki --template ma-cohen/wombat-wiki --clone
gh repo create travel-wiki  --template ma-cohen/wombat-wiki --clone
gh repo create work-wiki    --template ma-cohen/wombat-wiki --clone
```

Each is fully independent with its own categories and notes.

## `ww` Shortcut

Add the `ww` function to your shell profile so you can spin up a new
knowledge base in one command.

**bash** — add to `~/.bashrc` or `~/.bash_profile`:
```bash
ww() {
  gh repo create "$1" --template ma-cohen/wombat-wiki --clone && cd "$1"
}
```

**zsh** — add to `~/.zshrc`:
```zsh
ww() {
  gh repo create "$1" --template ma-cohen/wombat-wiki --clone && cd "$1"
}
```

**fish** — add to `~/.config/fish/functions/ww.fish`:
```fish
function ww
  gh repo create $argv[1] --template ma-cohen/wombat-wiki --clone && cd $argv[1]
end
```

After adding it, reload your shell (`source ~/.bashrc` / `source ~/.zshrc`) and use it:

```bash
ww cooking-wiki
ww dev-wiki
ww travel-wiki
```

This creates the GitHub repo from the template, clones it locally, and drops
you into the folder — ready to open in your AI agent.

## Customizing Agent Behavior

Edit `AGENT.md` to change how the agent works — adjust the note format,
add domain-specific rules, or restrict which categories are allowed.
