---
title: Expense Management bank account reconciliation
date: 10-06-2025
description:
id: EM-91
lang: en
---

# Expense Management bank account reconciliation

Find missing transactions and reconcile transactions with a statement, using the Expense Management Bank Account Reconciliation feature. 

This feature is very similar to the standard bank reconciliation feature in Dynamics 365 Business Central. However, Expense Management Bank Account Reconciliation comes with a few extra advantages:

* You can reconcile a bank account, G/L account, or vendor
* You can see the status of expenses

You can carry out monthly reconciliations by suggesting lines, importing statement transactions, or entering information from a statement manually while comparing paper statements from the bank to transactions in Expense Management.

You can match automatically or manually.

## Automatic matching

1. Search for {{search}} **Bank Account Reconciliation - Expense Management**.
1. On the action bar, click **New**.
1. Under **General**, choose a bank account type.
1. Select a bank account number. Any bank transaction entries connected to this account will display automatically.
1. To get bank statement lines, either:
	1. On the action bar, click **Bank** > **Import Bank Statement**.
	1. In the dialog box, click **Import a new Bank Statement File** or **Find existing statement transactions in the system**, then click **OK**.
	
	  Or
	
	1. On the action bar, click **Home** > **Suggest Lines**.
	1. Under **Options**, fill in the fields, then click **OK**.
1. On the action bar, click **Matching** > **Match Automatically**, then click **OK**.
1. After you've matched both sides, copy the amount from **Total Balance** and insert it into **Statement Ending Balance**.
1. On the action bar, click **Home** > **Post** to post the reconciliation.

To view posted reconciliations, search for {{search}} **Bank Account Statements - Expense Management**.

## Manual matching

1. Search for {{search}} **Bank Account Reconciliation - Expense Management**.

2. On the action bar, click **New**.

3. Under **General**, choose a bank account type.

4. Select a bank account number. Any bank transaction entries connected to this account will display automatically.

5. To get bank statement lines, either:   
   1. On the action bar, click **Bank** > **Import Bank Statement**.
   1. In the dialog box, click **Import a new Bank Statement File** or **Find existing statement transactions in the system**, then click **OK**.
	
	  Or
	
	1. Refer to your bank statement, fill in the fields for **Transaction Date**, **Type**, **Description**, and **Statement Amount**.
	
6. Select the bank statement line and the bank transaction entry you want to match, then on the action bar, click **Matching** > **Match Manually**. Repeat the process for each bank statement line.

8. To post the reconciliation, on the action bar, click **Home** > **Post**.


To view posted reconciliations, search for {{search}} **Bank Account Statements - Expense Management**, then choose the related link.

## Related information
[Importing transactions with custom templates](@EM-47)

[Overview of credit card transactions](@EM-213)