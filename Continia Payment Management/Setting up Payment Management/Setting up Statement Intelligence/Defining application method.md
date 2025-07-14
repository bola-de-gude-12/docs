---
title: Defining application method
description: Information on how to reconcile bank account statements.
date: 24-06-2022
id: PM-83
lang: en
---

# Defining Application Methods

When reconciling bank statement lines in the bank account reconciliation, Statement Intelligence will automatically apply bank statement lines based on various criteria on the bank statement line. However, if Statement Intelligence finds more entries that potentially match the bank statement line based on the matching criteria, you can define how the application should be managed. 



## To define a default application method

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Banks**, and then select the related link.
1. Open the relevant bank card to which a default application method must be defined.
1. On the bank card, on the **Statement Intelligence** FastTab, in the **Reconciliation Method Debit** field, use the dropdown arrow to choose how to reconcile bank account ledger entries that have the same date and amount as the bank account reconciliation line.
   - Select **Apply to Oldest** if you want to reconcile the bank account ledger entry occurring with the earliest date.
   - Select **Manual** if you manually want to select which bank account ledger to reconcile.
1. In the **Reconciliation Method Credit** field, use the dropdown arrow to choose how to reconcile bank account ledger entries that have the same date and amount as the bank account reconciliation line.
   - Select **Apply to Oldest** if you want to reconcile the bank account ledger entry occurring with the earliest date.
   - Select **Manual** if you manually want to select which bank account ledger to reconcile.



## To define an application method for a specific customer

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Customers**, then select the related link.
1. Open the customer card, for whom you want to specify an application method.
1. On the customer card, on the **Payments** FastTab, in the **Application Method** field, use the dropdown arrow to choose how you want payments to be applied in the bank account reconciliation.
   - Choose **Manual** if you manually want to manage the application of a bank statement line that does not have a unique match.
   - Choose **Apply to Oldest** if the bank statement line, for which more than one potential match is found, should automatically be applied to the ledger entry occurring with the earliest posting date.



## To define an application method for a specific vendor

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Vendors**, then select the related link.
1. Open the vendor card, for whom you want to specify an application method.
1. On the vendor card, on the **Payments** FastTab, in the **Application Method** field, use the dropdown arrow to choose how you want payments to be applied in the bank account reconciliation.
   - Choose **Manual** if you manually want to manage the application of a bank statement line that do not have a unique match.
   - Choose **Apply to Oldest** if the bank statement line, for which more than one potential match is found, should automatically be applied to the ledger entry occurring with the earliest posting date.



## To define an application method for a specific employee

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Employees**, then select the related link.
1. Open the employee card, for whom you want to specify an application method.
1. On the employee card, on the **Payments** FastTab, in the **Application Method** field, use the dropdown arrow to choose how payments must be applied in the bank account reconciliation.
   - Choose **Manual** if you manually want to manage the application of a bank statement line that do not have a unique match.
   - Choose **Apply to Oldest** if the bank statement line, for which more than one potential match is found, should automatically be applied to the ledger entry occurring with the earliest posting date. 



## To disable the use of application criteria

Statement Intelligence is set up by default to automatically search for and apply the customer-, vendor- and employee ledger entries when importing a bank account statement. If you disable the automatic search for customers, vendors, and employees, you must manually select which customer, vendor, or employee ledger entries to match with the bank account statement lines.

In addition, Statement Intelligence is also set up to automatically search to find and reconcile bank account ledger entries using the fields **Transaction Date**, **Statement Amount**, and **Difference** from the bank account reconciliation line. If you disable the automatic search, you must manually select the bank account ledger entries to match.

> [!NOTE]
> By default, these settings are enabled. 
> 

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Banks**, and then select the related link.
1. Open the relevant bank for which you want to activate or deactivate the use of application criteria.
1. On the bank card, on the **Statement Intelligence** FastTab, you can specify if you want Statement Intelligence to search for customer-, vendor- or employee matches: <br>
   - **Search for Customer**
   - **Search for Employee**
   - **Search for Vendor**
1. In the **Search for Date/Amount** field, specify if you want Statement Intelligence to automatically find and reconcile bank account ledger entries using the information in the fields: Transaction Date, Statement Amount, and Difference from the bank account reconciliation line.



