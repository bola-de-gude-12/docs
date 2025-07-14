---
title: Merging bank statement lines
description: How to merge bank statement lines in the bank account reconciliation
date: 15-03-2021
id: PM-46
lang: en
---

# Merging Bank Statement Lines

When importing bank account statements with Statement Intelligence, bank reconciliation lines can automatically be merged into one line based on the defined merge rules. If any reconciliation lines are not automatically merged, you can manually merge them during the bank account reconciliation process.

Merging bank account entries is commonly done when consolidating multiple credit card transfers into a daily total, which aligns with the amount posted in the general ledger.

## To merge lines by merge rules

When you have set up [merge rules](@PM-40) for bank account statement lines, those lines that adhere to the defined rules will automatically be merged during the import of the bank account statement.

However, if you have changed the lines after the import and still need them merged, you can manually initiate the merge rule from the reconciliation journal.

To merge bank account statement lines by merge rules:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Account Reconciliations**, then select the related link. This opens the list of bank account reconciliations.
1. On the required bank account reconciliation, go to the action bar and select **Matching** > **Merge Lines by Rule**.

Statement Intelligence will merge lines that can be merged according to the defined [merge rules](@PM-40).

## To merge lines manually

If merge rules have not been set up, or if the bank account statement lines can't be merged using the defined merge rules, bank statement lines can be merged manually.

To merge bank account statement lines manually:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Account Reconciliations**, then select the related link. This opens the list of bank account reconciliations.
1. On the required bank account reconciliation, mark the bank statement lines that should be merged, by pressing **Ctrl** on your keyboard while choosing those lines that should be merged. 
1. Navigate to the action bar and choose **Process** > **Merge Lines Manually**.

The lines chosen for manual merge are now merged into one line.

## To view merged lines

To get an overview of which lines have been merged into one line:

* Navigate to the merged bank statement line and select **Additional Information**. This action opens a list with an overview of a description and a notification for all the lines included in the merge.

## To undo merged lines

Once lines have been merged in the reconciliation journal, unmerging them is impossible. If you wish to keep the lines separate, you must delete the merged line and reimport it into the reconciliation journal as a standalone entry. If the merging occurred due to a merge rule, you must disable the merge rule before importing the account statement lines again.

## Related information

[Account statement merge rules](@PM-40).