---
title: "AI Automation Platform Strategy"
type: source
created: 2026-03-06
updated: 2026-04-13
tags: [ybaterra, architecture, data-model, agriculture, strategy]
sources: [YBAFlow - AI Automation Platform Strategy.md]
---

# AI Automation Platform Strategy

**Source:** ChatGPT conversation (clipped)
**Date:** ~2026-03-06 (early planning, predates deployment sessions)
**Origin:** https://chatgpt.com/g/g-p-69b271c633e08191bcbd104077ab77d7-ybaflow/

## Summary

The foundational architecture document for [[ybaterra]] — defining it as a **universal agricultural operating system** that models real-world operations. This is the deepest domain-design source so far, covering the full data model, production systems, and build strategy.

## Core Objective

Build a multi-industry agricultural operating system that can:
- Manage production across **all farming types**
- Track **full product lifecycle** (grow → process → sell)
- Enable task-based operations with location targeting
- Integrate environmental data
- Support AI-driven automation
- Scale from single farm to multi-site enterprise

## Critical Architecture Rule

> **NEVER mix these four domains:**
> 1. Physical Structure (where things exist)
> 2. Production System (how things are produced)
> 3. Product Flow (how goods move through the business)
> 4. Operations (what work is performed)

## Fundamental System Model

```
Enterprise → Site → Location (recursive hierarchy)
  → Production System → Production Space
    → Biological Batch
      → Operation / Task
        → Inputs (Inventory) + Assets Used + SOP Followed
          → Output (Product) → Customer
```

## Location Hierarchy — The Backbone

Uses a **recursive tree structure** (`location_node` with `parent_id`) to support any farm structure:

| Industry | Hierarchy |
|----------|-----------|
| Open Field | Farm → Field → Block → Section → Row |
| Hydroponics NFT | Farm → Tunnel → Bay → Zone → Channel |
| Hydroponics DWC | Farm → Tunnel → Bay → Tank → Raft/Board/Bucket |
| Aquaculture | Farm → Hall → System → Tank |
| Poultry | Farm → House → Pen |
| Mushrooms | Farm → Room → Rack → Shelf |
| Algae | Farm → Reactor Hall → Reactor Line → Reactor Unit |

Must support **task-level targeting** (e.g., "Farm A → Field A → Block A → Section A → Rows 1–3").

## Production Systems Supported

- **Hydroponics:** NFT, DWC, Drip, Flood & drain, Aeroponics, Towers, Microgreens
- **Open Field:** Dryland, Irrigated, Organic, Conventional
- **Aquaculture:** RAS, Ponds, Raceway, Hatchery, Grow-out
- **Aquaponics:** Coupled, Decoupled, Hybrid
- **Livestock:** Breeding, Feedlot, Pasture
- **Poultry:** Broilers, Layers, Breeders
- **Mushrooms:** Bag culture, Shelf culture
- **Algae:** Raceway, Photobioreactor

## Production Model — Batch is King

Must separate:
- **Structure** — physical location (location_node)
- **Biology** — crop, fish species, livestock type
- **Batch** — the MOST IMPORTANT entity (start date, location, production system, expected output, status)
- **Events** — planting, transplant, harvest, transfer, mortality, cleaning
- **Measurements** — rows/boards/buckets harvested, biomass, weight

## Critical Rule: Crop ≠ Product

- Crop = Lettuce
- Product = 150g Salad Bag

These are **different entities** with different lifecycle tracking.

## System Modules

| Module | Key Features |
|--------|-------------|
| Environment | Air/water/soil monitoring, control systems, threshold alerts |
| Packhouse | Intake, washing, grading, packing, labeling, cold storage |
| Procurement | Suppliers, pricing, contracts, delivery schedules, incoming lots |
| Commerce | Customers, products, orders, pricing, margins, delivery |
| Inventory | Raw inputs, biological stock, finished goods |
| Assets | Pumps, tanks, vehicles, sensors + maintenance/calibration tracking |
| Operations | Tasks, routines, maintenance, issues + location targeting, staff assignment, SOP linkage |
| SOP & Knowledge | Procedures, compliance, safety, troubleshooting |
| Training | Modules, certifications, competency, staff progress |

## V1 Database Entities

```
organisations, sites, location_nodes
production_systems, production_spaces
batches
tasks, operation_logs
inventory_items, inventory_lots, stock_movements
assets, asset_logs
suppliers, customers
products, sales_orders, order_lines
harvest_records
environment_logs
sops, training_records
```

## Worker Instruction Model

System must generate natural-language task instructions:
- "Harvest rows 1–3 in Field A Block A"
- "Feed fish in Tank 6"
- "Clean DWC Tank 3 Raft 4"
- "Collect eggs from House 3"

## Build Strategy

| Phase | Focus |
|-------|-------|
| 1 (V1) | Hydroponics: location hierarchy, production units, crop + batch, tasks, inventory, basic orders |
| 2 | Packhouse, procurement, environment |
| 3 | Aquaculture + aquaponics |
| 4 | Livestock + training |

## Key Risks

1. Mixing structure and process
2. Hardcoding location hierarchy
3. Treating crops as products
4. Ignoring batch-level tracking
5. Not linking records across domains
6. Overbuilding V1
