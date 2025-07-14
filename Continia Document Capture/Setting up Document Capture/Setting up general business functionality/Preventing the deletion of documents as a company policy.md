---
title: Preventing the deletion of documents as a company policy in Document Capture
date: 16-06-2025
description:  
id: DC-477
lang: en
---

# Preventing the deletion of documents as a company policy
Importing documents into Continia Document Capture can occasionally result in unwanted documents making their way into the system. Typical examples of this include:

* Documents that weren’t scanned correctly and therefore need to be rescanned.
* Documents that don’t belong in Document Capture, for example if an account statement (instead of a purchase invoice) is sent to the email address used for importing purchase documents into Document Capture.

It’s a good idea to get rid of such unwanted documents from time to time. By default, there are two ways of doing this:

* **By deleting the documents** - the document journal allows you to delete any unwanted documents. This will remove them completely from the database, making it impossible to retrieve them again.
* **By rejecting the documents** - in the document journal, you also have the option of rejecting the documents. This will keep the documents in the database but set their status to **Rejected**, meaning that you can still retrieve the documents, if necessary.

The benefit of deleting a document is that it doesn’t take up space, as it’s removed completely. The obvious disadvantage is that you’re then unable to retrieve it again. Rejected documents, on the other hand, are still retrievable after rejection but have the disadvantage of taking up storage space.

By default, Document Capture allows documents to be deleted. However, you can configure it to prevent the deletion of documents by setting up a document deletion policy. This may be useful if, for example, your company’s overall policy is to keep all documents in the database no matter how they got there in the first place.

To set up a document deletion policy, follow these steps:
1. Search ({{search}}) for and select **Document Categories**.
1. Open the relevant document category. For example, to open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself, as this opens the document journal), and then click **Edit** on the action bar.
1. On the **General** FastTab, either enable or disable **Allow Deleting Documents**, depending on what you want your document deletion policy to do.

> [!NOTE]
> Documents that have already been registered in Document Capture can’t be deleted, no matter if you’ve set up a document deletion policy or not.

## Related information
[Rejecting documents](@DC-478)