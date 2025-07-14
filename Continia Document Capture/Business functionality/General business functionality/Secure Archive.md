---
title: Secure Archive
date: 27-12-2024
description:  
id: DC-154
lang: en
---

# Secure Archive

With the Secure Archive, all digital documents that your organization uses for bookkeeping purposes and which are processed using Document Capture and/or Expense Management can be secured and preserved in their original form, so that no one accidentally deletes them or modifies them in any other undesirable way. In full compliance with local and national legislation, all of your archived documents will be fully traceable throughout the archive period that you define, and the built-in logging functionality automatically records every step in the processing of the documents, from initial receipt to final posting.

If you're only interested in the logging functionality, you can easily enable this as a stand-alone feature independent from the Secure Archive. By doing so, you'll have the processing of all Microsoft Dynamics 365 Business Central documents tracked and logged automatically – not just the documents processed by Continia's solutions – without any of the minor restrictions that come with the Secure Archive.

For information on how to set up the Secure Archive and/or the logging functionality, see [Setting up the Secure Archive](@DC-155).

> [!NOTE]
> The Secure Archive is available for both Continia Document Capture and Continia Expense Management. This article deals with both solutions.

With the Secure Archive, Document Capture and Expense Management have achieved certification in Germany as audit-compliant document management systems ("AC-DMS ready"). Known in Germany as 'PK-DML ready', this certification has served as the standard for legally compliant and audit-proof management of electronic documents for more than two decades. You can find the actual certificate awarded to Continia here: [VOI Compliance Certificate](https://partnerzone.blob.core.windows.net/articles/docs/dc/CERT_Urkunde_Continia_1.pdf).

## The scope of the archive

The Secure Archive stores purchase documents that have been processed by Document Capture and/or Expense Management and which are eventually posted and used for bookkeeping. This includes, but is not limited to, supplier invoices, supplier credit memos, scanned purchase documents, downloaded electronic documents, employee expense attachments received by email, and documents dragged into Document Capture or Expense Management.

> [!IMPORTANT]
> The archive does not cover documents that are processed in Business Central outside of Document Capture or Expense Management. For Document Capture, only the **PURCHASE** document category is covered, whereas no such restrictions apply to Expense Management.
> 
> For Document Capture, you must register your purchase documents by creating invoices or credit notes (or using order matching) in order to be able to use the Secure Archive. You can also use it when registering your documents in journals.

> [!WARNING]
> As regards the physical storage of document data, this is outside the control of both Document Capture and Expense Management. The Secure Archive does *not* protect your actual document files from modification or deletion, but it does ensure that you're notified of any such actions when you post or view a document. The prevention of any unauthorized access to your document files is the sole responsibility of your organization's IT department.

Due to company policies, storage space limitations, or for any other potential reasons, your organization may have chosen to host your document archive outside the database (for example, using local file storage or Azure Blob Storage). In such cases, storage security is the sole responsibility of your organization.

## Key features

One of the main features of the Secure Archive is that it blocks users from deleting any of the documents that are stored in the archive. This means that the standard Business Central purchase setting **Allow Document Deletion Before \<DATE\>** can't be used within the archive period that you've defined.

Another very important feature is that the Secure Archive ensures the originality of each document that's stored in the archive. It does so through the use of hash functions, which you can read more about below under [The use of hash functions](#the-use-of-hash-functions).

For Document Capture, if you realize that something isn't quite right with one of your documents (for example, the quality of the scanning is poor), you can mark it as deleted. This doesn't delete the document entirely though: Although it does indeed appear to be deleted on the face of it, it's actually kept in the Secure Archive behind the scenes, and it will be fully accessible from there.

> [!NOTE]
> This soft-delete feature is only available for Document Capture, not for Expense Management.

If you want to add a document after posting (a better scan, for example), you can easily do so. However, the new document will be marked **Added after posting** to clearly indicate that it's not the original document.

The Secure Archive also provides full backward traceability. From any given entry in **General Ledger Entries** and **Vendor Ledger Entries**, you can use **Find entries** to trace the original document as you received or scanned it, including all metadata such as sender email and time stamps. This traceability is retained even when you split or merge documents.

When the Secure Archive is enabled, any image file that's imported with Expense Management is converted into a PDF that's digitally signed. The original file is also kept in the archive. File signing takes place in the following situations:

* When you upload the file using the Expense Portal or the Expense App (mobile app), as long as **Sign Documents** has been enabled and synchronized with Continia Online.
* When the file is uploaded from within Business Central and **Sign Documents** has been enabled in the setup.

## The use of hash functions

To optimize security and ensure document originality, hash functions are used for both Document Capture and Expense Management, but in slightly different ways. The hash functionality of each of the solutions is described in the following two sections.

### Hash functions for Document Capture

Every document that's imported using Document Capture, either through the **PURCHASE** category or by being dragged into Document Capture, automatically gets a hash associated with it (SHA1). This hash will be recalculated if the imported document is split or merged, if pages in the document are rotated, or in case the order of any document pages is changed. The recalculated hash value will then replace the original hash value and form a new basis for comparison – a new original, so to speak.

When you post a document, the hash values of all attached documents are calculated again and checked against the original hash values. If they don't match, the posting will be rejected. In such cases, the only way forward is to delete all documents and start over again. This deletion will be recorded in the log, together with all other document activity.

When you view a posted document, the hash values are calculated anew and checked against the original hash values again. If they don't match, this will be clearly indicated on the **General** FastTab, under **Document Log**, where the following text will be displayed in red: "One or more documents have been changed after posting!". You can select this text to open the **Document Log Summary**, which will then show which documents have been altered.

If the original and the newly calculated hash values *do* in fact match, **Document Log** will simply display a message with the number of document log entries – for example, **2 Document Log Entries** – instead of the red warning message mentioned above. If you click this message to open the **Document Log Summary**, the **File Hash Check** column will read **OK** to indicate that there's a perfect match between the original and the current hash values, meaning that the documents are unchanged and haven't been tampered with in any way.

### Hash functions for Expense Management

As with Document Capture, every document that's imported using Expense Management, either when added manually in Business Central or if downloaded via synchronization with Continia Online, will have a hash associated with it (SHA1). The Secure Archive uses such hash values as a basis for comparison to ensure that incoming documents remain unchanged throughout the process until posting.

When you post a document, the hash values of all attached documents are calculated again and checked against the original hash values. If they don't match, the posting will be rejected, and an error message will be displayed along with an error comment in the **Comments** section. In such cases, the only way forward is to delete all documents and start over again. This deletion will be recorded in the log, together with all other document activity.

## The log functionality

For both Document Capture and Expense Management, the overall log functionality covers two different logging systems:

* The system log
* The document log

**The system log** automatically logs every change made to [the Secure Archive setup](@DC-155). So when a user configures any of the following setup settings, the changes are immediately logged in the system log:

* **Enable Secure Archive**
* **Document Activity Logging**
* **Archive Period Type**
* **Minimum Archive Period**
* **Sign Documents** (only applicable to Expense Management)

> [!TIP]
> You can access the system log from the **Document Capture Setup** and **Expense Management Setup** pages by selecting **Actions** > **Secure Archive** > **System Log**. The page that opens displays an unfiltered list of all setup changes.

**The document log** automatically logs the activity of all documents processed by Document Capture and/or Expense Management, from the moment they enter the system until they're posted. 

> [!TIP]
> You can access the document log in the following ways:
>
> * From the **Document Capture Setup** and **Expense Management Setup** pages: Select **Actions** > **Secure Archive** > **Document Log** to open the **Document Log** page, which displays an unfiltered list of all document activities.
> * From the document card: Select **Actions** > **Document** > **Document Log** to open the **Document Log** page, which displays a filtered list of activities relating to the selected document.
> * From a posted purchase invoice or credit memo: On the **General** FastTab, select the **Document Log** field to open the **Document Log Summary**, which displays a filtered list of activities relating to the Document Capture documents that are associated with the posted Business Central document.

There are certain differences between Document Capture and Expense Management in terms of what's logged in the document log. The following two sections provide an overview of the logged activity for Document Capture and Expense Management respectively:

### Logged activity for Document Capture documents

| Activity | Description |
| --- | --- |
| Received | A log entry is added when a document is imported and when a document is deleted before import. The entry contains the **From** email address and the name of the file in the incoming email. |
| Deleted before import | A log entry is added when a document is deleted from the **Ready to Import** page. |
| Imported | A log entry is added when a new document is created during the import process or by being dragged into Document Capture. |
| Deleted | A log entry is added when a document is deleted. |
| Split | A log entry is added when a document is split into multiple documents. |
| Merged | A log entry is added when one or more documents are merged into one. |
| Registered | A log entry is added when a document is registered. The entry specifies what standard document (invoice/credit memo) the Document Capture document is registered as. |
| Posted | A log entry is added when a standard document created from a Document Capture document is posted. The log entry includes details regarding the number of the posted document. |
| Reopened | A log entry is added when a registered document is reopened. |

### Logged activity for Expense Management documents

| Activity | Description |
| --- | --- |
| Received | A log entry is added when incoming documents (expenses, mileages, per diems, expense reports, or transactions) are downloaded from Continia Online or created in the Expense Management admin part of Business Central. |
| Attachments added/removed | A log entry is added when document attachments are added to or removed from expenses and mileages. |
| Duplicated transactions discarded at import | A log entry is added when a transaction is discarded because it has a duplicate ID. |
| Deleted | A log entry is added when a document is deleted. |
| Split | A log entry is added when an expense allocation creates a new expense. |
| Merged | A log entry is added when one or more expenses are merged into one. |
| Matched/unmatched | Log entries are added when expenses and transactions are matched and unmatched. |
| Added to/removed from Expense Report | A log entry is added when a document is added to or removed from an expense report. |
| Approved | A log entry is added when a document is approved. |
| Posted | A log entry is added when a document is posted. |
| Posted invoice or credit memo updates | A log entry is added when Expense Management generates a purchase invoice or credit memo. Important changes to these documents are logged. |

## Related information

[Setting up the Secure Archive](@DC-155)  








<style>
  .content table tr td:nth-child(1) {
    width: 160px;
  }
  .content table tr td:nth-child(2) {
    width: 570px;
  }  
</style>