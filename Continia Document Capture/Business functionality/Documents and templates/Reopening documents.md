---
title: Reopening documents in Document Capture
date: 20-03-2025
description: How to reopen most registered or rejected documents in Document Capture.
id: DC-442
lang: en
---

# Reopening documents
It's possible to reopen most registered or rejected documents. This is useful if, for example, you would like to either match a document again or correct any document-recognition errors – or if you rejected a document by mistake.

Note that not all types of documents support reopening, and that some documents can’t be reopened after being posted.

> [!NOTE]
> You can only reopen a purchase invoice or credit memo if it hasn’t been posted yet. If a document has already been posted, you may want to use the standard Microsoft Dynamics 365 Business Central functionality to correct or cancel it. However, if a purchase invoice or credit memo hasn’t been posted yet, Continia Document Capture deletes the document from the standard purchase tables and reopens it, thereby enabling you to work with it in the document journal or on the document card.

To reopen a document:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the code of the relevant document category – for example, **PURCHASE** – to open the document journal.
1. In the upper-right corner, above the action bar, go to **Status Filter** and select the box to display the filter options. Select **Registered** or **Rejected**, depending on what types of documents you want to view.
1. The document list is filtered to display only the selected type of documents. In the list, select the document that you want to reopen. Select the document line – not the number in the **No.** column, as this opens the document card.
1. On the action bar, click **Process** and then **Reopen**.
1. To find the reopened document, go to **Status Filter** in the upper-right corner and select **Open** to display all open documents in the document list. Your reopened document should now be in the list.