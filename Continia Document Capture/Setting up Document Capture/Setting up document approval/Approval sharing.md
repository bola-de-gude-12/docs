---
title: Setting up Approval Sharing 
date: 16-12-2024
description: How to set up automatic approval sharing, including Out of Office for approvers
id: DC-25
lang: en
---

# Setting up Approval Sharing

If you're unable to approve documents for a period of time, you can have all of your approval tasks automatically forwarded to another approver during that period. You essentially share your approval tasks with a designated approver, and this approver then acts as your substitute until you're able to approve documents again.

Approval sharing can be carried out [for any user and any purpose](#approval-sharing) (on behalf of other users) – typically done by admins – or [for and by yourself if you're out of office](#out-of-office-approval-sharing-for-individual-users).

## Approval sharing

To set up approval sharing:

1. Choose the {{search}} icon, enter **Approval Sharing**, and then choose the related link.
1. On the action bar, click **Edit List** to make the list editable.
1. In the **Owner User ID** and **Shared to User ID** columns, enter the user ID of the person who's sharing approval tasks – hereafter referred to as the original approver – and that of the substitute approver.
1. In the **Sharing Type** column, select **Normal** unless you specifically need to change the out-of-office settings of the original approver (a rather rare exception).
   > [!NOTE]
   > Individual users usually set up out-of-office approval sharing themselves using [the procedure described below](#out-of-office-approval-sharing-for-individual-users). However, it may occasionally be necessary for an admin to do it on behalf of a user. In such cases, the admin must select **Out of Office** instead of **Normal**, and the user will then be able to edit the entry later, if necessary. If the admin selects **Normal** (by far the most common scenario), the user will *not* be able to edit the entry at a later point. 
1. In the **Valid From** and **Valid To** columns, enter or select the start and end dates of the period in which approval tasks should be shared.
1. If you want the substitute approver to inherit the limits and permissions of the original approver, select the **Use Owner's Limits & Permissions** checkbox.
1. In the **Send Email To** column, specify if approval emails should be sent to the substitute approver, the original approver, or both.
1. If you want approval tasks to be shared for all companies in which both users are present, select the **Copy to All Companies** checkbox. If you don't select this checkbox, the approval sharing you're setting up will only apply to the company that you're currently in.

## Out-of-office approval sharing for individual users

Although you can indeed set up out-of-office approval sharing using [the above guide](#approval-sharing), which is particularly useful for admins setting it up for multiple users at the same time, there's a more user-friendly way to do it for each individual user, enabling you to do it yourself:

1. Choose the {{search}} icon, enter **Purchase Approval Entries**, and then choose the related link.
1. On the action bar, click **Out of Office Setup**.
1. Under **Forward from date** and **Forward to date**, enter or select the start and end dates of the period in which your approval tasks should be shared.
1. Under **Forward to**, enter the user ID of the substitute approver to whom your approval tasks should be forwarded.
1. If you want your approval tasks to be shared for all companies in which both you and the substitute approver are present, select the **Copy to All Companies** checkbox. If you don't select this checkbox, the out-of-office approval sharing you're setting up will only apply to the company that you're currently in.

> [!NOTE]
> Compared to [the **Approval Sharing** page that's intended for admins](#approval-sharing), the **Out of Office Setup** page is somewhat simpler, and it doesn't include the following two fields in the actual user interface:
>
> * **Use Owner's Limits & Permissions**
> * **Send Email To**
>
> Although hidden from users on the **Out of Office Setup** page, these two fields actually exist behind the scenes and are enabled by default whenever you set up approval sharing using this page. The **Send Email To** default setting is to only send approval emails to the substitute approver. If you wish to change either of these default settings, it must be done on the **Approval Sharing** page, typically by an admin.