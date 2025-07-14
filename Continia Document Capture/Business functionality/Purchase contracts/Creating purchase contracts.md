---
title: Creating Purchase Contracts
date: 01-10-2024
description: How to create purchase contracts in Document Capture.
id: DC-86
lang: en
---

# Creating Purchase Contracts

Like Continia Document Capture and most other Continia solutions and modules, the Purchase Contracts module is integrated directly into Microsoft Dynamics 365 Business Central, where you can access it using the {{search}} icon or from the **Purchase Contracts** Cue group on the Role Center. You can also use both of these access methods when you create purchase contracts, as described below.

Overall, you can create purchase contracts in the following three ways:

* [From scratch](#to-create-a-purchase-contract-from-scratch), via the **Purchase Contracts** page
* [Based on a purchase document](#to-create-a-purchase-contract-from-a-document), for example from the document journal
* [Based on patterns in your invoice history](@DC-163), detected by artificial intelligence

The first two methods are described in detail below, while the third one is described in [Creating Purchase Contracts Based on Invoice History](@DC-163). In any case, the **Approval Status** of a new purchase contract is set to **Approval Needed** by default – and the **Next Approval Date** is set to **TODAY** to ensure that at least one approval is done.

## To create a purchase contract from scratch

To create a purchase contract from scratch without basing it on an existing purchase document (invoice or credit memo):

1. Choose the {{search}} icon, enter **Purchase Contracts**, and then choose the related link to open the **Purchase Contracts** page.
   > [!NOTE]
   > You can also open this page from the Business Central Role Center: Under **Purchase Contracts**, select the **All** Cue to open it. Note that the page is called **All** when you access it this way, but in all other respects it's identical with the **Purchase Contracts** page.
1. On the action bar, click **New** to open the **Purchase Contract** page.
1. On the **General** FastTab, fill out the fields as needed. Some of the fields deserve special mention here, as they're particularly important to fill out and understand:
  
   <br>
   
   | Field | Description |
   | --- | --- |
   | **Purchaser Code (Approver)** | Enter or select the code of the person you want to approve the contract that you're setting up. |
   | **Price Type** | Specify if the amounts of the contract lines must exactly match the amounts of related invoice/credit memo lines for the invoices/credit memos to be approved automatically (**Fixed Amount**), or if a certain amount variance is acceptable (**Variable Amount**). <br><br> If you select **Variable Amount**, Document Capture uses the values entered under **Max. Allowed Line Variance %** for the relevant lines (on the **Lines** FastTab) to determine if the related invoice/credit memo line amounts are within the allowed variance. If you select **Fixed Amount**, Document Capture disregards any values entered under **Max. Allowed Line Variance %**. |
   | **Invoicing Period Code** | Specify how often you expect invoices/credit memos relating to this contract to be sent by the vendor. Your selection is used for calculating the **Yearly Amount** for each line on the **Lines** FastTab, together with the **Quantity** and **Unit Cost** fields. <div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Note</span></p><p>To create your own period codes, select the field to open the dropdown menu, and then select **+ New**. On the page that opens, fill out the fields as required. Under **Period Date Formula**, your entry must be an integer followed by <b>D</b> (days), <b>WD</b> (weekdays), <b>W</b> (weeks), <b>M</b> (months), <b>Q</b> (quarters), or <b>Y</b> (years) – for example, <b>2W</b> (two weeks). <br><br> On the same page, you can also specify how often the contract must be reviewed, by editing the <b>Approval Frequency</b> field. If you select <b>Date Formula</b> here, enter the formula under <b>Approval Frequency Date Formula</b>, using the guidelines mentioned above. Whatever you enter in these two fields is autofilled in the corresponding fields on the <b>Approvals</b> FastTab (see step 4 below).</p></div> |
   | **Auto Approve Within Variance** | Select **Yes** if you want Document Capture to automatically approve invoices/credit memos when they've been registered, provided that the invoice/credit memo line amounts match the corresponding contract line amounts within the variance defined under **Max. Allowed Line Variance %** on the **Lines** FastTab. <br><br> The following rules apply, depending on whether you select **Yes** or **No**: <ul><li><b>Yes</b>: If you've selected <b>Fixed Amount</b> under <b>Price Type</b> and/or entered no value under <b>Max. Allowed Line Variance %</b>, the invoice/credit memo line amounts must match the contract line amounts exactly in order for the invoices/credit memos to be automatically approved.</li><li><b>No</b>: If you've selected <b>Variable Amount</b> under <b>Price Type</b> and/or entered a value under <b>Max. Allowed Line Variance %</b>, these settings will be disregarded entirely.</li></ul> |
1. On the **Approvals** FastTab, fill out the fields as needed:
  
     > [!NOTE]
     > The **Approvals** FastTab is only shown if **Enable Purchase Contract Approval** is enabled on the **Purchase Contract Setup** page.
  
   <br>
   
   | Field | Description |
   | --- | --- |
   | **Approval Frequency** | Specify how often the contract must be approved. The default option is **Yearly**, unless you've edited this in the **Invoicing Period Code** field in step 3 – any changes you make to the **Approval Frequency** and **Approval Frequency Date Formula** fields under **Invoicing Period Code** are autofilled here. <div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Note</span></p><p>If you select <b>Date Formula</b>, the <b>Approval Frequency Date Formula</b> field appears. Here, you must enter a formula in the form of an integer followed by <b>D</b> (days), <b>WD</b> (weekdays), <b>W</b> (weeks), <b>M</b> (months), <b>Q</b> (quarters), or <b>Y</b> (years) – for example, <b>2W</b> (two weeks). For more advanced formulas, you can also use the mathematical symbols + and –, or you can enter the letter <b>C</b> (current) as a prefix to any of the previously mentioned time units – for example, <b>CM+10D</b> (current month plus ten days).</p></div> |
   | **Next Approval Date** | Specifies when the contract should be approved next. The default value of this field for a new contract is **Today**, which ensures that the contract is approved after being created. Afterward, the value of this field depends on what you selected under **Approval Frequency**. For example, if you selected **Yearly**, the default value is the the previous **Next Approval Date** value plus one year. |
1. On the **Lines** FastTab, enter the lines that you expect to find in the invoices/credit memos you receive from the vendor, by filling out all fields as needed. The following fields deserve special mention:
  
   <br>
   
   | Field | Description |
   | --- | --- |
   | **Type** | Select the type of account that you want to be associated with this line. |
   | **No.** | Select the account number that you want to be associated with this line. |
   | **End Date** | Specifies the end date of the purchase contract that's represented by the line. If a date appears in the **Contract End Date** field on the **General** FastTab, this date is autopopulated to the **End Date** field. If not, you can enter a date manually. Together with the **Start Date** field, **End Date** marks the interval that all linked purchase documents must be posted within. <div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Note</span></p><p>If any purchase document that's linked to this purchase contract line has a posting date that's outside the start and end date interval, an error message is displayed. <br><br> Similarly, if you edit the **Invoice Date** field in the document journal for a purchase document that's linked to a purchase contract line, an error message is displayed in the **Comments** section of the document journal if the new date is outside the start and end date interval of the contract line. </p></div> |
   | **Unit Cost** | When you fill out this field, the **Amount Excl. VAT** and **Yearly Amount** fields (which are both uneditable) are autofilled based on what you entered. Likewise, the two fields are autofilled if you edit the **Quantity** field. The value of the **Yearly Amount** field is also based on your selection in the **Invoicing Period Code** field on the **General** FastTab. |
   | **Max. Allowed Line Variance %** | If you enter a percentage here, invoice/credit memo line amounts are automatically approved if they match the contract line amounts within the entered variance percentage. <br> <div class="alarm alarm-important"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Important</span></p><p>This only applies if the following two settings have been set on the <b>General</b> FastTab: <b>Price Type</b> must be set to <b>Variable Amount</b>, and <b>Auto Approve Within Variance</b> must be set to <b>Yes</b>.</p></div> |

## To create a purchase contract from a document

You can create purchase contracts from a document in two ways: with line recognition disabled or enabled in the relevant template. No matter which of the methods you choose, the following two values are automatically added to the **Document Header** section of the document journal when you finish the relevant guide:
*   In the **Type** field, the value **Purchase Contract** is added.
*   In the **No.** field, the contract number is added.

To create a purchase contract from the document journal:

1. Search ({{search}}) for and select **Document Categories**.

1. Select the **PURCHASE** code to open the document journal.

1. In the list of documents, select the invoice/credit memo that you want to use as a basis for your purchase contract.

1. If there's no template associated with the invoice/credit memo, you must assign one by activating field recognition: On the action bar, click **Process** > **Recognize Fields**.

1. On the action bar, click **Purchase Contract** > **Create Purchase Contract** to open the **Create Purchase Contract** page.
   > [!NOTE]
   > The following fields on the **Create Purchase Contract** page are autofilled, mostly with data from the header of the selected invoice/credit memo:
   >
   >   * **Description** is autofilled with the **Posting Description** value.
   >   * **Purchaser Code** is autofilled with the **Our Contact** value.
   >   * **Approval Frequency** is autofilled with the default option **Yearly**.

1. If necessary, edit the autofilled fields, and fill out the remaining fields as required.

1. **Optional:** If line recognition is enabled, select the link below the **Prices Including VAT** field to open the **Assigned Amount Lines** page. Here you can review the amounts in the document, and edit the related **Type** and **No.** fields. It's also possible to create a single contract line with the total amount of the invoice/credit memo, and the specified account type and number. This line can be edited later, if necessary.

1. **Optional:** Enable the **Configure purchase contract as the default account** setting to set the created purchase contract as the default account on the template level.

1. Select **OK** to close the page and create the contract.

If **Open Purchase Contract** is enabled on the **Create Purchase Contract** page, the purchase contract opens – allowing you to make any necessary changes and fill out additional fields. For a description of this process, see steps 3-5 in the [guide above](#to-create-a-purchase-contract-from-scratch). You must use this method if you want to [create contract invoices](@DC-88) based on this contract.

## Related information

[Creating Purchase Contracts Based on Invoice History](@DC-163)  
[Purchase Contract Approvals](@DC-87)  
[Creating Contract Invoices](@DC-88)  
[Approving Contract Invoices](@DC-89)  
[Viewing the Purchase Contract Archive](@DC-90)  







<style>
  .content table tr td:nth-child(1) {
    width: 120px;
  }
  .content table tr td:nth-child(2) {
    width: 610px;
  }  
</style>