---
title: Matching bank account ledger entries by posting date and amount
description: Matching bank account ledger entries by posting date and amount
date: 25-03-2025
id: CB-215
lang: en
---
# Matching bank account ledger entries by posting date and amount

| Feature                                                      | General availability online | Public preview         |
| ------------------------------------------------------------ | --------------------------- | ---------------------- |
| Matching bank account ledger entries by posting date and amount | {{checkmark}} Apr 2025      | {{checkmark}} Mar 2025 |

## Business Value

This feature simplifies the bank account reconciliation process by automatically matching statement lines with existing bank account ledger entries based on the transaction date and statement amount. 

## Feature Details

When reconciling a bank account, users now have the option to search for bank account ledger entries using the transaction date and statement amount from the statement line. This feature matches entries where both the posting date and amount are identical to the statement line.

This setting can be enabled on the [Banking Import Setup](@CB-14) page and ensures that only exact matches based on both the date and amount are identified.