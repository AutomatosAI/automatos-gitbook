---
description: Workspace roles and what each one can do.
---

# Roles & Permissions

Every workspace member has one of three roles.

## Role comparison

| Permission | Admin | Member | Viewer |
| --- | --- | --- | --- |
| Chat with agents | Yes | Yes | Yes |
| View activity and reports | Yes | Yes | Yes |
| Create and edit agents | Yes | Yes | No |
| Upload documents | Yes | Yes | No |
| Run recipes | Yes | Yes | No |
| Install marketplace items | Yes | Yes | No |
| Connect tools | Yes | No | No |
| Manage team members | Yes | No | No |
| Access Settings | Yes | No | No |
| Access Analytics (Admin tab) | Yes | No | No |
| Manage credentials | Yes | No | No |
| View audit logs | Yes | No | No |

## Changing roles

1. Go to **Team Management**
2. Find the member in the list
3. Click the role dropdown
4. Select the new role
5. Confirm

{% hint style="warning" %}
A workspace must have at least one admin. You cannot demote the last remaining admin.
{% endhint %}

## Admin-only features

These pages and tabs are only visible to admins:
- **Team Management** — the entire page
- **Settings** — system configuration, credentials, audit logs
- **Context Engineering** — RAG system tuning
- **Analytics → Admin** — system-level metrics

## Context Engineering role

The **Context Engineering** permission allows users to:
- Edit global system prompts
- Modify the orchestrator soul and personality settings
- Configure heartbeat parameters
- Manage agent coordination rules

This is a specialised role for team members responsible for tuning how agents behave across the workspace.
