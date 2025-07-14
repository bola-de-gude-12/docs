---
title: Document Control Log
date: 18-04-2024
id: DC-212
lang: en
---

# Document Control Log

The logging functionality of [the Secure Archive](../../../Continia%20Document%20Capture/Business%20functionality/General%20business%20functionality/@DC-154/) automatically records every step in the processing of documents that have been imported into and processed by Continia Document Capture and/or Continia Expense Management. When any such documents are posted, a message is displayed on the **General** FastTab of the document card, under **Document Log**, indicating the number of log entries. If any changes have been made to a document at some point after it has been approved and/or posted, a red warning message will be displayed here instead to indicate that someone has somehow modified the document and/or its attachments.

You can always view the status of an individual posted document by opening its document card and checking the **Document Log** message and the **Document Log Summary** page. But in many cases it may be preferable to run a batch check of _all_ relevant documents instead, to get a quick overview of what documents require your attention. This kind of overview is exactly what the **Document Control Log** provides. When you use it to run a batch check, it carries out the following checks for all documents as filtered by you:

* It performs a [hash check](../../../Continia%20Document%20Capture/Business%20functionality/General%20business%20functionality/@DC-154/#hash-functions-for-document-capture) to find out if the documents have been modified after posting.
* It checks if any attachments have been modified between approval and posting.
* It validates if any drag-and-drop attachments have been deleted after posting.

It will then include all documents that meet the defined filter criteria in a color-coded list where documents that have failed one or more of the checks are written in red. This makes it both easy and more likely for you to identify documents that have been handled incorrectly, and to take action to resolve any issues. So by using the **Document Control Log**, you don't have to manually navigate to each individual posted document and its **Document Log Summary** page to reactively find out about any potential issues. Instead you can easily and proactively call up a list whenever it suits you.

The list of documents displayed on the **Document Control Log** page includes a number of columns with relevant document details as well as a number of columns relating to the document checks:

\


| Column                      | Description                                                                                                                                                                                                                                                                            |
| --------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Check Failed**            | Specifies if the document has failed a check. If it says **Yes**, the text in both this column and the **Last Check Performed** column will be red.                                                                                                                                    |
| **Last Check Performed**    | Specifies when the latest check was carried out. When you select **Perform Document Checks** on the action bar, this date wil be updated.                                                                                                                                              |
| **Check Fail Message**      | Specifies how the document failed the check. This is the same message as the one that's displayed under **Document Log** on the **General** FastTab of the posted document.                                                                                                            |
| **Failed Check Reconciled** | Specifies if a failed check has been reconciled, who did this, and when it was done. When you select **Reconcile** on the action bar, the text in this column wil be updated, and the text in the **Check Failed** and **Last Check Performed** columns will switch from red to black. |

## To perform a batch check

In order to perform a batch check and define a filter for which documents to check, follow these steps:

1. Choose the \{{search\}} icon, enter **Document Control Log**, and then choose the related link.
2. To carry out a batch check, go to the action bar and select **Perform Document Checks**. This will open the **Edit - Create Control Log Entries** page.
3. To narrow down the number of documents you want to perform the check for, you can apply a filter. Under **Show results**, the following fields are displayed as a default filter combination:
   * **Posting Date**
   * **Vendor Posting Group** If you want to filter on different fields, select each field to open a dropdown menu with all available fields, and then select the field(s) you want to filter on.
4. To add a new filter field, select **Add Filter**, and then select a filter from the list.
5.  To the right of each selected field, under **Enter a value**, enter the value that you want to use as a filter.

    > \[!TIP] For example, for the **Posting Date** field, you could enter **0101..T** to display documents that were posted between January 1 of the current year and today's date.
6. **Optional**: Performing the check may take a long time if you have many documents. In case you want to schedule the process for later to avoid interruptions in your workflow, select **Schedule** to open the **Edit - Schedule a Report** page, and then pick an appropriate time. Select **OK** to close the page.
7. Select **OK** to perform the check and return to the **Document Control Log** page.

The check will now be carried out, and a list of documents will be generated. If you selected **Schedule** in step 6 above, the check will be performed at the selected time.

## To find more information about list entries

You can find additional information for each of the entries in the list on the **Document Control Log** page. To do this, follow these steps:

1. Follow the guide above under [To perform a batch check](<Document control log.md#to-perform-a-batch-check>) to generate a list of documents.
2. To view the history of a listed document in terms of when it has been checked using the **Perform Document Checks** action, do as follows:
   1. Select the document whose check history you want to view.
   2. On the action bar, click **Control Log Entries** to open the **View - Document Control Log Entries** page.
   3. Select **Close** when you're done to close the page and return to the **Document Control Log** page.
3. To view all other entries relating to a document in the list, do as follows:
   1. Select the document whose related entries you want to view.
   2. On the action bar, click **Find Entries** to open the **Edit - Navigate** page.
   3. Select the entries that you want to view, and navigate back to the **Document Control Log** page when you're done.
4. To open the **Document Log Summary** page that you'd otherwise access from the document card of the posted document, do as follows:
   1. Select the document whose **Document Log Summary** you want to view.
   2. On the action bar, click **Document Log Summary**.
   3. When you're done, select **Close** to return to the **Document Control Log** page.

## To filter the list and reconcile failed documents

Using the **Reconcile** action, you can acknowledge that you've been informed about a failed check and that you've looked into it. When you reconcile a failed document, it will be excluded from any future checks and will no longer be marked as failed (formatted in red). If necessary, you can easily unreconcile a reconciled document using the same action.

It's also possible to filter the list to display only failed documents formatted in red. And you can easily toggle back to displaying all documents.

To reconcile or unreconcile documents and/or filter the list to display only failed documents, follow these steps:

1. Follow the guide above under [To perform a batch check](<Document control log.md#to-perform-a-batch-check>) to generate a list of documents.
2. In the list of documents, select the one you want to reconcile/unreconcile.
3. On the action bar, click **Reconcile**.
4. To display only failed documents formatted in red, select **Show Failed Lines** on the action bar. To display all documents, select it again.
