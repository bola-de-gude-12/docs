---
title: Applying split rules manually
description: Learn how to use the Apply Split Rule action on the Payment Reconciliation Journal and the Bank Account Reconciliation.
date: 14-04-2025
id: CB-235
lang: en
---

# Applying split rules manually

Sometimes, a transaction in your bank statement doesn’t match any existing search rule. In these cases, you can manually apply a split rule to accurately reflect how the payment should be recorded.

Continia Banking allows you to use the **Apply Split Rule** action to divide a single transaction into multiple lines, which is helpful for scenarios like payments with fees, partial refunds, or when multiple accounts are involved.

This article walks you through how to manually apply split rules in both the Payment Reconciliation Journal and the Bank Account Reconciliation.

## To manually assign split rules in the Payment Reconciliation Journal

On the Payment Reconciliation Journal, the **Apply Split Rule** action allows you to split a line when it doesn't match a bank transaction code rule or search rule. 

To manually apply a split rule in the Payment Reconciliation Journal:

1. On the **Payment Reconciliation Journal** page, on the action bar select **Rules** > **Apply Split Rules**. 
2. You can now assign a split rule code to create split lines that are displayed indented to the base line. Additionally, note that changing the account type or account number only affects the child line; previously made applications are deleted. Also, changes to posting groups can be made by updating the bank reconciliation split line. Use the lookup in the **Split Lines** field from the base line.

> [!NOTE]
>
> Child lines are indented, cannot have additional split rules applied, and any changes to them will update the base transaction amount.

## To manually assign split rules in the Bank Account Reconciliation

On the Bank Account Reconciliation page, the **Apply Split Rule** action allows you to split a line when it doesn't match a bank transaction code rule or search rule. 

To manually apply a split rule in the Bank Account Reconciliation:

1. On the **Bank Account Reconciliation** page, on the action bar select **Rules** > **Apply Split Rules**. 

2. Bank reconciliation split lines are created and accessible via the **Split Lines** field. Extra journal lines are generated based on these split lines when search rules, applied entries, or manual entries are used. Deleting or changing a bank recon split line will remove all related journal lines, reset previous applications, and delete any difference journal lines. Changes to account type, account number, dimensions, or posting groups will be reflected in the journal line.

   For example: a refund of 1,422 euros includes a 3 euro fee. The transaction is split into three lines:

   1. **Customer Account**: **1422 euros** (Refund amount)
   2. **G/L Account**: **-3 euros** (Fee deducted)
   3. **Bank Account**: **-1419 euros** (Amount refunded via bank)

These split lines are moved to the **Cash Receipt Journal**, reflecting the refund and associated fee.