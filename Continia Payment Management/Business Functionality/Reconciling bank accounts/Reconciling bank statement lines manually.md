---
title: Reconciling bank statement lines manually
description: how to manually reconcile bank account statements
date: 03-03-2021
id: PM-39
lang: en
---

# Reconciling Bank Statement Lines Manually

By using Statement Intelligence bank account statements will automatically be reconciled when imported to the bank account reconciliation. However, there may be cases where automatic reconciliation is not possible or where you do not necessarily want to apply a reconciliation rule. In that case, you can manually handle the process of generating journal lines that should be processed for reconciliation. 

## To manually reconcile bank statement lines

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Account Reconciliations**, then select the related link. This opens the list of bank account reconciliations.
1. Open the bank account reconciliation for which you want to manually reconcile bank account statement lines.
1. On the bank account statement, choose the bank statement line you want to manually reconcile.
1. Navigate to the column **Manual handling** and mark the box. 
1. In the action bar, navigate to **Process** > **Create journal lines**. You will now be notified that general journal lines are being created for those bank statement lines that have **Manual Handling** enabled. 
1. In the action bar, navigate to **Journals** > **General Journal**.
1. Identify the newly created general journal lines you want to process for the reconciliation.
1. Enter relevant information about the general journal lines, such as document type and account no.
1. In the action bar, navigate to **Post/Print** > **Post** to post the journal lines.

The general journal lines are being created in the table **Bank Account Ledger Entries** in the bank account reconciliation journal, and can now be applied to the bank statement lines.