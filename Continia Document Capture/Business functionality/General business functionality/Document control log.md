---
title: Document Control Log in Document Capture
date: 06-10-2025
description:  
id: DC-212
lang: en
---

# Document Control Log

The logging functionality of [the Secure Archive](@DC-154) automatically records every step in the processing of documents that have been imported into – and processed by – Continia Document Capture and Continia Expense Management. When these documents are posted, a message is displayed on the **General** FastTab of the document card, under **Document Log**, indicating the number of log entries. If any changes have been made to a document at some point after it has been approved and/or posted, a warning message is displayed to indicate that someone modified the document and/or its attachments.

You can view the status of a posted document by opening its document card and checking the **Document Log** message and the **Document Log Summary** page. In many cases, it may be preferable to run a batch check of all relevant documents to get a quick overview of what documents require your attention. When you use the **Document Control Log** to run a batch check:

* It performs a [hash check](@DC-154#hash-functions-for-document-capture) to find out if the documents have been modified after posting.
* It checks if any attachments have been modified between approval and posting.
* It validates if any drag-and-drop attachments have been deleted after posting.

It then includes all documents that meet the defined filter criteria in a color-coded list, where documents that have failed one or more of the checks are written in red. This makes it easier and more likely for you to identify documents that have been handled incorrectly – and to take action to resolve any issues. By using the **Document Control Log**, you don't have to manually navigate to each individual posted document and its **Document Log Summary** page to reactively find out about any potential issues. Instead, you can call up a list whenever it suits you.

The list of documents displayed on the **Document Control Log** page includes a number of columns with relevant document details, as well as a number of columns relating to the document checks:

<br>

| Column | Description |
| --- | --- |
| **Check Failed** | Specifies if the document has failed a check. If it says **Yes**, the text in both this column and the **Last Check Performed** column turns red. |
| **Last Check Performed** | Specifies when the latest check was carried out. When you select **Perform Document Checks** on the action bar, this date is updated. |
| **Check Fail Message** | Specifies how the document failed the check. This is the same message as the one that's displayed under **Document Log** on the **General** FastTab of the posted document. |
| **Failed Check Reconciled** | Specifies if a failed check has been reconciled, who did this, and when it was done. When you select **Reconcile** on the action bar, the text in this column is updated and the text in the **Check Failed** and **Last Check Performed** columns switches from red to black. |

## To perform a batch check

To perform a batch check and define a filter for which documents to check:

1. Search ({{search}}) for and select **Document Control Log**.
1. To carry out a batch check, click **Perform Document Checks** on the action bar. This opens the **Edit - Create Control Log Entries** page.
1. To narrow down the number of documents you want to perform the check for, you can apply a filter. Under **Show results**, the following fields are displayed as a default filter combination:
   * **Posting Date**
   * **Vendor Posting Group**
   To filter on different fields, select each field to open a dropdown menu with all available fields and select the field(s) you want to filter on.
1. To add a filter field, click **Add Filter** and select a filter from the list.
1. To the right of each selected field, under **Enter a value**, enter the value you want to use as a filter.
   > [!TIP]
   > For example, for the **Posting Date** field, you could enter **0101..T** to display documents that were posted between January 1 of the current year and today's date.
1. **Optional**: Performing the check may take a long time if you have many documents. To schedule the process for later to avoid interruptions in your workflow, click **Schedule** to open the **Edit - Schedule a Report** page, then pick an appropriate time. Click **OK** to close the page.
1. Click **OK** to perform the check and return to the **Document Control Log** page.

The check is carried out and a list of documents is generated. If you selected **Schedule** in step 6 above, the check is performed at the selected time.

## To find more information about list entries

You can find additional information for each of the entries in the list on the **Document Control Log** page. To do this:

1. Follow the guide above under [To perform a batch check](#to-perform-a-batch-check) to generate a list of documents.
1. To view the history of a listed document in terms of when it has been checked using the **Perform Document Checks** action: 
   1. Select the document whose check history you want to view. 
   1. On the action bar, click **Control Log Entries** to open the **View - Document Control Log Entries** page.
   1. Click **Close** when you're done to close the page and return to the **Document Control Log** page.
1. To view all other entries relating to a document in the list:
   1. Select the document whose related entries you want to view.
   1. On the action bar, click **Find Entries** to open the **Edit - Navigate** page.
   1. Select the entries that you want to view, and navigate back to the **Document Control Log** page when you're done.
1. To open the **Document Log Summary** page that you'd otherwise access from the document card of the posted document:
   1. Select the document whose **Document Log Summary** you want to view.
   1. On the action bar, click **Document Log Summary**.
   1. When you're done, click **Close** to return to the **Document Control Log** page. 

## To filter the list and reconcile failed documents

Using the **Reconcile** action, you can acknowledge that you've been informed about a failed check and that you've looked into it. When you reconcile a failed document, it's excluded from any future checks and is longer marked as failed (i.e.: formatted in red). If necessary, you can easily unreconcile a reconciled document using the same action.

It's also possible to filter the list to display only failed documents formatted in red or toggle back to displaying all documents.

To reconcile or unreconcile documents and/or filter the list to display only failed documents:

1. Follow the guide above under [To perform a batch check](#to-perform-a-batch-check) to generate a list of documents.
1. In the list of documents, select the one you want to reconcile/unreconcile. 
1. On the action bar, click **Reconcile**.
1. To display only failed documents formatted in red, click **Show Failed Lines** on the action bar. To display all documents, click it again.
