---
title: Setting up company identification texts in Document Capture
date: 15-10-2025
description: How to to set up company identification texts in Document Capture.
id: DC-443 
lang: en
---

# Setting up company identification texts
Company identification texts are used when you only have one email address for receiving documents and would like these documents to be moved automatically to other companies once you’ve imported them. Most organizations use a separate email address for each company, which means that they don’t have to move documents automatically using company identification texts. For more information, see [Moving a document to another company](@DC-74).

When you use company identification texts, you basically tell Continia Document Capture to automatically move any document that contains a specific text specified by you. Each document that contains the specified text will be moved to a company whose name you’ve mapped to this particular text. You can set up multiple company identification texts that all point to the same document. For example:

1. You have a company in Microsoft Dynamics 365 Business Central called **CRONUS Holding**. However, CRONUS Holding also has the two registered aliases **CRONUS Capital** and **CRONUS Invest**. Different vendors use different names when they send you invoices, but all documents should be moved to **CRONUS Holding**.
1. You have another company in Business Central called **CRONUS Distribution**. However, CRONUS Distribution also has the registered alias **CRONUS Wholesale**. Different vendors use different names when they send you invoices, but all documents should be moved to **CRONUS Distribution**.

In a scenario like this, you could use company identification texts and map them to the two companies as follows:

| Company name | Company identification text |
| --- | --- |
| CRONUS Holding | CRONUS Holding |
| CRONUS Holding | CRONUS Capital |
| CRONUS Holding | CRONUS Invest |
| CRONUS Distribution | CRONUS Distribution |
| CRONUS Distribution | CRONUS Wholesale |

> [!NOTE]
> Avoid using identification texts that aren’t unique to the company that you want to move documents to. Using a company identification text such as CRONUS wouldn’t serve the purpose, as it would be impossible for Document Capture to determine whether documents containing this text should be moved to CRONUS Holding or CRONUS Distribution.

## To set up company identification texts
To set up company identification texts, you must have two or more companies set up in Business Central – and Document Capture must be activated and set up in all of these.

To set up company identification texts:

1.	Search ({{search}}) for and select **Company Identification Texts**.
1.	On the action bar, click **New**.
1.	A new line is added to the table. In the **Company Name** column, select the company that you want to move incoming documents to.
1.	In the **Identification Text** column, enter a text that uniquely identifies the selected company in the incoming documents.
1.	Repeat steps 2-4 for every company identification text that you want to use.

When you’ve entered the number of company identification texts you need, you must enable automatic transfer of documents for each of the document categories in which documents should be moved automatically upon import. To do this, see [Moving documents to other companies automatically](@DC-74#moving-documents-to-other-companies-automatically).
