---
title: Support for reconciling employee payments in the bank account reconciliation
description: Information about the feature for reconciling employee payments in the bank account reconciliation
date: 01-10-2021
id: PM-190
lang: en
---

# Support for Reconciling Employee Payments in the Bank Account Reconciliation

| Feature | General availability on-premises | General availability online | Public preview |
| --- | :-: | :-: | :-: |
| Support for reconciling employee payments in the bank account reconciliation | {{checkmark}} Sep 1, 2021 | {{checkmark}} Oct 1, 2021 | - |

## Business value

Using employee reconciliation rules, you can specify one or more search rules for Payment Management to insert an employee number for unidentified bank statement lines. This will ease the process of identifying a match in the employee ledger entries.

## Feature details

With Statement Intelligence, Payment Management will automatically try to match payments by using the payment's unique payment reference ID which is created for all payments processed from the payment journal with Payment Management. If a payment has not been processed from the payment journal, the unique payment reference ID can't be used for matching the bank statement lines, in which case other parameters such as date and amount will be used. If a unique match can't be found the reconciliation rule will be applied in order to identify a match. When a rule has been met, the employee number will be inserted on the statement line, and you will be able to select and apply the matching employee ledger entries. For more information, see [Set up employee reconciliation rules](@PM-188).

This feature is available from Payment Management version 3.0.0.0.

