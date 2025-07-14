---
title: Importing payments in Continia Banking
description: Learn how to import CAMT.054 files
date: 02-04-2025
id: CB-163
lang: en
---


# Importing payments into the Payment Reconciliation journal

Continia Banking introduces a second action to import payments, specifically designed for CAMT.054 files. CAMT.054 files are used specifically to detail transaction data, unlike formats such as CAMT.053, which include balance and statement information. This feature allows you to reconcile incoming and outgoing payments efficiently without requiring statement files, balances, or fees.

On the **Bank Account Communication Setup** page, accessed from the Bank Account Card by selecting **Related** > **Communication Setup**, the CAMT.054 File type is now available. CAMT.054 (Payments) is configured similarly to CAMT.053 (Account Statements) during bank account setup but differs in key ways: it excludes summarized balances and is imported via the **Payment Reconciliation Journal**. Unlike CAMT.053, CAMT.054 cannot be imported from the **Bank Reconciliation** page.

## To import and apply payments

To import payments into the Payment Reconciliation journal:

1. Search ({{search}}) for and select **Payment Reconciliation Journals**.

2. On the Payment Reconciliation **Journals** page, on the action bar, select **New Journal**.

3. On the **Payment Bank Account List** page, select the relevant bank account.

4. On the **Payment Reconciliation Journal** page, navigate to the **Home** FastTab and select one of the following options:
   - **Import and apply payments** -  import a CAMT.054 file to begin the reconciliation process by identifying ledger entries and searching for matches. The account statement lines go through built-in matching and predefined search rules during reconciliation. You can monitor the progress using the **Status** field on the account statement lines. If you receive OCR payments, the **Payment Reference Rules** are applied to facilitate reconciliation by matching payment references accurately. For more information, refer to the [Introducing Payment Reference Rules](@CB-162) article. 
   
   - **Import new payments** - import new payments from a CAMT.054 file.
   
   - **Import existing payments** - re-import an existing CAMT.054 file.
   
     > [!TIP]
     >
     > If the action you're looking for isn't available, go to the **Page** tab and select **Show More Actions** to reveal additional options.

## To import debit or credit lines only

The **Import Lines** field is available on the **Banking Import Setup** page and individual **Bank Account Cards**. This field allows you to configure whether to import all transactions or only debit or credit lines, offering flexibility based on your specific requirements.

