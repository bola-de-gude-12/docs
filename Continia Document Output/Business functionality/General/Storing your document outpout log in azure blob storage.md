---
title: Storing your Document Output Log in Azure Blob Storage
description: 
date: 12-06-2025
id: DO-130
lang: en
---

# Storing your Document Output Log in Azure Blob Storage

Document Output logs and stores all emails and XML files that are sent through the solution. By default, the log is stored directly in the database in both on-premises and online versions of Document Output. However, it's also possible to export the log to Azure Blob Storage to free up database storage.

> [!IMPORTANT]
> When setting up your Azure Blob Storage account, make sure to set its **AllowBlobPublicAccess** property to **False**. This prevents a known security risk by forcing all blob data requests to be authenticated. For more information, see [Overview: Remediating anonymous read access for blob data](https://learn.microsoft.com/en-us/azure/storage/blobs/anonymous-read-access-overview) (Microsoft article).

To export the Document Output log to Azure Blob Storage, follow these steps:

1. Choose the {{search}} icon, enter **Document Output Setup**, and then choose the related link.
1. In the **Email Log** FastTab, enter the **Azure Storage Account Name**, the **Azure Blob Container Name**, and the **Azure Storage Account Key**.
1. Change  **Log Storage Type** to **Azure Blob Storage**.

The existing log is immediately transferred to the selected Azure storage account. If the transfer fails, you can revert it by setting **Log Storage Type** to **Database** or (if possible) **File System**.

> [!TIP]
> By default, an email job called *Delete-Log* is created but not enabled with the standard setup of Document Output. This can limit the size of the Document Output log but may also violate local legislation concerning email logging, so be sure to look into that before enabling the *Delete-Log* email job.
