---
title: Settings
description: Configure system settings, manage credentials, and review security audit logs
---

# ⚙️ Settings Guide

*Configure your Automatos AI Platform - system, credentials, and security*

---

## 📖 Table of Contents

1. [Overview](#overview)
2. [Quick Start](#quick-start)
3. [System Settings Tab](#system-settings-tab)
4. [Credentials Tab](#credentials-tab)
5. [Credential Types Tab](#credential-types-tab)
6. [Audit Logs Tab](#audit-logs-tab)
7. [Common Tasks](#common-tasks)
8. [Tips & Best Practices](#tips--best-practices)
9. [Troubleshooting](#troubleshooting)

---

## Overview

### What is Settings?

The Settings page is your control panel for platform configuration, credential management, and security auditing.

**Access**: Navigate to **Settings** from the sidebar (gear icon)

![Settings Overview](images/settings_overview.png)

### What Can You Do Here?

- ✅ **Configure system settings** (6 sub-sections)
- ✅ **Manage credentials** securely (encrypted storage)
- ✅ **Browse 400+ credential types**
- ✅ **Review audit logs** for compliance
- ✅ **Set API keys** for LLM providers
- ✅ **Configure logging** and rate limiting

### Page Layout

Settings has **4 main tabs**:

1. **⚙️ System Settings** - Platform configuration (6 sub-tabs)
2. **🔐 Credentials** - Secure credential management
3. **📋 Credential Types** - 400+ credential type templates
4. **📜 Audit Logs** - Security and compliance logging

---

## Quick Start

### Configure Your First Credential (5 Minutes)

**Goal**: Add OpenAI API key for agents

**Steps**:

1. Go to Settings → **Credentials** tab
2. Click **"Create Credential"**
3. **Type**: Select "OpenAI API"
4. **Name**: "Production OpenAI"
5. **API Key**: Paste your OpenAI key
6. **Test Connection**: Verify it works ✅
7. Click **"Save"**

⏱️ **Time**: 3 minutes  
🎯 **Result**: Agents can use OpenAI

**[See detailed walkthrough →](#credentials-tab)**

---

## System Settings Tab

### Overview

The System Settings tab has **6 sub-tabs** for different configuration areas:

![System Settings Tab](images/settings_system_tab.png)

### Sub-Tab 1: General

💡 *Tooltip: "Basic platform configuration and preferences"*

**Platform Information** (read-only):
- **Platform Version**: Current version
- **API Version**: API version number
- **Installation ID**: Unique instance ID
- **License Type**: Open Source / Enterprise

**General Settings**:

**Platform Name**  
💡 *Tooltip: "Custom name for your instance. Shown in UI and emails."*

- Default: "Automatos AI Platform"
- Customize: "Acme Corp AI Platform"

**Time Zone**  
💡 *Tooltip: "Default timezone for timestamps and scheduling"*

- Select from list
- Example: "America/New_York"
- Affects logs, schedules

**Language**  
💡 *Tooltip: "UI language. More languages coming soon."*

- English (default)
- Future: Spanish, French, German, etc.

**Theme**  
💡 *Tooltip: "UI color scheme"*

- Light mode
- Dark mode (default)
- Auto (system preference)

![General Settings](images/settings_system_general.png)

**Default Execution Settings**:

**Default Timeout**  
💡 *Tooltip: "Default timeout for agent tasks and workflows. Can override per agent/workflow."*

- Range: 30s to 30 minutes
- Recommended: 5 minutes

**Default Token Budget**  
💡 *Tooltip: "Default token limit for agent responses"*

- Range: 100-8000 tokens
- Recommended: 2000 tokens

**Auto-Start Agents**  
💡 *Tooltip: "Automatically activate agents on platform startup"*

- ✅ Enabled: Agents start automatically
- ❌ Disabled: Manual activation required

### Sub-Tab 2: Orchestrator LLM

💡 *Tooltip: "Configure the LLM used by the orchestrator for task decomposition and agent selection"*

![Orchestrator LLM Settings](images/settings_system_orchestrator.png)

**Orchestrator Model**:

**Provider**  
💡 *Tooltip: "LLM provider for orchestrator reasoning. Separate from agent models."*

- OpenAI (default)
- Anthropic
- HuggingFace

**Model**  
💡 *Tooltip: "Specific model for orchestration. Needs function calling support."*

- GPT-4 Turbo (recommended)
- GPT-4
- Claude 3 Opus

**Temperature**  
💡 *Tooltip: "Orchestrator creativity. Lower = more consistent decomposition."*

- Range: 0.0-1.0
- Recommended: 0.3 (consistent)

**Max Tokens**  
💡 *Tooltip: "Max tokens for orchestrator responses (task decomposition, agent selection reasoning)"*

- Range: 1000-4000
- Recommended: 2000

**Reasoning Mode**:

**LLM-Driven Selection**  
💡 *Tooltip: "Orchestrator uses reasoning to select agents. Higher quality but slower."*

- ✅ Enabled (recommended)
- ❌ Disabled (falls back to algorithm)

**Algorithmic Fallback**  
💡 *Tooltip: "Use algorithm if LLM selection fails"*

- ✅ Enabled for reliability

### Sub-Tab 3: CodeGraph

💡 *Tooltip: "Configure code indexing and search capabilities"*

![CodeGraph Settings](images/settings_system_codegraph.png)

**Indexing Settings**:

**Enabled**  
💡 *Tooltip: "Enable/disable CodeGraph feature platform-wide"*

- ✅ Enabled
- ❌ Disabled

**Supported Languages**  
💡 *Tooltip: "Programming languages to index"*

- Python ✅
- TypeScript ✅
- JavaScript ✅
- Java ✅
- Go ✅
- Rust ✅
- C++ ✅
- Add custom languages

**Max File Size**  
💡 *Tooltip: "Maximum file size to index (larger files skipped)"*

- Range: 100KB - 10MB
- Recommended: 1MB

**Exclude Patterns**  
💡 *Tooltip: "Glob patterns to skip during indexing"*

- Default: `node_modules, __pycache__, venv, .git, *.pyc`
- Add more as needed

**Cache Settings**:

**Cache TTL**  
💡 *Tooltip: "How long to cache search results"*

- Range: 0-3600 seconds
- Recommended: 300s (5 minutes)

**Auto-Reindex**  
💡 *Tooltip: "Automatically re-index on code changes (via webhooks)"*

- ✅ Enabled for active projects
- ❌ Disabled for archived projects

### Sub-Tab 4: Logging

💡 *Tooltip: "Configure system logging and retention"*

![Logging Settings](images/settings_system_logging.png)

**Log Levels**:

**Application Log Level**  
💡 *Tooltip: "Minimum severity to log. DEBUG = everything, ERROR = only errors."*

- DEBUG (development)
- INFO (default)
- WARNING (production)
- ERROR (minimal)

**Agent Log Level**  
💡 *Tooltip: "Logging for agent executions"*

- Same options as application

**Workflow Log Level**  
💡 *Tooltip: "Logging for workflow orchestration"*

- Same options

**Log Retention**:

**Keep Logs For**  
💡 *Tooltip: "How long to retain logs before auto-deletion"*

- 7 days
- 30 days (default)
- 90 days
- 1 year
- Forever

**Log Storage Limit**  
💡 *Tooltip: "Maximum disk space for logs. Oldest deleted when limit reached."*

- Range: 1GB - 100GB
- Recommended: 10GB

**Log Destinations**:
- ✅ Database (searchable)
- ✅ File system (for export)
- ❌ External service (Datadog, etc.) - configure separately

### Sub-Tab 5: Rate Limiting

💡 *Tooltip: "Protect against API abuse and control costs"*

![Rate Limiting Settings](images/settings_system_rate_limit.png)

**Global Rate Limits**:

**API Requests per Minute**  
💡 *Tooltip: "Maximum API calls per minute (all users combined)"*

- Range: 100-10,000
- Default: 1,000
- Protects against overload

**Workflow Executions per Hour**  
💡 *Tooltip: "Maximum workflows that can be created per hour"*

- Range: 10-1,000
- Default: 100
- Prevents runaway automation

**Agent Executions per Minute**  
💡 *Tooltip: "Maximum agent tasks per minute"*

- Range: 10-500
- Default: 50

**Per-User Limits**:

**User API Rate**  
- Requests per minute per user
- Default: 100

**User Workflow Rate**  
- Workflows per hour per user
- Default: 20

**LLM Provider Limits**:

**OpenAI Requests per Minute**  
💡 *Tooltip: "Limit to stay within OpenAI tier limits and control costs"*

- Based on your OpenAI tier
- Default: 3,500 (Tier 3)

**Anthropic Requests per Minute**  
- Based on Anthropic limits
- Default: 1,000

### Sub-Tab 6: API Keys

💡 *Tooltip: "Manage API keys for external access to Automatos AI"*

![API Keys Settings](images/settings_system_api_keys.png)

**Your API Keys**:

List of active API keys:
- **Key Name**: Identifier
- **Key Preview**: First/last 8 characters (middle hidden)
- **Permissions**: Scopes assigned
- **Last Used**: Timestamp
- **Created**: Creation date
- **Expires**: Expiration date (if set)

**Create API Key**:

Click **"Create API Key"**:

**Name** (required)  
💡 *Tooltip: "Descriptive name for this key. Example: 'CI/CD Pipeline', 'Mobile App'"*

**Permissions** (checkboxes)  
💡 *Tooltip: "Grant specific permissions. Use least privilege principle."*

- ✅ Read Agents
- ✅ Execute Agents
- ✅ Create Workflows
- ✅ Read Documents
- ❌ Delete Resources (rarely needed)
- ❌ Admin (very restricted)

**Expiration**  
💡 *Tooltip: "Auto-expire for security. Recommended: 90 days."*

- Never (not recommended)
- 30 days
- 90 days (recommended)
- 1 year
- Custom date

**Rate Limit**  
💡 *Tooltip: "Override default rate limit for this key"*

- Use default
- Custom: X requests/minute

**Created Key**:
- Shows full key ONCE
- Copy immediately
- Cannot view again (security)
- Store securely

**Revoking Keys**:
- Click "Revoke" button
- Immediate effect
- Cannot be undone
- All requests using key will fail

---

## Credentials Tab

### Overview

Securely manage authentication credentials for external services.

💡 *Tooltip: "Encrypted storage for API keys, passwords, tokens. Required for agents to use external tools."*

![Credentials Tab](images/settings_credentials_tab.png)

### Statistics Cards

**🔐 Total Credentials**  
💡 *Tooltip: "Number of stored credentials. All encrypted at rest."*

- Count of credentials
- Active vs inactive

**✅ Verified**  
💡 *Tooltip: "Credentials tested and working"*

- Count with successful tests
- Percentage verified

**⚠️ Expiring Soon**  
💡 *Tooltip: "Credentials nearing expiration (if configured)"*

- Count expiring <30 days
- Attention needed

**🔧 In Use**  
💡 *Tooltip: "Credentials actively assigned to agents"*

- Count assigned to agents
- Usage percentage

![Credentials Stats](images/settings_credentials_stats.png)

### Credential List

Each credential shows:

**Credential Card**:

- **Name**: Descriptive name (e.g., "Production OpenAI")
- **Type**: Credential type (OpenAI API, PostgreSQL, etc.)
- **Status Badge**: 
  - 🟢 Active & Verified
  - 🟡 Active & Unverified
  - 🔴 Inactive or Failed Test
- **Environment**: Production / Development / Staging
- **Created**: Date added
- **Last Used**: Recent usage timestamp

**Metadata**:
- Tags (for organization)
- Description
- Assigned to: X agents

![Credential Card](images/settings_credentials_card.png)

**Actions**:
- **🔧 Edit**: Modify credential
- **🧪 Test**: Test connection
- **👁️ View**: See details (values hidden)
- **🗑️ Delete**: Remove credential (with confirmation)

### Creating a Credential

Click **"Create Credential"** button:

**Create Credential Modal**:

![Create Credential Modal](images/settings_credentials_create.png)

**Step 1: Select Type**  
💡 *Tooltip: "Choose credential type. Determines required fields."*

- Search or browse credential types
- Popular: OpenAI API, PostgreSQL, Slack, GitHub, AWS
- Shows required fields preview
- Select type

**Step 2: Configure**:

**Credential Name** (required)  
💡 *Tooltip: "Descriptive name. Example: 'Production OpenAI', 'Dev Database'"*

**Environment**  
💡 *Tooltip: "Separate credentials by environment for safety"*

- Production
- Development
- Staging
- Testing

**Description** (optional)  
💡 *Tooltip: "Notes about this credential - when to use, special configuration, etc."*

**Tags** (optional):
- Add tags for organization
- Example: "ai", "production", "primary"

**Credential Fields** (depends on type):

**Example: OpenAI API**:
- **API Key** (required, secure) 🔒  
  💡 *Tooltip: "OpenAI API key starting with 'sk-'. Get from platform.openai.com"*
- **Organization ID** (optional)
- **Base URL** (optional, default: https://api.openai.com/v1)

**Example: PostgreSQL**:
- **Host** (required)
- **Port** (default: 5432)
- **Database** (required)
- **User** (required)
- **Password** (required, secure) 🔒
- **SSL Mode** (prefer, require, disable)

**Example: Slack**:
- **Bot Token** (required, secure) 🔒  
  💡 *Tooltip: "Slack Bot User OAuth Token (xoxb-...)"*
- **Signing Secret** (optional)
- **App ID** (optional)

![Credential Fields](images/settings_credentials_fields.png)

**Step 3: Test Connection**:

💡 *Tooltip: "Verify credential works before saving. Highly recommended!"*

- Click "Test Connection" button
- System attempts connection
- **✅ Success**: Ready to save
- **❌ Failure**: Shows error, fix before saving

**Step 4: Save**:

- Click "Save Credential"
- Encrypted and stored
- Available for tool assignments

### Editing Credentials

**Security Note**: Existing values are hidden (shown as •••••)

**When Editing**:
- All fields shown but values hidden
- Update only fields you want to change
- Leave others blank to keep existing
- Re-test after editing

### Testing Credentials

Click **"Test"** button on credential card:

**Test Connection Process**:

1. Decrypts credential
2. Attempts connection to service
3. Runs validation query/request
4. Returns result

**Test Results**:

**✅ Success**:
```
✅ Connection successful
Response time: 234ms
Test query: OK
Status: Verified
```

**❌ Failure**:
```
❌ Connection failed
Error: Invalid API key
Details: 401 Unauthorized
Action: Verify API key is correct
```

---

## Credential Types Tab

### Overview

Browse 400+ credential type templates.

💡 *Tooltip: "Pre-configured credential schemas for every major service. Don't create from scratch!"*

![Credential Types Tab](images/settings_credential_types_tab.png)

### Statistics

**📋 Total Types**: 417 credential types  
**📂 Categories**: 12 categories  
**⭐ Most Used**: OpenAI API (34 instances)

### Browsing Credential Types

**Category Filter**:

💡 *Tooltip: "Filter by service category"*

- **All Categories** (417 types)
- **AI & ML** (12 types)
  - OpenAI API
  - Anthropic API
  - HuggingFace API
  - Cohere API
  - etc.
- **Databases** (25 types)
  - PostgreSQL
  - MySQL
  - MongoDB
  - Redis
  - etc.
- **Cloud Providers** (38 types)
  - AWS
  - Azure
  - Google Cloud
  - DigitalOcean
  - etc.
- **Communication** (45 types)
  - Slack
  - Discord
  - Telegram
  - Email (various providers)
  - etc.
- **Developer Tools** (67 types)
  - GitHub
  - GitLab
  - Jira
  - Jenkins
  - etc.

![Credential Type Categories](images/settings_credential_types_categories.png)

**Search**:
- Search by name: "Slack"
- Search by provider: "Google"
- Search by capability: "notification"

### Credential Type Details

Click any type to see details:

**Type Information**:
- **Name**: Official type name
- **Provider**: Service provider
- **Icon**: Visual identifier
- **Category**: Organization category
- **Description**: What it's for

**Required Fields**:
- Field name
- Field type (string, password, number, etc.)
- Required vs optional
- Default values
- Validation rules

**Example Fields** (OpenAI API):
```
✅ api_key (string, secure, required)
   Pattern: ^sk-[a-zA-Z0-9]{48}$
   
🔵 organization_id (string, optional)
   Pattern: ^org-[a-zA-Z0-9]+$
   
🔵 base_url (string, optional)
   Default: https://api.openai.com/v1
```

**Documentation Links**:
- Provider documentation
- How to get credentials
- Setup instructions

**Usage Count**:
- How many credentials of this type exist
- "34 credentials using this type"

---

## Audit Logs Tab

### Overview

Complete security audit trail of all credential operations.

💡 *Tooltip: "Every credential access logged for compliance and security. SOC2, GDPR compliant."*

![Audit Logs Tab](images/settings_audit_logs_tab.png)

### Log Filters

**Time Range**  
💡 *Tooltip: "Filter by date range"*

- Last 24 hours
- Last 7 days
- Last 30 days
- Last 90 days
- Custom range

**Action Type**  
💡 *Tooltip: "Filter by operation type"*

- All Actions
- Created
- Updated
- Deleted
- Accessed (read)
- Tested

**User Filter**  
💡 *Tooltip: "Filter by who performed the action"*

- All Users
- Select specific user

**Credential Filter**  
💡 *Tooltip: "Filter by which credential"*

- All Credentials
- Select specific credential

**Result Filter**:
- All results
- Success only
- Failure only

![Audit Log Filters](images/settings_audit_filters.png)

### Audit Log Entries

Each log entry shows:

**Log Record**:

- **Timestamp**: Exact date/time
- **Action**: What happened
  - Created credential
  - Updated credential
  - Deleted credential
  - Accessed credential
  - Tested connection
- **User**: Who performed action
- **Credential**: Which credential (name + type)
- **Result**: ✅ Success or ❌ Failure
- **IP Address**: Source IP
- **Details**: Additional context

![Audit Log Entry](images/settings_audit_log_entry.png)

**Example Entries**:

```
🟢 2024-10-21 10:35:28 | SUCCESS
   Action: Created credential
   User: admin@company.com
   Credential: Production OpenAI (OpenAI API)
   IP: 192.168.1.100
   Details: New credential created via UI

🟡 2024-10-21 10:36:12 | SUCCESS
   Action: Tested connection
   User: admin@company.com
   Credential: Production OpenAI
   IP: 192.168.1.100
   Details: Connection test successful (245ms)

🟢 2024-10-21 10:37:45 | SUCCESS
   Action: Accessed credential
   User: system
   Credential: Production OpenAI
   Service: agent-executor
   Details: Retrieved for agent CodeReviewer-Pro (agent_id: 42)

🔴 2024-10-21 11:15:33 | FAILURE
   Action: Tested connection
   User: admin@company.com
   Credential: Slack Production
   IP: 192.168.1.100
   Details: Connection failed - Invalid token
```

### Audit Log Export

**Export Options**:

💡 *Tooltip: "Export audit logs for compliance reporting or analysis"*

- **CSV Export**: Excel-compatible
- **JSON Export**: Programmatic analysis
- **PDF Report**: Human-readable audit report

**Export Configuration**:
- Date range
- Include/exclude fields
- Filter by criteria
- Format and download

---

## Common Tasks

### Task 1: Adding OpenAI API Key

**Scenario**: Configure OpenAI for agents

**Steps**:

1. **Get API Key**:
   - Go to platform.openai.com
   - Create API key
   - Copy key (starts with `sk-`)

2. **Add to Automatos**:
   - Settings → Credentials
   - Click "Create Credential"
   - Type: "OpenAI API"
   - Name: "Production OpenAI"
   - Paste API key
   - Test connection ✅
   - Save

3. **Verify**:
   - Agents can now use OpenAI models
   - Create test agent
   - Execute sample task

⏱️ **Time**: 5 minutes  
🎯 **Result**: OpenAI configured

### Task 2: Setting Up Slack Notifications

**Scenario**: Agents can send Slack messages

**Steps**:

1. **Create Slack App**:
   - Go to api.slack.com/apps
   - Create new app
   - Add Bot Token Scopes: `chat:write`, `channels:read`
   - Install app to workspace
   - Copy Bot User OAuth Token (xoxb-...)

2. **Add to Automatos**:
   - Settings → Credentials
   - Create "Slack" credential
   - Name: "Slack Production"
   - Bot Token: Paste token
   - Test ✅
   - Save

3. **Assign to Agent**:
   - Tools page → Slack
   - Assign to agent
   - Select "Slack Production" credential
   - Permissions: ✅ Write
   - Save

4. **Test**:
   - Execute agent task with instruction to send Slack message
   - Check Slack for message

⏱️ **Time**: 10 minutes  
🎯 **Result**: Slack notifications working

### Task 3: Configuring Database Credentials

**Scenario**: Agents need database access

**Steps**:

1. Settings → Credentials
2. Create "PostgreSQL" credential
3. **Configure**:
   - Name: "App Database"
   - Host: `db.company.com`
   - Port: `5432`
   - Database: `production_db`
   - User: `app_user`
   - Password: `••••••••` (secure)
   - SSL Mode: `require`
4. Test connection ✅
5. Save
6. Assign PostgreSQL tool to agents that need it

⏱️ **Time**: 5 minutes  
🎯 **Result**: Database access configured

### Task 4: Reviewing Audit Logs

**Scenario**: Monthly compliance review

**Steps**:

1. Settings → Audit Logs
2. **Time Range**: Last 30 days
3. Review:
   - All credential creations
   - All deletions
   - Failed access attempts
   - Unusual activity
4. **Export**:
   - Click "Export"
   - Format: PDF Report
   - Download for records

⏱️ **Time**: 10 minutes  
🎯 **Result**: Compliance documentation

### Task 5: Rotating Credentials

**Scenario**: Regular 90-day credential rotation

**Steps**:

1. **Create new credential**:
   - Generate new API key at provider
   - Create new credential in Automatos
   - Name: "OpenAI Production v2"
   - Test ✅

2. **Update agent assignments**:
   - Tools page
   - For each agent using old credential
   - Edit assignment
   - Change to new credential
   - Save

3. **Verify**:
   - Test agent execution
   - Ensure using new credential

4. **Delete old credential**:
   - Settings → Credentials
   - Find old credential
   - Verify not in use (0 assignments)
   - Delete

⏱️ **Time**: 15 minutes for 5 agents  
🎯 **Result**: Credentials rotated securely

---

## Advanced Features

### Credential Templates

🔧 **Advanced**

Create custom credential types for internal services:

**Custom Credential Type**:

```json
{
  "name": "Internal API",
  "provider": "Company Name",
  "category": "custom",
  "fields": [
    {
      "name": "api_endpoint",
      "type": "string",
      "required": true,
      "default": "https://internal.company.com/api"
    },
    {
      "name": "api_key",
      "type": "password",
      "required": true,
      "secure": true
    },
    {
      "name": "client_id",
      "type": "string",
      "required": false
    }
  ]
}
```

### Environment Separation

**Best Practice**: Separate credentials per environment

**Setup**:

Production credentials:
- "Production OpenAI"
- "Production Database"
- "Production Slack"

Development credentials:
- "Development OpenAI"
- "Development Database"
- "Development Slack"

**Benefits**:
- No accidental prod access from dev
- Separate billing
- Different rate limits
- Clear audit trail

### Credential Sharing

🔧 **Advanced** (Enterprise feature)

Share credentials across team:

**Team Credential**:
- Marked as "Shared"
- All team members can view/use
- Only admins can edit/delete
- All access logged per user

**Personal Credential**:
- Private to creator
- Others can't view/use
- Full control

---

## Tips & Best Practices

### Credential Naming

💡 **Best Practices**:

**Good names**:
- ✅ "Production OpenAI - Primary"
- ✅ "Dev Database - PostgreSQL"
- ✅ "Slack - Engineering Channel"

**Poor names**:
- ❌ "OpenAI 1"
- ❌ "Test"
- ❌ "My API Key"

### Credential Security

**Security Checklist**:

1. ✅ **Use Settings → Credentials** (not .env files)
2. ✅ **Test before using** (verify they work)
3. ✅ **Set expiration** (for API keys)
4. ✅ **Rotate regularly** (90 days recommended)
5. ✅ **Delete unused** (reduce attack surface)
6. ✅ **Monitor audit logs** (catch unauthorized access)
7. ✅ **Backup encryption key** (`.credential_key` file)

### Testing Credentials

**Always test**:
- ✅ After creation
- ✅ After editing
- ✅ Before production use
- ✅ After API key rotation
- ✅ If tool assignment fails

💡 **Tip**: Test connection button is your friend!

---

## Troubleshooting

### Credential Test Failed

**Symptom**: "Connection test failed" with error

**Common Errors & Solutions**:

**"Invalid API key"**:
- Copy error (re-copy key)
- Expired key (regenerate)
- Wrong key type (check docs)

**"Authentication failed"**:
- Wrong username/password
- Account locked/expired
- 2FA required (not supported)

**"Connection timeout"**:
- Network issue
- Firewall blocking
- Wrong host/port

**"Permission denied"**:
- Insufficient scopes
- Wrong access level
- Need admin approval

**"Rate limit exceeded"**:
- Too many test attempts
- Wait a few minutes
- Check provider limits

### Credential Not Appearing in Dropdown

**Symptom**: Created credential but can't select it

**Solutions**:

1. **Check credential type**:
   - Must match tool type
   - GitHub tool needs GitHub credential
   - Can't use Slack credential for GitHub

2. **Check status**:
   - Must be active
   - Verify not deleted

3. **Refresh page**:
   - Browser cache issue
   - Hard refresh (Ctrl/Cmd + Shift + R)

### Can't Delete Credential

**Symptom**: "Cannot delete - credential in use"

**Solutions**:

1. **Find assignments**:
   - Credential details show agents using it
   - Go to each agent
   - Remove or replace credential

2. **After removal**:
   - Verify 0 assignments
   - Delete credential

⚠️ **Safety**: System prevents deleting credentials that would break agent tools.

### Audit Logs Not Showing

**Symptom**: Audit tab is empty

**Solutions**:

1. **Check time range**:
   - May be filtering to period with no activity
   - Try "Last 90 days"

2. **Check filters**:
   - All filters set to "All"?
   - Clear filters

3. **Verify logging enabled**:
   - System Settings → Logging
   - Audit logging enabled?

---

## Related Guides

- **[Tools Guide](../TOOLS.md)**: Use credentials with tools
- **[Agents Guide](../AGENTS.md)**: Tools require credentials
- **[Dashboard Guide](../DASHBOARD.md)**: System health overview

---

## Keyboard Shortcuts

- **Ctrl/Cmd + K**: Search credentials
- **Ctrl/Cmd + N**: New credential
- **Ctrl/Cmd + T**: Test selected credential
- **Tab**: Navigate between tabs
- **Esc**: Close modals

---

## FAQ

### Where are credentials stored?

**Database (encrypted)**:
- PostgreSQL `credentials` table
- `encrypted_data` column (Fernet encryption)
- Encryption key in `.credential_key` file
- ⚠️ **BACKUP `.credential_key`** - losing it = losing all credentials

### Can I import credentials from .env?

**Yes!** Migration script available:

```bash
cd orchestrator
python scripts/seed_credentials_from_env.py --dry-run
python scripts/seed_credentials_from_env.py
```

**[See Credential System Guide →](../CREDENTIAL_SYSTEM_GUIDE.md#migration-guide)**

### How do I backup credentials?

**Backup encryption key**:

```bash
cp orchestrator/.credential_key ~/secure_backup/
chmod 600 ~/secure_backup/.credential_key
```

**Store in**:
- Password manager
- Encrypted backup system
- Separate secure server
- ❌ NOT in git repository

### Can multiple agents use same credential?

**Yes!** Common pattern:

- Single "Production OpenAI" credential
- Used by 10+ agents
- All share rate limits
- All usage tracked per agent

**OR** separate credentials:

- "CodeReviewer OpenAI"
- "SecurityAuditor OpenAI"
- Separate billing
- Separate rate limits

### What happens if credential expires?

**Auto-detection** (some providers):
- System tests credentials periodically
- Failed test → status changes to "Failed"
- Notification sent
- Agents using it will fail with clear error

**Manual monitoring**:
- Check audit logs for failures
- Regular testing recommended
- Set expiration dates proactively

---

**Next**: [Analytics Guide →](../ANALYTICS.md)

*Monitor and optimize platform performance*


---

## API Reference


## Tenants
Create, rename, delete tenants to isolate data & configs.

**API**  
> **Authentication**  
> All API calls require headers:  
> ```http
> X-API-Key: <your_key>
> Authorization: Bearer <your_token>
> ```

- `GET /api/settings/tenants`
- `POST /api/settings/tenants`
- `PUT /api/settings/tenants/{id}`
- `DELETE /api/settings/tenants/{id}`

## Providers
Store provider keys; set default models.

**API**  
- `GET /api/settings/providers`
- `PUT /api/settings/providers`

## Feature Flags
Toggle modules (Playbooks, Code Graph, A/B).

**API**  
- `GET /api/settings/flags`
- `PUT /api/settings/flags/{key}` (body: `{"value":true}`)

## CORS
Manage allowed origins.

**API**  
- `GET /api/settings/cors`
- `PUT /api/settings/cors` (body: `{"origins":["http://localhost:3000"]}`)

## Audit
Export audit logs.

**API**  
- `GET /api/settings/audit/info`
- `POST /api/settings/audit/export` → `{"url":"https://.../audit-2025-08-10.ndjson"}`


