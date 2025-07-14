---
title: Defining allowed tolerances
description: How to set up allowed tolerances for matching bank account statement lines
date: 13-09-2021
id: PM-193
lang: en
---

# Defining Allowed Tolerances

You can manage allowed tolerances between the payment information stated on the bank statement lines and the information stated on the bank account ledger lines, for Statement Intelligence to automatically match and apply the statement lines. 

## To define tolerance in amount deviations

You can specify the maximum amount that a bank statement line is allowed to deviate from a customer-, vendor-, or employee ledger entry for the automatic creation of journal lines to take place. If the deviation exceeds the given amount the creation of cash journal lines must be handled manually.

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Accounts**, and then select the related link. 
1. On the bank account card, on the **Statement Intelligence** FastTab, define the allowed tolerance deviations for:
- **Tolerance Deviation Auto. Customer Suggestion** 
- **Tolerance Deviation Auto. Vendor Suggestion**
- **Tolerance Deviation Auto. Employee Suggestion** 



## To define tolerance in deviation of days

You can specify the tolerance days a customer-, vendor-, or employee ledger entry posting date is allowed to deviate from a bank statement line transaction date, for the automatic match of bank account ledger entries or creation of journal lines to take place. The transaction date is stated on the bank statement line.

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Banks**, and then select the related link. 
1. On the bank card, on the **Statement Intelligence** FastTab, specify the allowed number of days the posting date can deviate *prior to* and *after* the transaction date in the following two fields: 
- **Tolerance Days  - Before**
- **Tolerance Days  - After**

