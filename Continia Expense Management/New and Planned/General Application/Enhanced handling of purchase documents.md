---
title: Enhanced Handling of Purchase Documents Processed by Other Solutions
date: 22-10-2024
description:
id: EM-234
lang: en
---

# Enhanced Handling of Purchase Documents Processed by Other Solutions

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| Enhanced handling of purchase documents processed by other solutions | {{checkmark}} Sep 19 2024 | {{checkmark}} Oct 2024 |

## Business value

With this new feature, customers that use both Document Capture and Expense Management will be able to process the same purchase in both solutions: Document Capture for ease of purchase processing and for OCR capabilities and Expense Management for refunds.

## Feature details
This feature will make it possible to apply a purchase to an expense, making sure that Expense Management will no longer generate the purchase side of the transaction. Expense Management will then only process the payment and refund the user. 

Several checks will be carried out across the application to ensure that admins are made aware when similar purchases have been made, preventing possible errors in the form of double postings. The functionality is only available when cloud OCR is enabled in Document Capture.

For more information, refer to the [Processing Purchase Invoices across Expense Management and Document Capture](@EM-277) article.