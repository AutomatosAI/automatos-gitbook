---
description: Authenticate and connect external applications.
---

# Connecting Apps

To give your agents access to an external service, you need to connect it first.

## Step-by-step

1. Go to **Tools & Integrations** from the sidebar
2. Browse the Applications tab or search for the app you want
3. Click the app card
4. Click **Connect** or **Add**
5. Authenticate (OAuth flow or API key, depending on the app)
6. Confirm permissions

<!-- IMAGE: OAuth authentication flow for connecting GitHub -->

## Authentication methods

{% tabs %}
{% tab title="OAuth" %}
Most popular apps (GitHub, Slack, Google, Jira) use OAuth:
1. Click Connect
2. You're redirected to the app's login page
3. Authorise Automatos AI
4. You're redirected back — connection is live

No API keys to manage. Tokens refresh automatically.
{% endtab %}

{% tab title="API Key" %}
Some services require a manual API key:
1. Generate an API key in the external service
2. Paste it into the connection dialog
3. Click Save

Store keys securely in [Settings → Credentials](../settings/credentials.md).
{% endtab %}
{% endtabs %}

## Available categories

| Category | Example apps |
| --- | --- |
| **Developer Tools** | GitHub, GitLab, Bitbucket, Linear |
| **Productivity** | Slack, Microsoft Teams, Notion, Asana |
| **CRM** | Salesforce, HubSpot, Pipedrive |
| **Email** | Gmail, Outlook, SendGrid |
| **Analytics** | Datadog, PagerDuty, Sentry |
| **E-commerce** | Stripe, Shopify |
| **Storage** | Dropbox, Google Drive, S3 |
| **Databases** | PostgreSQL, MySQL, MongoDB |

<!-- IMAGE: App category tabs showing filtered results -->

## Disconnecting

To remove a connection:
1. Click the connected app card
2. Click **Disconnect**
3. Confirm

{% hint style="warning" %}
Disconnecting an app immediately revokes access for all agents using that tool. They will receive errors on the next tool call.
{% endhint %}
