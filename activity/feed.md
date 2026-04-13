---
description: Real-time activity log of everything your agents do.
---

# Feed

The Feed tab shows a chronological stream of all activity in your workspace.

<!-- IMAGE: Activity Feed showing timestamped events from multiple agents -->

## What appears in the feed

Every significant action generates a feed entry:
- Agent responses to user messages
- Tool calls (GitHub commits, Slack messages, API calls)
- Recipe step completions
- Report submissions
- Memory operations
- System events (agent start/stop, errors)

## Feed entry format

Each entry shows:
- **Timestamp** — when the action occurred
- **Agent** — which agent performed it
- **Action type** — icon indicating the type (chat, tool, report, etc.)
- **Summary** — brief description of what happened
- **Details** — expandable section with full output

## Filtering

Filter the feed by:
- **Agent** — show only one agent's activity
- **Action type** — tool calls, chat responses, reports, etc.
- **Time range** — narrow to a specific period
- **Search** — text search across feed entries

{% hint style="info" %}
The feed updates in real-time via server-sent events (SSE). New entries appear at the top automatically.
{% endhint %}

## Feed event types

The feed captures every platform action:

| Event type | Example |
| --- | --- |
| **Chat message** | User sent a message, agent responded |
| **Tool call** | Agent called GitHub API to fetch a PR |
| **Recipe step** | Step 3 of "Nightly Review" completed |
| **Mission update** | Mission "API Audit" task 2 marked complete |
| **Memory stored** | Agent saved a new fact to long-term memory |
| **Report generated** | Sentinel generated a security standup report |
| **Routing decision** | Universal Router selected Code Reviewer for a message |

### Filtering the feed

Use the filter controls at the top to narrow down:
- By agent
- By event type
- By time range
- By keyword search
