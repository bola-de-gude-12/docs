---
title: Setting up approval sharing in Document Capture
date: 11-06-2025
id: null
lang: en
description: >-
  How to set up automatic approval sharing, including out of office for
  approvers.
---

# Setting up approval sharing

If you're unable to approve documents for a period of time, you can have all of your approval tasks automatically forwarded to another approver during that period. You essentially share your approval tasks with a designated approver, and this approver then acts as your substitute until you're able to approve documents again.

Approval sharing can be carried out [for any user and any purpose](<Copy of Approval sharing.md#approval-sharing>) (on behalf of other users) – typically done by admins – or [for and by yourself if you're out of office](<Copy of Approval sharing.md#out-of-office-approval-sharing-for-individual-users>).

## To set up approval sharing

To set up approval sharing:

1. Search \{{search\}} for and select **Approval Sharing**.
2. On the action bar, click **Edit List** to make the list editable.
3. In the **Owner User ID** and **Shared to User ID** columns, enter the user ID of the person who's sharing approval tasks – hereafter referred to as the original approver – and that of the substitute approver.
4.  In the **Sharing Type** column, select **Normal** unless you specifically need to change the out-of-office settings of the original approver (a rather rare exception).

    > \[!NOTE] Individual users usually set up out-of-office approval sharing themselves using [the procedure described below](<Copy of Approval sharing.md#out-of-office-approval-sharing-for-individual-users>). However, it may occasionally be necessary for an admin to do it on behalf of a user. In such cases, the admin must select **Out of Office** instead of **Normal**, and the user will then be able to edit the entry later, if necessary. If the admin selects **Normal** (by far the most common scenario), the user will _not_ be able to edit the entry at a later point.
5. In the **Valid From** and **Valid To** columns, enter or select the start and end dates of the period in which approval tasks should be shared.
6. If you want the substitute approver to inherit the limits and permissions of the original approver, select the **Use Owner's Limits & Permissions** checkbox.
7. In the **Send Email To** column, specify if approval emails should be sent to the substitute approver, the original approver, or both.
8. If you want approval tasks to be shared for all companies in which both users are present, select the **Copy to All Companies** checkbox. If you don't select this checkbox, the approval sharing you're setting up will only apply to the company that you're currently in.

## To set up an approval group

If you’re managing multi-person approvals, you can create a user and employ it as an approval group. This approach is also useful if a company policy requires top-level approvers to have their own approval requests approved by someone other than themselves.

To create a user that functions like a group:

1. Search \{{search\}} for and select **Continia User Setup**.
2. On the action bar, click **New**.
3. On the **General** FastTab, click the three dots by the **Continia User ID** field.
4. In the dialog box that opens, either select an existing user ID or, on the action bar, click **New** to create a user.

> \[!IMPORTANT] The Continia user ID you created or chose from the **Continia Users** list for this approval group can only be used for this purpose.

4. Back on the **Continia User Setup Card** page, fill out the **Name** field.
5. Click the three dots by the **Approver ID (Manager)** field. In the dialog box that opens, select an existing approver ID. If approval sharing for the group is set to use the owner’s limits and the group doesn’t have an unlimited approval limit, the document is sent to the manager specified here.
6. Under the **Purchase Invoice and Credit Memo Approval** section, in the **Approval Limit** field, enter the desired value. Alternatively, enable the **Unlimited Approval** setting for this approval group.

Now you have an approval user that functions as an approval group.

### To add users to an approval group

1. Search \{{search\}} for and select **Approval Sharing - Document Capture**.
2. On the action bar, click **New**.
3. Under the **Owner User ID** column, select the user you created in the previous step.
4. Under the **Shared to User ID** column, select the user you want include in the approval sharing group.
5. Under the **Sharing Type** column, select **Normal**.
6. Under the **Use Owner's Limits & Permissions** column, select the checkbox to enable the permissions configured for the approval group. If the checkbox is cleared, the permissions assigned to each member of the approval group take precedence.
7. Under the **Send Email To** column, select:\

   * **Only Owner**
   * **Only Shared to User**
8. Repeat these steps for each user you want to add to the group.

To see the number of users added to the group, go to the **Continia User Setup** page and check the values under the columns **Approval Shared with this User** and **Approval Shared with Other Users**.

## To set up out-of-office approval sharing for individual users

Although you can indeed set up out-of-office approval sharing using [the above guide](<Copy of Approval sharing.md#approval-sharing>), which is particularly useful for admins setting it up for multiple users at the same time, there's a more user-friendly way to do it for each individual user – enabling you to do it yourself:

1. Search \{{search\}} for and select **Purchase Approval Entries**.
2. On the action bar, click **Out of Office Setup**.
3. Under **Forward from date** and **Forward to date**, enter or select the start and end dates of the period in which your approval tasks should be shared.
4. Under **Forward to**, enter the user ID of the substitute approver to whom your approval tasks should be forwarded.
5. If you want your approval tasks to be shared for all companies in which both you and the substitute approver are present, select the **Copy to All Companies** checkbox. If you don't select this checkbox, the out-of-office approval sharing you're setting up will only apply to the company that you're currently in.

> \[!NOTE] Compared to [the **Approval Sharing** page that's intended for admins](<Copy of Approval sharing.md#approval-sharing>), the **Out of Office Setup** page is somewhat simpler, and it doesn't include the following two fields in the actual user interface:
>
> * **Use Owner's Limits & Permissions**
> * **Send Email To**
>
> Although hidden from users on the **Out of Office Setup** page, these two fields actually exist behind the scenes and are enabled by default whenever you set up approval sharing using this page. The **Send Email To** default setting is to only send approval emails to the substitute approver. If you wish to change either of these default settings, it must be done on the **Approval Sharing** page, typically by an admin.
