---
title: Recursive Location Hierarchy
type: concept
created: 2026-04-13
updated: 2026-04-13
tags: [architecture, data-model, agriculture, ybaterra]
sources: [ai-automation-platform-strategy.md]
---

# Recursive Location Hierarchy

The backbone data structure of [[ybaterra]]. A single recursive `location_node` table with `parent_id` that can model **any farm structure** without hardcoding industry-specific hierarchies.

## Schema

```
location_node:
  - id
  - name
  - parent_id (self-referencing)
  - site_id
  - optional type
  - optional metadata
```

## Why Recursive

Different farming industries have completely different physical structures:
- A hydroponic farm has tunnels → bays → channels
- A fish farm has halls → systems → tanks  
- A poultry farm has houses → pens

A fixed hierarchy would either be too rigid or require separate tables per industry. The recursive tree handles all of them with one model.

## Key Requirement

Must support **task-level targeting** — workers receive instructions like:
- "Harvest rows 1–3 in Field A Block A"
- "Feed fish in Tank 6"
- "Clean DWC Tank 3 Raft 4"

This means the hierarchy must go deep enough to address individual production spaces.

## Related

- [[ybaterra]] — The system built on this hierarchy
- [[ai-automation-platform-strategy]] — Full architecture source
