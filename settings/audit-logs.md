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
The workspace audit log, under **Command Centre → Governance → Audit** (workspace admins), keeps entries for a set retention period, never less than 180 days, and deletes older entries automatically. The local edition keeps 365 days unless you change `AUDIT_RETENTION_DAYS`. Its entries can't be edited or deleted from the app. Credential entries in **Settings → Audit Logs** are removed when the credential they belong to is deleted.
{% endhint %}

## Exporting

The app has no export button. Workspace admins can read the workspace audit log through the API, page by page: `GET /api/v1/governance/audit-log` (see the [API Reference](../api-reference.md)).
