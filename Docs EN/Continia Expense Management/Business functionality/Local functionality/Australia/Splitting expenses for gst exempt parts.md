---
title: Splitting expenses for GST-exempt parts (AU)
date: 29-08-2025
description: 
id: EM-215
lang: en
---
# Splitting expenses for GST-exempt parts (AU)

Enable GST (Goods and Services Tax) calculations in the Australian version of Continia Expense Management. After setup, GST is calculated automatically and split into multiple lines when users submit expenses with the configured expense types through the Continia Expense Mobile App or the Continia Expense Portal.

Typically, you split expenses according to whether they attract GST or not. For example, in Australia, unprocessed food does not attract GST, whereas processed food does. Therefore, if an expense user receives an invoice from a company, such as a supermarket, the receipt may have a mix of lines that attract GST and lines that don't. Best practice is to create a Groceries expense type, to deal with mixed expenses such as these.

When you're done setting this up, expenses will automatically be allocated to different lines based on the GST posting setup tax percentage.

## Prerequisites
To ensure you meet the following requirements to set up automatic distribution of GST into multiple lines in the Australian version of Continia Expense Management, check the following:

* You are running an *AU installation* of Expense Management 12.1 or newer.
* The **Enable Amount Distribution** setting is enabled in **Expense Management Setup** under **Expenses**.
* You have a field type with the field code **AMOUNT INCLUDING TAX**. This is a standard field in Expense Management, and you can use the guide [Setting up fields](@EM-80) to add it to the **Configured Fields** page so that expense users can see it and use it. We recommend renaming this field to: **TAXABLE AMOUNT PLUS GST**.
* You have an additional expense type set up for the purpose of GST posting. When naming the expense type, give it a name such as 'Groceries GST-Free' as this will make it much easier to find. For more information, see [Setting up expense types](@EM-41).

## To set up GST split and allocation

For the GST-free expense type you've set up, you need to configure a setting that only exists in the AU version of Expense Management.

To configure the setting:

1. Search for {{search}} **Expense Types**. 
1. Select your GST free expense type, then, on the action bar, click **Setup**.
1. In **GST Prod. Posting Group**, choose **NON GST** from the dropdown menu.

Next, you'll need to set up a distribution code on an expense type and enter the associated information for it. 

To set up a distribution code:

1. Search for {{search}} **Expense Types**. 
1. On the action bar, click **Edit List**.
1. Select an expense type.
1. In the **Distribution Code** field, select **New** from the dropdown menu, and create a new distribution code by filling in the following fields:
   * **Distribution Code** - The name of the distribution code.
   * **Description** - A short description of the distribution code.
   * **Distribute By Tax Amount** - Check to allocate automatically based on a pre-defined tax percentage. The expense will be distributed into a taxable and a non-taxable allocation. This field is *only* visible if the field type **Amount Including Tax** has been added.

For a GST expense type, it's tempting to include a field that includes the GST Amount. However, we recommend that you hide such a field by default, and set up a field type dependency instead, so it will only be visible to users when needed.

To hide the **Amount including GST field**:

1. Search for {{search}} **Configured Fields**.
1. In the field types table > **Field description** column, find the field **Amount including GST**. You can make this field hidden, editable, or mandatory, your choice. We recommend that you hide the **Amount Including GST** field by default by selecting the checkbox for **Hide Visibility by Default**.

Include a field type dependency for mixed expense types (such as food), so you can have AI capture the expense or enter the amount (including GST) on mixed receipt documents. 

>  [!Note]
>  If the document is mixed and AI can't capture the field, calculate and enter eleven times the tax amount. If the document is not mixed, you can enter the full amount. Alternatively, you can enter the total amount of all the items marked on the receipt, as taxable items.

To set up a field type dependency for food:

1.  Search for {{search}} **Field Type Dependencies**.
1.  On the action bar, click **Home**.
1.  In the field type table > **Field Type Code** column, select **Expense Type.**
1.  In the **Condition** column, select **Has a specific value**.
1.  In the **Value** column, select **Groceries**.
1.  In the **Reference Field Type** column, select **Amount including tax**.
1.  In the **Expectation** column, select **Must have a value**.

To see how this functionality works, see the following video on how to Handle GST-free amounts in Expense Management.

<iframe src="https://player.vimeo.com/video/1097445190?h=d943c08166&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media; web-share" referrerpolicy="strict-origin-when-cross-origin" title="EM_Set up GST in Aust_video draft ROUGH"></iframe>

## Related information
[Setting up fields](@EM-80)  
[Setting up expense types](@EM-41)