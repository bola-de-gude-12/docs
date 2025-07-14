---
title: Expense Management Secure Archive
date: 20-05-2025
description: Secure and preserve your documents in their original form
id: EM-189
lang: en
---

# Secure Archive

With Secure Archive, you can secure all digital documents that your organization uses for bookkeeping purposes, documents which are processed using Document Capture/Expense Management, and preserve them in their original form. This safeguards against accidental deletion or modification. In full compliance with local and national legislation, all of your archived documents will be fully traceable throughout the archive period that you define. Moreover, the built-in logging functionality automatically records every step in processing the documents, from initial receipt to final posting.

If you're only interested in the logging functionality, you can enable this as a stand-alone feature independent from the Secure Archive. By doing so, you'll have the processing of all Microsoft Dynamics 365 Business Central documents tracked and logged automatically – not just the documents processed by Continia's solutions – without any of the minor restrictions that come with the Secure Archive.

For information on how to set up the Secure Archive/the logging functionality, see [Setting up the Secure Archive](@EM-190).

> [!NOTE]
> Secure Archive is available for both the Continia Document Capture and Continia Expense Management solutions. This article covers both.

With Secure Archive, Document Capture and Expense Management have achieved certification in Germany as audit-compliant document management systems ("AC-DMS ready"). Known in Germany as "PK-DML ready", this certification has served as the standard for legally compliant and audit-proof management of electronic documents for more than two decades. You can find the actual certificate awarded to Continia here: [VOI Compliance Certificate](https://partnerzone.blob.core.windows.net/articles/docs/dc/CERT_Urkunde_Continia_1.pdf).

## The scope of the archive

Secure Archive stores purchase documents that have been processed by Document Capture/Expense Management and which are eventually posted and used for bookkeeping. This includes, but is not limited to, supplier invoices, supplier credit memos, scanned purchase documents, downloaded electronic documents, employee expense attachments received by email, and documents dragged into Document Capture or Expense Management.

> [!IMPORTANT]
> The archive does *not* cover documents that are processed in Business Central outside of Document Capture or Expense Management. For Document Capture, only the **PURCHASE** document category is covered, whereas no such restrictions apply to Expense Management.
> 
> For Document Capture, you must register your purchase documents by creating invoices or credit notes (or using order matching) to be able to use the Secure Archive. You can't use it if you register your documents in journals.

### Storage of document data 
Continia recommends using the Business Central SQL database, which provides state-of-the-art security and document protection. However, the security setup of the SQL database is outside the control of both Document Capture and Expense Management. For advice, reach out to your Business Central partner.

If your organization has chosen to host your document archive outside its database, using local file storage or Azure Blob Storage for example, storage security is the sole responsibility of your organization. Commonly this sort of hosting is due to company policies or storage space limitations. 

## Key features

One of the main features of Secure Archive is that it blocks users from deleting any of the documents that are stored in the archive. This means that the standard Business Central purchase setting **Allow Document Deletion Before \<DATE\>** can't be used within the archive period that you've defined.

Another important feature is that Secure Archive ensures the originality of each document that's stored in the archive. It does so via secure hash functions, which you can read more about in the section Using hash functions

Document Capture has a soft-delete feature so if you realize that something isn't right with one of your documents (poor scan quality for example), you can delete it. However, this doesn't delete the document entirely; Although it appears to be deleted, Secure Archive keeps it behind the scenes, so it is still fully accessible from there.

> [!NOTE]
> This soft-delete feature is only available for Document Capture, not for Expense Management.

If you want to add a document after posting (a better scan, for example), you can do so. However, the new document will be marked **Added after posting** to clearly indicate that it's not the original document.

Secure Archive also provides full backward traceability: From any given entry in **General Ledger Entries** and **Vendor Ledger Entries**, you can use **Find entries** to trace the original document as you received or scanned it, including all metadata such as sender email and time stamps. This traceability is retained even when you split or merge documents.

When Secure Archive is enabled, any file that's imported with Expense Management is converted into a PDF that's digitally signed. The original file is also kept in the archive. File signing takes place in the following situations:

* When you upload the file using the Expense Portal or the Expense Mobile App, as long as **Sign Documents** was previously enabled and synchronized with Continia Online.
* When the file is uploaded from within Business Central and **Sign Documents** was enabled in the setup.

## Using hash functions

To optimize security and ensure document originality, hash functions are used for both Document Capture and Expense Management, but in slightly different ways. The hash functionality of each of the solutions is described in the following two sections.

### Hash functions for Document Capture

Every document that's imported using Document Capture, either through the **PURCHASE** category or by being dragged into Document Capture, automatically gets a hash associated with it (SHA1). This hash will be recalculated if the imported document is split or merged, if pages in the document are rotated, or in case the order of any document pages is changed. The recalculated hash value will then replace the original hash value and form a new basis for comparison – a new original, so to speak.

When you post a document, the hash values of all attached documents are calculated again and checked against the original hash values. If they don't match, the posting will be rejected. In such cases, you must delete all documents and start over again. This deletion is recorded in the log, together with all other document activity.

When you open a posted document, the hash values are calculated anew and again checked against the original hash values. If they don't match, it is clearly indicated under **General** > **Document Log**, where the following text is displayed in red: "One or more documents have been changed after posting!". You can select this text to open the **Document Log Summary**, which then shows which documents have been altered.

If the original and the newly calculated hash values *do* match, **Document Log** will display a message with the number of document log entries – for example, **2 Document Log Entries** – instead of the red warning message mentioned above. If you click this message to open the **Document Log Summary**, the **File Hash Check** column will read **OK** to indicate that there's a perfect match between the original and the current hash values, meaning that the documents are unchanged and haven't been tampered with in any way.

### Hash functions for Expense Management

As with Document Capture, every document that's imported using Expense Management, be it manually in Business Central or downloaded via synchronization with Continia Online, will have a hash associated with it (SHA1). Secure Archive uses such hash values as a basis for comparison to ensure incoming documents remain unchanged throughout the process until posting.

When you post a document, the hash values of all attached documents are again calculated and checked against the original hash values. If they don't match, the posting is rejected, and an error message displays along with an error comment in the **Comments** section. In such cases, you must delete all documents and start over again. This deletion is recorded in the log, along with all other document activity.

## The log functionality

The log functionality automatically logs the activity of all documents in Business Central (not just the documents processed by Document Capture/Expense Management) from the moment they enter the system until they're posted. For the documents that are processed by one or both of Continia's solutions, there are certain differences between the two solutions in terms of what's logged. The following two sections provide an overview of the logged activity for Document Capture and Expense Management respectively:

### Logged activity for Document Capture documents

| Activity | Description |
| --- | --- |
| Received | A log entry is added whenever a document is imported and when a document is deleted before import. The entry contains the **From** email address and the name of the file in the incoming email. |
| Deleted before import | A log entry is added when a document is deleted from the **Ready to Import** page. |
| Imported | A log entry is added when a new document is created during the import process or by being dragged into Document Capture. |
| Deleted | A log entry is added when a document is deleted. |
| Split | A log entry is added when a document is split into multiple documents. |
| Merged | A log entry is added when one or more documents are merged into one. | 
| Registered | A log entry is added when a document is registered. The entry specifies what standard document (invoice/credit memo) the Document Capture document is registered as. |
| Posted | A log entry is added when a standard document created from a Document Capture document is posted. The log entry includes details regarding the number of the posted document. |

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

[Setting up the Secure Archive](@EM-190)  








<style>
  .content table tr td:nth-child(1) {
    width: 160px;
  }
  .content table tr td:nth-child(2) {
    width: 570px;
  }  
</style>