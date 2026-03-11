---
description: Review all system activity and security events.
---

# Audit Logs

Audit Logs provide a complete record of every significant action in your workspace.

<!-- IMAGE: Audit Logs showing timestamped event list with filters -->

## What gets logged

| Category | Examples |
| --- | --- |
| **User actions** | Login, logout, settings changes |
| **Agent operations** | Agent created, edited, deleted |
| **Tool calls** | External API calls made by agents |
| **Credential changes** | Keys added, rotated, deleted |
| **Team changes** | Members invited, roles changed, removed |
| **Document operations** | Uploads, deletions, sync events |
| **Security events** | Failed auth attempts, permission denials |

## Log entry format

Each entry shows:
- **Timestamp** — when the action occurred
- **Actor** — who performed it (user or agent)
- **Action** — what was done
- **Target** — what was affected
- **Details** — additional context (expandable)
- **Status** — success or failure

## Filtering

Filter logs by:
- **Date range** — narrow to a specific period
- **Actor** — specific user or agent
- **Category** — user, agent, tool, security, etc.
- **Status** — success or failure only
- **Search** — text search across log entries

{% hint style="info" %}
Audit logs are retained for the lifetime of your workspace. They cannot be deleted — this ensures a complete audit trail for compliance.
{% endhint %}

## Exporting

Click **Export** to download logs as CSV for external analysis or compliance reporting.
