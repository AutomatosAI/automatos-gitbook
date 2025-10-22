---
title: AI Assistant
description: Use the AI assistant for quick help, code queries, and document search
---

# 💬 AI Assistant Guide

*Your intelligent assistant for platform help and knowledge queries*

---

## 📖 Table of Contents

1. [Overview](#overview)
2. [Quick Start](#quick-start)
3. [Chat Interface](#chat-interface)
4. [Message Types](#message-types)
5. [Code Snippets](#code-snippets)
6. [Document References](#document-references)
7. [Common Tasks](#common-tasks)
8. [Tips & Best Practices](#tips--best-practices)
9. [Troubleshooting](#troubleshooting)

---

## Overview

### What is the AI Assistant?

The AI Assistant is your built-in chatbot that can answer questions about:
- **Platform features**: How to use Automatos AI
- **Your documents**: Search and query your knowledge base
- **Your code**: Ask about code in indexed repositories
- **Troubleshooting**: Get help with errors and issues

**Access**: Click **Assistant** in sidebar, or click chat icon (💬) anywhere

![AI Assistant Overview](images/chatbot_overview.png)

### What Can You Ask?

**Platform Help**:
- "How do I create an agent?"
- "What's the difference between workflows and agents?"
- "How do I upload documents?"

**Document Queries**:
- "What does our security policy say about passwords?"
- "Summarize the Q4 report"
- "Find deployment procedures"

**Code Queries** (if CodeGraph enabled):
- "How is authentication implemented?"
- "Where is the payment processing code?"
- "Show me examples of error handling"

**Troubleshooting**:
- "Why did my workflow fail?"
- "Agent not executing tasks - help!"
- "Document upload stuck - what to do?"

---

## Quick Start

### Ask Your First Question (1 Minute)

**Goal**: Get help from AI Assistant

**Steps**:

1. Click **Assistant** in sidebar
2. Type question: "How do I create an agent?"
3. Press Enter
4. Get instant response with links
5. Follow links for detailed guides

⏱️ **Time**: 30 seconds  
🎯 **Result**: Answer with documentation links

---

## Chat Interface

### Layout

The chat interface has **3 main sections**:

![Chat Interface Layout](images/chatbot_interface_layout.png)

#### 1. Welcome Message (on first load)

💡 *Tooltip: "Introduces the assistant and suggests starter questions"*

**Displays**:
- Welcome text
- Suggested questions (click to ask)
- Feature highlights
- Quick tips

**Suggested Questions**:
- "How do I create my first agent?"
- "What are workflows?"
- "How do I upload documents?"
- "Show me example workflows"

![Welcome Message](images/chatbot_welcome.png)

#### 2. Message History

💡 *Tooltip: "Conversation history. Scroll to see previous messages."*

**Shows**:
- All messages in conversation
- Your messages (right side, blue)
- Assistant messages (left side, gray)
- Timestamps
- Code snippets (formatted)
- Document references (with links)

**Message Features**:
- Auto-scroll to latest
- Copy message text
- Regenerate response (if unsatisfied)
- Share conversation

![Message History](images/chatbot_messages.png)

#### 3. Input Area

**Text Input**  
💡 *Tooltip: "Type your question or message. Press Enter to send, Shift+Enter for new line."*

- Multi-line support
- Auto-resize as you type
- Character count (if long)

**Send Button**  
💡 *Tooltip: "Send message to assistant. Also: press Enter"*

- Disabled while assistant is typing
- Shows spinner during response
- Keyboard shortcut: Enter

**Attach Button** (optional)  
💡 *Tooltip: "Attach code snippet or document reference for context"*

- Paste code
- Link to document
- Add screenshot (future)

![Input Area](images/chatbot_input.png)

---

## Message Types

### User Messages

**Your messages appear**:
- Right-aligned
- Blue background
- Your avatar/initials
- Timestamp

**Message Actions** (hover):
- Copy text
- Edit message (resend)
- Delete message

![User Message](images/chatbot_message_user.png)

### Assistant Messages

**Assistant messages appear**:
- Left-aligned
- Gray background
- AI icon
- Timestamp

**Rich Content Support**:

#### Plain Text

Standard text responses with:
- Markdown formatting
- **Bold**, *italic*, `code`
- Lists and bullets
- Paragraphs

![Assistant Text Message](images/chatbot_message_text.png)

#### Code Blocks

Formatted code with syntax highlighting:

```python
# Example code snippet
def create_agent(name, agent_type):
    agent = Agent(name=name, type=agent_type)
    return agent
```

**Code Block Features**:
- Syntax highlighting (via Prism.js)
- Language badge (Python, JavaScript, etc.)
- Copy button (one-click copy)
- Line numbers (optional)

![Code Block](images/chatbot_message_code.png)

#### Links

Clickable links to:
- Documentation pages
- Agent details
- Workflow results
- Document previews

**Link Preview** (hover):
- Shows link destination
- Preview tooltip
- Safe link indicator

---

## Code Snippets

### Code References Panel

When assistant includes code, a side panel may appear:

💡 *Tooltip: "Extracted code snippets for easy reference and copying"*

![Code Snippets Panel](images/chatbot_code_snippets_panel.png)

**Features**:

**Code Snippet Cards**:
- **Title**: Description of what code does
- **Language**: Programming language
- **Source**: Where code is from (if from CodeGraph)
- **Code**: Formatted, highlighted code
- **Copy Button**: Copy to clipboard

**Example Snippet Card**:

```
Title: Create Agent Function
Language: Python
Source: agents/agent_factory.py:145

def create_specialized_agent(
    name: str,
    agent_type: str,
    model_config: dict
) -> Agent:
    """Create agent with configuration"""
    ...
```

**Actions**:
- **📋 Copy**: Copy code to clipboard
- **📄 View Full File**: Open source file (if CodeGraph)
- **🤖 Explain**: Ask assistant to explain this code
- **✏️ Modify**: Get help modifying code

### Code Execution (Future Feature)

🔧 **Advanced** (coming soon)

- Run code snippets in sandbox
- See execution results
- Test before using
- Save to library

---

## Document References

### Document Panel

When assistant references documents, a panel shows sources:

💡 *Tooltip: "Documents referenced in response. Click to view full document."*

![Document References](images/chatbot_document_references.png)

**Reference Cards**:

Each document shows:
- **📄 Document Name**
- **Page/Section**: Where content is from
- **Relevance**: Similarity score
- **Preview**: Relevant excerpt

**Example Reference**:

```
📄 Security Best Practices.pdf
Page: 15
Relevance: 94%
Preview: "SQL injection prevention requires parameterized 
queries in all database interactions..."
```

**Actions**:
- **👁️ View**: Open document viewer
- **📋 Copy**: Copy excerpt
- **🔍 Search More**: Find related content in document
- **⬇️ Download**: Download full document

### Context Sources

Shows where assistant got information:

**Source Types**:
- **📚 Knowledge Base**: Your uploaded documents
- **💻 CodeGraph**: Your indexed code
- **📖 Platform Docs**: Built-in documentation
- **🧠 Agent Memory**: Learned from past interactions

**Transparency**:
- All sources cited
- Click to verify
- See similarity scores
- Trust and verify responses

---

## Common Tasks

### Task 1: Getting Platform Help

**Scenario**: You don't know how to do something

**Steps**:

1. Open AI Assistant
2. Ask naturally: "How do I configure credentials for Slack?"
3. Get response with:
   - Step-by-step instructions
   - Links to Settings page
   - Relevant documentation links
4. Follow instructions
5. Ask follow-up if needed: "What permissions do I need?"

⏱️ **Time**: 1-2 minutes  
🎯 **Result**: Clear guidance

### Task 2: Searching Your Documents

**Scenario**: Find information in your knowledge base

**Steps**:

1. Open AI Assistant
2. Ask: "What does our API documentation say about rate limiting?"
3. Assistant searches your documents
4. Returns answer with document references
5. Click reference to open full document
6. Get exact information needed

⏱️ **Time**: 30 seconds  
🎯 **Result**: Found information with source

### Task 3: Understanding Your Code

**Scenario**: Need to understand code in your repository

**Prerequisites**: CodeGraph project indexed

**Steps**:

1. Open AI Assistant
2. Ask: "How does user authentication work in our app?"
3. Assistant searches CodeGraph
4. Returns explanation with code references
5. Click code reference to see full file
6. Ask follow-up: "Show me the password hashing function"

⏱️ **Time**: 1-2 minutes  
🎯 **Result**: Code understanding with examples

### Task 4: Troubleshooting Errors

**Scenario**: Workflow failed with error

**Steps**:

1. Copy error message from workflow
2. Open AI Assistant
3. Paste error: "Error: Agent timeout after 5 minutes"
4. Get explanation and solutions:
   - What this error means
   - Common causes
   - How to fix
5. Apply suggested solution
6. Ask if unclear: "How do I increase the timeout?"

⏱️ **Time**: 2-3 minutes  
🎯 **Result**: Error resolved

---

## Advanced Features

### Conversation Context

🔧 **Advanced**

The assistant maintains conversation context:

**Context Awareness**:
- Remembers previous questions in session
- Understands follow-up questions
- References earlier code snippets
- Builds on previous answers

**Example**:

```
You: "How do I create an agent?"
Assistant: [Explains agent creation...]

You: "What about adding skills to it?"
Assistant: "To add skills to the agent we just discussed, 
you can..." [Continues context]
```

**Managing Context**:
- **Clear Context**: Start fresh conversation
- **Export Conversation**: Save chat history
- **Bookmark Response**: Save specific answer

### Multi-Turn Conversations

**Complex questions** broken into turns:

```
You: "I need to set up automated code reviews"
Assistant: "I'll help you set up code reviews. What programming 
language is your code?"

You: "Python"
Assistant: "Great! For Python code reviews, I recommend:
1. Create a Code Architect agent with Python skills
2. Add GitHub tool for PR access
3. Create workflow with security checks
Would you like me to walk through each step?"

You: "Yes, start with creating the agent"
Assistant: [Detailed agent creation steps...]
```

**Benefits**:
- Break complex tasks into steps
- Interactive guidance
- Contextual follow-ups

### Session Management

**Sessions persist**:
- Conversation saved across page navigation
- Return to continue conversation
- Sessions expire after 24 hours inactivity

**Starting New Session**:
- Click "New Conversation" button
- Clears current context
- Fresh start

---

## Tips & Best Practices

### Asking Good Questions

💡 **Best Practices**:

**Good questions**:
- ✅ "How do I add Slack integration to an agent?"
- ✅ "What's causing error: 'Agent timeout exceeded'?"
- ✅ "Show me the authentication code in auth_service.py"

**Poor questions**:
- ❌ "help"
- ❌ "not working"
- ❌ "code"

**Question Tips**:
1. Be specific about what you need
2. Include error messages (copy-paste)
3. Mention what you've already tried
4. Provide context (which page, which agent, etc.)

### Using Code Queries

**For CodeGraph queries**:
1. Mention file names when known
2. Use technical terms from your codebase
3. Ask about specific functions/classes
4. Follow up for details

**Example Flow**:

```
You: "Where is the payment processing code?"
Assistant: [Shows PaymentService in services/payment.py]

You: "How does validate_payment work?"
Assistant: [Shows function code and explanation]

You: "Are there any security issues in that function?"
Assistant: [Analyzes for vulnerabilities]
```

### Getting Document Information

**For document queries**:
1. Mention document name if known
2. Ask specific questions
3. Request summaries for long docs
4. Ask for specific sections

**Example**:

```
You: "Summarize the Q4 financial report"
Assistant: [Provides summary with key metrics]

You: "What was the revenue growth?"
Assistant: "According to the Q4 report (page 3), 
revenue grew 23% year-over-year..."
```

---

## Troubleshooting

### Assistant Not Responding

**Symptom**: Message sent but no response

**Solutions**:

1. **Check connection**:
   - Look for connection status indicator
   - Green = connected, Red = disconnected
   - Refresh page if disconnected

2. **Wait longer**:
   - Complex queries take 5-10 seconds
   - Document searches take 3-5 seconds
   - Code queries take 2-4 seconds

3. **Check message length**:
   - Very long messages may timeout
   - Break into smaller questions

4. **Retry**:
   - Click retry button (if appears)
   - Or rephrase and send again

### Incorrect or Unhelpful Responses

**Symptom**: Assistant gives wrong answer

**Solutions**:

1. **Provide more context**:
   - Add details about what you're trying to do
   - Mention specific page or feature
   - Include error messages

2. **Rephrase question**:
   - Try different wording
   - Break into multiple questions
   - Be more specific

3. **Verify sources**:
   - Check document references
   - Verify code snippets
   - Cross-check with documentation

4. **Give feedback**:
   - Thumbs up/down on responses
   - Helps improve assistant

### No Code References

**Symptom**: Asked about code but no code shown

**Solutions**:

1. **Check CodeGraph**:
   - Is your code indexed?
   - Go to Knowledge → CodeGraph
   - Verify project exists

2. **Be specific**:
   - Mention file names
   - Include function/class names
   - Ask about specific files

3. **Check project selection**:
   - Some setups have multiple projects
   - Specify which project
   - "In the backend project, where is..."

### No Document References

**Symptom**: Asked about documents but assistant doesn't find them

**Solutions**:

1. **Check documents processed**:
   - Knowledge → Library
   - Verify status is "Processed" (green)

2. **Try keyword search**:
   - Use exact terms from document
   - Include document name if known

3. **Upload document**:
   - May not be in knowledge base
   - Upload and wait for processing
   - Try query again

---

## Related Guides

- **[Knowledge Base Guide](../KNOWLEDGE.md)**: Upload documents for chatbot queries
- **[CodeGraph](../KNOWLEDGE.md#codegraph-tab)**: Index code for code queries
- **[Agents Guide](../AGENTS.md)**: Learn about agents (chatbot can explain)

---

## Keyboard Shortcuts

- **Ctrl/Cmd + K**: Focus chat input
- **Enter**: Send message
- **Shift + Enter**: New line in message
- **Esc**: Close chat (if modal)
- **↑ Arrow**: Edit last message
- **Ctrl/Cmd + L**: Clear conversation

---

## FAQ

### Is the chatbot connected to my knowledge base?

**Yes!** The assistant can search:
- Your uploaded documents
- Your indexed code (CodeGraph)
- Platform documentation
- Agent memories

**How it works**:
1. You ask a question
2. Assistant searches knowledge base
3. Retrieves relevant content
4. Generates answer with citations

### What language models power the assistant?

**Default**: GPT-4 Turbo for best quality

**Can be configured** in Settings → System Settings → Chatbot Configuration

**Options**:
- GPT-4 Turbo: Best quality, moderate speed
- GPT-4: High quality, slower
- GPT-3.5 Turbo: Fast, lower cost

### Does it remember conversations?

**Within session**: Yes
- Conversation context maintained
- Follow-up questions work
- References previous messages

**Across sessions**: No (currently)
- Future feature: conversation history
- Workaround: Export important conversations

### Can I disable the assistant?

**Yes**, in Settings → System Settings → Features:
- Disable chatbot toggle
- Removes from navigation
- Clears chat data (optional)

### How accurate are the responses?

**Generally high accuracy** when:
- ✅ Asking about platform features (>95%)
- ✅ Querying your documents (>90%)
- ✅ CodeGraph queries (>85%)

**Less accurate** when:
- ⚠️ Complex multi-step questions
- ⚠️ Very recent features
- ⚠️ Ambiguous questions

**Always**:
- Check sources
- Verify code snippets
- Test suggestions before applying

---

**Next**: [Tools Guide →](../TOOLS.md)

*Learn to integrate 400+ tools with your agents*

