---
title: API Reference
cover: assets/social-card.png
---

> Base path: `/api`  
> **Authentication**  
> All API calls require headers:  
> ```http
> X-API-Key: <your_key>
> Authorization: Bearer <your_token>
> ```


## System
- `GET /api/system/health`
- `GET /api/system/metrics`

## Agents
- `GET /api/agents?q=&limit=&offset=&tenant_id=` → `{ items, total }`
- `GET /api/agents/{id}`
- `POST /api/agents`
- `PUT /api/agents/{id}`
- `DELETE /api/agents/{id}`
- `GET /api/runs?agent_id={id}&limit=50`

## Workflows
- `GET /api/workflows?q=&limit=&offset=`
- `GET /api/workflows/{id}`
- `POST /api/workflows`
- `PUT /api/workflows/{id}`
- `DELETE /api/workflows/{id}`
- `POST /api/workflows/{id}/run`
- `GET /api/runs?workflow_id={id}&limit=50`

## Policies
- `GET /api/policy/{policy_id}?tenant_id=`
- `PUT /api/policy/{policy_id}`
- `POST /api/policy/{policy_id}/assemble`
- `POST /api/policy/abtest/set`
- `GET /api/policy/abtest/get?policy_a=&policy_b=`

## Knowledge
- Sources:
  - `GET /api/sources`
  - `POST /api/sources`
  - `POST /api/sources/{id}/index`
  - `DELETE /api/sources/{id}`
- Documents:
  - `GET /api/documents?source_id=&q=&limit=&offset=&tag=`
  - `POST /api/documents/reindex`
- Code Graph:
  - `POST /api/codegraph/index`
  - `GET /api/codegraph/search?project=&q=&limit=`

## Playbooks
- `GET /api/playbooks?tenant_id=`
- `POST /api/playbooks/mine`
- Optional:
  - `POST /api/playbooks/promote`
  - `POST /api/playbooks/attach`

## Settings
- Tenants: `GET|POST /api/settings/tenants`, `PUT|DELETE /api/settings/tenants/{id}`
- Providers: `GET|PUT /api/settings/providers`
- Flags: `GET /api/settings/flags`, `PUT /api/settings/flags/{key}`
- CORS: `GET|PUT /api/settings/cors`
- Audit: `GET /api/settings/audit/info`, `POST /api/settings/audit/export`
