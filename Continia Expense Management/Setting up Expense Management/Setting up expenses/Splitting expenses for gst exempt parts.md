---
title: Splitting Expenses for GST-Exempt Parts (AU)
date: 23-04-2025
description: 
id: EM-215
lang: en
---
# Splitting Expenses for GST-Exempt Parts (AU)

This guide explains how to enable GST (Government Stamp Duty) calculations in the Australian version of Continia Expense Management. After setup, GST will be calculated automatically and split into multiple lines when submitting expenses with the configured expense types through the Continia Expense App or the Continia Expense Portal.

You would typically split expenses according to whether they attract GST or not. For example, in Australia, unprocessed food does not attract GST, whereas processed food does. Therefore, if an expense user receives an invoice from a company, such as a supermarket, the receipt may have a mix of lines that attract GST and lines that don't. Usually it's only the FOOD expense type that needs to cater for such mixed receipts.

When you're done setting this up, expenses will automatically be allocated to different lines based on the GST posting setup tax percentage.

## Prerequisites
The following is required to be able to set up automatic distribution of GST into multiple lines in the Australian version of Continia Expense Management:

* Make sure you run an AU installation of Expense Management 12.1 or newer.
* The **Enable Amount Distribution** setting is enabled in **Expense Management Setup** in the **Expenses** FastTab.
* A field type with the field code **AMOUNT INCLUDING TAX**. This is a standard field in Expense Management, and you can use the guide [Setting Up Fields](@EM-80) to add it to the **Configured Fields** page so that expense users can see and use it. We recommend renaming this field to: **TAXABLE AMOUNT INCLUDING TAX**.
* A new expense type set up for the purpose of GST posting. When naming the expense type, giving it name such as 'GST Free' will make it easier to find. Follow the guide [Setting up Expense Types](@EM-41).

## To set up GST split and allocation

For the GST free expense type you've set up, you need to configure a setting that only exists in the AU version of Expense Management.

1. Search {{search}} for **Expense Types**, then choose the relevant link. 
1. Select your GST free expense type, then select **Setup** on the action bar.
1. In **GST Prod. Posting Group**, choose **NON GST** from the dropdown menu.

Next, set up a distribution code on an expense type.

1. Search {{search}} for **Expense Types**, then choose the relevant link. 
1. On the action bar, select **Edit List**.
1. Select an expense type.
1. In the **Distribution Code** field, select **New** from the dropdown menu, and create a new distribution code by filling in the following fields:
   * **Distribution Code** - The name of the distribution code.
   * **Description** - A short description of the distribution code.
   * **Distribute By Tax Amount** - Check to allocate automatically based on a pre-defined tax percentage. The expense will be distributed into a taxable and a non-taxable allocation. This field is *only* visible if the field type **Amount Including Tax** has been added.

For a GST expense type it's tempting to include a field that includes the GST Amount. However, we recommend that you hide such a field and set up a field type dependency instead.

To hide the **Amount including GST field**:

1. Search {{search}} for **Configured Fields**, then choose the relevant link.
1. In the field types table, in the **Field description** column, find the field **Amount including GST**. You can choose to make this field hidden, editable, or mandatory. We recommend that you hide the **Amount Including GST** field by default by selecting the checkbox for **Hide Visibility by Default**.

Include a field type dependency for mixed expense types (such as food), so you can have AI capture the expense or enter the amount (including GST) on mixed receipt documents. 

>  [!Note]
>  If the document is mixed and AI can't capture the field, calculate and enter eleven times the tax amount. If the document is not mixed you can enter the full amount. 

To set up a field type dependency for food:

1.  Search {{search}} for **Field Type Dependencies**, then choose the relevant link.
1.  On the action bar, select **Home**.
1.  In the field type table, **Field Type Code** column, select **Expense Type.**
1.  In the **Condition** column, select **Has a specific value**.
1.  In the **Value** column, select **Food**.
1.  In the **Reference Field Type** column, select **Amount including tax**.
1.  In the **Expectation** column, select **Must have a value**.

## See also
[Setting Up Fields](@EM-80)  
[Setting up Expense Types](@EM-41)