---
title: Set up general reconciliation rules
description: How to set up general reconciliation rules
date: 02-03-2021
id: PM-38
lang: en
---

# Setting up General Reconciliation Rules

Reconciliation rules are employed during the import of a bank account statement to search for bank account lines for settlement in the bank account reconciliation journal. The search rules will be applied the description in the bank account reconciliation lines. If the search rule is complied with, a counter entry will be generated on a balance account (bank or ledger). Search rules will most often be applied in connection with recurring entries such as interests or fees.

> [!NOTE]
>
> General reconciliation rules and bank account reconciliation rules are basically the same, however the general reconciliation rules will apply to all bank account per default, as bank account reconciliation rules only applies to the specific bank account. 

## To set up general reconciliation rules

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **General Reconciliation Rules**, then select the related link.
1. On the page **General Reconciliation Rules** navigate to the action bar and select **New** to create a new reconciliation rule.
1. In the column **Search Text** specify the text to search for when the reconciliation rule is used on the bank account reconciliation lines in order to identify a match.
1. In column **Search Principle** specify how the search is carried out when searching for the specified search text.
   - **Exact** indicates that search text must be the exact same as the description on the bank account reconciliation line for the rule to be met.
   - **From left** indicates that search text must match the first part of the description on the bank account reconciliation line for the rule to be met.
   - **From right** indicates that search text must match the last part of the description on the bank account reconciliation line for the rule to be met.
   - **Within** indicates that search text must just appear some place in the description on the bank account reconciliation line for the rule to be met.
1. Select **Search in Description** if you want the search rule to search for Search text in the description of the payment line.
1. Select **Search in Additional Information** if you want the search rule to search for Search text in the payment line notification.
1. In the column **Balance Account No. (Positive)**, specify the balance account (bank account or ledger account) to which the entry will be generated in case of a positive amount. If the account type is a ledger account, an account of the balance type must be used, which allows direct bookkeeping.
1. In the column **Balance Account No. (Negative)**, specify the balance account (bank account or ledger account) to which the entry will be generated in case of a negative amount. If the account type is a ledger account, an account of the balance type must be used, which allows direct bookkeeping.
1. If you want to define more reconciliation rules navigate to the action bar and select **New.**
1. When you have finished setting up reconciliation rules you can close the page. 

The rules will be implemented when you run a reconciliation in the bank account reconciliation journal.