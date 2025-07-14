---
title: Importing bank statements with Continia Banking
description: Learn more about the import procedure, changing import settings, reviewing and managing imported data, and how to use search text.
date: 31-03-2025	
id: CB-17
lang: en
---


# Managing the import of bank account statements

Continia Banking has implemented an advanced process for importing data into the Bank Account Reconciliation or the Payment Reconciliation Journal. This approach enhances the reconciliation workflow by substituting the standard import actions with a more efficient, tailored solution.

On the **Banking Import Setup** page, you can decide which entries can automatically match, set limits for payment proposal variances, and specify the minimum details required for accurate matching. For more information on the settings of the **Banking Import Setup** page, refer to the [Configuring import settings](@CB-14) article.

## The import procedure

The import procedure begins by either showing a browse dialog or downloading the file directly from the bank, depending on the bank account setup. Once the account statement is imported, Continia Online converts the files and saves them in the file archive. Then, it imports the converted files into the [Bank Account Reconciliation](@CB-22) and [Payment Reconciliation Journal](@CB-106). During this conversion, the system stores data in various tables based on the type and location of the information in the bank statement.

- **Bank transaction header** - contains data related to the entire statement file, such as the creation date, unique file ID, balance, and totals.
- **Bank transaction line** - includes details about each transaction, including date, description, currency information, and amounts.
- **Bank transaction detail** - stores additional unstructured information related to transaction lines, accessible from the reconciliation pages.
- **Bank transaction interest** - contains information about interests associated with transaction lines.
- **Bank transaction charge** - records information about charges related to transaction lines.

## To use search text

In case a bank account statement is imported to the bank transaction tables but cannot be imported into the Bank Account Reconciliation or Payment Reconciliation Journal it may be due to a mismatch in account information. To resolve this, you can add a search term on the Bank Account Card to help identify the correct bank account. For example, enter the IBAN or BBAN of the bank account and try the import again. 

## To show more columns

Within the **Bank Transaction Card** page, there is an option to invoke an action and access more information about the statement or the individual transaction lines. Go to the **Page** tab and select **Show More Columns** or **Show Fewer Columns** to expand or reduce the available columns. For more information, refer to the [Bank Account Reconciliation Page](@CB-22) article. 

## To show more actions

On the **Bank Account Reconciliation** and **Payment Reconciliation Journal** pages, go to the **Page** tab and select **Show More Actions** or **Show Fewer Actions** to expand or reduce the available options.

## To manage imported data

From both the Bank Account Reconciliation and Payment Reconciliation Journal pages, users can access several actions to manage and review source data. These actions help address discrepancies, such as duplicate bank statement imports, or provide insights into bank transactions and their associated companies.

### Delete and set as Imported

This action lets you delete the current reconciliation while marking the data as imported, preventing it from being re-imported.

- **Bank Account Reconciliation** page - on the action bar, select **Actions** > **Functions** > **Delete and set as Imported.** 
- **Payment Reconciliation Journal** page - on the action bar, select **Related** > **Details** > **Delete and set as Imported**. 

This action can be reversed on the **Bank Transactions** page.

### Show Bank Transaction 

Use this action to get an overview of the source data for a specific reconciliation, including headers and transaction lines.

- **Payment Reconciliation Journal** page - on the action bar, selected **Related** > **Details Show Bank Transactions**.
- **Bank Account Reconciliation** page - on the action bar, select **Related** > **Show Bank Transactions**.

### Set Imported to Company

From the **Bank Transactions** page, users can mark a bank statement as already imported using the **Set Imported to Company** action, preventing duplicate imports. If necessary, this action can be reversed using the **Remove Imported to Company** option, allowing the data to be re-imported.

### Remove Imported to Company

If you accidentally removed a reconciliation line, go to the **Bank Transactions - Continia Banking** page, locate the specific line, and use the **Remove Imported to Company** action. This allows the line to be restored in the reconciliation by re-importing it.

## To change the import settings

In bank account statements, the placement of transaction descriptions varies depending on the bank, requiring users to configure the data source. Users can set up the field to be used as the statement description from the Bank Transaction Line table. In Bank Account Reconciliation, this data is moved to the **Description** field, and in the Payment Reconciliation Journal, it is moved to the **Transaction Text** field.

Users can create or select a bank statement description template, similar to the process for Search Field Templates or Posting Description Templates. During installation, the system sets up predefined templates by default. If no template is assigned in the **Banking Import Setup**, the system will use the Posting Description from the Bank Transaction Line table by default. This setup is multi-level and can be configured on the **Banking Import Setup** Page and the **Bank Account Card** page. If not specified on the Bank Account, the default from the Import Setup is used.
