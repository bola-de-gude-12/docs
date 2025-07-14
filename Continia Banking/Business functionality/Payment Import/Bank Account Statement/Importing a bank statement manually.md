---
title: Importing a bank statement manually in Continia Banking
description: How to import bank account statements.
date: 17-02-2025	
id: CB-86
lang: en
---

# Importing a bank statement manually

If the bank account is configured for direct communication, bank account files will be automatically downloaded and imported into the Bank Account Reconciliation or Payment Reconciliation Journal directly from the bank. If direct communication is not set up, you must download the files manually and select them for import. This article describes how to import bank statements into both the Bank Account Reconciliation Journal and the Payment Reconciliation Journal.

## To import a bank statement file into the Bank Acc Reconciliation Journal

To import a bank statement file into the Bank Account Reconciliation journal manually:

1. Search ({{search}}) for and select **Bank Account Reconciliations**.

2. On the bank account reconciliations page, navigate to the action bar and select **New**.

3. In the **Bank Account No.** field, select the relevant bank account.

4. On the **Bank Account Reconciliation** page, on the action bar, select Home and then select one of the following options:
   * **Import and Match New Bank Statement** - this action will import a statement and start the reconciliation process by identifying ledger entries and searching for matches. After import, the account statement will be processed for reconciliation, and you can use the **Status** on the account statement lines to review the reconciliation progress. If automatic matching is difficult, Continia Banking will typically offer matching suggestions, known as [Payment Application Proposals](@CB-19).
   * **Import New Bank Statement** - this action will import a statement. 
   * **Import Existing Bank Statement** - this action will re-import a statement. 

   > [!TIP]
   >
   > If the action you're looking for isn't available, go to the **Page** tab and select **Show More Actions** to reveal additional options.

5. Refer to the [Reconciling bank statement](@CB-18) article, for a detailed description of how to proceed with the reconciliation process.

## To import a bank statement file into the Payment Reconciliation Journal

To import a bank statement file into the Payment Reconciliation journal manually:

1. Search ({{search}}) for and select **Payment Reconciliation Journals**.
2. On the **Payment Reconciliation Journals** page, on the action bar, select **New Journal**.
3. On the **Payment Bank Account List** page, select the relevant bank account.
4. On the **Payment Reconciliation Journal** page, navigate to the **Home** FastTab and select one of the following options:
   * **Import and Match New Bank Transactions** - this action will import a statement and start the reconciliation process by identifying ledger entries and searching for matches. After import, the account statement will be processed for reconciliation, and you can use the **Status** on the account statement lines to review the reconciliation progress. If automatic matching is difficult, Continia Banking will typically offer matching suggestions, known as [Payment Application Proposals](@CB-19).
   * **Import New Bank Transactions** - this action will import a statement. 
   * **Import Existing Bank Transactions** - this action will re-import a statement.
    > [!TIP]
   >
   > If the action you're looking for isn't available, go to the **Page** tab and select **Show More Actions** to reveal additional options.