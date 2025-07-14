---
title: Approval user groups in Document Capture
date: 31-03-2025
description: How to set up approval user groups with specific account and dimension permissions in Document Capture.
id: DC-24
lang: en

---

# Approval user groups

It's possible to set up approval user groups with specific account and dimension permissions that apply to all members of the group. This is useful if you have a fairly large group of approvers who must all have the same set of assigning and approval permissions, as you then avoid having to reconfigure the approvers' permissions individually.

   > [!NOTE]
   > Enabling purchase invoice approval, purchase credit memo approval, order approval and/or return order approval automatically creates an approval user group with the code ALL – that is, with all permissions on all types and dimensions –, but only if such a group doesn’t already exist.

## To set up approval user groups

To create a group of approvers and add members to it:

1. Choose the {{search}} icon, enter **Approval User Groups**, and then choose the related link.

1. On the action bar, click **New** to create a approval user group.

1. In the **Code** column, enter the code by which you want to identify the new group.

1. In the **Name** column, enter the name of the new group.

1. To add members to the group, select the group in the list, and then select **Members** on the action bar to open the group's members page.

1. On the action bar, click **New**, and then select a member from the list. Repeat this step for all members you want to add, and return to the **Approval User Groups** page when you're done.

   > [!NOTE]
   > To add members to a group, the members must be [configured as approvers](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#to-set-up-users-as-approvers) first. Otherwise they're not available in the list.

## To configure account and dimension permissions for a group

> [!IMPORTANT]
> An important prerequisite for this guide is that you enable the **Use Account and Dimension Approval Permissions** feature on the **Document Capture Setup** page. To do this, see [To set up purchase approval](@DC-22#to-set-up-purchase-approval). Prior to enabling this feature, it's recommended that you create an approval user group containing all non-critical dimensions and account types (e.g.: jobs, resources, fixed assets, etc.) – allowing approvals, but without assigning permissions. Then, add all relevant approvers to this group. This approach allows the approvers to approve documents where non-critical dimension and account values are included.

Once you've set up an approval user group as described in [To set up approval user groups](#to-set-up-approval-user-groups), you can assign account and dimension permissions to it. You can configure the following two kinds of permissions:

* **Assigning permissions** – what accounts and dimensions the group members can choose from when assigning accounts/dimensions to invoice lines during approval using the Continia Web Approval Portal.
* **Approval permissions** – what invoice lines the group members can approve (only lines that have been assigned accounts/dimensions for which the members have permissions).

For more information on these two overall types of permissions, see [Additional details on assigning and approval permissions](#additional-details-on-assigning-and-approval-permissions) below.

> [!IMPORTANT]
> Note that assigning permissions can only be used with the Web Approval Portal.
>
> Also, in order for assigning permissions to take effect, the **Can Edit Posting Lines** feature must be enabled for all group members, as described under [To set up users as approvers](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#to-set-up-users-as-approvers) (step 4). Otherwise the members will receive documents for approval as read-only and will only be able to approve or reject them.

To assign account and dimension permissions to an approval user group:

1. Choose the {{search}} icon, enter **Approval User Groups**, and then choose the related link.

1. Select the group in the list, and then select **Permissions** on the action bar.

1. In the **Type** column, select the type of permission. **G/L Account**, **Item**, **Fixed Asset**, **Charge (Item)**, and **Job** are all types of account permissions – whereas **Dimension** represents dimension permissions.

1. If you selected **Dimension** in step 3 above: In the **Dimension Code** column, add a dimension code. If you selected anything other than **Dimension** in step 3, leave the field empty.

1. In the **Assigning Permission** column, specify how you want to set up the assigning permissions you want the group members to have.

   > [!TIP]
   > Explanatory notes on the options:
   >
   > * **All** - the group members can assign all accounts/dimensions to invoice lines during approval, and no further setup is required.
   > * **Include Selected** - the members can assign the accounts/dimensions that you select in the **No. of Assigning Selections** column (which is then mandatory to fill out).
   > * **Exclude Selected** - the members can assign all accounts/dimensions except the ones you select in the **No. of Assigning Selections** column (which is then mandatory to fill out).
   > * **Filter** - the members can assign the accounts/dimensions that you select in the **Assigning Filter** column (which is then mandatory to fill out).

1. In the **Approval Permission** column, specify how you want to set up the approval permissions you want the group members to have.

   > [!TIP]
   > Explanatory notes on the options:
   >
   > * **All** - the group members can approve invoice lines with any accounts/dimensions, and no further setup is required.
   > * **Include Selected** - the members can approve invoice lines with the accounts/dimensions that you select in the **No. of Approval Selections** column (which is then mandatory to fill out).
   > * **Exclude Selected** - the members can approve invoice lines with any accounts/dimensions except the ones you select in the **No. of Approval Selections** column (which is then mandatory to fill out).
   > * **Filter** - the members can approve invoice lines with the accounts/dimensions that you select in the **Approval Filter** column (which is then mandatory to fill out).
   > * **Same as Assigning** - the settings configured for assigning permissions in step 5 are copied and used as the members' approval permissions as well.

1. If you selected **Filter** in step 5 above: In the **Assigning Filter** column, select the accounts/dimensions that you want the group members to be able to assign to invoice lines during approval.

1. If you selected **Filter** in step 6 above: In the **Approval Filter** column, select the accounts/dimensions that you want the group members to be able to approve invoice lines for.

   > [!NOTE]
   > For both filter options (steps 7 and 8), you can enter ranges or multiple accounts/dimensions using standard filter notation. For example, **10100..10500** and **10100|10500**. 

1. If you selected **Include Selected** or **Exclude Selected** in step 5 above: In the **No. of Assigning Selections** column, select the accounts/dimensions that you want the group members to be (un)able to assign to invoice lines during approval.

1. If you selected **Include Selected** or **Exclude Selected** in step 6 above: In the **No. of Approval Selections** column, select the accounts/dimensions that you want the group members to be (un)able to approve invoice lines for.

## Additional details on assigning and approval permissions

Specifically for assigning permissions, note that whenever an approver uses a lookup field in the Web Approval Portal, the list of available options in the lookup field is limited by the assigning permissions of that approver – that is, whatever restrictions you've applied using the **Filter**, **Include Selected**, and/or **Exclude Selected** options mentioned [above](#to-configure-account-and-dimension-permissions-for-a-group) and [here](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#to-configure-individual-approver-permissions).

For example, only 5-10 % of the total number of G/L accounts are typically relevant to the approver, so when you set up assigning permissions for the approver, you can limit the list of available G/L accounts to only include the ones that are relevant to that particular approver. In the Web Approval Portal, any applicable lookup field will then only display your selection of G/L accounts. The same principle applies to items, fixed assets, item charges, jobs, and dimensions.

For both assigning and approval permissions, the following applies: If an approver is a member of multiple approval user groups with different permissions or has been assigned permissions both individually and as a member of one or more approval user groups, the approver is granted the sum of all permissions. In case there's a conflict between assigned permissions – for instance, if permissions for the same record have been included in one group but excluded in another – the excluded permissions take precedence.

For example, an approver may have access to ten G/L accounts as a member of an approval user group, but if one of these accounts is then excluded in the approver's individually assigned permissions, the approver only has access to the remaining nine accounts assigned via the approval user group. Again, the same principle applies to items, fixed assets, item charges, jobs, and dimensions.

Specifically for approval permissions, it's worth noting that approvers are identified using the standard procedures (either through approval flows or via **Purchaser Code** for the first approver and amount limits for any additional approvers) – they're not identified based on account/dimension types. However, when a document is approved and ready to be released, Document Capture checks that all lines have been approved by approvers that have the required permissions for the types of accounts/dimensions used.

> [!NOTE]
> Approval permissions are only checked when the last approver in the chain is approving the document. This permission check takes into account the permissions of all approvers in the chain, combining them into a single set of permissions. At the same time, changes made to key line values are also compared. If one of the approvers in the chain changes a value, such as a dimension in an order line, the previous approval is deemed obsolete.

## Related information

[Enabling purchase approval](@DC-22)  
[Continia user setup for approvals](Continia user setup for approvals.md)  