---
title: Knowledge
description: Complete guide to managing documents, semantic search, CodeGraph, and multimodal content
---

# 📚 Knowledge Base & Documents Guide

*Manage your organization's knowledge - documents, code, and multimodal content*

---

## 📖 Table of Contents

1. [Overview](#overview)
2. [Quick Start](#quick-start)
3. [Library Tab](#library-tab)
4. [Multimodal Tab](#multimodal-tab)
5. [Search Tab](#search-tab)
6. [Upload Tab](#upload-tab)
7. [Processing Tab](#processing-tab)
8. [Analytics Tab](#analytics-tab)
9. [CodeGraph Tab](#codegraph-tab)
10. [Common Tasks](#common-tasks)
11. [Advanced Features](#advanced-features)
12. [Troubleshooting](#troubleshooting)

---

## Overview

### What is the Knowledge Base?

The Knowledge Base is where you upload, organize, and search all your organization's knowledge - documents, code repositories, and data that your AI agents can reference.

**Access**: Navigate to **Documents** or **Knowledge** from the sidebar

![Knowledge Base Overview](images/knowledge_overview_page.png)

### What Can You Do Here?

- ✅ **Upload documents** (PDF, Word, Markdown, code files)
- ✅ **Semantic search** - find by meaning, not just keywords
- ✅ **Extract multimodal content** - tables, images, formulas
- ✅ **Index code repositories** with CodeGraph
- ✅ **Monitor processing** status and queue
- ✅ **Analyze usage** patterns and trends
- ✅ **Organize by categories** and tags

### Page Layout

The Knowledge Base has **7 main tabs**:

1. **📚 Library** - Browse and manage all documents
2. **🎨 Multimodal** - Tables, images, formulas extracted from docs
3. **🔍 Search** - Semantic search across all content
4. **📤 Upload** - Add new documents
5. **⚙️ Processing** - Queue status and processing details
6. **📊 Analytics** - Usage statistics and insights
7. **💻 CodeGraph** - Code repository understanding

---

## Quick Start

### Uploading Your First Document (2 Minutes)

**Goal**: Upload a PDF and search it

**Steps**:

1. Go to **Upload** tab
2. Drag and drop a PDF file
3. Wait for processing (30-60 seconds)
4. Go to **Search** tab
5. Type a question about the document
6. Get instant results!

⏱️ **Time**: 2 minutes  
🎯 **Result**: Searchable document in knowledge base

**[See detailed walkthrough →](#upload-tab)**

---

## Library Tab

### Overview

Browse and manage all documents in your knowledge base.

💡 *Tooltip: "Your document library. View, search, download, and delete documents."*

![Library Tab](images/knowledge_library_tab.png)

### Statistics Cards

**📁 Total Documents**  
💡 *Tooltip: "Total number of documents uploaded and processed"*

- Count of all documents
- Changes from last week
- Example: "47 documents"

**✅ Processed**  
💡 *Tooltip: "Documents fully processed and searchable"*

- Successfully processed count
- Processing success rate
- Example: "45 processed"

**⏳ Processing**  
💡 *Tooltip: "Documents currently being processed"*

- Active processing count
- Estimated completion time
- Example: "2 processing"

**⚠️ Failed**  
💡 *Tooltip: "Documents that failed processing. Click to see errors and retry."*

- Failed processing count
- Common error types
- Retry option

![Library Stats](images/knowledge_library_stats.png)

### Document List

Each document card shows:

**Document Info**:
- **📄 Filename**: Original file name with icon
- **File Type**: PDF, DOCX, MD, TXT, code extension
- **Size**: File size (MB/KB)
- **Status Badge**: 
  - 🟢 Processed (green)
  - 🟡 Processing (yellow)
  - 🔴 Failed (red)
- **Upload Date**: When added

**Document Stats**:
- **Pages/Lines**: Document length
- **Chunks**: Number of searchable chunks created
- **Embeddings**: Vector embeddings generated
- **Searches**: How many times searched

![Document Card](images/knowledge_library_document_card.png)

**Preview Section**:
- First 200 characters of content
- Expandable to see more
- Formatted preview

**Tags**:
- User-assigned tags
- Auto-generated category tags
- Click tag to filter

**Actions**:
- **👁️ View Details**: Opens [Document Details Modal](#document-details-modal)
- **⬇️ Download**: Download original file
- **🗑️ Delete**: Remove document (with confirmation)

### Search and Filter

**Search Bar**  
💡 *Tooltip: "Search documents by filename, content, or tags"*

- Search by filename
- Search by content snippet
- Search by tags
- Real-time filtering

**Category Filter**  
💡 *Tooltip: "Filter by document category (auto-detected or manually assigned)"*

- All Categories
- Technical Documentation
- Business Documents
- Code Files
- Research Papers
- User Guides
- Custom categories

**Status Filter**:
- All documents
- Processed only
- Processing only
- Failed only

**Sort Options**:
- Newest first
- Oldest first
- Most searched
- Largest first
- Alphabetical

![Library Filters](images/knowledge_library_filters.png)

### Bulk Actions

Select multiple documents (checkbox on cards):

**Bulk Operations**:
- **Add Tags**: Tag multiple documents at once
- **Download**: Download as ZIP
- **Delete**: Delete multiple documents
- **Re-process**: Retry failed processing
- **Export Metadata**: Export to CSV

---

## Multimodal Tab

### Overview

View and manage extracted multimodal content - tables, images, and formulas.

💡 *Tooltip: "Content extracted from documents beyond plain text. Makes tables, images, and math searchable."*

![Multimodal Tab](images/knowledge_multimodal_tab.png)

### Sub-Tabs

#### 1. Tables

**What it shows**:
- All tables extracted from documents
- Table structure and data
- Source document and page
- Searchable table content

**Table Cards**:

Each extracted table shows:
- **Source**: Document name and page number
- **Table Title**: Extracted or auto-generated
- **Dimensions**: Rows × Columns
- **Preview**: First few rows
- **Format**: CSV, Markdown, JSON

![Multimodal Tables](images/knowledge_multimodal_tables.png)

**Table Actions**:
- **👁️ View Full Table**: Expand to see all data
- **⬇️ Download**: Export as CSV/Excel
- **🔍 Search**: Search within table
- **📋 Copy**: Copy to clipboard
- **🤖 Query**: Ask AI about this table

**Table Search**  
💡 *Tooltip: "Search table content semantically. Example: 'revenue trends' finds relevant rows."*

- Semantic search within tables
- Filter by column values
- Sort by any column

#### 2. Images

**What it shows**:
- Images extracted from documents
- Image metadata and descriptions
- Source document and page
- AI-generated image descriptions

**Image Gallery**:

Each image shows:
- **Thumbnail**: Preview of image
- **Source**: Document and page
- **Caption**: Extracted or AI-generated
- **Size**: Dimensions and file size
- **Format**: PNG, JPEG, SVG

![Multimodal Images](images/knowledge_multimodal_images.png)

**Image Actions**:
- **🔍 View Full Size**: Open in lightbox
- **⬇️ Download**: Save original image
- **📝 Edit Description**: Modify AI description
- **🤖 Analyze**: Ask AI to describe/analyze image

**Image Search**:
- Search by caption/description
- Filter by document
- Filter by size/format

#### 3. Formulas

**What it shows**:
- Mathematical formulas extracted from documents
- LaTeX representations
- Rendered formula previews
- Context where formulas appear

**Formula Cards**:

Each formula shows:
- **Rendered Preview**: Beautiful math rendering
- **LaTeX Source**: Copy-paste ready LaTeX
- **Plain Text**: Text representation
- **Source**: Document and location
- **Context**: Surrounding explanation text

![Multimodal Formulas](images/knowledge_multimodal_formulas.png)

**Example Formula**:

```
Rendered: C = A(c₁, c₂, c₃, c₄, c₅, c₆)
LaTeX: C = A(c_1, c_2, c_3, c_4, c_5, c_6)
Context: "The context assembly function..."
```

**Formula Actions**:
- **📋 Copy LaTeX**: Copy to clipboard
- **🔍 View in Document**: Jump to source
- **🤖 Explain**: Ask AI to explain formula

---

## Search Tab

### Overview

Semantic search across your entire knowledge base.

💡 *Tooltip: "Find information by meaning, not exact keywords. Powered by AI embeddings."*

![Search Tab](images/knowledge_search_tab.png)

### Search Interface

**Search Bar**  
💡 *Tooltip: "Ask questions naturally. Example: 'How do I configure authentication?' or 'Security best practices'"*

- Natural language queries
- Keyword search also works
- Supports questions and phrases

**Search Modes**:

**Semantic** (default, recommended)  
💡 *Tooltip: "Finds conceptually similar content even with different words. Best for understanding-based search."*

- Finds by meaning
- Understands synonyms
- Context-aware

**Keyword**  
💡 *Tooltip: "Traditional exact-match search. Fast but less intelligent."*

- Exact text matching
- Faster but less flexible
- Good for finding specific terms

**Hybrid**  
💡 *Tooltip: "Combines semantic and keyword search for best of both"*

- Balances meaning and precision
- Recommended for technical searches

![Search Modes](images/knowledge_search_modes.png)

**Advanced Filters**:

🔧 **Advanced**

- **Document Types**: Filter to PDF, MD, code, etc.
- **Date Range**: Search within time period
- **Categories**: Limit to specific categories
- **Min Similarity**: Threshold for relevance (0.0-1.0)
- **Max Results**: How many results to return

### Search Results

Each result shows:

**Result Card**:

- **📄 Document Name**: Source document
- **Similarity Score**: 0-100% match
- **Chunk Preview**: Relevant text excerpt (highlighted)
- **Page/Line Number**: Location in document
- **Metadata**: Document tags, category, date

![Search Results](images/knowledge_search_results.png)

**Result Actions**:
- **👁️ View in Context**: See surrounding text
- **📄 Open Document**: View full document
- **📋 Copy**: Copy chunk text
- **🤖 Ask AI**: Query about this result

**Similarity Score Indicators**:
- 🟢 **90-100%**: Excellent match
- 🟡 **70-89%**: Good match
- 🟠 **50-69%**: Moderate match
- 🔴 **<50%**: Weak match (consider refining query)

### Search Tips

💡 **Best Practices**:

**Good queries**:
- ✅ "How to prevent SQL injection in Python?"
- ✅ "Best practices for API authentication"
- ✅ "Error handling patterns in microservices"

**Poor queries**:
- ❌ "code" (too vague)
- ❌ "python" (too broad)
- ❌ "help" (not specific)

**Improving Results**:

1. **Be specific**: Add context to your query
2. **Use questions**: "How do I...?" works well
3. **Include technology**: "Python", "React", "AWS"
4. **Refine iteratively**: Adjust based on results

---

## Upload Tab

### Overview

Upload documents to make them searchable by agents.

💡 *Tooltip: "Add documents to your knowledge base. Supports PDF, Word, Markdown, code files, and more."*

![Upload Tab](images/knowledge_upload_tab.png)

### Upload Methods

#### Method 1: Drag and Drop

**Steps**:

1. Drag files from your computer
2. Drop in the upload area
3. Files automatically start processing
4. Watch progress indicators

💡 *Tooltip: "Easiest method. Drag multiple files at once for batch upload."*

**Supported File Types**:
- **Documents**: PDF, DOCX, DOC, TXT, MD
- **Code**: .py, .js, .ts, .java, .go, .rs, .cpp, etc.
- **Data**: CSV, JSON, XML, YAML
- **Images**: PNG, JPEG (for analysis)

![Drag and Drop](images/knowledge_upload_dragdrop.png)

#### Method 2: File Browser

**Steps**:

1. Click **"Browse Files"** button
2. Select files from file picker
3. Choose multiple files (Ctrl/Cmd + click)
4. Click **"Open"**
5. Files start uploading

#### Method 3: URL Upload

🔧 **Advanced**

Upload from URL:

1. Click **"Upload from URL"** tab
2. Enter document URL
3. Supported: Direct file links, Google Docs, Notion pages
4. Click **"Fetch and Upload"**

💡 *Tooltip: "Upload documents from URLs without downloading first"*

### Upload Progress

**During Upload**:

Each uploading file shows:
- **Filename** and size
- **Progress bar**: Upload percentage
- **Status**: Uploading → Processing → Complete
- **Cancel button**: Stop upload

![Upload Progress](images/knowledge_upload_progress.png)

**After Upload**:

- Success message
- Document added to Library
- Automatic processing begins
- Go to Processing tab to monitor

### Upload Settings

**Metadata Assignment**  
💡 *Tooltip: "Add metadata during upload to organize documents better"*

Before uploading, configure:
- **Category**: Select or create category
- **Tags**: Add relevant tags
- **Access Level**: Public (all agents) or Private (specific agents)
- **Auto-Process**: Enable/disable automatic processing

![Upload Settings](images/knowledge_upload_settings.png)

---

## Processing Tab

### Overview

Monitor document processing queue and status.

💡 *Tooltip: "Documents are processed asynchronously. Track progress and troubleshoot issues here."*

![Processing Tab](images/knowledge_processing_tab.png)

### Sub-Tabs

The Processing tab has **4 sub-tabs**:

#### 1. Queue Status

**What it shows**:
- Current processing queue
- Active workers
- Queue depth
- Processing rate

**Queue Metrics**:

**Active Processing**  
💡 *Tooltip: "Documents currently being processed by workers"*

- Count of documents in processing
- Worker assignments
- Estimated completion time

**Queued**  
💡 *Tooltip: "Documents waiting to be processed. FIFO order unless priority set."*

- Count in queue
- Position in queue for each document
- Estimated wait time

**Processing Rate**  
💡 *Tooltip: "How many documents processed per minute. Higher = faster processing."*

- Current rate: docs/minute
- Average rate: last hour
- Peak rate: today

![Queue Status](images/knowledge_processing_queue.png)

**Queue List**:

Each queued item shows:
- Filename
- Queue position (#1, #2, #3...)
- Priority (High/Medium/Low)
- Estimated start time
- Actions: Cancel, Increase Priority

#### 2. Active Processing

**What it shows**:
- Documents actively being processed right now
- Processing stages for each
- Real-time progress

**Processing Stages**  
💡 *Tooltip: "Each document goes through 5 stages: Extract → Chunk → Embed → Index → Verify"*

**Active Document Cards**:

Shows each processing document with:
- **Filename**
- **Current Stage**: 
  1. 📄 Text Extraction
  2. ✂️ Chunking
  3. 🧮 Embedding Generation
  4. 💾 Database Indexing
  5. ✅ Verification
- **Stage Progress**: Percentage within current stage
- **Overall Progress**: Total percentage
- **Time Elapsed**: Since processing started

![Active Processing](images/knowledge_processing_active.png)

**Stage Details**:

Click on a processing document to see detailed stage info:

**Text Extraction**  
💡 *Tooltip: "Extracting text from PDF/Word. Also extracts tables, images, formulas."*

- Text extraction progress
- Pages processed / Total pages
- Images found
- Tables found
- Formulas found

**Chunking**  
💡 *Tooltip: "Splitting text into searchable chunks. Overlap ensures context preservation."*

- Chunks created
- Average chunk size
- Overlap tokens
- Chunking strategy used

**Embedding Generation**  
💡 *Tooltip: "Creating vector embeddings for semantic search. Uses AI model."*

- Embeddings generated
- Embedding model used
- Vector dimension
- Batch processing progress

**Database Indexing**  
💡 *Tooltip: "Storing in PostgreSQL with pgvector. Makes content searchable."*

- Chunks indexed
- Index building progress
- Database insert rate

**Verification**  
💡 *Tooltip: "Final quality checks. Ensures all chunks are searchable."*

- Quality checks passed
- Test search executed
- Verification results

#### 3. Completed

**What it shows**:
- Recently completed processing
- Processing statistics
- Success/failure breakdown

**Completed List**:

Shows last 50 completed items:
- Filename
- Status: ✅ Success or ❌ Failed
- Processing Time: Duration
- Chunks Created: Count
- Completion Time: Timestamp

![Completed Processing](images/knowledge_processing_completed.png)

**Success Details** (click to expand):
- Total chunks created
- Total embeddings generated
- Processing time breakdown by stage
- Quality score

**Failure Details** (click to expand):
- Error message
- Failed stage
- Retry button
- Error logs

#### 4. Failed

**What it shows**:
- All failed processing attempts
- Error messages
- Retry status

**Failed Processing List**:

Each failed item shows:
- **Filename**
- **Failed Stage**: Which stage failed
- **Error Message**: Detailed error
- **Failure Time**: When it failed
- **Retry Count**: How many retries attempted

![Failed Processing](images/knowledge_processing_failed.png)

**Common Errors**:

**"Unsupported file format"**  
- File type not supported
- Convert to PDF or TXT
- Check file extension

**"Text extraction failed"**  
- PDF may be scanned/image-based
- Use OCR tool first
- Or upload as image

**"Embedding generation failed"**  
- OpenAI API issue
- Check API key in Settings
- Retry after verification

**"Database error"**  
- Connection issue
- Check system health
- Contact administrator

**Actions**:
- **🔄 Retry**: Attempt processing again
- **🗑️ Delete**: Remove failed document
- **📋 Copy Error**: Copy error for support
- **ℹ️ Help**: Context-specific troubleshooting

---

## Analytics Tab

### Overview

Analyze knowledge base usage and performance.

💡 *Tooltip: "Understand how your knowledge base is being used. Optimize based on real data."*

![Analytics Tab](images/knowledge_analytics_tab.png)

### Sub-Tabs

The Analytics tab has **4 sub-tabs**:

#### 1. Usage Statistics

**What it shows**:
- Document search frequency
- Most popular documents
- Search trends over time
- Agent usage patterns

**Usage Metrics Cards**:

**📊 Total Searches**  
💡 *Tooltip: "Total semantic searches executed across knowledge base"*

- All-time search count
- Searches this week
- Trend indicator

**📈 Searches This Week**  
💡 *Tooltip: "Search volume for last 7 days"*

- Weekly count
- Comparison to previous week
- Daily average

**⭐ Avg Relevance**  
💡 *Tooltip: "Average similarity score of search results. Higher = better search quality."*

- Average: 0.0-1.0
- Target: >0.75
- Trend

**🎯 Cache Hit Rate**  
💡 *Tooltip: "Percentage of searches served from cache. Higher = faster, cheaper."*

- Cache effectiveness
- Hit rate percentage
- Cache size

![Usage Statistics](images/knowledge_analytics_usage_stats.png)

**Charts**:

**Search Volume Over Time**:
- Line chart of searches per day
- Last 7/30/90 days
- Peak usage times

**Most Searched Documents**:
- Bar chart of top 10 documents
- Search count per document
- Helps identify important content

**Search Success Rate**:
- Percentage of searches returning results
- Results with similarity >0.7
- No results searches (queries to improve)

#### 2. Document Performance

**What it shows**:
- Which documents are most useful
- Document search rankings
- Quality scores

**Top Documents Table**:

| Rank | Document | Searches | Avg Similarity | Chunks | Last Search |
|------|----------|----------|----------------|---------|-------------|
| 1 | Security Guide.pdf | 234 | 0.89 | 45 | 2 min ago |
| 2 | API Documentation.md | 189 | 0.87 | 38 | 5 min ago |
| 3 | Architecture Overview.pdf | 156 | 0.85 | 52 | 1 hour ago |

💡 *Tooltip: "Documents ranked by utility. Top documents are most valuable to agents."*

![Document Performance](images/knowledge_analytics_document_perf.png)

**Insights**:
- **Underused Documents**: Uploaded but rarely searched (consider removing)
- **High-Value Documents**: Frequently searched with high relevance (keep updated)
- **Failed Searches**: Queries that found no good results (upload relevant docs)

#### 3. Quality Metrics

**What it shows**:
- Search result quality
- Embedding quality
- Processing quality

**Quality Score Distribution**:

Histogram showing search result similarity scores:
- Most results should be >0.7
- Few results <0.5
- Normal distribution is healthy

![Quality Metrics](images/knowledge_analytics_quality.png)

**Processing Quality**:
- **Successful Processing**: % of uploads processed successfully
- **Chunk Quality**: Average tokens per chunk (target: 300-700)
- **Embedding Quality**: Dimensionality and model used
- **Index Health**: Database index performance

**Recommendations**:

Based on metrics, system suggests:
- "Consider re-processing documents with low search scores"
- "Add more documents in 'deployment' category (many searches, few results)"
- "Processing success rate excellent (98%)"

#### 4. Agent Access Patterns

**What it shows**:
- Which agents search which documents
- Access frequency by agent
- Agent preferences

**Agent-Document Matrix**:

Heatmap showing:
- Rows: Agents
- Columns: Documents
- Color intensity: Access frequency
- Helps understand agent knowledge needs

![Agent Access Patterns](images/knowledge_analytics_agent_access.png)

**Insights**:
- "SecurityExpert-003 frequently accesses 'OWASP Guide.pdf'"
- "CodeArchitect-001 uses 'Python Best Practices.md' most"
- "DataAnalyst-007 rarely accesses knowledge base (may need more relevant docs)"

---

## CodeGraph Tab

### Overview

Index and search code repositories for AI understanding.

💡 *Tooltip: "Turn code into AI-readable knowledge graphs. Agents can understand your codebase."*

![CodeGraph Tab](images/knowledge_codegraph_tab.png)

### Statistics Cards

**💻 Projects Indexed**  
💡 *Tooltip: "Code repositories indexed and searchable"*

- Count of indexed projects
- Example: "3 projects"

**📁 Files Analyzed**  
💡 *Tooltip: "Total code files across all projects"*

- Total file count
- Lines of code
- Example: "1,847 files"

**🔗 Relationships**  
💡 *Tooltip: "Code relationships mapped (imports, calls, dependencies)"*

- Symbol relationships tracked
- Call graphs generated
- Example: "15,234 relationships"

**⚡ Queries This Week**  
💡 *Tooltip: "How many code searches performed this week"*

- Weekly query count
- Trend vs last week
- Example: "89 queries"

![CodeGraph Stats](images/knowledge_codegraph_stats.png)

### Indexed Projects

**Project Cards**:

Each indexed project shows:

- **Project Name**: Identifier
- **Source Type**: 
  - 📁 Local Directory
  - 🔗 GitHub URL
  - 🦊 GitLab URL
- **Language**: Python, TypeScript, Java, etc.
- **Files**: Count of indexed files
- **Last Indexed**: Timestamp
- **Status**: 🟢 Active, 🟡 Indexing, 🔴 Failed

![CodeGraph Projects](images/knowledge_codegraph_projects.png)

**Project Actions**:
- **🔍 Search**: Search within this project
- **🔄 Re-index**: Update index with latest code
- **⚙️ Settings**: Configure indexing options
- **🗑️ Delete**: Remove project index

### Add New Project

Click **"Add Project"** to open index configuration:

![Add Project Modal](images/knowledge_codegraph_add_modal.png)

**Project Settings**:

**Project Name** (required)  
💡 *Tooltip: "Unique identifier for this codebase"*

- Example: "automatos-backend", "client-acme-ecommerce"

**Source Type** (required)  
💡 *Tooltip: "Where the code lives"*

- **Local Directory**: Path on server
- **GitHub**: Repository URL
- **GitLab**: Repository URL
- **Bitbucket**: Repository URL

**Source Details** (depends on type):

**For Local Directory**:
- **Path**: `/path/to/code`
- **Language**: Auto-detect or specify
- **Exclude Patterns**: `node_modules, __pycache__, .git`

**For Git Repositories**:
- **Repository URL**: `https://github.com/org/repo.git`
- **Branch**: `main` or specify
- **Auth Token**: For private repos
- **Clone Depth**: 1 (shallow) or full

**Indexing Options**:

**Auto Re-index**  
💡 *Tooltip: "Automatically re-index when code changes (via webhooks)"*

- ✅ Enable for active projects
- ❌ Disable for archived projects

**Exclude Patterns**  
💡 *Tooltip: "Glob patterns to skip. Default: node_modules, __pycache__, .git"*

- Comma-separated patterns
- Standard: `node_modules, venv, .git, *.pyc`

**Languages** (auto-detected)  
💡 *Tooltip: "Programming languages in this codebase. Auto-detected but can override."*

- Python, TypeScript, JavaScript, etc.
- Multi-language projects supported

**Click "Index Project"**:
- Indexing starts in background
- Progress shown in Processing tab
- Typically takes 1-5 minutes

### Searching Code

**Code Search Interface**:

1. Select project from dropdown (or "All Projects")
2. Enter natural language query:
   - "How is authentication handled?"
   - "Where are database queries executed?"
   - "Find payment processing code"
3. Click **"Search"**

**Results Show**:
- **File**: Path to code file
- **Line**: Line number
- **Symbol**: Function/class name
- **Code Snippet**: Relevant code (highlighted)
- **Relevance**: Similarity score

![CodeGraph Search](images/knowledge_codegraph_search.png)

**Code Result Actions**:
- **👁️ View in Context**: See surrounding code
- **📄 Open File**: Full file view
- **📋 Copy**: Copy code snippet
- **🔗 View Dependencies**: See what this code calls/is called by

### Code Insights

🔧 **Advanced**

**Symbol Browser**:
- Browse all classes, functions, variables
- See relationships between symbols
- Navigate call graphs

**Dependency Graphs**:
- Visual module dependencies
- Identify circular dependencies
- Find entry points

**Complexity Heatmap**:
- Visual representation of code complexity
- Highlight complex files needing refactoring
- Cyclomatic complexity scores

---

## Common Tasks

### Task 1: Upload and Search a Document

**Scenario**: Upload company security policy and search it

**Steps**:

1. Go to **Upload** tab
2. Drag `Security_Policy.pdf` into upload area
3. Wait for upload (5-10 seconds)
4. Processing starts automatically (30-60 seconds)
5. Go to **Search** tab
6. Query: "What is our password policy?"
7. Get results from the security policy

⏱️ **Time**: 2 minutes total  
🎯 **Result**: Policy document searchable

### Task 2: Extract Tables from Document

**Scenario**: Extract financial tables from annual report

**Steps**:

1. Upload `Annual_Report_2024.pdf`
2. Wait for processing to complete
3. Go to **Multimodal** tab → **Tables**
4. Find extracted tables
5. Click **"View Full Table"**
6. Download as CSV if needed

⏱️ **Time**: 2-3 minutes  
🎯 **Result**: Tables extracted and downloadable

### Task 3: Index a Code Repository

**Scenario**: Make your codebase searchable for agents

**Steps**:

1. Go to **CodeGraph** tab
2. Click **"Add Project"**
3. **Project Name**: "my-app"
4. **Source Type**: GitHub
5. **URL**: `https://github.com/myorg/myapp.git`
6. **Branch**: `main`
7. Click **"Index Project"**
8. Monitor progress in Processing tab (2-5 minutes)
9. Search code once indexing completes

⏱️ **Time**: 5 minutes  
🎯 **Result**: Code searchable by agents

### Task 4: Finding Specific Code

**Scenario**: Find where authentication is implemented

**Steps**:

1. Go to **CodeGraph** tab
2. Select your project
3. Search: "user authentication implementation"
4. Review results:
   - `auth/middleware.py:authenticate_user`
   - `services/auth_service.py:verify_credentials`
5. Click result to view code
6. Explore dependencies if needed

⏱️ **Time**: 1 minute  
🎯 **Result**: Authentication code located

### Task 5: Monitoring Processing Status

**Scenario**: You uploaded 50 documents, want to track progress

**Steps**:

1. Go to **Processing** tab
2. **Queue Status** sub-tab shows:
   - Active: 5 documents
   - Queued: 45 documents
   - Processing rate: 6 docs/min
3. **Active Processing** sub-tab shows:
   - Current document being processed
   - Stage progress
   - Estimated completion
4. Wait or navigate away (processing continues)
5. Get notification when all complete

⏱️ **Time**: Passive monitoring  
🎯 **Result**: Awareness of processing status

---

## Advanced Features

### Semantic Search Configuration

🔧 **Advanced**

Fine-tune semantic search parameters:

**Embedding Model**  
💡 *Tooltip: "Model used to create vector embeddings. Better models = better search."*

- Default: `text-embedding-ada-002`
- Advanced: `text-embedding-3-large`
- Dimension: 1536 or 3072

**Similarity Threshold**  
💡 *Tooltip: "Minimum similarity score for results. Higher = more relevant but fewer results."*

- Range: 0.0 to 1.0
- Recommended: 0.7
- Adjust based on result quality

**Chunk Size**  
💡 *Tooltip: "Size of searchable text segments. Larger = more context, fewer chunks."*

- Range: 200-1000 tokens
- Recommended: 512 tokens
- Overlap: 50-100 tokens

**Re-ranking**  
💡 *Tooltip: "Re-order results with more sophisticated model. Slower but better quality."*

- Enable/disable
- Re-ranking model
- Performance trade-off

### Document Categories and Taxonomy

🔧 **Advanced**

Organize documents with hierarchical categories:

**Creating Categories**:

1. Library tab → **"Manage Categories"**
2. Create category structure:
   ```
   Technical Documentation
   ├── API Guides
   ├── Architecture Docs
   └── Security Policies
   
   Business Documents
   ├── Contracts
   ├── Policies
   └── Reports
   ```
3. Assign documents to categories
4. Filter by category for focused search

### CodeGraph Advanced Features

🔧 **Advanced**

**Call Graph Visualization**:
- See function call relationships
- Identify code hotspots
- Trace execution paths

**Dependency Analysis**:
- Module dependency trees
- Circular dependency detection
- Import optimization suggestions

**Code Metrics**:
- Cyclomatic complexity
- Lines of code per file
- Function length distribution
- Comment coverage

**Webhook Integration**:
- Auto-reindex on git push
- GitHub/GitLab webhook setup
- Incremental updates (only changed files)

### Custom Processing Pipelines

🔧 **Advanced**

Configure custom processing for specific file types:

**Processing Rules**:

```json
{
  "file_pattern": "*.py",
  "chunk_size": 600,
  "overlap": 100,
  "extract_code_blocks": true,
  "extract_docstrings": true
}
```

**Advanced Extraction**:
- Custom regex patterns
- Code syntax highlighting
- API endpoint extraction
- Database schema extraction

---

## Tips & Best Practices

### Document Upload

💡 **Best Practices**:

1. **Use clear filenames**: Descriptive, organized names
2. **Tag immediately**: Add tags during/after upload
3. **Categorize**: Assign to appropriate category
4. **Monitor processing**: Check for errors
5. **Verify searchability**: Test search after processing

**Optimal Document Formats**:
- ✅ PDF with text (not scanned images)
- ✅ Markdown (.md)
- ✅ Word documents (.docx)
- ✅ Plain text (.txt)
- ⚠️ Avoid: Scanned PDFs without OCR

### Search Effectiveness

💡 **Tips**:

1. **Be specific**: "Python authentication security" > "security"
2. **Use questions**: "How to deploy?" > "deployment"
3. **Include context**: "FastAPI error handling" > "errors"
4. **Iterate**: Refine query based on results
5. **Check similarity scores**: >0.8 is excellent, <0.6 consider refining

### CodeGraph Indexing

💡 **Best Practices**:

1. **Exclude build artifacts**: Add to exclude patterns
2. **Include tests**: Test code often has good examples
3. **Update regularly**: Re-index after major changes
4. **Multiple projects**: Keep projects separate for clarity
5. **Use webhooks**: Auto-update on commits

**Exclude Patterns**:
```
node_modules, __pycache__, venv, .git, *.pyc, 
dist, build, .next, target, bin, obj
```

### Performance Optimization

**Make searches faster**:

1. **Enable caching**: Frequently searched queries cached
2. **Appropriate chunk size**: 512 tokens is optimal balance
3. **Limit max results**: 10-20 results is usually enough
4. **Archive old documents**: Remove outdated content
5. **Use categories**: Narrow search scope

---

## Troubleshooting

### Search Returns No Results

**Symptom**: Query returns no results or very low similarity

**Solutions**:

1. **Check document processing**:
   - Processing tab → Verify documents processed
   - Library tab → Check status badges (should be green)

2. **Refine query**:
   - Make more specific
   - Use different keywords
   - Try simpler query first

3. **Check embeddings**:
   - Analytics tab → Verify embeddings exist
   - Re-process if embeddings missing

4. **Add more documents**:
   - May not have relevant content
   - Upload documents covering the topic

### Document Won't Upload

**Symptom**: Upload fails or file rejected

**Solutions**:

1. **Check file size**:
   - Max size: 50MB per file
   - Compress or split large files

2. **Check file format**:
   - Verify supported format
   - Convert to PDF if unsure

3. **Check file name**:
   - No special characters
   - No extremely long names
   - Use ASCII characters

4. **Check storage space**:
   - System may be at capacity
   - Contact administrator

### Processing Takes Forever

**Symptom**: Document stuck in processing >10 minutes

**Solutions**:

1. **Check document size**:
   - Large documents (>100 pages) take longer
   - 1,000 pages might take 5-10 minutes
   - This is normal

2. **Check queue position**:
   - Processing tab → Queue Status
   - If many documents queued, wait time increases

3. **Check system health**:
   - Dashboard → System status
   - Processing may be paused
   - Or system under heavy load

4. **Check for errors**:
   - Processing tab → Active Processing
   - Look for error messages
   - May be stuck on specific stage

**If truly stuck (>30 min)**:
- Cancel and retry
- Or contact support

### CodeGraph Index Failed

**Symptom**: Code indexing failed with error

**Solutions**:

1. **Check repository access**:
   - Private repos need auth token
   - Verify URL is correct
   - Test git clone manually

2. **Check repository size**:
   - Very large repos (>100K files) may timeout
   - Use exclude patterns to limit scope

3. **Check language support**:
   - Verify language is supported
   - Python, TypeScript, JavaScript, Go, Rust, Java supported

4. **Check exclude patterns**:
   - Make sure not excluding all files
   - Verify pattern syntax

**Common Auth Issues**:
- GitHub token needs `repo` scope
- GitLab token needs `read_repository` scope
- Token may have expired

---

## Document Details Modal

**How to open**: Click document card or "View Details" button

💡 *Tooltip: "Complete document information and management"*

![Document Details Modal](images/knowledge_modal_details.png)

### Tab 1: Information

**Shows**:
- Full filename
- File path (if applicable)
- Upload date and time
- Uploaded by user
- File size
- File type and format
- Processing status
- Category and tags

**Metadata**:
- Custom metadata fields
- Auto-detected metadata
- Edit metadata button

**Actions**:
- Download original
- Re-process document
- Delete document
- Share (if permissions allow)

### Tab 2: Content

**Shows**:
- Extracted text preview
- Chunk breakdown
- Table of contents (if available)
- Extracted multimodal content counts

**Content Preview**:
- First 5,000 characters
- Expandable to see more
- Formatted view
- Copy to clipboard

**Chunks View**:
- All chunks listed
- Chunk boundaries
- Chunk preview
- Search within chunks

### Tab 3: Analytics

**Shows**:
- Search frequency
- Average relevance score
- Which agents use this document
- Search queries that found this

**Performance**:
- Times searched
- Last search timestamp
- Average similarity score
- Most common queries

**Agent Usage**:
- Which agents accessed
- How many times
- In which workflows
- Success rate when used

---

## Related Guides

- **[Context Engineering Guide](../CONTEXT.md)**: RAG and optimization
- **[Agents Guide](../AGENTS.md)**: How agents use knowledge
- **[Workflows Guide](../WORKFLOWS.md)**: CodeGraph in workflows
- **[Chatbot Guide](../CHATBOT.md)**: Ask questions about documents

---

## Keyboard Shortcuts

- **Ctrl/Cmd + U**: Quick upload
- **Ctrl/Cmd + F**: Focus search
- **Ctrl/Cmd + K**: Quick search (opens modal)
- **Tab**: Navigate between tabs
- **Esc**: Close modals

---

## FAQ

### What file types are supported?

**Documents**:
- PDF (text-based, searchable)
- Microsoft Word (.docx, .doc)
- Markdown (.md)
- Plain text (.txt)
- Rich text (.rtf)

**Code**:
- Any text-based code file
- Python, JavaScript, TypeScript, Java, Go, Rust, C++, etc.

**Data**:
- CSV, JSON, XML, YAML

**Maximum size**: 50MB per file

### How long does processing take?

**Typical times**:
- Small document (5 pages): 10-20 seconds
- Medium document (50 pages): 30-60 seconds
- Large document (500 pages): 2-5 minutes
- Code repository (1,000 files): 3-10 minutes

Processing is parallel - multiple documents processed simultaneously.

### Can I search multiple documents at once?

**Yes!** Semantic search searches ALL processed documents by default.

Use filters to narrow:
- Filter by category
- Filter by tags
- Filter by document type
- Filter by date uploaded

### What is semantic search?

**Traditional keyword search**:
- Finds exact word matches
- "authentication" finds only "authentication"
- Misses related concepts

**Semantic search**:
- Understands meaning
- "user login" finds "authentication", "sign in", "credentials"
- Context-aware

### How does CodeGraph help agents?

When you add `codegraph_project` to workflow context:

```json
{
  "codegraph_project": "myapp"
}
```

Agents automatically:
- Search relevant code
- Get code context
- Understand architecture
- Reference specific files/functions

**No manual code copying needed!**

### Can I delete a document?

**Yes**, but be careful:

1. Click document → Details
2. Click **"Delete"** button
3. Confirm deletion
4. Document removed from:
   - Library
   - Search index
   - All embeddings
   - Analytics history

⚠️ **Warning**: Deletion is permanent. Download first if you might need it later.

---

**Next**: [Context Engineering Guide →](../CONTEXT.md)

*Master RAG optimization and context engineering*


---

## API Reference


## Sources
Add, index, and delete sources; track status and size.

**API**  
> **Authentication**  
> All API calls require headers:  
> ```http
> X-API-Key: <your_key>
> Authorization: Bearer <your_token>
> ```

- `GET /api/sources`  
- `POST /api/sources` (body: `{"name":"Repo","type":"git","config":{"url":"..."}}`)  
- `POST /api/sources/{id}/index`  
- `DELETE /api/sources/{id}`

## Documents
Search and filter documents; reindex when schemas change.

**API**  
- `GET /api/documents?source_id=&q=&limit=&offset=&tag=`  
- `POST /api/documents/reindex` (body: `{"source_id":"..."}`)

## Code Graph
Search project code and emit a compact **CODE slot** block.

**API**  
- `POST /api/codegraph/index` (body: `{"project":"automatos-ai","root_dir":"/repo"}`)  
- `GET /api/codegraph/search?project=&q=&limit=`
