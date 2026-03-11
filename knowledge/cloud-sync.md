---
description: Sync folders from Dropbox and cloud storage into your knowledge base.
---

# Cloud Sync

Cloud Sync lets you connect external storage services and automatically sync documents into your knowledge base. Files are downloaded, processed, and indexed — and kept in sync as changes occur.

<!-- IMAGE: Cloud Sync interface showing Dropbox connection with folder browser -->

## Supported providers

| Provider | Status |
| --- | --- |
| **Dropbox** | Available |
| **Google Drive** | Coming soon |
| **OneDrive** | Coming soon |
| **S3** | Available (for custom buckets) |

## Connecting Dropbox

1. Go to **Knowledge Bases → Documents**
2. Click **Dropbox** in the cloud provider section
3. Authenticate with your Dropbox account
4. Browse and select a folder to sync
5. Click **Sync Folder**

<!-- IMAGE: Dropbox folder browser showing Root Folder Selected with file count -->

## Sync status

Once connected, the sync panel shows:

| Metric | Description |
| --- | --- |
| **Total Files** | Files in the synced folder |
| **Synced** | Successfully downloaded and processed |
| **Pending** | Awaiting processing |
| **Chunks** | Vector chunks generated from synced files |

## How sync works

1. **Initial sync** — all files in the selected folder are downloaded and processed
2. **Incremental sync** — on subsequent runs, only new or modified files are processed
3. **Processing** — each file goes through the same pipeline as manual uploads (parse → chunk → embed → index)

{% hint style="info" %}
Sync runs can be triggered manually with the **Sync Folder** button or scheduled to run automatically.
{% endhint %}

## Managing synced files

Synced files appear in the Library alongside manually uploaded documents. They're tagged with their cloud source for easy identification.

To stop syncing:
1. Go to the cloud provider section
2. Click **Back to Root** to navigate folders
3. Click **Disconnect** or select a different folder

{% hint style="warning" %}
Disconnecting a cloud sync does not delete already-processed documents. They remain in your knowledge base until manually removed.
{% endhint %}
