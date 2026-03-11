---
description: Document templates for consistent content generation.
---

# Templates

Templates are pre-built document structures that agents use to generate consistent, formatted output.

<!-- IMAGE: Templates tab showing available document templates -->

## What are templates?

Templates define the structure, sections, and formatting for a type of document. When an agent needs to create a report, summary, or analysis, it follows the template to ensure consistent output.

## Example templates

| Template | Purpose |
| --- | --- |
| **Daily Standup** | Agent's daily report of activities and findings |
| **Security Audit** | Structured security review with severity ratings |
| **Code Review** | PR review with sections for issues, suggestions, approvals |
| **Research Summary** | Research findings with sources and recommendations |

## Using templates

Templates are automatically available to agents. When a recipe or task calls for a specific output format, the agent references the matching template.

You can also request a template in chat:
> "Write a security audit report for the auth module using the Security Audit template"

## Creating templates

1. Click **+ New Template**
2. Define the template name and description
3. Write the template structure using markdown
4. Set placeholder variables (e.g., `{{agent_name}}`, `{{date}}`)
5. Save

{% hint style="info" %}
Templates support markdown formatting, tables, and placeholder variables that are filled in automatically at generation time.
{% endhint %}
