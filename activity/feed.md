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
