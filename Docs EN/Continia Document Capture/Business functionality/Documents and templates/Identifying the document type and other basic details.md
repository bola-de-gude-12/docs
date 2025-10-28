---
title: Identifying the Document Type and Other Basic Details 
date: 08-06-2023
description: A description of how Document Capture attempts to identify certain basic details for each incoming document, including currency, document type, due date, salesperson/purchaser, G/L account, and other account types. 
id: DC-146
lang: en
---

# Identifying the Document Type and Other Basic Details

When an imported [document has been OCR-processed](@DC-145) and a [document source (such as a vendor) has been assigned](@DC-109) either automatically or manually, Continia Document Capture will try to automatically identify the document type and a number of other fundamental document details. The details to be identified depend on the overall document category. For the purchase category, the details that Document Capture will attempt to identify are the following:

* Currency
* Document type
* Due date
* Salesperson/purchaser
* G/L account and other account types, if relevant

If Document Capture fails to identify any of these details, you'll have to enter them manually yourself.

Note that for illustrative purposes, this article will be based on invoices imported in the purchase category. Much of the information and all of the underlying principles also apply to other categories and document types though.

## Identifying the document type

To identify the document type, Document Capture checks the first page of the imported document for any captions that may signify a document type (such as the words *invoice* or *credit memo*). If it identifies one or more relevant captions, it picks the one with the highest position on the page. So if, for example, the word *Invoice* is located vertically higher than any other identified captions, the document is identified as an invoice.

> [!NOTE]
> This method differs from the standard method of identification: For other template fields, the caption length (that is, the number of characters in each identified caption) determines the recognition order.

Even if it says *Credit Memo* immediately below the word *Invoice*, the document will by default be regarded as an invoice. However, it's possible to change this default behavior by setting up Document Capture to prioritize credit memos over invoices during recognition. To do this, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. To open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself), and then select **Edit** on the action bar.
1. On the **Templates** FastTab, in the list of templates, select the template that you want to edit, and then select **Edit** to open the template card.
1. On the **Purchase Documents** FastTab, enable **Prioritize Credit Memo as Document Type**.

With this setting enabled, Document Capture will identify any imported document that uses this template and includes the text *Credit Memo* (or similar) as a credit memo, even if the word *Invoice* is located higher than *Credit Memo* in that document.

## Identifying other basic details

**To identify the currency**, Document Capture initially searches for a currency code in the imported invoice. If no such code is present in the document, it checks if there's one on the vendor card. In case no currency code is found here either, Document Capture uses the local currency (LCY), provided that this has been defined in the **General Ledger Setup**.

**To identify the due date**, Document Capture searches for it in the imported invoice. If this fails, it creates a due date based on the vendor's payment terms combined with the posting date that's typically included in the document.

**To identify the salesperson/purchaser**, Document Capture checks the **Our Contact** field of the imported invoice. If this is empty, it searches for an order number in the invoice and then fetches the salesperson/purchaser code from the related purchase order, if present.

**To identify the G/L account number and any potential other account codes**, Document Capture checks if any rules have been set up in **Accounts for Amounts**. Using this setup, Document Capture may be able to apply codes for G/L accounts, items, resources, fixed assets, item charges, [amount distribution codes](@DC-118), and/or [purchase contracts](@DC-85).

## Related information

[Set Up Currencies](https://learn.microsoft.com/en-us/dynamics365/business-central/finance-set-up-currencies) (Microsoft article)  
[Working with Paper and PDF Documents](@DC-71)  
[Capturing Fields in a Document](@DC-110)  
[Purchaser Code Translation](@DC-128)  