---
description: Real-time overview of your AI workspace.
---

# Dashboard

The Dashboard tab is the default view on the Activity page. It gives you a real-time snapshot of everything happening in your workspace.

<!-- IMAGE: Activity Dashboard showing status cards, schedule, active tasks, and reports -->

## Schedule

A weekly calendar view showing:
- Today highlighted with a marker
- Dots indicating days with scheduled routines
- Upcoming schedule listed chronologically below

Example scheduled items:
- `23:45` — Sentinel Routine
- `08:00` — Comms Routine
- `20:00` — Nightly Self-Test Suite
- `06:00` — API Health Check & Regression Detector
- `09:00` — QA Engineer Routine

<!-- IMAGE: Schedule section showing weekly calendar and upcoming tasks list -->

{% hint style="info" %}
Scheduled routines are created through [Recipes](../agents/recipes.md) with cron triggers. Click any item to view or edit the schedule.
{% endhint %}

## Active Now

Shows tasks currently in progress:
- Task name and assigned agent
- Progress bar (percentage complete)
- Elapsed time
- Step count (e.g., "Step 1/4")

<!-- IMAGE: Active Now section showing a running task with progress bar -->

## Agent Reports

A grid of your agents with their latest report status:

| Column | Description |
| --- | --- |
| **Agent** | Name and icon |
| **Last active** | Time since last activity |
| **Status** | "Checked 1 item", "No reports yet", etc. |
| **Action** | **View Report** link to open the full report |

<!-- IMAGE: Agent Reports grid showing agents with View Report links -->

## Customise

Click **Customise** in the top right to configure which sections appear on your dashboard and their layout.

## Time range

Use the time range selector (top right) to view activity for:
- 1 Day (default)
- 7 Days
- 30 Days
