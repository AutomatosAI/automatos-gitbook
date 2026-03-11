---
description: Create multi-step workflows that coordinate agents.
---

# Recipes

Recipes are multi-step workflows that chain multiple agents together to complete complex tasks. Think of them as playbooks — define the steps once, run them on demand or on a schedule.

<!-- IMAGE: Recipes tab showing a list of saved recipes -->

## What is a recipe?

A recipe defines:
- **Steps** — ordered list of tasks, each assigned to an agent
- **Inputs** — parameters the recipe accepts when triggered
- **Flow control** — conditional logic, branching, and error handling
- **Schedule** — optional cron-based triggers for recurring execution

## Creating a recipe

1. Click **+ Create Recipe** from the Recipes tab
2. Give it a name and description
3. Add steps, assigning each to an agent
4. Configure inputs and flow control
5. Save

<!-- IMAGE: Recipe creation dialog with steps editor -->

## Example: Nightly code review

| Step | Agent | Task |
| --- | --- | --- |
| 1 | Scout | Pull latest commits from GitHub |
| 2 | Code Reviewer | Review each commit for issues |
| 3 | Sentinel | Run security scan on changed files |
| 4 | Scribe | Write a summary report |
| 5 | Comms | Post report to Slack |

## Running a recipe

{% tabs %}
{% tab title="Manual" %}
Click **Run** on any recipe card. Fill in required inputs and confirm.
{% endtab %}

{% tab title="Scheduled" %}
Set a cron schedule (e.g., daily at 23:00) and the recipe runs automatically. View execution history in [Activity → Dashboard](../activity/dashboard.md).
{% endtab %}

{% tab title="From Chat" %}
Ask in chat: "Run the nightly code review recipe" and the router will trigger it.
{% endtab %}
{% endtabs %}

## Monitoring execution

Active recipe runs appear in:
- **Activity → Dashboard** — schedule and live status
- **Activity → Feed** — step-by-step execution log
- **Analytics → Workflows** — success rates and duration trends

{% hint style="info" %}
Recipe execution uses a scratchpad for intermediate state. Each step can read the previous step's output through the workflow pipeline.
{% endhint %}
