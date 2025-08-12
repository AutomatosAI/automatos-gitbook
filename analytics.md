---
title: Analytics
cover: assets/social-card.png
---

Measure quality, latency, usage, and cost.

## Performance
Trends for **success**, **latency**, and **retrieval** quality.

**API**  
> **Authentication**  
> All API calls require headers:  
> ```http
> X-API-Key: <your_key>
> Authorization: Bearer <your_token>
> ```

`GET /api/analytics/performance?start=&end=`  
```json
{ "success_rate":0.91,"latency":{"p50":850,"p95":2400},"retrieval":{"hit_rate":0.64} }
```

## Usage
Runs per agent/workflow; peak hours.

**API**  
`GET /api/analytics/usage?start=&end=`  
```json
{ "runs_total": 5200, "by_agent":[{"agent":"Code Assistant","runs":1200}] }
```

## Cost
Daily/weekly spend; top contributors.

**API**  
`GET /api/analytics/cost?interval=daily&start=&end=`  
```json
[{"date":"2025-08-01","cost_usd":4.12}]
```

## Tips
- Compare **A/B** results over the same window.  
- Track cost per successful run.
