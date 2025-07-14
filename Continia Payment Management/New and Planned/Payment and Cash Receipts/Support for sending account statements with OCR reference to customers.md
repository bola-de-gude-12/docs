---
title: Support for sending account statements with OCR reference to customers
description: Support for sending account statements with OCR reference to customers, making it possible to identify and match the payments in Business Central
date: 01-03-2022
id: PM-80
lang: en
---

# Support for Sending Account Statements With OCR Reference to Customers

| Feature | General availability online | Public preview |
| --- | :-: | :-: |
| Support for sending account statements with OCR reference to customers | Oct 2023 | - |

## Business value

When sending account statements to customers, with a summary of all account activity, such as invoices sent, payments received, and charged fees, over a given period, each statement is generated with an OCR reference. Using the OCR a corresponding reference number on the statement lines will be generated in Business Central, making it possible for Payment Management to automatically match the payments to the associated invoices and credit notes in the cash receipt journal, when the customer payments are imported to the journal.

## Feature details

This feature will generate an OCR reference number on the customer account statements. The reference will then be used by Payment Management to match the customer payments when these are imported to the cash receipt journal.  