---
title: "Terra Operating Model"
type: source
created: 2026-03-08
updated: 2026-04-13
tags: [ybaterra, data-model, database, schema, hydroponics, v0.1, architecture]
sources: [YBAFlow - Terra Operating Model.md]
---

# Terra Operating Model

**Source:** ChatGPT conversation (~4,443 lines)
**Date:** ~2026-03-08
**Origin:** https://chatgpt.com/g/g-p-69b271c633e08191bcbd104077ab77d7-ybaflow/
**Platform:** [[ybaflow]]

## Summary

The most **database-level detailed** source in the entire collection. Converts the domain architecture from [[ai-automation-platform-strategy]] into a concrete v0.1 database schema with table definitions, field lists, relationships, and confirmed architecture decisions. Also defines the versioning roadmap and v0.1 screen/workflow requirements.

## Architecture Decisions Confirmed

| # | Decision | Choice |
|---|----------|--------|
| 5.1 | Multi-organisation | Yes, from day one — Terra is a product/service |
| 5.2 | Batch model | Separate tables per production type (crop_batches, fish_batches, etc.) |
| 5.3 | Commerce/procurement | Included in platform scope |
| 5.4 | Traceability | Strict, GMP-compliant from day one |
| 5.5 | Production scope | Mixed farm from day one (architecture supports all, v0.1 exposes hydroponics) |
| 5.6 | Location depth | Full tree to lowest operational unit |
| 5.7 | Task granularity | One task per location unit, separate execution |
| - | Multi-tenant isolation | Option A: single database with `organisation_id` everywhere |
| - | Crop batch tracking | Crop + variety + sowing date + expected harvest window |
| - | Harvest/sales units | Mixed allowed (heads, bunches, packets, kg, crates) |
| - | Packhouse depth | Full: wash → sort → trim → pack → label → cold room → dispatch |
| - | Device model | Tablet-first (stationed at work areas) + phone (field/issues) |
| - | Worker interface | Simple task-based, configurable by admin, with KPI visibility |
| - | Dashboards | Customizable per organisation |
| - | Workflows | Customizable per farm |
| - | Permissions | Admin-only grant authority |

## Versioning Roadmap

| Version | Scope |
|---------|-------|
| v0.1 | Hydroponics only (all systems) — pilot for Richard's farm |
| v0.2 | Packhouse, dispatch, procurement |
| v0.3 | Aquaculture |
| v0.4 | Aquaponics |
| v0.5 | Conventional farming + livestock |
| v1.0 | Full farm operating platform |

## v0.1 Database Schema (~50 tables)

### Entity Groups

**A. Tenant & Location:** organisations, sites, location_types, location_nodes, production_systems, production_spaces

**B. Crop & Batch:** crops, crop_varieties, seed_lots, crop_batches

**C. Worker & Tasks:** staff, staff_site_assignments, task_templates, tasks, operational_logs, issue_incidents, corrective_actions, approvals

**D. Technical Logs:** environment_logs, nutrient_mix_logs, nutrient_mix_lines, ph_ec_adjustment_logs, irrigation_logs, scouting_logs

**E. Environment:** environment_logs (air temp, humidity, CO2, light, root zone, water temp, pH, EC, DO)

**F. Inventory & Assets:** inventory_items, inventory_lots, stock_movements, assets, asset_usage_logs, maintenance_logs, calibration_logs

**G. Procurement:** suppliers, purchase_orders, purchase_order_lines, incoming_lots

**H. Harvest & Products:** products, harvest_records, finished_goods_lots

**I. Sales & Delivery:** customers, sales_orders, sales_order_lines, deliveries, claims_returns

**J. Governance:** sops, sop_links, training_modules, training_records, compliance_records

### Key Innovation: `location_types` Table

Configurable hierarchy level definitions per organisation/site. Customers can rename hierarchy levels while Terra keeps a clean recursive structure. Fields include `parent_location_type_id`, `hierarchy_level`, and `applies_to_system_type`.

### Minimum Linked Fields Rule

Most operational tables should include: `organisation_id`, `site_id`, `location_node_id`, `production_system_id`, `production_space_id`, `biological_batch_id`, `task_id`, `inventory_item_id`, `asset_id`, `sop_id`, `staff_id`, `created_at`, `updated_at`, `status`

## v0.1 Screens (~37 core)

### Worker-facing:
Worker dashboard, My Tasks, Task Detail/Execute, Environment quick entry, pH/EC adjustment, Irrigation check, Scouting, Incident reporting, Harvest entry, Stock usage

### Admin/Manager:
Org & site setup, Location tree, Production systems/spaces, Crop batches, Dashboards, Workflow templates, Inventory, Procurement, Sales/dispatch, Assets, Roles/permissions, Reports

## OpenClaw Timing

> Do NOT make OpenClaw the core of Terra. Make Terra a normal app first. Then use OpenClaw as a developer speed layer, an automation layer, and a chat interface layer later.

Bring OpenClaw in **after v0.1 scope is defined** — for code scaffolding, CRUD generation, admin screens, repetitive endpoints.

## Build Order (5 Phases)

1. **Foundation:** organisations, sites, location_nodes, production_systems, production_spaces, staff, biological_batches, task_templates, tasks, operational_logs
2. **Stock & Assets:** inventory_items, inventory_lots, stock_movements, assets, maintenance_logs, calibration_logs
3. **Output & Sales:** products, harvest_records, finished_goods_lots, customers, sales_orders, deliveries
4. **Governance:** sops, sop_links, training_modules, training_records, compliance_records
5. **Procurement:** suppliers, purchase_orders, purchase_order_lines, incoming_lots
