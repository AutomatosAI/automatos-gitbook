---
description: Upload, browse, and manage documents in your knowledge base.
---

# Documents

The Documents tab is the main document management interface. It has six sub-tabs for different aspects of document handling.

## Library

Browse all documents in your knowledge base:
- File name, size, and upload date
- Processing status (pending, processing, completed, failed)
- Chunk count — how many searchable segments were created
- Actions — view, re-process, delete

<!-- IMAGE: Document library showing file list with status indicators -->

### File types supported

| Type | Extensions |
| --- | --- |
| **Text** | `.md`, `.txt`, `.csv`, `.json` |
| **Office** | `.docx`, `.xlsx`, `.pptx` |
| **PDF** | `.pdf` (including scanned documents via OCR) |
| **Code** | `.py`, `.js`, `.ts`, `.go`, `.java`, and more |
| **Web** | `.html` |

## Upload

Bulk upload interface:
1. Click **Upload Documents** or drag files onto the page
2. Files are queued for processing
3. The ingestion pipeline runs automatically:
   - **Parse** — extract text from the file format
   - **Chunk** — split into semantic segments
   - **Embed** — generate vector embeddings
   - **Index** — store in the vector database

<!-- IMAGE: Upload interface with drag-and-drop zone and processing queue -->

{% hint style="info" %}
Large files are processed asynchronously. Check the Processing sub-tab for status updates.
{% endhint %}

## Processing

Monitor the ingestion pipeline:
- Files in queue
- Currently processing (with progress)
- Recently completed
- Failed (with error details)

## Search

Test semantic search across your knowledge base:
1. Type a natural language query
2. See ranked results with relevance scores
3. Click a result to view the source document and chunk

This is exactly what your agents see when they search your knowledge base during chat.

<!-- IMAGE: Search interface showing query results with relevance scores -->

## RAG

Configure retrieval-augmented generation settings:
- **Top K** — number of chunks retrieved per query
- **Similarity threshold** — minimum relevance score
- **Reranking** — enable/disable result reranking
- **Context window** — how much surrounding text to include

## Multimodal

Documents with rich media:
- Images with extracted text (OCR)
- PDFs with embedded graphics
- Mixed-content documents

{% hint style="info" %}
The embedding model used is configurable in [Settings](../settings/README.md). Default is `qwen/qwen3-embedding-8b` with 2048 dimensions.
{% endhint %}
