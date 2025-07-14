---
title: Data maintenance using job queues for Continia Document capture tables
date: 11-12-2024
description:
id: DC-380
lang: en
---

# Data Maintenance Using Job Queues for Continia Document Capture Tables

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Data maintenance using job queues for Continia Document Capture tables | {{checkmark}} Mar 2024 | {{checkmark}} Apr 2024 |

## Business value

Introducing a number of cleanup job queues for tables like **CDC Document** (6085590) and **CDC Document Word** (6085592) will enable you to automate the cleanup process, thereby ensuring smoother handling of document-related data. By automating the deletion of captured words, generated values, and entire documents based on the status and age of each document, the feature will simplify data management, significantly reduce manual effort, streamline the database, and substantially improve overall system performance.

## Feature details

Job queues for the following activities will be added:

* Delete words and values based on document status.
* Delete words and values based on document age (based on setup fields).
* Delete document and all related files and data from storage (such as emails, PDFs, metadata, images, or XMLs).

If you use a job queue to delete words or values, the **CDC Document Word** and **CDC Document Value** tables will be cleaned up automatically, whereas using the job queue to delete an entire document and its related data will result in an automatic cleanup of all the tables and files/objects below:

* **CDC Document** table
* **CDC Document Word** table
* **CDC Document Value** table
* **CDC Document Email** table
* **CDC Document Page** table
* **CDC Document Comment** table
* BLOBs or files with data 

For more information, see [Setting up Data Maintenance](@DC-187).

## Related information

[Setting up Job Queues](@DC-16)  
