---
title: Setting up new template fields in Document Capture
date: 10-09-2025
description: How to create, customize, and add template fields, including master template fields.
id: DC-19
lang: en
---

# Setting up new template fields

If some of the default template fields don't meet your needs, you can create fields or customize existing ones. You can create and customize fields either for a master template or for each individual vendor template, but it's generally recommended that you create fields in a master template and then copy them from there to the vendor templates.

This article uses vendors and purchase documents as an illustrative basis, but the functionality works equally well with other sources and types of documents.

## To create a master template field using the assisted setup guide

The assisted setup guide allows you to create template fields without the risk of deleting mandatory existing fields or breaking the template. Only field settings that are configured frequently are available in the guide.

To create a field for a master template using the assisted setup guide:

1. Search ({{search}}) for and select **Document Categories**.
1. To open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself), and then click **Edit** on the action bar.
1. On the **Templates** FastTab, in the list of templates, select the master template for PDF files (**PURCHASE-GB**), and then click **Edit** to open the template card.
1. On the **Fields** FastTab, click **Create new Template Field** to open the **Assisted Template Field Setup Guide**.
1. Click **Next** to start the guide, and then follow the on-screen instructions to set up the field you need. When you're done, click **Finish**.

The new field is added to the template card, under the **Fields** FastTab.

## To manually create a master template field

You can also create a field for a master template manually. To do this:

1. Search ({{search}}) for and select **Document Categories**.
1. To open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself), and then click **Edit** on the action bar.
1. On the **Templates** FastTab, in the list of templates, select the master template for PDF files (**PURCHASE-GB**), and then click **Edit** to open the template card.
1. On the **Fields** FastTab, click **New** to open the new field's **Template Field Card**.
1. On the **General** FastTab, enter a code for the new template field (mandatory), and fill out the remaining configuration fields as needed. If you're creating a dimension field, make sure that the field's **Code** is the exact same as the name of the related dimension.
   > [!WARNING]
   > Spaces and the following special characters aren't allowed in template field codes: /\*-+()|\<\>%^&=.?$#@'". The reason for this is that if you set up a formula that includes one or more fields whose codes have spaces or special characters (for example, "AMOUNT 1 + AMOUNT 2"), the formula fails. If you use spaces and/or any of the mentioned characters in your code, these are automatically removed when the template field is created.

   > [!NOTE]
   > On the **Template Field Card**, the visibility of some of the configuration fields depends on what you select under **Data Type**. For more information, see [The template field card](#the-template-field-card).
1. **Optional**: If you want the new field to be automatically included in all new vendor templates that are created on the basis of the master template, enable **Insert on new Templates**. If you don't enable this, the field can be added manually to individual templates later instead, [as described below](#to-add-a-new-field-to-a-vendor-template).
1. On the **Field Translations** FastTab, enter any text that should be translated for this field in order for Document Capture to recognize the field. Select the checkbox in the **Case-sensitive** column if the entered text should be case-sensitive.
   > [!TIP]
   > If you don't enter anything in the **Translate To** column, the text you've entered in the **Translate From** column is removed from any relevant value identified by Document Capture, which is useful for honorific titles and similar. For example, if you enter **Dr.** under **Translate From** and nothing under **Translate To**, Document Capture knows that whenever it captures a value containing this honorific in a document – for example, 'Dr. Mary Doe' – it should remove the honorific and leave only the actual name for further processing, in this case 'Mary Doe'. This enables Document Capture to identify the correct user in the system.

The new field is added to the template card, under the **Fields** FastTab. It's inserted right below the list entry that was selected when you opened the template field card in step 4 above.

>[!NOTE]
>The order of the formula fields in a template affects calculations. To change the order, select the desired field and use the **Move Up** and **Move Down** actions on the action bar.

## The template field card

The template field card is where you can edit the properties of a given template field, including its data type, what captions Document Capture should search for, which rules should be used to validate the captured data, and whether to add the field to all new templates. You configure these properties using a number of different configuration fields and toggles, which are all accompanied by explanatory tooltips in the Business Central user interface.

Note that on the **Template Field Card** page, the visibility of some of the configuration fields and toggles depends on what you select under **Data Type**. Most of the fields and toggles are the same for all data types though, so the following table simply outlines the differences between the types:

<br>

| Data type | Settings that are specific to this type |
| --- | --- |
| **Text** | **Enable Rule Generation** is included as an extra toggle under **Rules and Captions**. |
| **Number** | **Number Settings** is included as an additional section with various number configuration fields and toggles. |
| **Date** | **Enable Rule Generation** is included as an extra toggle under **Rules and Captions**. Also **Date Settings** is included as an additional section with a number of date configuration fields. |
| **Boolean** | The configuration field **Search for Value** is not available, and the **Formula** field must have one of the two values **'Yes'** or **'No'**. The default value is **'No'**. |
| **Lookup** | **Lookup Values** is included as an additional section with a number of lookup configuration fields. |

For the data type **Date**, you can enter the keywords **TODAY** (**T**) or **WORKDATE** (**W**) in the **Formula** field. This automatically inserts today's date or the specified work date into the applicable template field during field recognition for all documents using that template. So if, for example, you set this up for the template field **Due Date** and the work date is September 30, 2024, the **Due Date** field under **Document Header** in the document journal of all incoming documents with this template will read **09/30/24**.

## To create a vendor template field

To create a vendor template field using the assisted setup guide, follow the [guide for master template fields above](#to-create-a-master-template-field-using-the-assisted-setup-guide) – but select a vendor template in step 3.

Likewise, the process of creating vendor template fields manually is exactly the same as the one for master template fields [described above](#to-manually-create-a-master-template-field), except that:

* You must select a vendor template in step 3.
* Step 6 is not applicable to vendor templates, and should therefore be skipped.

It's recommended that you create all fields in master templates, but it may occasionally be relevant to create fields that only apply to one specific vendor.

## To add a new field to a vendor template

Once you've created a new field in the master template as described above, it's available to be added to any vendor template you prefer. If you enabled **Insert on new Templates** when creating the master template field (step 6 in [the above guide](#to-manually-create-a-master-template-field)), the field is automatically added to all new vendor templates created as copies of the master template. If you didn't enable **Insert on new Templates** when creating the field, you can manually add the field to a vendor template in one of the following ways:

* Using the document journal, as described under [To customize vendor template fields](#to-customize-vendor-template-fields)
* Using the template card, as described below

To add a field to a vendor template using the template card:

1. Search ({{search}}) for and select **Document Categories**.
1. To open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself), and then click **Edit** on the action bar.
1. On the **Templates** FastTab, in the list of templates, select the template to which you want to add the field, and then click **Edit** to open the template card.
1. On the **Fields** FastTab, click **Add Template Field** to open the **Template Field List**.
1. In the list of fields, find and select the relevant field.

The field is added to the list of template fields and displayed in the template card, on the **Fields** FastTab.

## To customize master template fields

To customize master template fields:

1. Search ({{search}}) for and select **Document Categories**.
1. To open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself), and then click **Edit** on the action bar.
1. On the **Templates** FastTab, in the list of templates, select the master template for PDF files (**PURCHASE-GB**), and then click **Edit** to open the template card.
1. On the **Fields** FastTab, customize the individual template fields and their availability as needed:
   * To specify that a field value must be present in an imported document for the document to be registered - select the field's checkbox in the **Required** column.
   * To move or delete a field - select the relevant field line, and then click **Manage** followed by the action you want to perform. If you're deleting a field, you have the option to delete it across all related templates.
   * To edit the properties of each individual field, including its data type, what captions to search for, which rules to use, and whether to add the field to all new templates - in the **Field Name** column, click the name of the field to open its **Template Field Card**, and then make any necessary changes there.
   > [!NOTE]
   > On the **Template Field Card**, the visibility of some of the configuration fields depends on what you select under **Data Type**. For more information, see [The template field card](#the-template-field-card).
1. **Optional**: To copy a template field (such as the one you've just customized) to all templates that were created on the basis of the master template: On the **Fields** FastTab, in the list of fields, select the relevant field, and then click **Copy Field**.
   
   > [!IMPORTANT]
   > The field is only copied to templates in which it doesn't yet exist – it doesn't update a previously copied field of the same kind. If you've previously copied the field to all templates but need to update it, you must do this manually.

## To customize vendor template fields

The process of customizing fields for vendor templates is very similar to that of customizing master template fields, but there are a few notable differences – as indicated below.

To customize vendor template fields:

1. Search ({{search}}) for and select **Document Categories**.
1. To open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself), and then click **Edit** on the action bar.
1. On the **Templates** FastTab, in the list of templates, select the template whose fields you want to edit, and then click **Edit** to open the template card.
1. On the **Fields** FastTab, customize the individual template fields and their availability as needed:
   * To specify that a field value must be present in an imported document for the document to be registered - select the field's checkbox in the **Required** column.
   * To move or delete a field - select the relevant field line, and then click **Manage** followed by the action you want to perform.
   * To add a field from the master template - click **Add Template Field**.
   * To edit the properties of each individual field, including its data type, what captions to search for, and which rules to use - in the **Field Name** column, click the name of the field to open its **Template Field Card**, and then make any necessary changes there.
   > [!NOTE]
   > On the **Template Field Card**, the visibility of some of the configuration fields depends on what you select under **Data Type**. For more information, see [The template field card](#the-template-field-card).

## Related information

[Working with templates](@DC-18)  