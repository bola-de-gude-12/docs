---
title: Creating purchase contracts
date: 08-07-2025
description:  
id: EM-131
lang: en
---

# Creating purchase contracts

Similar to Continia Expense Management and most other Continia solutions and modules, the Purchase Contracts module integrates directly with Microsoft Dynamics 365 Business Central. Access it by using the Search {{search}} icon when you want to create purchase contracts.

You can create purchase contracts in two ways:

* [From scratch](#create-a-new-purchase-contract), via the **Purchase Contracts** page
* [Based on an expense](#create-a-purchase-contract-from-an-expense)

The method you use depends on your requirements and the page you're navigating from. Both methods are described in detail below.

## Create a new purchase contract

You can create a purchase contract from scratch, without basing it on an existing expense.

To create a new purchase contract:

1. Search {{search}} for **Purchase Contracts**.
   > [!NOTE]
   > You can also open this page from the Business Central Role Center: Under **Continia Expense Management Activities** > **Purchase Contracts** >  **All**.
1. On the action bar, click **New** to open the **Purchase Contract** page.
1. Under **General**, fill in the fields as needed. Refer to the following table to understand the different fields. 
  
   | Field | Description |
   | --- | --- |
   | **Purchaser Code (Reviewer)** | Enter or select the code of the person you want to review the contract that you're setting up. |
   | **Price Type** | Specify whether the amounts of the contract lines must *exactly* match the amounts of related expenses for the expenses to be approved automatically (**Fixed Amount**), or if a certain amount variance is acceptable (**Variable Amount**). <br>Selecting **Variable Amount** instructs Expense Management to use the values entered under **Max. Allowed Line Variance %** for the relevant lines (under **Lines**) to determine if the related expense amount is within the allowed variance. Selecting **Fixed Amount** instructs Expense Management to disregard any values entered under **Max. Allowed Line Variance %**. |
   | **Invoicing Period Code** | Specify how often you expect expenses relating to this contract to be sent by the employees. Your selection is used for calculating the **Yearly Amount** for each line under **Lines**, together with the **Quantity** and **Unit Cost** fields. <div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Note</span></p><p>You can create your own period codes by  opening the drop-down menu of the field, and selecting **+ New**. Next, fill in the fields as required. Under **Period Date Formula**, your entry must be an integer followed by <b>D</b> (days), <b>W</b> (weeks), <b>M</b> (months), <b>Q</b> (quarters), or <b>Y</b> (years) – for example, <b>2W</b> (two weeks). <br>You can also specify how often the contract must be reviewed, by editing the <b>Approval Frequency</b> field. If you select <b>Date Formula</b>, enter the formula under <b>Review Date Formula</b>, using the above guidelines. The information you enter in these two fields is auto filled in the corresponding fields under <b>Review</b> in step 4 below.</p></div> |
   | **Auto Approve Within Variance** | If you want Expense Management to automatically approve expenses, where the amount matches the corresponding contract line amount within the variance defined under **Max. Allowed Line Variance %** under **Lines**, select **Yes**. <br>Depending on whether you select **Yes** or **No**, the following rules apply: <ul><li><b>Yes</b>: If you selected <b>Fixed Amount</b> under <b>Price Type</b> and/or entered no value under <b>Max. Allowed Line Variance %</b>, the expense amount must match the contract line amount exactly for the expense to be automatically approved.</li><li><b>No</b>: If you selected <b>Variable Amount</b> under <b>Price Type</b> and/or entered a value under <b>Max. Allowed Line Variance %</b>, these settings will be disregarded.</li></ul> |
1. Under **Approvals**, fill in the fields as needed. Refer to the following table to understand the different fields. 
  
   | Field | Description |
   | --- | --- |
   | **Approval Frequency** | Specify how often the contract must be reviewed. The default option is yearly. However you can change this in the **Approval Frequency** drop-down menu. Any changes you make to the **Approval Frequency** and **Approval Frequency Date Formula** fields under **Invoicing Period Code** are auto filled in this field. <div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Note</span></p><p>If you select <b>Date Formula</b> from the drop-down menu, the <b>Approval Frequency Date Formula</b> field appears. Enter a formula in the form of an integer followed by <b>D</b> (days), <b>W</b> (weeks), <b>M</b> (months), <b>Q</b> (quarters), or <b>Y</b> (years) – for example, <b>2W</b> (two weeks). For more advanced formulas, you can also use + and –, or you can enter the letter <b>C</b> (current) as a prefix to any of the previously mentioned time units, for example, <b>CM+10D</b> (current month plus ten days).</p></div> |
   | **Next Approval Date** | Specify when the contract should be reviewed next. The default value depends on what you selected under **Approval Frequency**. For example, if you selected yearly, the default value is the contract start date plus a year, minus one month. |
1. Under **Lines**, create a line for each employee that you expect to receive an expense, by filling in all fields as needed. Refer to the following table to understand the different fields. 
  
   | Field | Description |
   | --- | --- |
   | **Expense user** | Select the expense user that you want to be associated with this line. |
   | **Unit Cost** | The **Amount Excl. VAT** and **Yearly Amount** fields (which are both uneditable) are auto filled based on the information you enter in the **Unit Cost** field. The same two fields are also auto filled if you edit the **Quantity** field. <br />The value of the **Yearly Amount** field is based on your selection in the **Invoicing Period Code** field under **General**. |
   | **Max. Allowed Line Variance %** | The expense amount is automatically approved if it matches the contract line amount within the percentage variance that you enter in this field. <br> <div class="alarm alarm-important"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Important</span></p><p>This only applies if  under <b>General</b>, you have set <b>Price Type</b> to <b>Variable Amount</b>, and <b>Auto Approve Within Variance</b> to <b>Yes</b>.</p></div> |

## Create a purchase contract from an expense

Another way to create a purchase contract is to create one from an expense.

To create a purchase contract from an expense:

1. Search for {{search}} **Expenses**.

1. In the list of expenses, select the expense that you want to use as a basis for your purchase contract.

1. Click **Edit**.

1. On the action bar, click **Actions** > **Purchase Contracts** > **Create Purchase Contract** (this opens the **Create Purchase Contract** page).
   > [!NOTE]
   > The following fields auto fill with data from the header of the selected expense:
   >
   >   * **Description** auto fills with the **Description** value from the expense.
   >   * **Purchaser Code (Reviewer)** auto fills with the **Salesperson/Purchaser** value from **Expense Approver ID** on the **Continia User Setup** page.
   >   * **Approval Frequency** auto fills with the default option **Yearly**.
   >   * **Vendor No.** auto fills with the **Vendor No.** from the expense.

1. Check the auto filled fields and edit if necessary, then fill in the remaining fields as required.

1. Click **OK** to close the page and create the contract.

This opens the contract on the **Purchase Contract** page, where you can make any necessary changes and fill in additional fields. For a detailed description of this process, see steps 3-5 in the above section.

### Add an expense to an existing contract

Adding an expense to an existing purchase contract is also an option.

To add an expense:

1. Search for {{search}} **Expenses**.
1. In the list of expenses, select the expense that you want to use as a basis for your purchase contract.
1. Click **Edit**.
1. Under **Purchase Contracts**, in the **Purchase Contract No.** field, select the contract that you want to add the expense to.
1. Under **Purchase Contracts**, in the **Purchase Contract Line No.** field, click the menu (...) icon to see the dialogue that asks whether you want to create a new contract line based on this expense or not. Choose **Yes** to create a contract line.
   > [!NOTE]
   > If the contract already has a line for this employee, you can choose from a list that shows contract lines filtered by this employee number.

## Related information

[Purchase Contract Reviews](@EM-132)  
[Approving Expenses Based on a Contract](@EM-133)  
[Viewing the Purchase Contract Archive](@EM-134)  







<style>
  .content table tr td:nth-child(1) {
    width: 120px;
  }
  .content table tr td:nth-child(2) {
    width: 610px;
  }  
</style>