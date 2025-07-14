---
title: Set up Employee Reconciliation Rules
description: a guide on how to set up employee reconciliation rules
date: 27-08-2021
id: PM-188
lang: en
---

# Setting up Employee Reconciliation Rules

You use employee reconciliation rules in the bank account reconciliation, for Payment Management to insert an employee number for unidentified bank statement lines. This will ease the process of identifying a match in the employee ledger entries. 

With Statement Intelligence, Payment Management will automatically try to match payments by using the payment's unique payment reference ID which is created for all payments processed from the payment journal with Payment Management. If a payment has not been processed from the payment journal, the unique payment reference ID can't be used for matching the bank statement lines, in which case other parameters such as date and amount will be used. If a unique match can't be found the reconciliation rule will be applied in order to identify a match. When a rule has been met, the employee number will be inserted on the statement line, and you will be able to select and apply the matching employee ledger entries. You'll find information about how to apply the suggested employee ledger entries in the guide [Applying Ledger Entries](@PM-163).

> [!IMPORTANT]
>
> Due to a limitation in Business Central only Bank Accounts where the "Currency Code" is blank is supported when reconciling employees. If the bank account does not have a blank currency code then the reconciliation is not executed and related page elements are hidden.

## To set up employee reconciliation rules

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Employee Reconciliation Rules**, then select the related link.
1. In the action bar, select **New** to create a new reconciliation rule.
1. In **Account No.** chose the employee number that should be applied to the payment line when a payment line meets the search rule.
1. In **Search text** enter the text to be searched for in the employee payment.
1. In **Search Principle** specify how you want the engine to search for the specified text in the fields enabled for searching.
   - **Exact** indicates that search text must be the exact same as the description or notification on the payment, for the rule to be met.
   - **From left** indicates that search text must match the first part of the description or notification on the payment, for the rule to be met.
   - **From right** indicates that search text must match the last part of the description or notification on the payment, for the rule to be met.
   - **Within** indicates that search text must just appear some place in the description or notification on the payment, for the rule to be met.
1. Select **Search in Description** if you want the search rule to search for **Search text** in the description of the payment line.
1. Select **Search in Notification** if you want the search rule to search for **Search text** in the payment line notification.
1. If you want to set up more rules, go to the action bar and select **New.**
1. When you have finished setting up reconciliation rules you can close the page. 

## Related information

[Applying Ledger Entries](@PM-163)

