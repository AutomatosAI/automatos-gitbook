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
