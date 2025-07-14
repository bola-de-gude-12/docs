---
title: Matching Bank Statement Lines Manually on the Bank Account Reconciliation Page
description: Learn how to match lines manually when there are no suggestions for automatic reconciliation.
date: 29-01-2025	
id: CB-25
lang: en
---

# Matching Lines Manually on the Bank Account Reconciliation Page

When uploading bank statements for bank account reconciliation, Continia Banking can reconcile most of the statement lines automatically. However, if some information is missing or there are no suggestions for reconciliation, manual matching of the bank statement lines and the bank account ledger entries may be necessary.

To match lines manually on the Bank Account Reconciliation Page, there are different methods depending on the type of ledger entries you need to match.

## To manually match bank account ledger entries

You can directly match bank account ledger entries in the Bank Account Reconciliation using the **Match Manually** action.

To match lines manually on the Bank Account Reconciliation Page:

1. Use the {{search}} icon and search for Bank Account Reconciliations, then select the related link.

2. Open the bank account reconciliation for which you want to match lines manually.

3. On the **Bank Account Reconciliation** page, navigate to an unsolved line and on the action bar, select **Matching** > **Match Manually**.

   

## To manually match customer, vendor, employee ledger entries

If you need to manually match ledger entries other than [bank account ledger entries](#to-manually-match-bank-account-ledger-entries-in-the-bank-account-reconciliation), such as customer, vendor, and employee ledger entries, use the **Apply Entries** action or open the **Payment Application Review** page.

When applying entries, note that filters are set to ensure only relevant entries are displayed. These filters include posting date, open status, employee ledger entry conditions, and currency settings.

- The posting date of the ledger entry must be later than the transaction date on the reconciliation line.
- Only open ledger entries are included.
- If available, Account Type and Account No. are considered.
- Employee ledger entries are shown only if the related bank account is in LCY.
- Currency filters apply based on the **Appln. between currencies** setting in the **Sales and Receivables Setup** and **Purchase and Payables Setup**. If cross-currency application is not allowed, only entries with the same currency as the bank account being reconciled will be shown.

To match lines manually on the Bank Account Reconciliation Page:

1. Use the {{search}} icon and search for Bank Account Reconciliations, then select the related link.
2. Open the bank account reconciliation for which you want to match lines manually.
3. On the **Bank Account Reconciliation** page, navigate to an unsolved line and on the action bar, select **Home** > **Apply Entries**.

   > [!IMPORTANT]
   >
   > When applying entries, note that there are filters in place to ensure only relevant entries are displayed. These filters consider posting date, open status, employee ledger entry conditions, and currency settings. 

4. On the **Apply Ledger Entries** page, you can choose from a list of open ledger entries and apply them if required. You have the option to enter an amount or directly apply the entry. The system automatically fills in the applied amount, and you can view the total amount applied at the bottom of the page, just like in standard application pages.
   On the right panel, you can find some information about the current reconciliation line and the reconciliation details, if there are any. 
5. Alternatively, open the **Payment Application Review** page. Note that filters are set to ensure only relevant entries are displayed. See the [Working with Payment Application Proposals](@CB-19) to learn more. 

   