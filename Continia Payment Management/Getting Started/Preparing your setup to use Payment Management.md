---
title: Preparing your setup for Payment Management
date: 12-01-2023
description: Checklist to get ready for Payment Management
id: PM-311
lang: en
---

# Preparing your setup for Payment Management
To make it easier to start working with Payment Management, see the following checklist:

| Area                        | Make sure to:                                                |
| --------------------------- | ------------------------------------------------------------ |
| BC setup                    | Make sure to use bank accounts.<br />Set up an ending number on all number series related to the bank module (payment journal, cash receipt, reconciliation, and so on.) |
| Bank account ledger entries | [Close and reconcile all bank account ledger entries](@PM-163) in BC up to a date that is close to the PM implementation date. |
| Vendor bank account setup   | Make sure that the [vendors contain the following information](@PM-85): Payment Method, Bank, Master data, Branch number, Account number, IBAN, and Swift. |
| Bank accounts               | Make sure that all bank accounts contain master data, branch number, account number, IBAN and so on.</br> For some direct communication connections such as Bizcuit to allow multiple approvers, you must have the required permissions in the bank environment. |
| Bank agreement              | Create a bank agreement with the bank related to direct data exchange through API.<br />Order or set up recurring reconciliation and cash receipt files from the bank (CAMT 53 and CAMT 54). See the [Bank integration](@PM-98) article for more information. |

