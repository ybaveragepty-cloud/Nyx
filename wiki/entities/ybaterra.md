---
title: YBATerra
type: entity
created: 2026-04-13
updated: 2026-04-13
tags: [product, agriculture, farming, saas, yba]
sources: [ybaflow-openclaw-deployment-plan.md, ai-automation-platform-strategy.md, terra-operating-model.md]
---

# YBATerra

A **universal agricultural operating system** — the first vertical product built on [[ybaflow]]. Designed to model real-world farm operations, not software assumptions.

## Core Design Principle

> The system must model **real-world operations**. Everything must be traceable, relational, location-aware, and batch-aware.

## Critical Architecture Rule

**Never mix these four domains:**
1. **Physical Structure** — where things exist
2. **Production System** — how things are produced
3. **Product Flow** — how goods move through the business
4. **Operations** — what work is performed

## Location Hierarchy — The Backbone

Uses a **[[recursive-location-hierarchy|recursive tree structure]]** (`location_node` with `parent_id`) to support any farm type:

| Industry | Example Hierarchy |
|----------|------------------|
| Open Field | Farm → Field → Block → Section → Row |
| Hydroponics NFT | Farm → Tunnel → Bay → Zone → Channel |
| Hydroponics DWC | Farm → Tunnel → Bay → Tank → Raft/Board/Bucket |
| Aquaculture | Farm → Hall → System → Tank |
| Poultry | Farm → House → Pen |
| Mushrooms | Farm → Room → Rack → Shelf |
| Algae | Farm → Reactor Hall → Reactor Line → Reactor Unit |

Must support **task-level targeting** (e.g., "Harvest rows 1–3 in Field A Block A").

## Production Systems

- **Hydroponics:** NFT, DWC, Drip, Flood & drain, Aeroponics, Towers, Microgreens
- **Open Field:** Dryland, Irrigated, Organic, Conventional
- **Aquaculture:** RAS, Ponds, Raceway, Hatchery, Grow-out
- **Aquaponics:** Coupled, Decoupled, Hybrid
- **Livestock:** Breeding, Feedlot, Pasture
- **Poultry:** Broilers, Layers, Breeders
- **Mushrooms / Algae**

## The Batch — Most Important Entity

Every production run is tracked as a **batch** (crop batch, fish batch, livestock herd, poultry flock) with:
- Start date, location, production system
- Expected output, current status
- Events: planting, transplant, harvest, transfer, mortality, cleaning
- Measurements: rows/boards harvested, biomass, weight

## Critical Rule: Crop ≠ Product

- Crop = Lettuce (biology)
- Product = 150g Salad Bag (commerce)

These are **separate entities** with different lifecycle tracking.

## System Modules

| Module | Purpose |
|--------|---------|
| Environment | Air/water/soil monitoring, control systems, threshold alerts |
| Packhouse | Intake → washing → grading → packing → labeling → cold storage |
| Procurement | Suppliers, pricing, contracts, delivery schedules |
| Commerce | Customers, products, orders, pricing, margins |
| Inventory | Raw inputs, biological stock, finished goods |
| Assets | Equipment tracking + maintenance/calibration |
| Operations | Tasks with location targeting, staff assignment, SOP linkage |
| SOP & Knowledge | Procedures, compliance, safety standards |
| Training | Modules, certifications, competency tracking |

## Versioning Roadmap (from [[terra-operating-model]])

| Version | Scope |
|---------|-------|
| **v0.1** | Hydroponics only (all systems) — pilot for Richard's farm |
| v0.2 | Packhouse, dispatch, procurement |
| v0.3 | Aquaculture |
| v0.4 | Aquaponics |
| v0.5 | Conventional farming + livestock |
| **v1.0** | Full farm operating platform |

## v0.1 Database Schema (~50 tables)

Confirmed in [[terra-operating-model]] with full table definitions. Key entity groups:
- Tenant/location (organisations, sites, location_types, location_nodes)
- Production (production_systems, production_spaces, crop_batches)
- Operations (tasks, operational_logs, environment_logs, scouting_logs)
- Inventory/assets, procurement, harvest/products, sales/delivery, governance/SOPs

**Key decisions:** Separate batch tables per type, single DB with `organisation_id`, mixed harvest units, GMP-compliant traceability, customizable location hierarchy names via `location_types` table.

## v0.1 Screens (~37 core)

Worker: simple task-based interface with configurable KPIs
Admin: full org/site/location/batch/workflow/permission management
Device: tablet-first + phone support

## Important Rule

> Do **not** build YBATerra until the [[ybaflow]] platform core is stable.

## Long-term Goal

Support multi-organization SaaS deployments. Scale target: **1000+ farms and enterprise clients**.

## Key Risks

1. Mixing structure and process domains
2. Hardcoding location hierarchy (must be recursive/flexible)
3. Treating crops as products
4. Ignoring batch-level tracking
5. Not linking records across domains
6. Overbuilding V1

## Sources

- [[openclaw-deployment-planning]] — 100-task agent build plan and Terra master data model v1 (72+ entities)
- [[eastern-cape-aquaponics]] — Consulting project: Eastern Cape tilapia/pangasius facility assessment and rebuild
- [[commercial-aquaponics-discussion]] — Technical accreditation discussion (water chemistry, risk philosophy, Ichthys)
- [[la-buschagne-aquaponic-empire]] — Early strategic thinking on farm operations and AI agents (pre-OpenClaw)

## Related

- [[ybaflow]] — The platform YBATerra is built on
- [[la-foods]] — First real-world user (via [[packhouse-admin-copilot]])
- [[openclaw]] — AI build system + operational AI layer
- [[yba-systems]] — Parent company/brand
- [[ai-automation-platform-strategy]] — Full architecture source document
