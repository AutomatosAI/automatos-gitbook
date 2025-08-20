---
title: Settings
cover: assets/social-card.jpeg
---

Configure tenants, providers, feature flags, CORS, and audit.

## Tenants
Create, rename, delete tenants to isolate data & configs.

**API**  
> **Authentication**  
> All API calls require headers:  
> ```http
> X-API-Key: <your_key>
> Authorization: Bearer <your_token>
> ```

- `GET /api/settings/tenants`
- `POST /api/settings/tenants`
- `PUT /api/settings/tenants/{id}`
- `DELETE /api/settings/tenants/{id}`

## Providers
Store provider keys; set default models.

**API**  
- `GET /api/settings/providers`
- `PUT /api/settings/providers`

## Feature Flags
Toggle modules (Playbooks, Code Graph, A/B).

**API**  
- `GET /api/settings/flags`
- `PUT /api/settings/flags/{key}` (body: `{"value":true}`)

## CORS
Manage allowed origins.

**API**  
- `GET /api/settings/cors`
- `PUT /api/settings/cors` (body: `{"origins":["http://localhost:3000"]}`)

## Audit
Export audit logs.

**API**  
- `GET /api/settings/audit/info`
- `POST /api/settings/audit/export` → `{"url":"https://.../audit-2025-08-10.ndjson"}`


