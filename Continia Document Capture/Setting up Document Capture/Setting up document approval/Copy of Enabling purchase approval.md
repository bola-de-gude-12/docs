---
title: Enabling purchase approval in Document Capture
date: 01-04-2025
description: How to enable purchase approval and edit the basic document approval settings.
id: 
lang: en
---

# Enabling purchase approval

Most of the basic document approval settings for Continia Document Capture – including those for approval workflows, force approval, four-eye approval, and approval checks and validations – can be edited from the **Document Capture Setup** page. This article describes how to access and edit these settings and how to enable purchase approval in the first place.

## To enable purchase approval using the assisted setup guide

You can easily enable Document Capture purchase approval using the assisted setup guide. To do this, follow these steps:

1. Choose the {{search}} icon, enter **Assisted Setup**, and then choose the related link to open the corresponding page.
1. Under **Continia Document Capture**, select **Create approval workflow** to open the assisted setup guide.
1. Select **Next**, and then select the approval workflows that you want to set up. Select **Next** to continue.
1. If you want to set up users as approvers right away, select **Open Continia User Setup** to open the user setup page, and then edit the list of users as needed. You can also do this later, following [this guide](@DC-23).
1. If you want to configure a number of more advanced approval settings immediately, select **Approval Setup** to open the **Document Capture Setup** page, and then make any necessary changes. You can also do this later, following the [guide below](#to-set-up-purchase-approval).
1. Select **Next** > **Finish** to complete the guide.

Once you've completed the assisted setup guide, go to the **Continia Solution Management** page and enable the **Document Approval** module. For information on how to do this, see [Using Continia Solution Management](@DC-107).

## To set up purchase approval

> [!NOTE]
> You may have already configured some or all of the settings mentioned in the following guide if you enabled purchase approval using the assisted setup guide [as described above](#to-enable-purchase-approval-using-the-assisted-setup-guide).

To set up Document Capture purchase approval, follow these steps:

1. Search {{search}} for and select **Document Capture Setup**.
1. On the action bar, click **Setup > Purchase Approval**.
1. Under **General**, you can enable the following types of approval and approval settings:
   * **Enable Order Approval**
   * **Enable Return Order Approval**
   * **Enable Invoice Approval**
   * **Enable Credit Memo Approval**

   > [!NOTE]
   > Enabling any of the above settings automatically creates an [approval user group](@DC-24) with the code ALL – that is, with all permissions on all types and dimensions –, but only if such a group doesn’t already exist.

   * **Allow Force Approval** – to actually apply force approval, see [Force Approval](@DC-36).
   * **Use Account and Dimension Approval Permissions** – to configure account and dimension permissions for a group or an individual user, see [Approval User Groups](Approval user groups.md) and [Configuring account and dimension permissions](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#configuring-account-and-dimension-permissions).
   * **Keep On Hold** – if you enable this, the **Remove On Hold** dialog won't be displayed to approvers when they approve documents that have been put on hold. Instead, the on-hold status will be kept by default throughout the approval process.
   * **Copy Document Comment to Approval Comment** - if enabled, document comments added prior to registration are made available as approval comments on purchase invoices, credit memos, and purchase orders when the document is registered.
   > [!TIP]
   > If, for example, the on-hold status of an invoice is removed, the invoice will appear to have been paid although it actually hasn't. Enabling **Keep On Hold** will ensure that approvers aren't presented with the option of removing 'on hold', thereby preventing them from performing any such unwanted actions.
1. Under **Email Setup**, you can customize the notification emails that are sent to approvers. For more information, see [To customize notification emails](@DC-26#to-customize-notification-emails).
1. To enable [four-eye approval](@DC-35), go to **4-eyes Approval** and select either **Required** or **Required - both with full amounts limits**, depending on what you prefer. Besides enabling four-eye approval, this makes the following two fields editable:
   1. **2nd Approver**: This allows you to specify if the second approver should be selected manually or automatically. For more details, see [Manual or automatic approver identification](@DC-35#manual-or-automatic-approver-identification).
   1. **4-eyes Threshold Amount (LCY)**: If you enter an amount in this field, four-eye approval will be applied only to invoices that exceed this amount in the local currency. All invoices with lower values will only need a single approver rather than two.
   > [!NOTE]
   > If document approval is initiated by an [approval flow code](@DC-33), four-eye approval won't apply even when enabled here.
1. If you want amounts and/or dimensions to be checked during or before approval (the latter only applies to dimensions), go to **Checks and Validation** and fill in the fields as needed.
1. Under **Purchase Allocation**, you can configure automatic or manual creation and posting of purchase allocation entries, if necessary. For more information, see [Setting up Purchase Allocations](@DC-41).

## See also

[Approval User Groups](Approval user groups.md)  
[Continia User Setup for Approvals](Continia user setup for approvals.md)  
[Four-Eye Approval](@DC-35)  