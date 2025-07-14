---
title: Setting Up Fields
date: 18-03-2025
description:
id: EM-80
lang: en
---

# Setting Up Fields

With Expense Management, you can easily configure the fields relevant to your organization when creating expenses, mileages, per diems, and expense reports. For each document type, it’s possible to define what fields are visible to expense users in the Expense App and the Expense Portal. 

> [!NOTE]
> How you order the fields will be reflected in the order that the fields display in the Expense App and the Expense Portal.

To specify the visibility of fields:

1. Search {{search}} for **Configured Fields**, then choose the related link.
1. On the action bar, select the type of expense document (per diem, mileage, expense, or expense report) you want to configure.
1. To add a new field:
   1. Under **Fields on Header**, select **New Line** to add a new line to the table.
   1. In the **Field Code** column of the new line, select the field to open a drop down menu.
   1. Either select a field directly from the dropdown menu, or enter a search phrase to search for the field you want to add, and then select the field from the menu to add it.
1. To delete a field, select the relevant field, then select **Delete Line**. In the dialog that opens, select **Yes** to confirm deletion.
1. To hide any of the fields by default, select the checkbox(es) in the **Hide visibility by default** column. 
1. To make any of the fields editable, select the checkbox(es) in the **Editable** column.
1. To make any of the fields mandatory, select the checkbox(es) in the **Mandatory** column.
   > [!TIP]
   > If the **Mandatory** box is *not* ticked in the **Description** line, the text from the expense type is copied to the **Description** field in the Expense App and the Expense Portal.
1. On the action bar, select **Continia Online** > **Force Synchronize with Continia Online**, to synchronize your changes. The fields you configure are only visible in the Continia Expense App or the Continia Expense Portal after you synchronize with Continia Online.

## Considerations for labelling fields
You have control over how you label fields. Tailoring field labels to suit the different document types of Expense, Mileage, Per Diem, and Expense Reports, makes tracking information easier and more precise for your organization.

The following best practices help reduce errors and misunderstandings, and bring clarity to a user's workflow. When you define field labels:

* Use specific terms that align with the policies and regulations of your organization, as this makes it easier for employees to submit expenses correctly.
* Be specific about the type of information you're seeking for each field. Describe a  field label should describe precisely the field in relation to its document type for expenses, mileage, and per diems. For example, to describe an expense-type for expenses, label the field "Description". Whereas for mileage, label that same field-type "Purpose".
* Remember every field label you create is an opportunity to bring yet more clarity. For example, where you would use "Attendee" for expenses, use "Passenger" for mileage. 

## Setting up user-defined field types

The Expense Management assisted setup downloads a wide range of field types that you can use in most common scenarios. However, you can add more field types to support your specific business cases. The standard configuration provides a large selection of the most common fields, but you can also configure new fields yourself.

To set up a new field type, follow these steps:

1. Search {{search}} for **Configured Fields**, then select the related link.
2. Under **Field Code**, select the first available line, then select **Select from the full list**.
3. On the action bar, select **New**.
4. On the **Field Type Card** page, add the **Code** and **Description** for your new field type and select the **Data Type**. The data type you select affects the field dependencies options for the field type. For example, if you require the field type to have a value, you can only use the data types *Option* and *Code*.
5. Synchronize with Continia Online. The fields you configured to be visible are visible in the Continia Expense App or the Continia Expense Portal after you’ve synchronized with Continia Online.

> [!NOTE]
> Adding a new field type doesn't change anything in the system. You must add the field to **Configured Fields** or **Custom Fields**. You'll see **Custom Fields** from the Expense Management Setup and can configure it on the main pages for each document in Business Central.

## Custom fields in the Web Approval Portal

If you're using the Web Approval Portal, you can see how to enable custom fields for it in [Customizing the Web Approval Portal](@EM-61).

## See also
[Setting up field dependencies](@EM-250)  
[Setting up restrictions on field value access](@EM-296)  