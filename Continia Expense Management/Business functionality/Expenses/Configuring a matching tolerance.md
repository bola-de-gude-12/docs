---
title: Configuring a matching tolerance
date: 12-06-2025
description:
id: EM-319
lang: en
---
# Configuring a matching tolerance

If an expense is logged after banking hours, the bank posting date will automatically set to the next day (when the transaction is processed). For example, an Expense user may have a business dinner in the evening of 04-05-2025 for which they submit their receipt. As the expense has been submitted outside of the bank's working hours, the bank will not process the transaction until the next day, and will instead have the date 05-05-2025. 

However, to avoid confusion and automatically match between the expense and the transaction, you can set up a matching tolerance in Expense Management.

To set up a matching tolerance:

1. Search {{search}} for **Payment Types**.
2. Select a payment type from the **Code** column (for example, a credit card).
3. On the **Payment Type Card**, go to **Bank Transactions/Credit Card** > **Matching tolerance**. 
4. In the **Amount (%)** field specify the percentage of difference allowed. This allows a matching tolerance if a perfect match isn't available (for example, due to rounding). Set the maximum matching tolerance (for example, 2).
5. In the **Date (Days)** field specify an allowed variance in days. This allows a tolerance if no perfect match is available (such as a scenario where the transaction is submitted after banking hours). Set the maximum matching tolerance in days (for example, 2).

## Related information

For more information about automatic and manual matching, see:

[Expense Management Bank Account Reconciliation](@EM-91)