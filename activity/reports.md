---
description: Browse and grade agent reports.
---

# Reports

The Reports tab is where you review what your agents have produced. Agents submit reports after completing tasks, scheduled routines, or when they find something noteworthy.

<!-- IMAGE: Reports tab showing grid of report cards with filters -->

## Report cards

Each report appears as a card showing:
- **Agent name** and icon
- **Report title** and type
- **Timestamp** — when it was submitted
- **Status** — unread, reviewed, graded
- **Preview** — first few lines of content

Click a card to open the full report in a slide-over panel.

## Report viewer

The report viewer shows:
- Full markdown-rendered report content
- Referenced files and artifacts
- Linked agent and task details

<!-- IMAGE: Report viewer slide-over showing full report content -->

## Grading reports

Rate report quality with a star rating system:
1. Open a report
2. Click the grade button
3. Select a star rating (1-5)
4. Optionally add a comment

Grading helps track agent quality over time and appears in [Analytics → Agents](../analytics/agents.md).

{% hint style="info" %}
Reports are stored persistently in the workspace filesystem at `/reports/{agent}/{date}_{slug}.md` and in the database for querying.
{% endhint %}

## Filters

Filter reports by:
- **Agent** — show only one agent's reports
- **Date range** — narrow to a time period
- **Status** — unread, reviewed, graded
- **Type** — routine, task completion, incident
