---
description: Query your data with SQL or natural language.
---

# Database

The Database tab provides direct access to your workspace data through SQL and natural language queries.

<!-- IMAGE: Database tab showing SQL Explorer with query results -->

## Sub-tabs

{% tabs %}
{% tab title="SQL Explorer" %}
Write and execute SQL queries directly:
- Full SQL editor with syntax highlighting
- Query results displayed as a table
- Export results as CSV
- Save queries for reuse

<!-- IMAGE: SQL Explorer with a query and tabular results -->
{% endtab %}

{% tab title="Semantic Layer" %}
Natural language to SQL mappings. Define how business terms map to database columns and tables, so agents can answer data questions without writing SQL.

Example: "How many agents are active?" maps to `SELECT COUNT(*) FROM agents WHERE status = 'active'`
{% endtab %}

{% tab title="Query Templates" %}
Pre-built query templates for common operations:
- Agent performance summaries
- Document processing statistics
- Workflow execution history
- Usage analytics

Click a template to run it instantly or customise it first.
{% endtab %}

{% tab title="Training" %}
Teach the NL2SQL system with examples:
1. Enter a natural language question
2. Provide the correct SQL query
3. The system learns to handle similar questions

More training examples = better accuracy for your agents' data queries.
{% endtab %}

{% tab title="Schema Browser" %}
Explore your database schema:
- Tables and their columns
- Column types and constraints
- Relationships between tables
- Indexes
{% endtab %}

{% tab title="Audit History" %}
Log of all database queries executed:
- Query text
- Who ran it (user or agent)
- Execution time
- Result row count
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
SQL queries execute with read-only access by default. Write operations require explicit permission in Settings.
{% endhint %}
