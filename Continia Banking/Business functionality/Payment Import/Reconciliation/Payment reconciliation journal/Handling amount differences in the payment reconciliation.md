---
title: Handling Amount Differences in Payment Reconciliation Journal
description: How to identify and handle amount differences in the Payment Reconciliation Journal
date: 01-10-2024
id: CB-141
lang: en
---

# Handling Amount Differences in the Payment Reconciliation Journal

When performing a bank account reconciliation, you may encounter lines where there are amount differences. These differences are flagged with a status *Difference*, indicating that further action is needed to resolve the discrepancy. 

In the Payment Reconciliation Journal, you handle amount differences directly in the journal.

## To configure settings for handling differences automatically

Continia Banking lets you use predefined settings for handling differences. These settings can reduce manual intervention by determining how the system processes amount differences. Here are the key options available:

- **Show Dialog** - in the [Banking Import Setup](@CB-14), there is a choice to enable or disable a dialog that appears when handling discrepancies in amounts. If this option is disabled and an account for amount differences is set up, the dialog will not be displayed, and the system will automatically handle the difference.
  
- **Default Account Type** - in the Banking Import Setup, you can define the default journal template type used for handling differences. The account type for amount difference lines is determined based on the account type of the bank statement or payment reconciliation line. By default, the account type from the Bank Account Reconciliation line is used but this can be adjusted in the difference-handling dialog.
  
- **Default Account No.** - in the Banking Import Setup, you can specify the account no. to use when creating lines for amount differences.  This account will be automatically applied when resolving discrepancies.

  > [!NOTE]
  >
  > When you want to use a G/L Account No. for handling differences, make sure that the account permits direct posting.

- **Posting Description Template** - in the Banking Import Setup, you can specify a posting description template to provide a consistent description when handling amount differences.

- **Search Rules** - if specific accounts for amount differences are needed, they can be set up within the search rules. These settings mirror those in the Banking Import Setup.


## To handle amount differences in the Payment Reconciliation Journal

In the Payment Reconciliation Journal, amount differences are managed by transferring them into new reconciliation lines. The system creates new, indented lines under the main reconciliation line, adjusting the transaction amount accordingly.

To handle amount differences in the Payment Reconciliation Journal:

* Once a line has status *Difference*, you can do the following:

  * In Payment Reconciliation Journal, select the line and select **Manual Application** > **Transfer Difference to Account**. 

  * On the **Transfer Difference to Account** dialog enter the needed information and select **OK**.
