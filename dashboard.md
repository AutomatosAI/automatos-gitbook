---
title: Dashboard
cover: assets/social-card.jpeg
---

The **Dashboard** is your control room: live **KPIs**, **runs**, and **A/B state**.

## KPIs
- **Success rate** — fraction of successful runs.  
- **Latency (p50/p95)** — median & tail.  
- **Retrieval hit‑rate** — how often retrieved context was used.  
- **Cost (24h)** — spend estimate.

**API**  
> **Authentication**  
> All API calls require headers:  
> ```http
> X-API-Key: <your_key>
> Authorization: Bearer <your_token>
> ```

`GET /api/system/metrics`  
```json
{ "quality":{"success_rate":0.92}, "latency":{"p50":850,"p95":2400}, "cost":{"usd_24h":7.43}, "retrieval":{"hit_rate":0.64} }
```

## Live Runs
A rolling feed of recent executions with quick drill‑in.

**API (recommended shim)**  
`GET /api/runs/summary?limit=50`  
```json
{ "runs":[{"id":"run_1","agent_id":"agent_1","status":"SUCCESS","latency_ms":920,"cost_usd":0.02,"started_at":"2025-08-10T12:00:00Z"}], "total": 1 }
```

## A/B Testing
Toggle which **policy variant** is active.

**API**  
`GET /api/policy/abtest/get?policy_a=code_assistant_A&policy_b=code_assistant_B`  
`POST /api/policy/abtest/set`  
```json
{ "policy_a":"code_assistant_A","policy_b":"code_assistant_B","active":"A"}
```

## Troubleshooting
- KPIs empty → ensure `/api/system/metrics` returns JSON.
- 401s in the browser → add CORS + ensure headers are forwarded.
