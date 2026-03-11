---
description: Plugins and skills that extend agent functionality.
---

# Capabilities

The Capabilities tab has two sub-sections: **Plugins** and **Skills**.

{% tabs %}
{% tab title="Plugins" %}
Plugins are bundled packages that extend agent functionality. A plugin can include:
- Skills (git-based capabilities)
- Commands (custom tool definitions)
- Agent configurations
- Prompt templates

**Installing a plugin:**
1. Browse the Plugins sub-tab
2. Click a plugin card for details
3. Click **Install**
4. Assign to agents from the [Agent Details → Plugins](../agents/details.md) tab

<!-- IMAGE: Plugins sub-tab showing available plugin cards -->
{% endtab %}

{% tab title="Skills" %}
Skills are individual capability modules loaded from git repositories. They give agents specific abilities like:
- Code analysis patterns
- Document summarisation strategies
- Domain-specific knowledge
- Custom tool implementations

**Installing a skill:**
1. Browse the Skills sub-tab
2. Click a skill card
3. Click **Install**
4. Assign to agents

Skills are defined by a `SKILL.md` file in a git repository with instructions, prompts, and tool definitions.

<!-- IMAGE: Skills sub-tab showing available skill cards -->
{% endtab %}
{% endtabs %}

## Installed vs. available

- **Installed** items appear in your workspace inventory and can be assigned to agents
- **Available** items are in the marketplace but not yet installed

{% hint style="info" %}
You can also create custom plugins and skills from your own repositories. See [Agent Plugins & Skills](../agents/details.md) in the Agent Details section.
{% endhint %}
