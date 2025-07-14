---
title: The Bank Account Reconciliation page in Continia Banking
description: Learn how to reconcile bank statement lines using the Bank Account Reconciliation page.
date: 30-01-2025	
id: CB-22
lang: en
---

# The Bank Account Reconciliation Page

After importing bank account statements, Continia Banking converts the bank's file format to list all the required information for reconciling your bank account on the Bank Account Reconciliation page. This article describes the available fields on this page. For details on how to reconcile bank statement lines, refer to the [Reconciling Bank Statements](@CB-18) article. 

## The general settings of the Bank Acc Reconciliation page

On the **General** FastTab, within the **Related Lines in Journal** section, Continia Banking provides easy access to related journal lines by displaying the number of entries automatically created during bank account reconciliation. The sections lists the entries found in the cash receipt journal, the general journal, and the payment journal.

The table below outlines the function of the columns added by Continia Banking to the Bank Statement Lines section on the Bank Account Reconciliation page:

| **Column**       | **Description**                                              |
| ---------------- | ------------------------------------------------------------ |
| Status           | Specifies the reconciliation status of the chosen bank statement line. For details on the different statuses and their meaning, refer to the [The Reconciliation Statuses in the Bank Acc Reconciliation](@CB-107) article. |
| Proposals        | Specifies the number of possible matches found in the ledger entries for the selected bank statement line. Select the number to open the Payment Application Review page. On this page, you will find automated recommendations for matching the bank statement line to an open ledger entry. For details on how to work with proposals, refer to the [Working with Payment Application Proposals](@CB-19) article. |
| Details          | Select to view specific payment-related information associated with the selected bank statement line. By clicking this option, you can access and edit detailed data crucial for reconciliation, including account specifics and ledger entries. You can also add information or add a search rule directly, which helps with reconciling the bank statement efficiently. |
| Difference Lines | Indicates how many lines have been created to handle amount differences related to the bank statement line. |

> [!NOTE]
> To display more columns for more details, on the action bar, select **Related** > **Page** > **Show more columns**.



## The actions available on the Bank Acc. Reconciliation page

The Bank Acc. Reconciliation page offers a range of actions designed to simplify and streamline the reconciliation of your bank accounts. These actions enable you to import bank statements, manage reconciliation entries, and perform various operations to ensure that bank records are accurately reflected in the system. Below is a summary of the key actions available on the page, along with the procedures to execute them effectively.

| Action                                      | Procedure                                                    |
| ------------------------------------------- | ------------------------------------------------------------ |
| To import a bank statement                  | On the **Bank Acc. Reconciliation** page, on the Home tab, select **Import Bank Statement**. <br />For more information, refer to the [Importing a bank statement manually](@CB-86) article. |
| To match lines manually                     | On the **Bank Acc. Reconciliation** page, navigate to an unsolved line and on the action bar, select **Matching** > **Match Manually**.<br />For more information, refer to the [Matching bank statement lines manually](@CB-25) article. |
| To work with application proposals          | On the **Bank Acc. Reconciliation** page, navigate to the line and in the **Proposals** column, select the number. Alternatively, select the line, and on **Home** tab, select **Application Proposals**. <br />For more information, refer to the [Working with payment application proposals](@CB-19) article. |
| To apply entries                            | On the **Bank Acc. Reconciliation** page, on **Home** tab, select to apply or remove a proposal. You can select multiple lines and apply actions to all of them. |
| To transfer amount differences to journals  | On the Bank Acc. Reconciliation Page, on the **Home** tab, select **Transfer Difference to Journal**. |
| To set manual handling                      | On the **Bank Account Reconciliation** page, navigate to an unsolved line and on the action bar, select **Matching** > **Match Manually**.<br />For more information, refer to the [Importing a bank statement manually](@CB-86) article. |
| To create a journal line manually           | On the **Bank Acc. Reconciliation** page, on the action bar, select **Manual Application** > **Create Manual Journal Line.** |
| To create a journal line from a search rule | On the **Bank Acc. Reconciliation** page, on the **Home** tab, select **Create journal line from search rule** action. For more information, refer to the [Introducing Search Rules](@CB-87) article. |
| To show more columns                        | On the **Back Account Reconciliation** page, on the **Page** tab, select **Show More Columns** or **Show Fewer Columns**. This allows you to get more detailed information. |
| To delete and set as Imported               | On the  **Back Account Reconciliation** page, on the **Actions** tab, select **Functions** and select **Delete and set as Imported**. This will allow you to delete the lines in the journal and mark it as already processed. |
| View data imported from the bank            | On the  **Back Account Reconciliation** page, on the **Related** tab, select **Show Bank Transaction**. |























<style>

 .content table tr td:nth-child(1) {

 width: 200px;

 }

 .content table tr td:nth-child(2) {

 width: 600px;

 }

</style>
