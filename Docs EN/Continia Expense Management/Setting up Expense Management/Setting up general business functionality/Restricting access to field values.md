---
title: Restricting Access to Field Values
date: 29-01-2025
description:
lang: en
---

# Restricting Access to Field Values

You can help expense users focus on what's relevant to them when they create expenses, by stipulating which field values are visible to specific types of users in the Expense App and the Expense Portal. Specifying which fields are visible minimizes errors and means bookkeepers spend less time double-checking to see if expenses were posted correctly. 

This feature allows you to set up access to specific field values for individual expense users or for a group of expense users.

> [!NOTE]
> By default, all field values are accessible. Therefore restricting field value access means specifying which field values are visible to a user. For example, if you specify which field values are available for a user group, that group sees only those field values. Whereas a group using the default setup, sees all field values.

Limiting access to certain field values is particularly useful for large setups that may have hundreds of different projects to choose between, and many different field types, including field types that represent dimensions such as Job, Task, Department, or Cost Group. Field values such as Expense Type depend on the requirements of your organization.

## To restrict user access to field values

To set up a restricted view of field values for one or more expense users:

1. Use {{search}} to search for Configured Fields, then choose the related link.
1. In the **Fields on Header** table > **Field Description** column, select the link to the record of the field you want to include access to.
1. In the action bar of the Field Type Card, select **Field Type** > **Lookup Value Access**.
1. On the **Lookup Value Access** page, fill in the fields in the top line of the table as needed:
   * **Value Code**: In the drop-down menu, select the value you want to allow access to for the field that you selected in step two.
   * **Type**: In the drop-down menu, select **User**  or **Group** to apply settings to an individual expense user, or to a group of expense users.
   * **Code**: In the drop-down menu, select a user or user group.
   * **Description**: Select the field and it will automatically fill-in a description based on the values you selected. Selecting the field also automatically opens the **Lookup Values** page. Use the back arrow to return to the **Lookup Value Access** page.
1. Repeat step four to add any additional field values to the restricted view you are setting up.
   > [!NOTE]
   > You must create a table entry for each field value that you want to allow the user or group access to. If there's only one line in the table of the **Lookup Value Access** page, then the user or group that you defined under **Type** will only have access to that value.

You have now set up the field value(s) that are accessible for the field(s) and user or user group that you specified.