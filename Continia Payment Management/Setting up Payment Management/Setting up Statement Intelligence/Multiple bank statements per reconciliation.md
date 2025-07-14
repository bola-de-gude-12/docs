---
title: Multiple Bank Statements per Bank Account Reconciliation
description: How to allow for multiple bank account statements per reconciliation
date: 15-11-2021
id: PM-144
lang: en
---

# Enabling Multiple Bank Statements per Bank Account Reconciliation

Statement Intelligence settings on the bank account define if you can import multiple bank account statements to the same bank account reconciliation. You can choose to import the statements by a given period. For example, if you select the current week, only those bank account statements with a date within the current week can be imported into the same bank account reconciliation. 

You can also enable Statement Intelligence to automatically create a new bank account reconciliation if the statement date lies outside the allowed period for the given bank account reconciliation.

## To enable multiple bank statements

1. Use the ![Search for page or report](https://docs.continia.com/images/search_small.png) icon to search for Bank Accounts and select the related link.

1. Open the relevant bank account card for which you want to allow for multiple bank statements.

1. On the **Statement Intelligence** FastTab, navigate to the **Multiple Bank Statements per Reconciliation** section and enter information for the following fields:

   | Multiple Bank Statement per Reconciliation field | Description                                                  |
   | ------------------------------------------------ | ------------------------------------------------------------ |
   | Allow multiple bank statements                   | Switch to on to allow aggregation for multiple bank statements in one bank account reconciliation. |
   | Aggregation period                               | Specify if the Statement Date of a bank account statement must be within a given period for it to be aggregated with other bank statements in a bank account reconciliation. The options are:<br />**Field left empty**: no period limitations for aggregating bank statements apply.<br />**Current Week**: bank statements can only be imported to the bank account reconciliation if the Statement Date of the imported bank statement is within the current week.<br />**Current Month**: bank statements can only be imported to the bank account reconciliation if the Statement Date of the imported bank statement is within the current month.<br /><div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Warning</span></p><p>If you set the Aggregation Period to a given period, make sure to order bank statements daily using automatic import, to avoid date discrepancies.</p></div> |
   | Create new reconciliation                        | If switched on, Statement Intelligence automatically creates a new bank account reconciliation if the statement date on the imported bank statement is outside the allowed period for aggregating bank statements in the existing bank account reconciliation. |
   | Import all available statements                  | If switched on, all available statements for the reconciliation are imported. |



## To copy the notification to the bank account reconciliation line

Sometimes, banks do not provide sufficient information in the posting description for bank export data. To solve this, you can automatically add the notification to the description. The first notification is used if multiple notifications exist for a bank account reconciliation line. If no notification is available, the description is used.

To copy the notification to the bank account reconciliation line:

1. Use the ![Search for page or report](https://docs.continia.com/images/search_small.png) icon and search for **Bank,** then select the related link.
2. Open the relevant bank card for which you want to copy the notification.
3. On the **Statement Intelligence** FastTab, enable the **Copy Notification to Description** setting. 
