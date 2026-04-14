---
title: "Turn Claude Code Into Your Executive Assistant in 27 Mins"
type: source
created: 2026-04-14
updated: 2026-04-14
tags: [claude-code, executive-assistant, ai-automation, skills, sub-agents, workflow]
sources: [Turn Claude Code Into Your Executive Assistant in 27 Mins.md]
---

# Turn Claude Code Into Your Executive Assistant in 27 Mins

- **Author:** [[nate-herk]] (AI Automation)
- **Published:** 2026-03-05
- **Source:** YouTube video + transcript
- **Length:** ~27 minutes

## Summary

[[nate-herk]] walks through building a personal AI executive assistant using [[claude-code-ea-framework]] in Claude Code. The approach turns Claude Code from a generic chatbot into a personalized system that knows your business, follows your processes, and compounds intelligence over time. The framework has four phases.

## Four Phases

### Phase 1 — Give It a Home (Project Structure)
- Create a dedicated folder (the "home" for the assistant)
- Open it in VS Code with the Claude Code extension
- Create a `CLAUDE.md` file as the "brain" — this gets loaded before every message
- Keep `CLAUDE.md` lean (~150 lines max) — point to other files instead of stuffing everything in
- Structure evolves: `.claude/`, `projects/`, `contexts/`, `decisions/`, `archives/`, `references/`, `templates/`

### Phase 2 — Give It Life (Context & Rules)
- Run an onboarding interview where Claude Code extracts info about you
- Create context files: `me.md`, `work.md`, `team.md`, `current-priorities.md`, `goals-and-milestones.md`
- Set communication rules (tone, formatting, style)
- `CLAUDE.md` points to these files: "if you need info about X, read this file" — saves tokens
- Initialize Git for version control (ideally push to GitHub for backup/portability)

### Phase 3 — Give It Hands (Skills & Sub-Agents)
- **Skills** = reusable markdown instructions stored in `.claude/skills/`
  - Example: research skill using Perplexity API
  - Skill instructs Claude to: understand question → load context → formulate queries → call API → synthesize → save report → present summary
  - Use YAML frontmatter for configuration (better token efficiency, more consistent results)
- **Sub-Agents** = delegated workers with their own context window
  - Stored in `.claude/agents/`
  - Can use different (cheaper) models (e.g., Haiku instead of Opus)
  - Good for: parallel work, cheaper research, isolated tasks
  - Also use YAML frontmatter
- API keys go in `.env` file (never in conversation history)
- Skills update `CLAUDE.md` so Claude knows they exist

### Phase 4 — Let It Grow
- Use the assistant daily instead of ChatGPT/custom GPTs
- Every interaction leaves artifacts (research reports, decisions, project updates) that compound
- Migrate existing prompts/workflows into skills
- Iterate: "this is what I didn't like, update it"
- Regular maintenance: compact `CLAUDE.md`, update context files quarterly
- GitHub for version control, backup, and cross-device portability

## Key Architectural Insights

> The Claude.md file should have only the most important rules... Because if you fill it super super full of random information, then you're going to go through your tokens and your context window faster.

> Every time you do research, every time you generate content... all of that still lives in this project, which is why it gets smarter and smarter.

- `CLAUDE.md` is a routing table, not a knowledge store
- Context files are the actual knowledge — read on demand
- Skills and agents should use YAML frontmatter for best results
- Sub-agents are useful for parallel execution and cost optimization
- The system compounds: more usage = more saved artifacts = smarter assistant
- Decision logging creates institutional memory

## Demo Capabilities Shown

1. **Morning Coffee skill** — reads calendar + project management + quarterly goals, plans entire day, blocks calendar
2. **Research + Content Creation** — sub-agent does research, generates LinkedIn post and Twitter carousel in brand voice
3. **Team Pulse Check** — reviews all initiatives, task status, gives follow-ups against goals
4. **Visualization** — generates PNG assets for YouTube videos

All four ran in parallel across separate windows.

## Notable Quotes

> "If I don't have to have that decision fatigue of what should I do with my next 15 minutes... I'm way more productive."

> "A month from now, this thing is going to look crazy different. There's going to be way more docs, way more decisions, way more skills."

## Relevance to Richards Brain

This is directly the pattern Richard is using — an LLM-maintained wiki that compounds over time. Key differences:
- Richard's implementation uses [[openclaw]] and the wiki schema in `CLAUDE.md` rather than the EA folder structure
- The skill/sub-agent architecture maps well to potential future capabilities
- The "context files as pointers" pattern aligns with how Richard's `CLAUDE.md` already references wiki pages
- The compounding knowledge principle is identical to Richard's "compound, don't repeat" rule
