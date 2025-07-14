---
title: Reconciling bank statements on the Bank Account Reconciliation Page
description: How to import and reconcile bank account statements on the Bank Account Reconciliation page.
date: 17-03-2025	
id: CB-18
lang: en
---

# Managing reconciliation on the Bank Account Reconciliation page

Once bank account statements are imported, the bank's file format is converted to list all the information needed to reconcile your bank account. Continia Banking ensures accurate matching by aligning the statement lines with your bank account's ledger entries. Additionally, it prepares accounts receivable for matching and generates proposals for potential matches.

Before you start using Continia Banking for bank account reconciliation, we recommend closing the open bank account ledger entries. Select a bank account and suggest a specific date to close entries, to ensure that Continia Banking focuses on relevant bank transactions from that point onward. To close all open bank entries, refer to the [To fill in bank reconciliation lines with the Suggest lines action](https://learn.microsoft.com/en-us/dynamics365/business-central/bank-how-reconcile-bank-accounts-separately#to-fill-in-bank-reconciliation-lines-with-the-suggest-lines-action) article on Microsoft Learn.

To initiate a bank account reconciliation:

1. Search ({{search}}) for and select **Bank Account Reconciliations**.

2. Select **New**.

3. Navigate to the **Bank Account No.** field and assign a bank account.

4. On the bank account reconciliation page, navigate to the action bar and select **Bank** > **Import Bank Statement**. 

5. To import the statement and initiate the reconciliation process, a dialog box will appear, either prompting the user to select a file or providing information related to communication with the bank. The content of the dialog depends on whether the bank account uses direct communication or not.

6. On the action bar, select **Matching** > **Match Automatically**.

7. On the left side is an overview of statement lines received from the bank. The next step is to match the lines on the left side with the lines on the right side. The lines will be matched based on the setup of Continia Banking Import. You can use **Status** on the account statement lines to get started. For an overview of the statuses, their meaning, and the appropriate action to take, refer to the [Reconciliation Statuses](@CB-107) article. 

   > [!TIP]
   >
   > Use the reconciliation information at the bottom of the page to see if the entire statement line amount has been applied or if there is a difference that still needs to be applied.
   
   

## Related information

For general information on reconciliation with Business Central, refer to Microsoft Learn:

* [Reconcile bank accounts](https://learn.microsoft.com/en-us/dynamics365/business-central/bank-how-reconcile-bank-accounts-separately)
* [Reconcile Payments Using Automatic Application](https://learn.microsoft.com/en-us/dynamics365/business-central/receivables-how-reconcile-payments-auto-application)
