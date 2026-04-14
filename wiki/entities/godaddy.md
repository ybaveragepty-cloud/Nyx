---
title: GoDaddy
type: entity
created: 2026-04-13
updated: 2026-04-13
tags: [infrastructure, dns, domains]
sources: [resource-establishment-overview.md]
---

# GoDaddy

Domain registrar for [[yba-systems]] domains.

## Domains Managed

- `ybasystems.com`
- `ybaflow.com`

## Key Gotcha

GoDaddy parking IPs (`15.197.225.128`, `3.33.251.168`) override A records if domain parking/forwarding is enabled. Must disable these before DNS changes take effect.

## Related

- [[yba-systems]] — The domains
- [[hostinger]] — VPS the domains point to (31.187.72.210)
