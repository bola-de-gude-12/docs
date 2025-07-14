---
title: Direct Debit in Continia Banking
description: Introducing Direct Debit
date: 01-10-2024	
id: CB-129
lang: en
---

# Introducing Direct Debit

With Continia Banking Direct Debit, your company can collect payments in euros across various regions. This system supports both onetime and recurring payments, making it ideal for subscriptions. Direct Debit ensures no duplicate payments, includes eligible payment discounts, and groups entries to reduce file upload failures. For setup details, see [Setting up Direct Debit](@CB-130).

When payments are successfully processed, as communicated by your bank, you can post the payment receipts either directly from the Direct Debit Collect. Entries page or by moving the payment lines to the Continia Banking Direct Debit journal where you post payment receipts.

## How it's done

To manage Direct Debit collections similarly to how you work with the payment journal, Continia Banking has introduced a General Journal template. This template is automatically installed and uses the cash receipt format. This method distinguishes direct debit payments from other types of payments by using a unique page ID.

To facilitate suggesting the correct transactions for Direct Debit, Banking enhanced the SEPA Direct Debit Mandates page by adding the **Debit Counter** and **Closed** columns. When the Direct Debit collections reach the expected number of debits, the Debit Counter column value will match the number in the standard BC Expected Number of Debits column, and the system will select the Closed column to prevent further direct debit payment suggestions. 

## Requirements

The minimum requirements for setting up Direct Debit are:

* Supported banks - Commerzbank
* Pain.008 file upload only.
* Mandate ID - before you can collect payment by Direct Debit, your customer must issue you with a mandate that authorizes you to collect future payments.
* Transactions must be in euros.