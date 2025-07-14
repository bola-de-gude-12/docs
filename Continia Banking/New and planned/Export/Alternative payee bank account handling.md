---
title: Alternative Payee Bank Account Handling
description: Alternative Payee Bank Account Handling
date: 31-03-2025
id: CB-198
lang: en
---

# Alternative payee bank account handling

| Feature | General availability online | Public preview |
| --- | :-: | :-: |
| Alternative Payee Bank Account Handling |        {{checkmark}} Apr 2025        | {{checkmark}} Mar 2025 |

## Business Value

Supports cases where a centralized payer, such as a factor, needs to receive the payment instead of the original vendor.


## Feature Details

This feature enables specifying an alternative beneficiary bank account in cases where the vendor invoice is paid, but the funds are directed to a different entity, such as a factor. If the newly added fields in bank accounts contain alternative payee information, it will automatically be included in the payment suggestion and subsequently in the exported payment entry.

For more information, refer to the [Adding an alternative account holder](@CB-218) article.

