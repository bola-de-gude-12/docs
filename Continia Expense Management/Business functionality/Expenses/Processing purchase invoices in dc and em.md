---
title: Processing Purchase Invoices in Document Capture and Expense Management
date: 17-03-2025
description: Learn how to avoid duplicate postings in EM and DC.  
id: EM-277
lang: en
---

# Processing Purchase Invoices in Document Capture and Expense Management

Customers using both Document Capture and Expense Management can now streamline their workflow by processing the same purchase in both solutions. Document Capture offers an easy way to process purchases and utilize Optical Character Recognition (OCR), and Expense Management handles payment processing and refunds. 

The integration of Document Capture and Expense Management ensures that after Document Capture processes a purchase, Expense Management manages only the payment and refund. This avoids a duplicate purchase transaction being generated. Built-in checks across the applications alert you if similar purchases are detected, avoiding double postings.

For a quick overview, watch the following video.
<iframe src=https://player.vimeo.com/video/1020171075?h=ad9b32a8ca&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479 width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media" title="EM_Process invoices with DC"></iframe>

## Processing purchase invoices across both solutions
To process a purchase invoice in Document Capture and Expense Management:

1. In Business Central, open Expense Management.
1. Search {{search}} for **Expenses**, and choose the related link. 
1. If an invoice is detected, a comment will appear automatically. The system identifies the document as an invoice, based on OCR data extracted by the Expense App and the Expense Portal, then synchronizes the document with Business Central.
1. Send the invoice to Document Capture. On the action bar select **Home** > **Process with Document Capture**. 
1. After OCR processing, the document is ready to be imported in the same way as any other DC document: in the **Documents for Import** queue. For more information, see [Registering Documents in Document Capture](@DC-67).
1. Continue the approval process for the expense in Expense Management, then post the expense. 
1. In Document Capture, on the **Posted Purchase Invoice** page, use the **Find Entries** feature to confirm the invoice was only processed once and handled jointly as both a Document Capture invoice and an expense in Expense Management. Alternatively, you can go to the **Posted Expenses** page in Expense Management. 

The user will be reimbursed after the Document Capture document and its associated invoice are posted.

## Understanding image to PDF conversion

You can automatically convert image-based invoices to PDFs for seamless integration with Document Capture.

When you process expenses and select **Process with Document Capture**, supported image-format documents automatically convert to a PDF before they're sent to Document Capture. This results in a more efficient and accurate invoice processing experience.

## See also
[Posting expenses](@EM-11)