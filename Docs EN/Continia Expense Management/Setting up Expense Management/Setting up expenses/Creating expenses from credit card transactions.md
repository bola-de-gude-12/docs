---
title: Creating expenses from credit card transactions
date: 23-07-2025
description: 
id: EM-201
lang: en
---
# Creating expenses from credit card transactions

When credit card transactions have been imported, either automatically – by setting up an automatic feed – or manually, you can have Expense Management automatically create new expenses from the transactions, or you can have Expense Management attempt to match transactions to expenses that have already been created by the card owner. This is configured for each payment type.

## Prerequisites
To set up automatic creation of expenses from credit card transactions, you must have:

* One or more payment types that have already been set up.

## Create expenses automatically

If **Create expense from transaction** is enabled for a payment type, Expense Management will always automatically create new expenses from transactions and send them to the card owner. They can then attach receipt images and categorize the expense.

Date, currency, amount, and description of a transaction are always added to the expense.

To set it up for a payment type so that expenses are created automatically from transactions, you first need to assign a card to a user:

1. Search for {{search}} **Bank Transaction Inbox**. You can also access this inbox using the **Unhandled Bank Transaction Inbox** cue in the Role Center. 
1. On the action bar, click **Assign card to User**.
2. In the list of available Continia user IDs, select the user you want to assign a card to.
3. In the dialogue box asking *A payment type must be assigned to the credit card. Do you wish to proceed?*, select **Yes**.
4. In the list of payment types, select the credit card you want to assign to the user you selected in step 2.

Expense Management synchronizes and checks if imported transactions can be matched to any of the submitted credit card expenses. If no matches are possible, Expense Management will create new expenses and send them to the users.  

You only need to go through the procedure described above the first time transactions are imported for the selected credit card.

## Create expenses manually

If you prefer to create expenses manually, the process is as described below. One reason to use the manual method is that when you begin using Expense Management, you can delete credit card transactions that have been processed using another solution than Expense Management.

This manual process also makes it possible to set up mapping rules to assign expense types or exclude transactions from the expense creation process.

1. Search for {{search}} **Bank Transaction Inbox**. You can also access this inbox using the **Unhandled Bank Transaction Inbox** cue in the Role Center. 
1. On the action bar, click **Assign card to User**.
2. In the list of available Continia user IDs, select the user you want to assign a card to.
3. In the dialogue box asking *A payment type must be assigned to the credit card. Do you wish to proceed?*, select **Yes**.
4. In the list of payment types, select the credit card you want to assign to the user you selected in step 2.

Now all credit card transactions pertaining to the selected credit card will be moved to the **Unmatched** cue in the Role Center. If you instead want to access your unmatched transactions via search, then search for {{search}} **Bank Transactions**.

From here, you can manually match the transaction to an existing expense or create a new expense by selecting **Match or Create Expenses**. The expense will automatically display in the card owners Mobile Expense App, where they can attach images and add extra information and then send for approval.

## Related information
[Setting up Payment Types](@EM-81)

[Automatic Import of Credit Card Transactions ](@EM-202)