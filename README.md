# Microsoft 365 Identity & Security Labs

**Status:** Coursework analyzed; independent tenant revalidation planned  
**Project source:** Coursework-derived concepts with independent extensions

## Overview

Sanitized case studies demonstrating identity and security administration in Microsoft 365 and Microsoft Entra. All tenant names, IDs, users, domains, and screenshots must use fictional or redacted values.

## Lab roadmap

| Lab | Focus | Source | Status |
|---|---|---|---|
| [Hybrid identity and privileged access](docs/hybrid-identity-and-privileged-access.md) | Licensing, RBAC, Graph, audit, PTA, PIM | Coursework-derived | Case study complete; rebuild pending |
| Identity lifecycle | Users, groups, roles | Coursework-derived | Rebuild planned |
| Conditional Access design | Access policy and risk | Coursework-derived + independent extension | Planned |
| Audit investigation | Sign-in and audit logs | Independent extension | Planned |

## Repository structure

```text
docs/       Original case studies
images/     Sanitized screenshots and diagrams
policies/   Pseudocode or redacted policy examples
```

## Case-study standard

Each lab should include a scenario, objective, environment, design decisions, validation evidence, security impact, limitations, and lessons learned. Use the template in `docs/CASE-STUDY-TEMPLATE.md`.

## Skills demonstrated

Microsoft Entra ID, Conditional Access, role-based access, identity governance, authentication, audit logs, secure documentation.

## Disclosure

This repository does not contain exported tenant data, real user information, credentials, tokens, proprietary course content, or instructions copied from Microsoft Learn or another lab provider.
