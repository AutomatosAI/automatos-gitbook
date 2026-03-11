---
description: Tool connection security, permissions, and auditing.
---

# Security

The Security tab on the Tools page shows the health and security posture of your tool connections.

<!-- IMAGE: Tools Security tab showing connection health status -->

## Connection health

Each connection shows:
- **Status** — healthy, warning, or expired
- **Last validated** — when the connection was last tested
- **Expiry** — for OAuth tokens, when the refresh is needed
- **Scope** — what permissions were granted

## Credential management

Tool credentials are:
- Encrypted at rest
- Never exposed in logs or agent responses
- Rotatable without agent downtime
- Scoped to your workspace

Manage credentials in [Settings → API Keys & Credentials](../settings/credentials.md).

## Audit trail

Every tool call is logged:
- Which agent made the call
- What action was performed
- Timestamp and response status
- Input parameters (with sensitive data redacted)

View the audit trail in [Settings → Audit Logs](../settings/audit-logs.md).

{% hint style="warning" %}
If a connection shows "expired", re-authenticate it immediately. Agents will receive errors until the connection is restored.
{% endhint %}
