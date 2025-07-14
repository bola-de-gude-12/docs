---
title: Reconciliation FAQ
date: 27-05-2024
description: Find the answer to frequently asked questions about reconciliation
id: PM-369
lang: en
---

# Reconciliation FAQ

## How can I fix the account statement import error?

If you experience difficulties with the account statement import while reconciling the bank account and receive the following error message:

`The import process was interrupted`

The error message you encountered indicates a mismatch between starting and ending balances of the statements, triggered during an attempt to import multiple statements. Possible reasons for this interruption include files being imported in the wrong order or corrected/deleted lines in previously imported statements. Here's how to resolve the issue:

**Identify discrepancies**:

To find out what statement is causing the error, you can use a filter to display the account statements available in the system for the account that you are trying to import:

1. Go to **Bank Export Data**, and set the following filter:
   * **Record Type**: Accounts Statement
   * **Record Subtype**: Header
   * **IBAN/BBAN**: enter the account number with a preceding asterisk: *account number
2. Verify the starting and ending balance columns. Normally, the ending balance of the previous account statement should match the starting balance of the subsequent statement. If there is a discrepancy, it is likely to be the cause of the error.

   > [!TIP]
   >
   > If you want to know date range covered by a specific account statement, select the corresponding header line and remove the **Record Subtype** filter.

**Resolve mix-ups**:

Once you detected the statement that caused the error, such as a duplicated or old statement, you can modify Statement Intelligence to import multiple bank account statements in the same reconciliation manually: 

1. To manually import multiple bank account statements into the same reconciliation, go to **Statement Intelligence Setup** and apply the following settings:

   * **Multiple Bank Statements** - enabled
   * **Create New Reconciliation** - disabled
   * **Import all Available Statements** - disabled

2. Import the statements one at a time until you identify the misplaced account statement.
3. Create a new reconciliation, select **Import** and delete the misplaced statement. Mark it as *imported* before importing the next statement.

For more information about reconciliation processes, refer to the [Importing and Reconciling Bank Statements](@PM-48) article.

## How can I solve an error in the payment journal or purchase invoice?
If you can't export payments, post invoices, or send approval requests, it's important to understand that the errors you see in the Payment File Error FactBox (payment journal) and the Validation FactBox (purchase invoice) are validation errors and not actual errors in Payment Management. 

![Payment file error FactBox](/images/PM365/Payment-file-error.png)

Validation errors can occur in different scenarios, such as incomplete data, exceeding specified limits, or not meeting specific criteria set by the bank you want to transfer money from (the balance account). For example, you may encounter error messages indicating that:

* The payment method you have defined is not supported by your bank.
* The country code on the vendor bank account does not match the vendor IBAN.
* The bank account number must be numerical.
* The Purchase Header must have a value in Balance Account No.

## How can I solve a timestamp error?
If you are trying to post a purchase document and get the following error:

` Maximum 16 characters are allowed in timestamp `

This error typically occurs when the payment journal generates a value that references a field that does not exist in the purchase document undergoing validation. These fields usually include the **Sender Reference** or **Recipient Reference** fields.

To solve this issue:

1. **Check whether the Sender Reference Template Code has been defined** - fix the error by choosing another sender reference definition code: SEND-REF3. To do this, go to the **Bank Account Card**, and on the **Transfer** FastTab, navigate to the **Sender Reference Template Code** field and select *SEND-REF3*.

2. **Check whether the Recipient Reference Template Code has been defined** -  verify if it is the recipient reference or external document number that exceeds the permissible character count. If so, create a new reference code that accommodates a shorter character length. To do this, go to the **Payment Notification Setup** and add a template for the short notification. Go to the **Recipient Reference Template** field, and on the **Template Field Property** page, set the length for the **External Document No.**.

   



