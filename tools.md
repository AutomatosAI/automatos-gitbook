---
title: Tools
description: Browse, configure, and assign MCP tools to agents
---

# 🔧 Tools Management Guide

*Connect agents to 400+ integrations via MCP protocol*

---

## 📖 Table of Contents

1. [Overview](#overview)
2. [Quick Start](#quick-start)
3. [Tools Dashboard](#tools-dashboard)
4. [Tool Categories](#tool-categories)
5. [Tool Modals](#tool-modals)
6. [Common Tasks](#common-tasks)
7. [Tips & Best Practices](#tips--best-practices)
8. [Troubleshooting](#troubleshooting)

---

## Overview

### What are MCP Tools?

MCP (Model Context Protocol) Tools are external integrations that agents can use during task execution - like GitHub, Slack, databases, cloud services, and 400+ other integrations.

**Access**: Navigate to **Tools** from the sidebar

![Tools Overview](images/tools_overview_page.png)

### What Can You Do Here?

- ✅ **Browse 400+ tools** organized by category
- ✅ **Assign tools to agents** with custom permissions
- ✅ **Configure tool settings** and credentials
- ✅ **Test connections** before use
- ✅ **Monitor tool usage** and performance
- ✅ **Create custom tools** (advanced)

### Key Concepts

**Tool**: External service integration (e.g., GitHub MCP)

**Credential**: Authentication info for tool (API key, OAuth token)

**Assignment**: Linking tool to agent with permissions

**Permission**: What agent can do (read/write/execute)

---

## Quick Start

### Assign Your First Tool (3 Minutes)

**Goal**: Give an agent GitHub access

**Steps**:

1. Go to Tools page
2. Find "GitHub" tool (search or browse Developer Tools)
3. Click **"Assign to Agent"**
4. Select your agent
5. Choose credential (or create new)
6. Set permissions: ✅ Read ✅ Write
7. Click **"Assign Tool"**

⏱️ **Time**: 3 minutes  
🎯 **Result**: Agent can use GitHub

**[See detailed walkthrough →](#common-tasks)**

---

## Tools Dashboard

### Statistics Cards

**🔧 Available Tools**  
💡 *Tooltip: "Total tools in registry. 400+ integrations available."*

- Count of all available tools
- New tools this month
- Example: "417 tools"

**✅ Active Assignments**  
💡 *Tooltip: "Tool-agent connections currently active. Shows integration usage."*

- Count of active assignments
- Total possible assignments
- Example: "23 active"

**📂 Tool Categories**  
💡 *Tooltip: "Tools organized by type (Developer, Cloud, Communication, etc.)"*

- Number of categories
- Tools per category
- Example: "12 categories"

**📊 Usage This Week**  
💡 *Tooltip: "Tool calls made by agents this week"*

- Total tool calls
- Trend vs last week
- Example: "1,247 calls"

![Tools Stats](images/tools_stats_cards.png)

### Search and Filter

**Search Bar**  
💡 *Tooltip: "Search tools by name, description, or provider"*

- Find tools quickly
- Search by name: "Slack"
- Search by capability: "notifications"
- Real-time results

**Category Filter**  
💡 *Tooltip: "Filter by tool category"*

- All Categories
- Developer Tools
- Communication
- Cloud Services
- Databases
- AI Services
- Monitoring
- etc.

**Status Filter**:
- All Tools
- Active (assigned to agents)
- Available (not yet assigned)
- Inactive (disabled)

![Tools Filters](images/tools_filters.png)

---

## Tool Categories

### Developer Tools 💻

**GitHub**  
💡 *Tooltip: "Interact with GitHub repos, PRs, issues, commits"*

- Read repos, create PRs, comment on issues
- Requires: GitHub Personal Access Token
- Use cases: Code review, PR automation

**GitLab**  
- Similar to GitHub for GitLab
- Merge requests, pipelines, issues

**Bitbucket**  
- Bitbucket Cloud/Server support
- Repository management

**Jira**  
- Create/update issues
- Project management
- Sprint tracking

![Developer Tools](images/tools_category_developer.png)

### Communication Tools 💬

**Slack**  
💡 *Tooltip: "Send messages, create channels, manage users"*

- Send notifications
- Post workflow results
- Channel management
- Requires: Slack Bot Token

**Discord**  
- Discord webhooks
- Channel messages
- Server management

**Email (SendGrid, SMTP)**  
- Send automated emails
- Email templates
- Delivery tracking

**Microsoft Teams**  
- Teams messages
- Channel posts
- Adaptive cards

![Communication Tools](images/tools_category_communication.png)

### Cloud Services ☁️

**AWS**  
💡 *Tooltip: "Interact with AWS services (S3, Lambda, EC2, etc.)"*

- S3: File storage
- Lambda: Function execution
- EC2: Instance management
- Requires: AWS Access Key + Secret

**Google Cloud**  
- GCS: Storage
- Compute Engine
- Cloud Functions

**Microsoft Azure**  
- Blob Storage
- Virtual Machines
- Functions

**DigitalOcean**  
- Droplets
- Spaces
- Kubernetes

![Cloud Tools](images/tools_category_cloud.png)

### Database Tools 🗄️

**PostgreSQL**  
💡 *Tooltip: "Execute queries, manage tables, run migrations"*

- Query execution
- Schema management
- Data export
- Requires: Database credentials

**MySQL / MariaDB**  
- Similar to PostgreSQL

**MongoDB**  
- NoSQL database operations
- Document queries
- Aggregation pipelines

**Redis**  
- Cache operations
- Key-value storage
- Pub/sub

**Elasticsearch**  
- Full-text search
- Index management
- Query DSL

![Database Tools](images/tools_category_database.png)

### AI Services 🤖

**OpenAI**  
💡 *Tooltip: "Additional OpenAI capabilities beyond agent models"*

- Image generation (DALL-E)
- Embeddings
- Fine-tuning management

**Anthropic**  
- Claude API access
- Vision capabilities

**HuggingFace**  
- Model inference
- Dataset access
- Model management

![AI Tools](images/tools_category_ai.png)

### Utilities 🛠️

**File Operations**  
💡 *Tooltip: "Read, write, list files. Essential for most agents."*

- Read files
- Write files
- List directories
- File permissions
- Built-in, always available

**Shell Commands**  
💡 *Tooltip: "Execute shell commands. ⚠️ Security risk - restrict carefully."*

- Run bash/shell commands
- Environment variables
- Command output capture
- ⚠️ Requires explicit enablement

**HTTP Client**  
- Make HTTP requests
- REST API calls
- Webhook triggers

**Date/Time**  
- Current time
- Date formatting
- Timezone conversions

---

## Tool Modals

### Create Tool Modal

**How to open**: Click "Create Custom Tool" button

💡 *Tooltip: "Define custom tool integration for services not in the registry"*

![Create Tool Modal](images/tools_modal_create.png)

**Fields**:

**Tool Name** (required)  
💡 *Tooltip: "Unique identifier for this tool"*

**Provider** (required)  
💡 *Tooltip: "Company or service providing this integration"*

**Description**  
💡 *Tooltip: "Explain what this tool does and when agents should use it"*

**MCP Server URL**  
💡 *Tooltip: "WebSocket URL for MCP server. Format: ws://host:port or wss://host:port"*

**Capabilities** (JSON)  
💡 *Tooltip: "Define what methods this tool exposes"*

Example:
```json
{
  "methods": [
    {
      "name": "sendNotification",
      "description": "Send notification to users",
      "parameters": {
        "message": "string",
        "channel": "string"
      }
    }
  ]
}
```

**Credentials Schema** (JSON)  
💡 *Tooltip: "Define what credentials this tool needs"*

Example:
```json
{
  "fields": [
    {
      "name": "api_key",
      "type": "string",
      "required": true,
      "secure": true
    },
    {
      "name": "base_url",
      "type": "string",
      "default": "https://api.example.com"
    }
  ]
}
```

**Category**:
- Select category or create custom

**Icon** (emoji):
- Choose emoji for visual identification

**Tags**:
- Add tags for organization

---

### Tool Details Modal

**How to open**: Click tool card or "View Details" button

💡 *Tooltip: "Complete tool information and usage statistics"*

![Tool Details Modal](images/tools_modal_details.png)

**Displays**:

**Tool Information**:
- Name, provider, version
- Description and capabilities
- Category and tags
- Status (active/inactive)

**Credentials Required**:
- Lists required credentials
- Shows credential type
- Link to create credential

**Methods Available**:
- All callable methods
- Method parameters
- Return types
- Usage examples

**Usage Statistics**:
- Total calls: All-time
- Calls this week
- Success rate
- Average latency
- Errors encountered

**Assigned To**:
- Which agents have this tool
- Permission levels
- Last used timestamp

**Actions**:
- Configure tool
- Test connection
- View usage logs
- Assign to agent
- Disable/Enable

---

### Tool Configuration Modal

**How to open**: Click "⚙️ Configure" on tool card

💡 *Tooltip: "Modify tool settings and test configuration"*

![Tool Config Modal](images/tools_modal_config.png)

**Configuration Fields**:

**Tool Settings**:
- Tool name
- Provider
- Version
- Status (active/inactive)

**Connection Settings**:
- MCP server URL
- Timeout settings
- Retry configuration
- Rate limits

**Default Credentials**  
💡 *Tooltip: "Default credential used when assigning to new agents. Can be overridden per agent."*

- Select from available credentials
- Or leave blank for per-agent selection

**Performance Settings**:
- Cache results: Enable/disable
- Cache TTL: Duration
- Max concurrent calls
- Circuit breaker threshold

**Test Connection**:
- Click "Test Connection" button
- Verifies MCP server accessible
- Tests with default credential
- Shows test results

---

### Agent Tool Assignment Modal

**How to open**: Click "Assign to Agent" on tool card

💡 *Tooltip: "Connect tool to agent with specific permissions and configuration"*

![Assign Tool Modal](images/tools_modal_assign.png)

**Assignment Fields**:

**Select Agent** (required)  
💡 *Tooltip: "Which agent gets access to this tool"*

- Dropdown of all agents
- Shows agent type and status
- Filter by agent type

**Select Credential** (required for most tools)  
💡 *Tooltip: "Which credential to use for authentication. Must be configured in Settings."*

- Dropdown of available credentials
- Shows credential environment (prod/dev)
- Create new credential link
- ⚠️ Must exist first

**Permissions** (checkboxes)  
💡 *Tooltip: "Control what operations agent can perform with this tool"*

- ✅ **Read**: Query data, retrieve information
- ✅ **Write**: Create, update, delete data
- ✅ **Execute**: Run commands, trigger actions

**Example Permissions**:
- GitHub: ✅ Read (view repos) ✅ Write (create PRs) ❌ Execute (no admin)
- Database: ✅ Read (SELECT) ✅ Write (INSERT/UPDATE) ❌ Execute (no DROP)
- Slack: ✅ Read (read messages) ✅ Write (send messages) ❌ Execute (no admin)

**Enable Tool**  
💡 *Tooltip: "Tool assignment can be active or inactive without deleting"*

- ✅ Enabled: Agent can use immediately
- ❌ Disabled: Assignment exists but inactive

**Configuration** (JSON, optional)  
💡 *Tooltip: "Tool-specific settings for this agent. Overrides defaults."*

Example for GitHub:
```json
{
  "default_repo": "myorg/myapp",
  "auto_assign_prs": true,
  "pr_template": "default"
}
```

**Test Assignment**:
- Test before saving
- Verifies credential works
- Tests permissions
- Shows test result

---

## Common Tasks

### Task 1: Assigning GitHub to Agent

**Scenario**: Agent needs to read repos and create PRs

**Prerequisites**:
- GitHub Personal Access Token (PAT)
- PAT with `repo` scope

**Steps**:

1. **First: Create credential** (if not exists)
   - Go to Settings → Credentials
   - Create "GitHub" credential
   - Paste PAT
   - Test connection

2. **Assign to agent**:
   - Tools page → Find "GitHub"
   - Click "Assign to Agent"
   - Select agent: "CodeReviewer Pro"
   - Select credential: "GitHub Production"
   - Permissions: ✅ Read ✅ Write ❌ Execute
   - Click "Assign"

3. **Verify**:
   - Assignment appears in agent's tools list
   - Test with simple task: "List repositories"

⏱️ **Time**: 5 minutes  
🎯 **Result**: Agent can use GitHub

### Task 2: Testing Tool Connection

**Scenario**: Verify Slack tool works before assigning

**Steps**:

1. Tools page → Find "Slack"
2. Click tool card → "View Details"
3. Click **"Test Connection"** button
4. Select credential to test
5. Test executes:
   - Connects to Slack API
   - Sends test message (if configured)
   - Returns result
6. ✅ Success: Tool ready to assign
7. ❌ Failure: Fix credential or configuration

⏱️ **Time**: 1 minute  
🎯 **Result**: Verified working tool

### Task 3: Viewing Tool Usage

**Scenario**: See which agents use which tools

**Steps**:

1. Tools page → Select a tool
2. Click "View Details"
3. **Usage Statistics** section shows:
   - Total calls made
   - Calls by agent
   - Success rate
   - Most used methods
4. Identify heavy users
5. Optimize if needed

⏱️ **Time**: 2 minutes  
🎯 **Result**: Tool usage understanding

### Task 4: Removing Tool from Agent

**Scenario**: Agent no longer needs a tool

**Steps**:

1. Agents page → Select agent
2. Configuration tab → Edit Configuration
3. Tools section
4. Find tool to remove
5. Click **"✕ Remove"**
6. Confirm removal
7. Tool unassigned

⏱️ **Time**: 1 minute  
🎯 **Result**: Tool removed safely

---

## Advanced Features

### Custom MCP Tools

🔧 **Advanced**

Create custom tools for internal services.

**Requirements**:
- MCP server implementation
- Server accessible to Automatos
- Credential schema defined
- Method capabilities documented

**[See Developer Guide for MCP server development →](../TOOLS_INTEGRATION_GUIDE.md)**

### Tool Rate Limiting

Configure rate limits to prevent API exhaustion:

**Per-Tool Limits**:
- Calls per minute
- Calls per hour
- Calls per day
- Concurrent call limit

**Per-Agent Limits**:
- Override tool defaults
- Agent-specific rate limits

### Tool Monitoring

**Real-Time Monitoring**:
- Active tool calls
- Response times
- Error rates
- Queue depth

**Alerts**:
- Tool failures
- Rate limit approaches
- Slow responses
- Connection errors

---

## Tips & Best Practices

### Tool Selection

💡 **Best Practices**:

1. **Assign only needed tools**: Don't give agents unnecessary access
2. **Use least privilege**: Minimal permissions required
3. **Test before production**: Always test tool assignments
4. **Monitor usage**: Remove unused tools
5. **Rotate credentials**: Regular credential updates

### Credential Management

**Security**:
- Store credentials in Settings → Credentials (encrypted)
- Never hardcode credentials
- Use different credentials for dev/prod
- Test credentials before tool assignment
- Rotate periodically

**[See Settings Guide →](../SETTINGS.md#credentials-tab)**

### Permission Levels

**Guidelines**:

| Tool Type | Read | Write | Execute |
|-----------|------|-------|---------|
| **GitHub** | ✅ Always | ✅ For automation | ❌ Admin not needed |
| **Database** | ✅ Always | ⚠️ Careful | ❌ Never (DDL) |
| **Slack** | ✅ If needed | ✅ For notifications | ❌ Admin not needed |
| **Cloud** | ✅ Always | ⚠️ Cost risk | ❌ Dangerous |

💡 **Tip**: Start with Read only, add Write when needed, avoid Execute.

---

## Troubleshooting

### Tool Assignment Failed

**Symptom**: "Failed to assign tool to agent"

**Solutions**:

1. **Check credential exists**:
   - Settings → Credentials
   - Credential must exist first
   - Create if missing

2. **Verify credential works**:
   - Test credential connection
   - Update if expired

3. **Check agent status**:
   - Agent must be active
   - Inactive agents can't receive tools

### Tool Connection Failed

**Symptom**: "Connection test failed"

**Solutions**:

1. **Check credential**:
   - Verify API key is correct
   - Check for typos
   - Regenerate if needed

2. **Check MCP server**:
   - Server must be running
   - URL must be accessible
   - Check firewall rules

3. **Check permissions**:
   - Credential may lack required scopes
   - GitHub: needs `repo` scope
   - Slack: needs `chat:write` scope

### Tool Not Working in Workflow

**Symptom**: Agent has tool but can't use it

**Solutions**:

1. **Check permissions**:
   - Agent may need Write permission
   - Review assignment permissions

2. **Check credential**:
   - May have expired
   - Test connection
   - Update if needed

3. **Check tool status**:
   - Tool must be active/enabled
   - Check in Tool Details

---

## Related Guides

- **[Agents Guide](../AGENTS.md)**: Assign tools to agents
- **[Settings Guide](../SETTINGS.md)**: Manage credentials
- **[Workflows Guide](../WORKFLOWS.md)**: Use tools in workflows

---

## FAQ

### How many tools can I assign to one agent?

**No hard limit**, but recommendations:
- **3-7 tools**: Optimal for focused agents
- **10+ tools**: Generalist agents
- **20+ tools**: Rarely needed, may confuse agent

💡 **Tip**: Assign tools based on actual need, not "just in case".

### Do tools cost extra?

**Tool usage** may incur costs:
- API calls to third-party services (their pricing)
- Token usage for tool responses
- Automatos doesn't charge extra for tools

**Examples**:
- GitHub API: Free (rate limited)
- AWS S3: AWS pricing
- OpenAI API: OpenAI pricing

### Can tools access my data?

**Yes, with credentials**:
- Tools use your provided credentials
- Access what credential allows
- Subject to permission restrictions
- All access logged in audit trail

**Security**:
- Credentials encrypted in database
- Access logged
- Permissions enforced
- Can revoke anytime

### What's MCP?

**MCP** = Model Context Protocol

Standard protocol for tool integrations:
- Defined by Anthropic/community
- Language-agnostic
- Supports streaming
- Bi-directional communication

**[Learn more →](../MCP_INTEGRATION.md)**

---

**Next**: [Playbooks Guide →](../PLAYBOOKS.md)

*Discover and reuse successful patterns*

