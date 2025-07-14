---
title: Adding Captions to PDF Master Templates
date: 03-08-2023
description:  
id: DC-117
lang: en
---

# Adding Captions to PDF Master Templates

To improve the recognition accuracy of PDF master templates, you can ask Continia Document Capture to suggest captions for the templates based on captions already used in existing source templates (such as vendor templates). The suggestions can then be added to the fields of the master templates.

As Document Capture will use such customer-specific captions added over time in addition to the standard setup, it will be increasingly easier for Document Capture to recognize the fields of imported PDF documents from new vendors (or whenever a new template is created for an existing vendor), resulting in greater overall accuracy.

## To add suggested captions to master template fields

1. Search ({{search}}) for and select **Document Categories**.
1. To open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself), and then select **Edit** on the action bar to open the **Document Category** card.
1. On the **Templates** FastTab, in the list of templates, select the master template for PDF files (**PURCHASE-GB**).

   > [!NOTE]
   > If there's more than one PDF master template in the category and you don't select a specific one, the first one in the list is used by default.

1. On the action bar, click **Suggest Header Field Captions** to open the corresponding page.
1. Do one of the following:
   1. On the action bar, click **Create Suggestions**, and then select **Create Suggestions for all fields** > **OK** in the dialog that opens.
   1. In the list of fields, select the one that you want to create suggestions for, and then select **Create Suggestions** on the action bar. In the dialog that opens, select **Create Suggestions for [selected field]** > **OK**.
1. A dialog notifies you that a number of captions were suggested. Select **OK** to close this.
1. In the list of fields, in the **No. of Suggestions** column, select the number displayed for the field that you want to view suggestions for.
1. In the list of suggested captions, in the **Select** column, select the checkbox(es) of the caption(s) that you want to add to the master template. Select **Close** to return to the **Suggest Header Field Captions** page.

   > [!TIP]
   > If you want to ignore some or all of the suggested captions, simply select the **Ignore** checkbox for each caption that you want Document Capture to leave out of consideration. Any ignored captions won't be suggested anymore when you run the **Create Suggestions** routine again in the future.

1. Repeat steps 7-8 for any additional fields that you want to update with suggested captions in the master template. 
1. Do one of the following:
   1. On the action bar, click **Update Template**, and then select **Update all template fields** > **OK** in the dialog that opens.
   1. In the list of fields, select the one that you want to update in the master template, and then select **Update Template** on the action bar. In the dialog that opens, select **Update the [selected field] template field** > **OK**.
1. A dialog notifies you that a number of captions were created. Select **OK** to close this.

This will add the selected captions to the PDF master template, either for all relevant template fields (step 10a) or for the one you specifically selected (step 10b). 

## To view added captions

If you want to see the caption(s) you've added using the guide above, follow these steps:

1. Open the **Document Category** card (as described in steps 1-2 of the guide above).
1. On the **Templates** FastTab, in the list of templates, select the relevant PDF master template, and then select **Manage** > **Edit** to open the template card.
1. On the **Fields** FastTab, in the list of template fields, select the one that you'd like to view. This will open the template field card.
1. On the **General** FastTab, under **Caption**, select the displayed caption to open the **Edit - Field Captions** page.

This will display a list of all registered captions for the selected template field, including the one(s) you've added yourself.

## Related information

[Working with Templates](@DC-18)  
[Setting up New Template Fields](@DC-19)  