---
title: Setting up document storage in Document Capture
date: 08-07-2025
description:
id: DC-3
lang: en
---

# Setting up document storage

When you import documents into Continia Document Capture, the files you import are by default stored directly in the Microsoft Dynamics 365 Business Central database. However, storage space limitations may make it necessary or desirable for you to store these files in other locations instead.

To calculate how much space you need in order to store your files, use the following guidelines:
* The average PDF file takes up approximately 100 KB of space per page.
* For the vast majority of Document Capture customers, the average invoice has two pages.

Multiplying these two numbers by your total number of PDF files will give you a good indicator of the amount of storage space needed.

The table below outlines the various storage options, enabling you to decide which one is right for you:

| Storage type | Description |
| --- | --- |
| **File System** (on-premises only) | Documents are stored on a file server on the same LAN as the Business Central Service Tier. |
| **Database** | Documents are stored in the Business Central database. |
| **Azure Blob Storage** | Documents are stored in an Azure Blob container that you need to host yourself. For more details on how to set it up, see [Setting up Azure Blob Storage](@DC-171). |
| **Continia File Service** (on-premises only) | Documents are stored in cloud-compatible, predefined repositories that point to a specific folder. This folder can be local or shared. For details on how to set it up, see [Installing the Continia File Service](@DC-124). |

## To change document storage settings

To set up your document storage:

1. Search {{search}} for and select **Storage Migration Assisted Setup Guide**.
1. Follow the on-screen instructions.
1. When you're done, click **Finish** to close the guide and implement the settings.

To check, pause, or resume a storage migration:

* Search {{search}} for and select **Storage Migration Status**.

For more advanced storage configurations (such as changing storage settings without actually migrating any data):

1. Search {{search}} for and select **Document Capture Setup**.
1. On the **General** FastTab, go to **Document Storage Type** and select your preferred storage type in the box.
1. If you select **Azure Blob Storage**, a dialog box appears, asking you if you want to continue. Click **Yes**.
1. The **Update Storage Settings** window opens. Under **General**, fill out all fields with the relevant details from your Azure Blob account. Click **OK** to close the window and update the settings.

## Custom storage

Some customers prefer to store documents in their own document management system (DMS). This is somewhat more complicated and requires the assistance of a developer. If this is what you need though, you need to implement your own storage functions. For more details on how to set this up, see [Customizing storage](@DC-73).

## Related information

[Considerations when migrating to the cloud](@DC-106#considerations-when-migrating-to-the-cloud)  



<style>
  .content table tr td:nth-child(1) {
    width: 130px;
  }
  .content table tr td:nth-child(2) {
    width: 700px;
  }  
</style>