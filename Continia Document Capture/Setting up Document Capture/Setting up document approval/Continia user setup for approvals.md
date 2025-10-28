---
title: Continia user setup for approvals in Document Capture
date: 01-10-2025
description: How to configure users as approvers, including an overview of approval administrator permissions.
id: DC-23
lang: en
---

# Continia user setup for approvals

To approve documents in either Continia Document Capture or the Continia Web Approval Portal, a user must first be configured as an approver. This article provides details on how to do so.

> [!NOTE]
> You configure users as approvers in the **Continia User Setup**, which is also relevant for Continia Expense Management. For more information, see [Expense user setup for Expense Management](@EM-36).

The **Continia User Setup** is an extension of the standard Microsoft Dynamics 365 Business Central (BC) user setup table, and many of the fields displayed in the **Continia User Setup** originate from this table – and also appear in the **Approval User Setup**. Any settings you change in one of the two setups are automatically changed accordingly in the other setup.

When you create a **Continia User Setup** record, a BC user setup record is also created automatically. Likewise, if you delete a **Continia User Setup** record, the corresponding BC user setup record may be automatically deleted for clean-up purposes – but only under certain circumstances. If you delete the **Continia User Setup** after a period of time but have previously populated the BC user setup record with fields that aren't visible in the **Continia User Setup**, the BC user setup record isn't deleted.

## To set up users as approvers

To enable a user to approve documents:

1. Search ({{search}}) for and select **Continia User Setup**.
1. Select the user who you want to set up as an approver.
1. On the action bar, click **Edit** to open the selected user's **Continia User Setup Card**.
1. On the **General** FastTab, fill out the fields as necessary. The following fields are mandatory:
   * In **Salesperson/Purchaser**, enter the name of the selected user as registered in Business Central. This name is kept in synchronization with the designated user.
   * In **Approver ID (Manager)**, enter the ID of the selected user's manager (or any other next-level approver that can approve documents if the user's own limits are insufficient).
   * Under **Purchase Invoice and Credit Memo Approval**, be sure to either enter a maximum approval amount for the selected user under **Approval Limit** or, if applicable, select **Unlimited Approval**.
   > [!NOTE]
   > To configure assigning permissions for the user or for a group that the user is a member of (see [To configure individual approver permissions](#to-configure-individual-approver-permissions) and [To configure account and dimension permissions for a group](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/approval-user-groups#to-configure-account-and-dimension-permissions-for-a-group)), you must enable **Can Edit Posting Lines** as well.
   > 
   > In case you want the user to be an approval administrator, enable the **Approval Administrator** setting. Note that this also automatically enables the corresponding setting in the **Approval User Setup**, and that the user is granted a number of standard approval administrator permissions in addition to the Continia-specific permissions mentioned under [Approval administrator permissions](#approval-administrator-permissions) below.
1. On the **Web Approval** FastTab, select the approval client that the selected user will use to approve documents. The selected approval client is opened whenever the user selects a link in a [notification email](Email notifications.md). Note that only users with a value under **Approval Client** in the **Continia User Setup** are shown in the forward list. For more information, see [Creating user-specific lists of approvers for approval forwarding](@DC-138).

> [!IMPORTANT]
> Once you've set up a user as an approver, you must assign this user an appropriate Business Central license in order for the user to be able to sign in and function as an approver. A Team Members license should be sufficient for this, subject to the Microsoft licensing conditions stipulated in the Microsoft Dynamics 365 Business Central Licensing Guide, which is available for download in the [Business Central](https://dynamics.microsoft.com/business-central/overview/) website. For details on how to assign licenses to users, see the Microsoft article [Create users according to licenses](https://learn.microsoft.com/en-us/dynamics365/business-central/ui-how-users-permissions).

## Approval administrator permissions

Approval administrators have more permissions than ordinary approvers. When you set up a user as an approval administrator, the user is able to:

* Forward approval requests on behalf of other users. Ordinary approvers receive an error message if they attempt to do so.
* Use [the **Force Approval** feature](@DC-36).
* [Delete or edit approval requests](@DC-39), including adding and changing approvers.
* Approve documents for which imported and assigned amounts don't match. Ordinary approvers receive an error message in such cases, whereas approval administrators can choose to continue.
* Enable automatic approval and automatic posting in **Invoice Reg. Step 2** on the template level. Non-approval administrators trying to set **Invoice Reg. Step 2** to either **Release** or **Post** receive an error message explaining their limitations.
* Change [imported amounts](/continia-document-capture/setting-up-document-capture/setting-up-purchase-documents/configuring-purchase-documents#customization-of-imported-amounts).

## Configuring account and dimension permissions 

When you've set up a user as an approver [as described above](#to-set-up-users-as-approvers), you can configure the account and dimension permissions of that user. You do this using the following two actions on the action bar of the **Continia User Setup** page (also available in the **Continia User Setup Card**):

* **Approval User Groups** - this enables you to [assign one or more group permissions to the individual user](#to-assign-group-permissions-to-an-approver).
* **Approval Permissions** - this allows you to [configure the individual permissions of the user](#to-configure-individual-approver-permissions).

> [!IMPORTANT]
> For both of these actions to work, the **Use Account and Dimension Approval Permissions** feature on the **Document Capture Setup** page must first be enabled. To do this, see [To set up purchase approval](@DC-22#to-set-up-purchase-approval). To assign group permissions to an individual user, one or more [approval user groups must be set up](Approval user groups.md).

## To assign group permissions to an approver

To assign one or more group permissions to a user that's been configured as an approver:

1. Search ({{search}}) for and select **Continia User Setup**.
1. Select the user whose permissions you want to configure.
1. On the action bar, click **Document Capture** > **Approval User Groups**.
1. On the page that opens, add the group(s) whose permissions you want to assign to the user.
   > [!NOTE]
   > If you assign group permissions to a user, these permissions are inherited by – and impose certain restrictions on – the user's individual permissions, meaning that you may be somewhat limited if you also decide to [configure individual approver permissions](#to-configure-individual-approver-permissions). However, it's perfectly fine to do both at the same time, and the system lets you know if there are any conflicts between the individual permissions of a user and any assigned group permissions.

## To configure individual approver permissions

When setting up the individual permissions of an approver, you can configure the following two kinds of permissions:

* **Assigning permissions** - what accounts and dimensions the user can choose between when assigning accounts/dimensions to invoice lines during approval
* **Approval permissions** - what invoice lines the user can approve (only lines that have been assigned accounts/dimensions for which the user has permissions)

> [!IMPORTANT]
> Note that assigning permissions can only be used with the Web Approval Portal.
> 
> Also, for assigning permissions to take effect, the **Can Edit Posting Lines** feature must be enabled – as described above under [To set up users as approvers](#to-set-up-users-as-approvers) (step 4). Otherwise, the user receives documents for approval as read-only and is only able to approve or reject them.

To configure the individual permissions of a user that's been set up as an approver:

1. Search ({{search}}) for and select **Continia User Setup**.
1. Select the user whose permissions you want to configure.
1. On the action bar, click **Document Capture** > **Approval Permissions**.
1. On the page that opens, in the **Type** column, select the type of permission. **G/L Account**, **Item**, **Fixed Asset**, **Charge (Item)**, and **Job** are all types of account permissions, whereas **Dimension** represents dimension permissions.
1. If you selected **Dimension** in step 4 above: In the **Dimension Code** column, add a dimension code. If you selected anything other than **Dimension** in step 4, leave the field empty.
1. In the **Assigning Permission** column, specify how you want to set up the assigning permissions you want this user to have.
   > [!TIP]
   > Explanatory notes on the options:
   > * **All** - the user can assign all accounts/dimensions to invoice lines during approval, and no further setup is required.
   > * **Include Selected** - the user can assign the accounts/dimensions that you select in the **No. of Assigning Selections** column (which is then mandatory to fill out).
   > * **Exclude Selected** - the user can assign all accounts/dimensions *except* the ones you select in the **No. of Assigning Selections** column (which is then mandatory to fill out).
   > * **Filter** - the user can assign the accounts/dimensions that you select in the **Assigning Filter** column (which is then mandatory to fill out).
1. In the **Approval Permission** column, specify how you want to set up the approval permissions you want this user to have.
   > [!TIP]
   > Explanatory notes on the options:
   > * **All** - the user can approve invoice lines with any accounts/dimensions, and no further setup is required.
   > * **Include Selected** - the user can approve invoice lines with the accounts/dimensions that you select in the **No. of Approval Selections** column (which is then mandatory to fill out).
   > * **Exclude Selected** - the user can approve invoice lines with any accounts/dimensions *except* the ones you select in the **No. of Approval Selections** column (which is then mandatory to fill out).
   > * **Filter** - the user can approve invoice lines with the accounts/dimensions that you select in the **Approval Filter** column (which is then mandatory to fill out).
   > * **Same as Assigning** - the settings configured for assigning permissions in step 6 are copied and used as the user's approval permissions as well.
1. If you selected **Filter** in step 6 above: In the **Assigning Filter** column, select the accounts/dimensions that you want the user to be able to assign to invoice lines during approval.
1. If you selected **Filter** in step 7 above: In the **Approval Filter** column, select the accounts/dimensions that you want the user to be able to approve invoice lines for.
   > [!NOTE]
   > For both filter options (steps 8 and 9), you can enter ranges or multiple accounts/dimensions using standard filter notation – for example, **10100..10500** and **10100|10500**. 
1. If you selected **Include Selected** or **Exclude Selected** in step 6 above: In the **No. of Assigning Selections** column, select the accounts/dimensions that you want the user to be (un)able to assign to invoice lines during approval.
1. If you selected **Include Selected** or **Exclude Selected** in step 7 above: In the **No. of Approval Selections** column, select the accounts/dimensions that you want the user to be (un)able to approve invoice lines for.

## Related information

[Enabling purchase approval](@DC-22)  
[Approval user groups](Approval user groups.md)  
[Email notifications](Email notifications.md)