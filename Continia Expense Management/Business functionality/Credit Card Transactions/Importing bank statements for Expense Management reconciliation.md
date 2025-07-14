---
title: Importing bank statements for Expense Management reconciliation
date: 02-07-2025
description: Learn how to import a bank statement into BC for EM reconciliation
id: EM-323
lang: en
---

# Importing bank statements for Expense Management reconciliation
To use bank account reconciliation, you must first upload a bank statement to Business Central, after which you can reconcile transactions for a period that you specify.

## Importing a bank statement


To import a bank statement into Business Central:

1. Search for {{search}} **Bank Transactions**.
1. On the action bar, click **Import Statement Transactions** (or open the **More** menu (**...**) if it isn't displaying directly on your action bar).
1. Select your bank from the list. Alternatively you can create a new bank import template, for more information, see [Importing transactions with custom templates](@EM-47).
1. Fill in all relevant information.
1. On the action bar, click **Transaction Import Journal**, under **General**, toggle **Statement Transactions** to on, and click **OK**.
1. On the action bar, click **Approve and Transfer**.
1. Verify that the statement transactions have been imported; On the **Bank Transactions Inbox** page, add the filter **Bank Statement Transaction** and select **Yes** from the dropdown menu.

You'll now see the imported statement transactions.
## Reconciling transactions

After you've imported a bank statement (or bank statements), you can begin to reconcile transactions for the duration of the dates that you specify. 

To reconcile the bank transactions of a specified period of time:

1. Search for {{search}} **EM Bank Account Reconciliation**.
1. On the action bar, click **New** to create a new reconciliation.
1. Under **General**, fill in all relevant fields that match your setup.
1. On the action bar, click **Bank** > **Import Bank Statement**.
1. In the dialog that pops up, select **Find existing statement transactions in the system**.
1. Fill in the dates matching the period that you want to reconcile, then click **OK**. 

## Related information

[Expense Management bank account reconciliation](@EM-91)

[Importing transactions with custom templates](@EM-47)

