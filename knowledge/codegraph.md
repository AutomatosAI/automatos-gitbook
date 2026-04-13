---
description: Index code repositories as a searchable knowledge graph.
---

# CodeGraph

CodeGraph indexes your code repositories so agents can search and understand your codebase semantically.

<!-- IMAGE: CodeGraph tab showing indexed repository with symbol browser -->

## What CodeGraph does

- **Parses** source code into a graph of symbols (classes, functions, variables)
- **Indexes** relationships between symbols (calls, imports, inheritance)
- **Enables** agents to answer questions like:
  - "Where is the User class defined?"
  - "What calls the authentication middleware?"
  - "Show me all API endpoints"

## Connecting a repository

1. Go to **Knowledge Bases → CodeGraph**
2. Click **+ Add Repository**
3. Enter the repository URL (or select from connected GitHub repos)
4. Choose branches to index
5. Click **Index**

<!-- IMAGE: Add Repository dialog with URL input and branch selection -->

## Browsing the graph

Once indexed, you can:
- Browse files and symbols
- See call graphs and dependency trees
- Search by symbol name or description
- View code snippets with syntax highlighting

## How agents use CodeGraph

When you ask a code question in Chat, the agent:
1. Searches CodeGraph for relevant symbols and files
2. Retrieves the source code context
3. Uses it alongside the LLM to generate an accurate answer

This is especially powerful for large codebases where agents need to understand relationships between components.

## Entity extraction

CodeGraph doesn't just index symbols — it also extracts semantic entities:
- API endpoints and their parameters
- Configuration keys and their usage
- Business logic patterns
- Error handling flows

These entities feed into the broader Knowledge Graph, connecting your code knowledge with your document knowledge.

## Re-indexing

CodeGraph re-indexes in two ways:
- **Automatic** — when new commits are pushed to connected GitHub repositories
- **Manual** — click **Re-index** to trigger a full rebuild

Indexing runs in the background. You can continue using the platform while it processes.

{% hint style="info" %}
CodeGraph re-indexes automatically when new commits are pushed to connected repositories (if GitHub integration is active).
{% endhint %}
