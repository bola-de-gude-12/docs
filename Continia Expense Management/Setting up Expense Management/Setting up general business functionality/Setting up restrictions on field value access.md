---
title: Setting up restrictions on field value access
date: 11-07-2025
description: Specify which field values are visible to different user-types in the Expense Mobile App and Expense Portal
id: EM-296
lang: en
---

# Setting up restrictions on field value access

You can help expense users focus on what's relevant to them when they create expenses by stipulating exactly which field values are visible to specific types of users in the Expense Mobile App and the Expense Portal.  Specifying which fields are visible minimizes errors and means bookkeepers spend less time double-checking to see if expenses were posted correctly.

This feature allows you to set up access to specific field values for each individual expense user or for a whole group of expense users by limiting access to expense types, dimensions, or other lookup values.

> [!NOTE]
> By default, all field values are accessible. Therefore restricting field value access means specifying which field values are visible to a user. For example, if you specify which field values are available for a user group, that group sees only those field values. Whereas a group using the default setup, sees all field values.

Limiting access to certain field values is particularly useful for large setups that may have hundreds of different projects to choose between, and many different field types, including field types that represent dimensions such as Job, Task, Department, or Cost Group. Field values such as Expense Type depend on the requirements of your organization.

## To restrict user access to field values

Depending on the version of Expense Management that you're running, step three of the following setup process differs slightly.

To set up a restricted view of field values for one or more expense users:

1. Search for {{search}} **Configured Fields**.
1. In the **Fields on Header** table > **Field Description** column, select the link to the record of the field you want to include access to (for example Expense Type).
1. From 2022 R1 onwards - On the action bar of the **Field Type Card**, click **Manage** > **Field Type**. 
   Prior to 2021 R2 - On the action bar of the **Field Types Card**, click **Field Type** > **Lookup Value Access**.
1. On the **Lookup Value Access** page, fill in the fields on the top line of the table as needed:
   * **Value Code**: In the drop-down menu, select the value you want to allow access to for the field that you selected in step two.
   * **Type**: In the drop-down menu, select **User** or **Group** to apply settings to an individual expense user, or a group of expense users.
   * **Code**: In the drop-down menu, select a user or user group.
   * **Description**: Select the field and it will automatically fill-in a description, based on the values you have selected. Selecting the field automatically opens the **Lookup Values** page. Use the back arrow to return to the **Lookup Value Access** page.
1. Repeat step four to add any additional field values to the restricted view you are setting up.

   > [!NOTE]
   > You must create a table entry for each field value that you want to allow the user or group access to. If there's only one line in the table of the **Lookup Value Access** page, then the user or group that you defined under **Type** will only have access to that value.

You have now set up the field value(s) that are accessible for the field(s) and user, or user group, that you specified.

### Example setup

In this example, you want a group of internal users (INT) to only see "Accommodation" as an option in the Expense Type field of the Expense Mobile App and Expense Portal. Users who aren't in that group (and therefore don't have a restricted view) will instead see all expense type fields. Users who are in another group, for example, external (EXT) will see only the restricted view for their group.

1. Search for {{search}} **Configured Fields**.
2. Click **Expense Type**, this open the Field Type Card.
3. On the action bar, click **Lookup Value Access**.
4. On the action bar, click **Edit List**.
5. On the Expense Type line, 
   1. In the **Value Code** column, select **Accommodation**.
   2. In the **Type** column, choose **Group**.
   3. In the **Code** column, choose **INT**.
   4. In the **Value Description** column, choose **Accommodation**.
6. Click **Process and Update Lookup Values**.
7. Click **Continia Online** > **Force Synchronize with Continia Online**.

## Related information

[Setting up fields](@EM-80)

[Setting up field dependencies](@EM-250)