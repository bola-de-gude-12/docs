---
title: Working with the journals
date: 16-10-2024
description: Learn how to use integrated journal functionality in the Bank Account Reconciliation.
id: CB-88
lang: en
---

# Optimizing bank account reconciliation with integrated journal functionality

Continia Banking enhances the standard Business Central Bank Account Reconciliation page when the bank account linked to the Bank Account Reconciliation is configured with the Banking app. You can access various journals directly from the Bank Account Reconciliation page, including general, cash receipt, and payment journals, to perform tasks such as deleting, editing, and posting journal lines. This feature eliminates the need to leave the Bank Account Reconciliation page to perform postings elsewhere, thereby making the reconciliation process of the bank account more convenient. Upon posting, the related Bank Account Ledger entry generated is automatically reconciled, which simplifies the reconciliation process.

## Managing journal lines on the Bank Acc. Reconciliation page

Applying or unapplying payment proposals automatically handles the creation or deletion of journal lines, removing the need for manual intervention. The bank account statement line's reconciliation status will show when a journal line is created, but in most cases, posting the lines is all that's needed for reconciliation.

You can easily delete or post individual journal lines directly from the **Bank Acc. Reconciliation** page:

* **To post all journal lines across multiple journals** - on the action bar select **Journals** > **Post All Journal Lines**.

* **To post lines for a specific journal** - on the **General** FastTab, in the **Related Lines in Journal** section, Continia Banking provides a summary of the number of entries automatically generated during bank account reconciliation for:

  * Cash Receipt Journal
  * General Journal
  * Payment Journal

  Select the number to open the specific journal and post the line. 

For more information, refer to the [Handling Amount Differences](@CB-140) article or the [Reconciliation Statuses](@CB-107) article.

## To reconcile bank account ledger entries without corresponding entries

To simplify reconciling bank account ledger entries that lack corresponding entries, journals are automatically linked to the **Bank Account Reconciliation**. Any payment application proposal not directly tied to a bank account ledger entry will create a journal line in one of the designated reconciliation journals. 

To set up the journals used for this process, navigate to **Banking Import Setup**, go to the **Bank Account Reconciliation** FastTab, and locate the **Default Journals** section, where you'll find the **Journal Template Name** and **Journal Batch Name** fields. For more information, refer to the [Configuring Bank Statement Import Settings](@CB-14) article.
