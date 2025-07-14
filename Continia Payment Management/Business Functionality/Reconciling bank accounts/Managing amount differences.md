---
title: Managing amount differences in Payment Management
description: How to manage amount differences on bank statement lines.
date: 08-04-2021
id: PM-55
lang: en
---

# Managing Amount Differences

During automatic reconciliation by Statement Intelligence, a bank statement line may show a bank ledger entry difference in the status box. Differences in amounts between imported bank statement lines and bank account ledger entries can occur for various reasons, such as customers not considering cash discounts.

When matched lines deviate, Statement Intelligence automatically creates a new line in the ledger journal for the amount difference. This allows the ledger entry to be posted and applied to the bank statement line in the bank account reconciliation process.

To handle amount differences in bank account reconciliation, you must specify a general journal batch and general journal template for the bank account. For more information, see [Set up bank accounts for Statement Intelligence](@PM-35).

To manage amount differences during the bank account reconciliation:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Account Reconciliations**, then select the related link. This opens the list of bank account reconciliations.
1. On the required bank statement, navigate to the **Bank Statement Lines** and see the column **Status**. Bank statement lines with amount differences will have the status **Bank Ledg. Entry Diff**. 
1. In the action bar, select **Journals** > **General Journal**. This will open the general journal where ledger entries for amount differences have been created.
1. Validate the ledger entries.
1. Post the ledger entries from the action bar by selecting **Post/Print** > **Post**.

Bank account ledger entries will now be created for the amount differences, and the bank statement line can be fully applied. 

