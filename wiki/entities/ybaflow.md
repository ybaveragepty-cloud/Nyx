---
title: YBAFlow
type: entity
created: 2026-04-13
updated: 2026-04-13
tags: [product, saas, platform, yba]
sources: [ybaflow-openclaw-deployment-plan.md, openclaw-container-setup.md, structure-confirmation.md]
---

# YBAFlow

A modular SaaS automation platform being built as the **core platform** for YBA Systems. Designed to support multiple vertical products, with [[ybaterra]] as the first product built on top.

## Purpose

- Multi-tenant SaaS automation platform
- Supports workflow/automation engine, role-based access control, integrations
- Must be modular, stable, scalable, secure, and production-minded from day one

## Core Modules (from [[structure-confirmation]])

Auth, organizations (multi-tenant), permissions (role-based), workflow engine, automation engine, dashboards (customizable), audit logs, notifications, integrations, API layer.

**Critical rule:** No farm/product logic in platform core. Everything configurable, not hardcoded.

### 12-Step Build Sequence

1. Monorepo scaffolding → 2. Auth → 3. Org/tenant → 4. Roles/permissions → 5. Dashboard metadata → 6. Workflow metadata → 7. Audit log → 8. Event bus → 9. Notifications → 10. Integrations → 11. Tests → 12. CI

## Technical Stack (planned)

- **Monorepo** (TypeScript)
- **Backend:** Node.js + PostgreSQL + Redis
- **Frontend:** Modern React
- **Queue:** BullMQ or Temporal
- **Infrastructure:** Docker, Coolify, Kubernetes-ready
- **AI Build System:** [[openclaw]]

## Key URLs

- `app.ybaflow.com` → frontend (planned)
- `api.ybaflow.com` → backend (planned)

## GitHub

- Repo: `ybaflow-platform` under `ybaveragepty-cloud` org
- Branches: `main` (protected), `dev` (AI development)

## Strategic Pivot (from [[openclaw-container-setup]])

Instead of building YBAFlow as a full platform first, the strategy shifted to building a **narrow, high-value business tool** — the [[packhouse-admin-copilot]] — and letting the platform evolve from real usage data.

## Build Order

YBAFlow platform must be complete **before** [[ybaterra]] business logic:

1. Infrastructure
2. Identity system (org, user, role, permission, membership)
3. Workflow engine
4. Automation framework
5. Agent system
6. Then vertical products

## Sources

- [[ybaflow-overview]] — SaaS positioning, product hierarchy, landing page messaging

## Related

- [[openclaw]] — AI agent system building YBAFlow
- [[ybaterra]] — First product on the platform
- [[coolify]] — Deployment manager
- [[yba-systems]] — Parent company/brand
