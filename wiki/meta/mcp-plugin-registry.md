---
title: MCP & Plugin Registry
type: meta
created: 2026-04-14
updated: 2026-04-14
tags: [meta, nyx, infrastructure, mcp, plugins, tools]
sources: []
---

# MCP & Plugin Registry

Central registry of all MCP servers and plugins configured for Richards Brain and the agent framework.

---

## Active MCP Servers (.mcp.json)

| MCP | What It Does | Auth Required | Status |
|---|---|---|---|
| **Playwright** | Browser automation — navigate, click, screenshot, test UIs | None | Active |
| **Memory** | Persistent memory across Claude Code sessions | None | Active |
| **Mermaid** | Render Mermaid diagrams as actual images | None | Active |
| **Context7** | Pull live docs for any library/framework into prompts | None (optional API key) | Active |
| **GitHub** | Full GitHub API — repos, issues, PRs, actions | `${GITHUB_TOKEN}` env var | Active |
| **Filesystem** | Structured file access to Richards Brain + Documents | None | Active |
| **n8n** | Build/manage n8n workflows from Claude Code | None | Active |
| **arXiv** | Search/download academic papers from arXiv | None | Active |

## Plugins

| Plugin | Source | What It Does | Install Command |
|---|---|---|---|
| **Claude HUD** | jarrodwatts/claude-hud | Live dashboard — context usage, active tools, agents, todos | `/plugin marketplace add jarrodwatts/claude-hud` then `/plugin install claude-hud` |
| **Cartographer** | kingbootoshi/cartographer | Maps codebases with parallel subagents → CODEBASE_MAP.md | `/plugin marketplace add kingbootoshi/cartographer` then `/plugin install cartographer` |

## Available But Not Installed (install when needed)

### MCP Servers

| MCP | What It Does | When to Install |
|---|---|---|
| **Stripe** | Payment API integration | When YBAFlow goes live |
| **Bright Data** | Web scraping at scale (60+ tools) | When doing heavy scraping |
| **ElevenLabs** | Voice/audio generation, cloning, transcription | When doing audio content |
| **Figma Dev Mode** | Design-to-code from Figma files | When doing frontend design work |
| **Notion** | Notion API — pages, databases, search | If Richard uses Notion |
| **Firecrawl** | Advanced web scraping/crawling | When Bright Data isn't enough |
| **SearXNG** | Privacy-respecting metasearch engine | If self-hosting search |
| **PostgreSQL** | Direct PostgreSQL integration | When doing heavy DB work |
| **Supabase** | Supabase integration | When using Supabase |
| **Redis** | Redis integration | When using Redis |
| **MongoDB** | MongoDB integration | When using MongoDB |
| **Sentry** | Error tracking and monitoring | When deploying production apps |
| **Grafana** | Metrics dashboards | When monitoring production |

### Plugins

| Plugin | What It Does | Why Skipped |
|---|---|---|
| **Claude Mem** | Auto-captures and compresses session memory | Conflicts with our file-based memory system |
| **Review Loop** | Automated code review with Codex | Requires OpenAI Codex CLI (external dependency) |
| **Adversarial Spec** | Multi-LLM debate for spec refinement | Requires OpenAI/OpenRouter API keys + Python |
| **Pg Aiguide** | PostgreSQL skills + docs from Timescale | Requires Docker |

## How MCP Servers Work

```
Claude Code (client) → MCP Protocol → MCP Server → External Service
                                         ↓
                              (Gmail, Slack, DB, GitHub, etc.)
```

- MCP servers are configured in `.mcp.json` at the project root
- Each server gives Claude new tools specific to that service
- Servers run as local processes (npx/uvx) or connect to remote URLs
- `.mcp.json` is gitignored (contains token references)

## How Plugins Work

- Plugins are installed via `/plugin marketplace add <repo>` + `/plugin install <name>`
- They can add skills, agents, commands, hooks, and MCPs
- Managed through the Claude Code CLI's plugin system
- Stored in `~/.claude/plugins/`

## Environment Variables Needed

| Variable | Purpose | Where to Set |
|---|---|---|
| `GITHUB_TOKEN` | GitHub MCP authentication | System env or `.env` |
| `BRIGHTDATA_API_KEY` | Bright Data scraping (when installed) | System env or `.env` |
| `STRIPE_SECRET_KEY` | Stripe payments (when installed) | System env or `.env` |
