---
title: Expense Management Setting up Approval Sharing 
date: 18-02-2025
description: How to set up automatic approval sharing, including Out of Office for approvers
id: EM-64
lang: en
---

# Setting up Approval Sharing

You can automatically forward all of your approval tasks to another approver if you cannot approve documents for a period of time. By sharing your approval tasks with a designated approver, they can  operate as your substitute until you return to approve documents yourself.

## Set up approval sharing

Approval sharing works well if you're out of office and want to avoid bottlenecking approval processes. A designated approver is an admin.

To set up approval sharing:

1. Search {{search}} for Approval Sharing, then choose the related link.
1. On the action bar, select **Edit List**.
1. In the **Owner User ID** column, enter the user ID of the person who is sharing approval tasks
1. In the **Shared to User ID** column, enter the user ID of the person who will be the substitute approver.
1. In the **Sharing Type** column, select **Normal**.
   > [!NOTE]
   > If it's necessary for an admin set up out of office approval on behalf of a user, the admin must select **Out of Office** instead of **Normal** so the user can edit the entry later, if need be.
1. In the **Valid From** and **Valid To** columns, enter or select the start and end dates of the period where the approval tasks are shared.
1. If you want the substitute approver to inherit your limits and permissions, select the **Use Owners Limits & Permissions** checkbox.
1. Specify who will receive approval emails during the specified time. For **Send Email To**, choose :<br><ul><li>**Only Owner**</li><li>**Only Shared To User**</li><li>**Both Users**</li></ul>

## Set up a fictional user as a group

In situations where you must manage multi-person approvals, you can create a new fictional user and  use the account as a group approver. Use this solution too if there's a company policy that requires top-level approvers to have their own approval requests approved by someone other than themself.

The approval limit set for the group (the fictional user) overrides the individual approval limit set for each user in the group. You must be an admin for this process.

To create a new fictional user that you can use as a group:

1. Search {{search}} for Continia User Setup, then choose the related link.
2. On the action bar, select **New**.
3. Under **General**, in the **Continia User ID** field, select the menu (...) and either choose an existing User ID or, on the action bar, select **New** and create a new User ID.
4. Fill in the **Name** field.

> [!IMPORTANT]
> The Continia User ID you created or chose from the Continia Users list for this fictional user can only be used for this purpose, it cannot be used for anything else.

4. Under **Expense Management** > **Approval Limit**, either toggle **Unlimited** or specify the approval limit in the **Amount** field.

> [!NOTE]
> If you set an approval limit for the fictional user in the **Approver Name** field, ensure their approval limit is higher than anyone else in the group or assign them an unlimited approval limit.

Now you have a new fictional user that you can use as a group. 

### Add users to the group

To add users to the group you just created: 

1. Search {{search}} for Approval sharing, then choose the related link.
2. On the action bar, click **Edit List**.
3. In the **Owner User ID** column, choose the user you created in the previous step.
4. In the **Shared to User ID** column, choose a user that you want include in the approval sharing group.
5. In the **Sharing Type** column, choose **Normal**.
6. In the **Use Owner's Limits and Permissions** column, select the checkbox.
7. In the **Send Email To** column, choose:<br><ul><li>**Only Owner**</li><li>**Only Shared To User**</li><li>**Both Users**</li></ul>
8. Repeat these steps for each user you want to add to the group.

You can see the number of users who have been added to the group on the Continia Users page under **Shared to this User**.

## Set up out of office approval sharing

You do not need to be an admin for this process, as individual users can also set up approval sharing for when they're out of office. 

To set up approval sharing yourself:

1. Search {{search}} for Expense Management Approval Entries, then choose the related link.
1. On the action bar, select **Out of Office Setup**.
1. Under **General** in the **Forward from date** and **Forward to date** fields, enter or select the start and end dates of the period where your approval tasks will be shared.
1. In the **Forward to** field, enter the user ID of the substitute approver that you want your approval tasks forwarded to.
1. If you want to share your approval tasks for all companies where you and the substitute approver are present, select the **Copy to All Companies** checkbox. If you don't select this checkbox, the out of office approval sharing you're setting up will only apply to the company that you're currently in.

> [!NOTE]
> The **Use Owners Limits & Permissions** and the **Forward Emails** fields are hidden from users on the **Out of Office Setup** page in the user interface. However, they're enabled by default. If you want to change these default settings, an admin can do this from the **Approval Sharing** page.