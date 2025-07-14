---
title: Accounts for amounts
date: 08-07-2025
description:  
id: DC-149
lang: en
---

# Accounts for Amounts

The **Accounts for Amounts** page (previously known as **Posting Setup**) allows you to specify which accounts should be used as posting suggestions for the header amount fields that are captured in your incoming documents. The header fields that are listed on the page are displayed automatically by Continia Document Capture, and only header fields that have been categorized as amount fields will appear here – no text fields, date fields, or other types of fields.

If, for example, **Amount Excl. VAT** appears in the table of amount fields, you could set this field up to be translated (i.e., mapped) to a certain G/L account number – such as **34100** – for the given document template. When an imported document is then assigned to this template and an amount is captured in the **Amount Excl. VAT** field for this document, the G/L account number you specified – **34100** – will be automatically suggested for any purchase or sales line that's created using the captured amount.

## To set up Accounts for Amounts 

To specify which accounts should be suggested as posting accounts for amounts captured in your incoming documents, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the relevant document category code – for example, **PURCHASE** – to open the document journal.
1. In the list of documents, select the one whose template you want to edit.
1. On the action bar, click **Template** > **Accounts for Amounts** to open the **Accounts for Amounts** page.
1. In the table, go to the line of the amount field whose account mapping properties you want to edit.
1. For the selected line, fill in the table fields as needed. The first table field (in the **Field** column) represents the document field that contains the captured amount which you want to map to a specific account type, account number, etc., when purchase or sales lines are created for this amount. For the remaining table fields, specify exactly which values you want to map the captured amount to:
   * **Translate to Type** - select the type of account you want to map the captured amount to.
   * **Translate to No.** - select the account number you want to map the captured amount to.
   * **VAT Prod. Posting Group** - select the VAT product posting group you want to map the captured amount to. This allows you to overwrite the default VAT product posting group.
   * **Translate to VAT Bus. Posting Group** - select the VAT business posting group you want to map the captured amount to. This allows you to overwrite the default VAT business posting group.
   * **[Global dimensions 1 and 2]** - select the dimension value(s) you want to map the captured amount to. This allows you to overwrite the default dimension values of the account type and number.
   > [!NOTE]
   > Only the two preconfigured global dimensions are displayed as columns in the table by default, and you can only add and view values for these two dimensions directly in the table. However, you can easily add other dimensions and values as follows: Select the relevant line, select **Related** > **Line** > **Dimensions** to open the **Line Dimensions** page, and then select a dimension code and a dimension value code in the table. Although these additional dimensions and values will indeed be added, note that they won't be visible in the **Accounts for Amounts** table by default. To make them visible in this table, you must [customize the table](#to-customize-the-table).
   * **Deferral Code**: Select the deferral code that you want to map the captured amount to.
1. Repeat steps 5-6 for any additional amount fields whose account mapping properties you want to edit.

## To customize the table

As mentioned above, only the two global dimensions are displayed by default as columns in the table of amount fields on the **Accounts for Amounts** page. However, you can easily customize the table by adding additional dimension columns to it. To do this, [personalize the page](https://docs.microsoft.com/en-us/dynamics365/business-central/ui-personalization-user) by following these steps:

1. Click **Settings** {{settings}} icon > **Personalize**.
1. In the upper-left corner, click **+ Field** to open the **Add Field to Page** pane.
1. Drag the relevant dimension field(s) from the pane to the table header. 
1. Click **Done** to close the **Personalizing** banner.

The new dimension columns are added to the table. You may have to refresh the page for them to be visible though.

> [!TIP]
> The dimension fields **UOM Code** and **Variant Code** may be particularly relevant for you to add to the table, as it's sometimes necessary to map amount fields to specific item variants (such as colors) or to certain units of measure (such as packs instead of pallets).

## Related information

[Using amount distribution codes](@DC-118)  
