---
title: Managing files in the File Archive
description: Access information about files imported and exported using Payment Management
date: 19-07-2021
id: PM-162
lang: en
---

# Managing Files in the File Archive

You can access information about files imported and exported from Business Central, using Payment Management in the file archive. The file archive lists information about all files managed by Payment Management, such as file date and type, together with a status of whether the file has been processed by Payment Management.

You can reimport a file, or mark it as processed or unprocessed, by using the actions located under **More Options** in the action bar.

## To enable file log

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Banks**, then select the related link.
1. Select and open a bank card.
1. On the bank card, navigate to the FastTab **Advanced**, and in the **Log Period** field, specify the period of time files must be stored in the archive before they are deleted. For example, if you write *30D*, files are stored for 30 days. If the field is empty, stored files will never be deleted.

## To view or export files in the file archive

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **File archive**, then select the related link.
   To access the old file archive used by Payment Management version 2.1.0.1 and older, search for **File archive (depreciated)**.
1. Use the filter to search for a specific file in the list.
1. To view or export the file, navigate to the action bar and select **File export** > **Save/show file**. This saves the file locally on your desktop. You can export multiple files at once in one zip file, by selecting multiple lines, then performing file export.

## To access files for a specific bank

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Banks**, then select the related link.
1. Select and open a bank card.
1. On the bank card navigate to the action bar and select **Archive** > **File Archive**.

The file archive will open and the list of files will be filtered by the system code for the given bank.

## To access files for a specific payment

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Journals**, then select the related link.
1. Select the payment line for which you want to access the logged file. Please note, that files are only available for payments that have been sent to the bank.
1. In the information box, located at the right side of the screen, navigate to the FastTab **Payment Management**, and select the **Payment Status** link. This will open the **Credit Transfer Log**.
1. In the action bar, select **Log** > **File Archive**.

The file archive will open and the list of files will be filtered by the given payment.

## To move old files to the new file archive

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **File archive (depreciated)**, then select the related link.
1. In the depreciated file archive, select the files that should be moved to the new archive.
1. Navigate to the action bar and select **Actions** > **Move files to new archive**.



