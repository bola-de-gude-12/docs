---
title: The Payment Reconciliation Journal
description: Learn how to match payments with corresponding ledger entries in the Payment Reconciliation Journal.		
date: 17-03-2025
id: CB-106
lang: en
---

# Introducing the Payment Reconciliation Journal

In the Payment Reconciliation Journal, the primary goal is to match payments with corresponding ledger entries. Unlike the Bank Account Reconciliation, which transfers transferring multiple entries into different journals for posting, the Payment Reconciliation Journal doesn't transfer the lines to a journal. Instead, the reconciliation of bank ledger entries created in this journal happens when the journal is posted. You have the flexibility to either reconcile the bank ledger entries at this stage or simply apply payments and skip the reconciliation.  If you choose to skip reconciliation, it can be completed later when the journal is posted.

When working in the payment reconciliation journal, you can efficiently manage payments and other transactions. Additionally, you can post journal entries and handle reconciliation at the same time using the **Post and Reconcile** button.

## Continia Banking enhancements to the Payment Reconciliation Journal

Continia Banking offers the following enhancement to the Payment Reconciliation Journal:

* **Import** - lets you import bank transactions.
* **Apply proposals** - automatically suggest matches for payments and ledger entries.
* **Search rules** - implement criteria to improve matching accuracy. For more information on search rules, refer to the [Introducing Search Rules](@CB-87) article.
* **Show more columns** - customize your journal view by adding extra data columns for enhanced insights. Navigate via the action bar to **Page** > **Show More Columns** to display more information.
* **Show more actions** - if the action you're looking for isn't available, go to the **Page** tab and select **Show More Actions** to reveal additional options.
* **FactBox** - access an extended FactBox that provides detailed matching information, aiding in accurate reconciliation.

When you configure a bank account in the Payment Reconciliation Journal using Continia Banking, these enhancements become available.

## The actions available on the Payment Reconciliation Journal

The Payment Reconciliation Journal page offers a range of actions designed to simplify matching payments with corresponding ledger entries. These actions enable you to 

| Action                                       | Procedure                                                    |
| -------------------------------------------- | ------------------------------------------------------------ |
| To import a bank statement                   | On the **Payment Reconciliation Journal** page, on the **Home** tab, select **Import and Apply Bank Statement/Import New Bank Statement/Import Existing Bank Statement**.  For more information, refer to the [Importing a bank statement manually](@CB-86) article. |
| To import payments                           | On the Home tab, select **Import and Apply Payments/Import New Payments/Import Existing Payments** for importing CAMT.054 files. |
| To work with application proposals           | On the **Payment Reconciliation Journal** page, navigate to the line and in the **Proposals** column, select the number. Alternatively, select the line, and on **Home** tab, select **Application Proposals**.  For more information, refer to the [Working with payment application proposals](@CB-19) article. |
| To apply entries                             | On the **Payment Reconciliation Journal** page, on **Home** tab, select **Apply Entries**. You can select multiple lines and apply actions to all of them. |
| To transfer amount differences to an account | On the **Payment Reconciliation Journal** page (and the **Payment Application Review** page), you can manually trigger the action to transfer an amount difference to an account. On the **Payment Reconciliation Journal** page, on the action bar, select **Manual Application** > **Transfer Difference to Account**. You can then select the account details. |
| To add a search rule                         | On the  **Payment Reconciliation Journal** page, on the **Home** tab, select **Add Search Rule**. This allows you to quickly add a rule and apply the journal line. <br /><br />For more information, refer to the [Introducing Search Rules](@CB-87) article. |
| To show a bank transaction                   | On the  **Payment Reconciliation Journal** page, on the **Related** tab, select **Details** and select **Show Bank Transaction**. This will show the source data received from the bank statement file. |
| To delete and set as Imported                | On the  **Payment Reconciliation Journal** page, on the **Related** tab, select **Details** and select **Delete and set as Imported**. This will allow you to delete the lines in the journal and mark it as already processed. |
| To show more columns                         | On the  **Payment Reconciliation Journal** page, on the **Page** tab, select **Show More Columns** or **Show Fewer Columns**. This allows you to get more detailed information. |
| To apply automatically                       | On the  **Payment Reconciliation Journal** page, on the **Home** tab, select **Apply Automatically**. |
| To accept and remove account applications    | You can accept or remove an application after the matching procedure has been run. On the  **Payment Reconciliation Journal** page, on the **Home** tab, select **Apply To Account** or **Remove Account Applications**. |
