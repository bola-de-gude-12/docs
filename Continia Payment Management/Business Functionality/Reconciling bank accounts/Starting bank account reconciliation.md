---
title: Starting bank account reconciliation in Payment Management
description: A guide on how to prepare for reconciliation in Payment Management.
date: 27-11-2024
id: PM-318
lang: en
---

# Starting Bank Account Reconciliation

Before you start using Continia Statement Intelligence for Bank Account Reconciliation, we recommend closing all the open bank account ledger entries. You can select a bank account and make a suggestion for a specific date. This suggestion helps you to close bank entries up to the date when you start using Statement Intelligence. This way, Statement Intelligence searches and matches the relevant bank entries only. For more general information on reconciling bank accounts, refer to the [To fill in bank reconciliation lines with the Suggest lines action](https://learn.microsoft.com/en-us/dynamics365/business-central/bank-how-reconcile-bank-accounts-separately#to-fill-in-bank-reconciliation-lines-with-the-suggest-lines-action) article on Microsoft Learn.

## To close bank entries

Before starting reconciliation, you’ll need to close your bank entries to ensure that old, irrelevant transactions don’t interfere with Statement Intelligence. 

To start bank account reconciliation:

1. On the **Bank Acc. Reconciliation page**, select **Home** > **Suggest Lines**.
2. On the **Suggest Bank Acc. Recon. Lines** dialog box, navigate to the Date fields to select the dates. After selecting OK, all related entries are now moved to the left side. 
3. On the **Bank Acc. Reconciliation** page, select **Match Automatically** to open the **Match Bank Entries** page.
4. Make sure that the total balance amount is filled in the **Statement Ending Balance** field and fill in the **Statement Date**.
   ![Statement Ending Balance](/images/PM365/PM-statement-ending-balance.png)

## To close old statements from Bank Export Data

If you have outdated statements that need to be addressed before starting reconciliation, you can close them using the **Bank Export Data** page. This step ensures your records are clean and up to date.

To close old statements from Bank Export Data:

1. Use the {{search}} icon, search for Bank Export Data and select the related link.
2. On the **Bank Export Data** page, in the left panel, set the following filters to find the data you need: **Bank Account No.** (enter the bank account you want to close records for), **Record Type** (Account Statement), and  **Record Subtype** (Header).
3. After filtering, select the **Imported to Company** cell and on the action bar select **Set Imported to Company**.
