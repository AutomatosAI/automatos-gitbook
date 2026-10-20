---
description: Create multi-step workflows that coordinate agents.
---

# Playbooks

Playbooks are multi-step workflows that chain multiple agents together to complete complex tasks. Define the steps once, run them on demand or on a schedule.

<!-- IMAGE: Playbooks tab showing a list of saved playbooks -->

## What is a playbook?

A playbook defines:
- **Steps** — ordered list of tasks, each assigned to an agent
- **Inputs** — parameters the playbook accepts when triggered
- **Flow control** — conditional logic, branching, and error handling
- **Schedule** — optional cron-based triggers for recurring execution

## Creating a playbook

1. Click **+ Create Playbook** from the Playbooks tab
2. Give it a name and description
3. Add steps, assigning each to an agent
4. Configure inputs and flow control
5. Save

<!-- IMAGE: Playbook creation dialog with steps editor -->

## Example: Two-minute brief

A fresh local install includes this demo playbook. It takes one input, a topic, and needs nothing beyond your AI key:

| Step | Agent | Task |
| --- | --- | --- |
| 1 | Researcher | Research the topic and write research notes |
| 2 | Writer | Write a one-page brief from the Researcher's notes |
| 3 | Analyst | Review the brief, fix gaps or unsupported claims, and output the final brief |

## Running a playbook

{% tabs %}
{% tab title="Manual" %}
Click **Run** on any playbook card. Fill in required inputs and confirm.
{% endtab %}

{% tab title="Scheduled" %}
Set a cron schedule (e.g., daily at 23:00) and the playbook runs automatically. View execution history in [Activity → Dashboard](../activity/dashboard.md).
{% endtab %}

{% tab title="From Chat" %}
Ask Auto in chat: "Run the Two-minute brief playbook on electric bikes". Auto shows the run on a card for you to approve, then starts it.
{% endtab %}
{% endtabs %}

## Monitoring execution

Active playbook runs appear in:
- **Activity → Dashboard** — schedule and live status
- **Activity → Feed** — step-by-step execution log
- **Analytics → Workflows** — success rates and duration trends

{% hint style="info" %}
Playbook execution uses a scratchpad for intermediate state. Each step can read the previous step's output through the workflow pipeline.
{% endhint %}

## Webhook triggers

Playbooks can be triggered automatically by external events:

| Trigger | Source | Example |
| --- | --- | --- |
| **Jira** | Issue created or updated | Run a triage playbook when a bug is filed |
| **GitHub** | Push, PR, or issue event | Run code review on every pull request |
| **Slack** | Message in a channel | Run a research playbook when tagged |

Set up webhook triggers in the playbook's trigger configuration. The platform automatically registers the webhook URL with the external service.

## Saving missions as playbooks

Completed missions can be saved as reusable playbook templates. From the mission detail page, click **Save as Routine** to extract the task pattern into a playbook that can be re-run on demand or on schedule.
