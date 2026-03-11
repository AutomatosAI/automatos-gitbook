---
description: Knowledge base processing and search analytics.
---

# Document Analytics

The Documents tab tracks your knowledge base health and search performance.

<!-- IMAGE: Document Analytics showing processing stats and search metrics -->

## Key metrics

| Metric | Description |
| --- | --- |
| **Documents Indexed** | Total files processed and searchable |
| **Vector Chunks** | Number of embedding chunks stored |
| **Search Queries** | Total searches performed (by agents and users) |
| **Hit Rate** | Percentage of searches that returned relevant results |
| **Processing Throughput** | Documents processed per hour |

## Storage trends

- **Document growth** — cumulative document count over time
- **Storage usage** — S3 storage consumed
- **Chunk growth** — vector chunk count over time

## Search quality

- **Query volume** — searches per day
- **Hit rate trend** — are search results improving?
- **Top queries** — most common search terms
- **Zero-result queries** — searches that found nothing (content gap indicators)

{% hint style="info" %}
Zero-result queries highlight topics your knowledge base doesn't cover. Upload more documents on those topics to improve agent accuracy.
{% endhint %}
