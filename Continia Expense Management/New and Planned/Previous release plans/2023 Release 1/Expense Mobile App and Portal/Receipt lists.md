---
title: Receipts List
date: 22-05-2023
description: Share documents and attach receipts
id: EM-156
lang: en
---

# Receipts List

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| Receipts List | - | June 2023 |

## Business value
The Receipts Lists feature replaces the Saved Images List features, making it possible to add documents, for example, PDF files, to the Continia Expense App. Additionally, when you send and share receipt documents to the Continia Expense App, AI Receipt Scanning is performed.

## Feature details
The Receipts List feature makes it easy for users to share documents from any app with the Continia Expense App. For example, users can share a PDF file from the email app they use and select the Expense App as the target. 

With the Receipts List feature, we now also help the user in the following scenarios:

* The user shares a receipt document to the Continia Expense App:

  * if the expense exists, and the document AI Receipt Scanning values match, the user will be prompted to attach the receipt to the existing expense.
  * If the expense does not exist or the document AI Receipt Scanning values do not match, the document will be added to the Receipts List for further handling.
  * if the receipt document already exists, the user will receive a warning message indicating the receipt document is already present.

* The user creates a new expense in the Continia Expense App:

  * if the user attempts to add a new photo of the receipt, but a matching receipt document is already present in the Receipts List, the user will be prompted to attach the existing receipt document.
  * if the user creates a new expense from the receipt document and a matching expense already exists, the user will be suggested to attach the receipt to the existing expense.
  * if the receipt document does not match the values on the expense, the user will receive a warning message indicating a mismatch between the receipt document and expense values. 

  