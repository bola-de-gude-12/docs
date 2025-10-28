---
title: Expense Management setting up document storage
date: 28-07-2025
description: 
id: EM-144
lang: en
---
# Setting up Document Storage

When you import expense documents into Continia Expense Management, the files you import are by default stored directly in the Microsoft Dynamics 365 Business Central database. However, storage space limitations may make it necessary or desirable for you to store these files in other locations instead.

To calculate how much storage space you need for your files, use the following guidelines:

- The average attachment file takes up approximately 500 KB of space.
- For the vast majority of Expense Management clients, expense users will store 10 documents per month on average.

Multiplying these two numbers by the number of users expected in the system will give you a fairly precise indication of how much storage space you need.

The table below outlines the various storage options, enabling you to decide which one is right for you:

| Storage type | Description |
| --- | --- |
| **Database** | For this type of storage, documents are stored in the Business Central database. |
| **Azure Blob** | With this storage type, documents are stored in an Azure Blob container that you need to host yourself. For more details on how to set it up, see [Setting up Azure Blob Storage](/Continia Expense Management/Development and Administration/Setting up Azure Blob storage.md). |
| **File System** (on-premises only) | For this storage type, documents are stored on a file server on the same LAN as the Business Central Service Tier. |

## Changing document storage settings

To set up your document storage, follow these steps:

1. Search for {{search}} **Expense Management Setup**.
2. Under **General**, go to **Document Storage Type** and select your preferred storage type in the box.
3. If you select **Azure Blob Storage**, a dialog box appears asking you if you want to continue. Click **Yes**.
4. The **Update Storage Settings** window opens. Under **General**, fill out all fields with the relevant details from your Azure Blob account. Click **OK**  to close the window and update the settings.

## Custom storage

Some customers prefer to store documents in their own document management system (DMS). This is somewhat more complicated and requires the assistance of a developer. If this is what you need though, you have to implement your own storage functions.

## Related information
[Setting up Azure Blob Storage](/continia-expense-management/development-and-administration/setting-up-azure-blob-storage)  
[Customizing Storage](/Continia Expense Management/Development and Administration/Development and customization/Customizing your storage.md)  
[Storage considerations when migrating to the cloud](/continia-expense-management/development-and-administration/on-premises/upgrade/migrate-from-on-premises-to-cloud)  
