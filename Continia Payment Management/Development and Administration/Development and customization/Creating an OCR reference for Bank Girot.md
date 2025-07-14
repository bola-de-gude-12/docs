---
title: Create an OCR reference for Bankgirot
description: A guide on how to use the OCR reference
date: 01-10-2024
id: PM-323
lang: en
---

# Creating an OCR reference for Bankgirot

An OCR (Optical Character Recognition) number is a specially formulated reference number that is usually found at the bottom of a payment advice slip. Its purpose is to identify the payer and the payment. Bankgirot uses OCR as a means of transaction security and risk management.

> [!IMPORTANT]
>
> This feature is only available in Payment Management (SE).

You can use Payment Management's OCR reference interface to create BankGirot OCR-strings to use for reports on, for example, invoices. Every time you print or send an invoice to the customer, the Bankgirot OCR is on the invoice, and the customer can use it as a payment method.

To set up the OCR type for Bankgirot:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Sales & Receivables Setup**.
2. On the **General** FastTab, navigate to the **Payment Reference Type** field, and from the drop-down box, select *Bank Giro*.  
3. Use the ![Search for page or report](/images/search_small.png) icon and search for **Reports Layouts**.
4. On the **Report Layouts** page, in the search box, enter 1306 and select the *StandardSalesInvoicewithOCR.docx* layout.
5. Run the report and verify that the OCR reference is created.
