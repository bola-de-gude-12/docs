---
title: Using Continia Banking enhancements in the Payment Reconciliation Journal
description: How to work in the Payment Reconciliation Journal
date: 01-10-2024
id: CB-26
lang: en
---
# Working in the Payment Reconciliation Journal

The Payment Reconciliation Journal in Business Central that is enhanced by Continia Banking, simplifies matching and applying payments to ledger entries. When importing bank transactions, Continia Banking will be able to automatically reconcile most of the lines. However, if some information is missing or there are no suggestions for reconciliation, manual matching of the bank statement lines and the ledger entries may be necessary.

## To handle proposals from automatic matching

To handle proposals from automatic matching:

1. You can populate lines in the journal by importing a bank statement via direct or manual import and use the journal to reconcile bank accounts. Continia Banking automatically applies its advanced matching rules to suggest how these transactions should be applied. On the **Payment Reconciliation Journal** page, select a line and on the action bar, select **Manual Application** > **Apply Entries**.

1. When a match is found for an open ledger entry and the amounts align (considering currency exchange rates, discounts, and tolerances), the payment application proposal is automatically matched, and the status is set to **Completed**. You can then move on to the next lines or post the journal. For example, the system proposes a match if:
   - **Transaction text and amount match** - the system will auto apply the proposals. The line is ready for posting. 
   - **External document number match found** - the system automatically applies the proposal and status on the line is set to **Completed**.
   - **End-to-End ID match found** - payments sent with a unique end-to-end ID are matched directly to the corresponding entries, facilitating a seamless match and readying them for posting. 

1. Once all matching and adjustments are complete, you can post the applied lines. This closes the ledger entries. On the action bar, use the **Post Payments Only** feature to close the ledger entries without reconciling them to the bank account ledger. Afterwards, you can go into the Bank Account reconciliation and then reconcile the bank ledger entries that were created in the payment reconciliation journal. Select **Post and reconcile** to reconcile the bank account and you're done. For more details on how to handle posting in the Payment Reconciliation Journal, refer to the [Handling Payment Reconciliation Journal Postings](@CB-105) article.

## To apply matching rules manually

If a transaction doesn’t automatically match, you can manually edit the fields or add a search rule.

To apply matching rules manually: 

1. If a transaction doesn’t automatically match, you can do the following:
      * **Use search rules** - you can add a search rules and apply them manually. This involves identifying related parties or other matching criteria not automatically processed. For example, use specific rules to find related customer or vendor records when automatic matching doesn't apply, ensuring that the correct entries are matched. For more information on search rules, refer to the [Introducing Search Rules](@CB-87) and [Setting up Search Rules](@CB-104) articles.
      * **Adjust and apply amounts** - for entries where amounts do not match exactly, you can manually adjust the amount to fit or split transactions across multiple lines as needed. For example,<ul><li>If a payment covers multiple invoices, you can split the payment across these lines and apply the amounts accordingly</li><li>If a transaction in your bank account is not in the bank statement, you can create the missing transaction and reimport the bank statement file or enter the transaction manually.</li><li>If a transaction in the internal bank account corresponds to a bank transaction but the information is too different to give a match, you can review the information and then match the two manually. </li></ul>
1. Once all matching and adjustments are complete, you can post the applied lines. This closes the ledger entries. On the action bar, use the **Post Payments Only** feature to close the ledger entries without reconciling them to the bank account ledger. Afterwards, you can go into the Bank Account reconciliation and then reconcile the bank ledger entries that were created in the payment reconciliation journal. Select **Post and reconcile** to reconcile the bank account and you're done. 