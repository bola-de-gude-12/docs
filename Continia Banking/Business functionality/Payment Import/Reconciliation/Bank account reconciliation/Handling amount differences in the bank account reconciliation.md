---
title: Handling Amount Differences in Bank Account Reconciliation
description: How to identify and handle amount differences in the Bank Account Reconciliation
date: 13-09-2024
id: CB-140
lang: en
---

# Handling amount differences in the bank account reconciliation

When performing a bank account reconciliation, you may encounter lines where there are amount differences. These differences are flagged with a status *Difference*, indicating that further action is needed to resolve the discrepancy. 

In the Bank Account Reconciliation journal, you can resolve these differences by either applying the amount to a ledger entry or using predefined settings for handling differences. 

## To configure settings for handling differences automatically

Continia Banking lets you use predefined settings for handling differences. These settings can reduce manual intervention by determining how the system processes amount differences. Here are the key options available:

- **Show Dialog** - in the [Banking Import Setup](@CB-14), there is a choice to enable or disable a dialog that appears when handling discrepancies in amounts. If this option is disabled and an account for amount differences is set up, the dialog will not be displayed, and the system will automatically handle the difference.
  
- **Default Account Type** - in the Banking Import Setup, you can define the default journal template type used for handling differences. The account type for amount difference lines is determined based on the account type of the bank statement or payment reconciliation line. By default, the account type from the bank statement or payment reconciliation line is used but this can be adjusted in the difference-handling dialog.
  
- **Default Account No.** - in the Banking Import Setup, you can specify the account no. to use when creating lines for amount differences.  This account will be automatically applied when resolving discrepancies.

  > [!NOTE]
  >
  > When you want to use a G/L Account No. for handling differences, make sure that the account permits direct posting.

- **Default Journal Template Type** - In the Banking Import Setup, you can define what type of journal template to use for the difference.

- **Posting Description Template** - in the Banking Import Setup, you can specify a posting description template to provide a consistent description when handling amount differences.

- **Search Rules** - if specific accounts for amount differences are needed, they can be set up within the search rules. These settings mirror those in the Banking Import Setup.


## To handle amount differences in the journals

Once the amount difference is recognized, you can transfer the difference to a journal and post it. 

You can decide to post both the journal lines for the entries being reconciled and the journal line for the amount difference simultaneously.

To transfer the difference to a journal:

- Select **Home** > **Transfer Difference To Journal**. 
- On the Transfer Difference to Account dialog enter the needed information and select **OK**.

To post all lines:

* Select **Home** > **Journals** > **Post All Journal Lines**. 

Alternatively, users can post each journal line individually in their respective journals.

To post lines individually for each bank statement or payment reconciliation line:

1. Select the line and select **Home** > **Application Proposals**
2. Select **Post Journals** on the notification on the **Payment Application Review Page**.

