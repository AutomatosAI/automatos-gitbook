---
description: Global agent configuration and default settings.
---

# Configuration

The Configuration tab on the Agents page manages workspace-wide agent settings that apply as defaults across your fleet.

<!-- IMAGE: Configuration tab showing global settings panel -->

## Default model settings

Set the default LLM provider and model for new agents. Individual agents can override these.

| Setting | Description |
| --- | --- |
| **Default Provider** | The LLM provider used when creating new agents |
| **Default Model** | The model ID used as the starting point |
| **Default Temperature** | Base creativity setting for new agents |
| **Max Token Limit** | System-wide cap on response length |

## System prompt defaults

Configure base system prompt snippets that are injected into all agents:
- **Global instructions** — rules every agent follows
- **Safety guidelines** — content filtering and guardrails
- **Output formatting** — response structure preferences

{% hint style="info" %}
Agent-specific system prompts are appended after global defaults. The agent's own prompt takes priority when there's a conflict.
{% endhint %}

## Agent categories

Manage the available agent categories (code_architect, security_expert, data_analyst, custom, etc.). Categories help with:
- Organising the roster
- Routing decisions
- Analytics grouping

## Orchestrator soul

The orchestrator soul defines the overarching personality and behaviour of your entire agent fleet. It sets:
- **Global tone** — professional, casual, or technical
- **Safety boundaries** — what agents are not allowed to do
- **Response guidelines** — length, formatting, and style rules

This is applied as a base layer to every agent's system prompt. Individual agent prompts are appended after and can override specific behaviours.

## Heartbeat settings

Configure the heartbeat mode — periodic background tasks that agents run independently:
- **Interval** — how often agents check for scheduled work
- **Scope** — which agents participate in heartbeat cycles
- **Context** — heartbeat mode uses minimal context (no conversation history) to keep costs low
