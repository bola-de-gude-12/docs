---
title: Using Document Search in Document Capture
date: 30-06-2025
description: How to search for documents in Document Capture.
id: DC-475
lang: en
---

# Using Document Search

The Document Search functionality in Continia Document Capture allows you to find documents based on one or more keywords. These keywords may be values that were recognized, automatically translated, or even manually entered by a user – including G/L accounts, approval flow codes, formula results, etc – in documents and XML files.

## To use Document Search
1. Search ({{search}}) for and select **Document Search**.
2. On the **Document Search** page, enter the desired keywords in the **Find What** field.

>[!NOTE]
>The search results appear as soon as you move on from the Find What field or click Search on the action bar, but you can refine the results by configuring the other fields.

3. In the **Search Mode** field, define how the desired keywords should be searched.
   * **Must contain all words** - only results that include all the keywords are shown. I.e.: if you enter 'freight shipping delivery' in the **Find What** field, Document Capture searches for 'freight AND shipping AND delivery'.
   * **Must contain at least one word** - results that include any of the keywords are shown. I.e.: if you enter 'freight shipping delivery' in the **Find What** field, Document Capture searches for 'freight OR shipping OR delivery'.
4. **Optional**: in the **Document Category** field, select the document category where the search should take place.

To see further information on a search result, select it and, on the action bar, click one of the following:

* **Show Document Card** - opens the document card of the selected document.
* **Show File** - opens the related document using your default application associated with the file type.
* **Show Incoming Email** – opens the email containing the PDF or XML file used to create the document.
* **Find Entries** – opens the document created when the original document was registered, as long as the new document is unposted. If the new document has been posted, it’s handled by standard Business Central instead.
