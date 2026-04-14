---
title: Status Report Template
type: meta
created: 2026-04-14
updated: 2026-04-14
tags: [meta, template, status, agents, operations]
sources: []
---

# Status Report Template

Sub-agents write this to `status/latest.md` in their project folder after every major task.

---

```markdown
# Status Report

- **Agent:** {agent name or role}
- **Task:** {what was done}
- **Time:** {YYYY-MM-DD HH:MM SAST}
- **Status:** done | failed | blocked | needs-review

## Result

{2-3 sentences on what happened}

## Files Changed

- `path/to/file` — what changed

## Issues

{any problems, blockers, or things Nyx should know — or "None"}

## Next

{what should happen next — or "Awaiting Captain's direction"}
```

## How Nyx Uses This

1. Sub-agent finishes a task
2. Sub-agent writes `status/latest.md` using this format
3. Nyx reads all status reports across active projects
4. Nyx audits: did the work match the plan? Any errors?
5. Nyx summarizes for Captain in conversation
