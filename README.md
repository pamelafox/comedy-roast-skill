# 🔥 Comedy Roast Skill

An agent skill that roasts you based on what you *actually* did last week — pulling material from your GitHub activity, X/Twitter posts, and Microsoft 365 work data.

Every joke is grounded in real data: your commits, your meetings, your tweets. No generic punchlines. The best roasts come from cross-referencing what you said publicly versus what you actually worked on.

## How it works

When you ask your coding agent to "roast me," the skill:

1. **Gathers material** from three data sources in parallel:
   - **GitHub** — PRs, commits, issues (tiny PRs with huge descriptions, 2 AM commits, self-merges…)
   - **X (Twitter)** — posts, likes, trends (hot takes with zero engagement, ratio'd posts…)
   - **WorkIQ (Microsoft 365)** — meetings, emails, files (meetings that could have been emails…)
2. **Cross-references** for contradictions (tweeted "deep work day 🔥" but GitHub shows zero commits)
3. **Delivers a full roast monologue** — opener, work roast, code roast, timeline roast, and a backhanded compliment to close

## Installation

Install the skill using the [`skills`](https://www.npmjs.com/package/skills) CLI:

```sh
npx skills add pamelafox/comedy-roast-skill
```

## Required MCP Servers

This skill queries three MCP servers for roast material. You'll need to have them connected to your agent:

| Source | MCP Server | What It Provides |
|--------|-----------|-----------------|
| GitHub | [github/github-mcp-server](https://github.com/github/github-mcp-server) | Commits, PRs, issues |
| X (Twitter) | [xdevplatform/xmcp](https://github.com/xdevplatform/xmcp) | Posts, likes, trends |
| Work IQ (Microsoft 365) | [microsoft/work-iq](https://github.com/microsoft/work-iq) | Emails, meetings, files |

> **Note:** The skill gracefully handles missing sources. If a server isn't connected, it roasts the silence instead.

## Usage

Once installed, just ask your coding agent:

- "roast me"
- "roast my week"
- "give me a comedy roast"

## Example

> *"You mass-produced 47 meetings this week and then sent an email about 'protecting focus time.' Your GitHub was so quiet I thought you'd been laid off — until I saw you mass-liking tweets about productivity at 11 PM. But hey, at least your one PR description was longer than your actual code. That takes commitment."*
