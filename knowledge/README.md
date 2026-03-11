---
description: Upload documents, sync cloud folders, and give your agents knowledge.
---

# Knowledge Bases

The Knowledge Bases page is where you manage all the documents, databases, and code repositories your agents can search and reference.

<!-- IMAGE: Knowledge Bases page showing document stats and library -->

## Page layout

{% tabs %}
{% tab title="Documents" %}
Your document library with sub-tabs:
- **Library** — browse all uploaded files
- **Processing** — monitor ingestion pipeline status
- **Multimodal** — images, PDFs, and rich media documents
- **Search** — test semantic search across your knowledge base
- **RAG** — retrieval-augmented generation configuration
- **Upload** — bulk upload interface

[Full guide →](documents.md)
{% endtab %}

{% tab title="Database" %}
SQL and semantic database tools:
- **SQL Explorer** — query your data directly
- **Semantic Layer** — natural language to SQL mappings
- **Query Templates** — saved queries
- **Training** — teach the NL2SQL system
- **Schema Browser** — explore table structures
- **Audit History** — query execution logs

[Full guide →](database.md)
{% endtab %}

{% tab title="Templates" %}
Document templates for standardised content creation. Agents can use templates to generate consistent reports, summaries, and documentation.

[Full guide →](templates.md)
{% endtab %}

{% tab title="CodeGraph" %}
Code repository indexing. Connect repos and browse your codebase as a knowledge graph — agents can search code semantically.

[Full guide →](codegraph.md)
{% endtab %}
{% endtabs %}

## Stats bar

| Metric | Description |
| --- | --- |
| **Total Documents** | Number of files in your knowledge base |
| **Processed** | Files that have been chunked and embedded |
| **Storage Used** | Total disk space consumed |
| **Vector Chunks** | Number of searchable embedding chunks |

<!-- IMAGE: Stats bar showing 100 Total Documents, 3.2 MB Storage, 7135 Vector Chunks -->

## Quick start

1. Click **Upload Documents** in the top right
2. Drag and drop files (PDF, MD, DOCX, TXT, and more)
3. Wait for processing (chunking + embedding)
4. Test with a search query in the Search sub-tab
5. Your agents can now reference these documents in chat

{% hint style="success" %}
Documents are automatically chunked using semantic boundaries and embedded for vector search. No manual configuration needed.
{% endhint %}

## Subpages

| Page | Description |
| --- | --- |
| [Documents](documents.md) | Uploading, browsing, and managing documents |
| [Cloud Sync](cloud-sync.md) | Syncing folders from Dropbox and cloud storage |
| [Database](database.md) | SQL Explorer and semantic querying |
| [Templates](templates.md) | Document templates |
| [CodeGraph](codegraph.md) | Code repository indexing |
