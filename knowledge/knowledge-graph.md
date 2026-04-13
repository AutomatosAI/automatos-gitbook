---
description: Explore entity relationships and enhance search with knowledge graph features.
---

# Knowledge Graph

The Knowledge Graph automatically extracts entities and relationships from your documents, creating a connected web of knowledge that goes beyond keyword search.

## What the Knowledge Graph does

When you upload documents, the system doesn't just chunk and embed them — it also extracts:
- **Entities** — people, concepts, technologies, processes mentioned in your documents
- **Relationships** — how entities connect (references, depends on, implements, etc.)
- **Context** — the surrounding information that gives relationships meaning

This creates a graph structure that agents can traverse to find connections that vector search alone would miss.

## Browsing the graph

Go to **Knowledge Bases → Knowledge Graph** to:
- **Search entities** — find specific concepts with full-text search
- **View entity details** — see all relationships and source documents for an entity
- **Explore connections** — navigate from entity to entity, following relationships
- **Visualise** — see a graph visualisation of entities and their connections
- **Find paths** — discover how two concepts are connected through intermediate entities

## Graph-enhanced RAG

When an agent searches your knowledge base, the Knowledge Graph enriches results:

1. **Vector search** finds the most relevant document chunks
2. **Graph traversal** discovers related entities and their connected documents
3. **Combined results** give the agent both directly relevant and contextually related information

This means agents can answer questions that require connecting information across multiple documents — something pure vector search struggles with.

## Entity types

The system automatically categorises extracted entities:
- Technologies and tools
- People and organisations
- Processes and workflows
- Concepts and terms
- APIs and endpoints
- Data structures

Filter by type when browsing to focus on specific categories.

## Managing the graph

- **Rebuild** — trigger a full re-extraction from all documents
- **Import** — import entity data from external sources
- **Statistics** — view entity counts, relationship counts, and graph density
- **Snapshots** — the system takes daily snapshots and computes diffs so you can track how your knowledge graph evolves

## Team access control

Entity visibility respects team access settings. If a document is restricted to certain team members, its extracted entities are only visible to those members.

{% hint style="info" %}
The Knowledge Graph builds automatically as you upload documents. No manual configuration needed — but you can trigger a rebuild if you want to re-extract entities after updating the extraction model.
{% endhint %}

## Related

- [Documents](documents.md) — uploading and managing source documents
- [Database](database.md) — structured data querying
- [CodeGraph](codegraph.md) — code-specific knowledge graph
