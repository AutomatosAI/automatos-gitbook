---
description: Explore and manage what your agents remember.
---

# Memory

The Memory tab lets you explore the memory system — what your agents have stored, recalled, and learned across interactions.

<!-- IMAGE: Memory tab showing stored memories with search and browse interface -->

## How agent memory works

Agents automatically store important information from conversations and tasks:
- Key facts and decisions from chat interactions
- Results from completed tasks
- User preferences and corrections
- Cross-agent shared knowledge

Memory is persisted across conversations, so agents build context over time.

## Browsing memories

The memory explorer shows:
- **Memory entries** — individual facts or learnings
- **Source** — which agent stored it
- **Timestamp** — when it was created
- **Relevance** — how often it's been recalled

## Searching

Search across all stored memories by keyword or topic. The search uses vector similarity, so natural language queries work well:
- "What do we know about the authentication system?"
- "Previous security findings"
- "Customer preferences"

## Managing memories

- **Delete** — remove incorrect or outdated memories
- **Edit** — correct factual errors in stored memories
- **Pin** — mark important memories to prevent pruning

{% hint style="warning" %}
Deleting a memory is permanent. The agent will no longer recall that information.
{% endhint %}

## Memory per agent

Each agent has its own memory scope, plus access to workspace-level shared memories. This means:
- Sentinel's security findings don't clutter Code Reviewer's memory
- Shared knowledge (project context, team preferences) is available to all agents

## Memory architecture

The memory system has two tiers:

| Tier | Name | What it stores | Retention |
| --- | --- | --- | --- |
| **L2** | Short-term memory | Recent conversation context, active task state | Session-scoped, stored in PostgreSQL |
| **L3** | Long-term memory | Important facts, decisions, user preferences, cross-conversation learnings | Persistent, survives across sessions |

### How memories are created

Agents automatically extract and store important information during conversations and task execution. The system identifies:
- Key decisions and their rationale
- User preferences and corrections
- Task outcomes and findings
- Cross-agent shared knowledge

### Memory consolidation

The platform periodically consolidates memories — merging related facts, removing duplicates, and strengthening frequently-recalled information. This happens automatically as part of the session lifecycle.

### Memory augmentation

Agents can be instructed to store specific knowledge via the memory API. External data (from tools, documents, or manual input) can also be injected into the memory system.
