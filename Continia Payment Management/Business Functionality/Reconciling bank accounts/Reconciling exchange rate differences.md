---
title: Reconciling exchange rate differences
description: How to reconcile exchange rate differences with Statement Intelligence
date: 22-01-2024
id: PM-45
lang: en
---

# Reconciling Exchange Rate Differences

When you transfer funds to a foreign bank account, there may be differences in exchange rates between the rate used in Business Central while exporting and the rate used by the bank. These differences will be noticeable when importing the bank statement to the reconciliation page. Any such variance will affect the reconciliation process.

During automatic bank account reconciliation, Statement Intelligence examines the bank account entries for settlement by looking for the Transaction ID associated with each bank account line. The Transaction ID is a unique reference number generated on the payment record in the payment journal, which tracks the payment from the bank back to the account reconciliation journal. If a payment is made in a foreign currency and there is a discrepancy in the amount between two entries sharing the same Transaction ID, it will be treated as an exchange rate difference.

> [!NOTE]
>
> Exchange rate differences are automatically handled for bank accounts using the local currency (LCY) but not those set up in foreign currency.

Statement Intelligence automatically creates general journal entries for exchange rate differences when importing the bank account statement into the reconciliation journal if you turn on the **Create Currency Exchange Rate Amount Differences** setting:

![Currency exchange rate amount differences](/images/PM365/currency-exchange-rate-difference.png)

You need to post the general ledger entries to generate bank account entries in the reconciliation journal.

To manage exchange rate differences in the bank account reconciliation journal:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Account Reconciliations**, then select the related link. This opens the list of bank account reconciliations.
1. Open the bank account reconciliation page. 
1. Navigate to the **Bank Statement Lines** and see the column **Status**. After importing a bank statement, the lines with exchange rate differences will have the status **Exchange rate difference**.
1. On the action bar, navigate to **Journals** > **General Journals**. This opens the general journal where ledger entries have been created for the exchange rate differences.
1. Validate that the ledger entries are correct and post the entries.
1. Close the ledger journal. When closing the ledger journal, Statement Intelligence will automatically create bank account ledger entries for the posted ledger entries and reconcile these entries with the bank statement lines. 
1. Navigate to the bank statement line from which the exchange rate difference occurred, and see that the line status is now **OK**.

The exchange rate differences have now been reconciled. 