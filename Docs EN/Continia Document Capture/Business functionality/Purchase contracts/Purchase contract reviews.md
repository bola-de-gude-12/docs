---
title: Purchase contract approvals in Document Capture
date: 23-07-2025
description: How purchase contract approvals work in Document Capture.
id: DC-87
lang: en
---

# Purchase contract approvals

The purchase contract approval process is a central part of the Purchase Contracts module. The purpose of contract approvals is to ensure that one person in an organization – the approver – is responsible for periodically checking one or more of the organization's current contracts and making sure that they're up to date, renewed, canceled, or modified – if necessary. You can assign different approvers to different contracts, or have one person approve all contracts – whatever makes the most sense for your organization.

Prior to the release of Continia Document Capture 25.00, this process was known as purchase contract reviews. It has since been overhauled to bring it in line with the approval of purchase invoices. Note that:

* The following Document Capture approval module features are currently not supported: advanced approval, four-eye approval, and approval flows.
* After upgrading to 25.00, the status of existing purchase contracts that have already been reviewed is set to **Released**, while all others are set to **Approval Needed**. Therefore, these need to be reviewed.
* If the Document Approval module isn't activated in your environment, the purchase contracts functionality process is limited. Therefore, many of the features described in this article aren't available.

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src=https://player.vimeo.com/video/1028406654?h=c686b4ad1c&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479 frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="DC_purchase_contracts approvals_produced"></iframe></div><script src=https://player.vimeo.com/api/player.js></script>

## To use the approval functionality
To start using the approval functionality:

   1. Search ({{search}}) for and select **Purchase Contracts Setup**.
   2. On the **Approval** FastTab, switch on the **Enable Purchase Contract Approval** setting and, if needed, the **Enable Purchase Contract Force Approval** setting.
   3. On the action bar, click **Workflows and Users** > **Continia User Setup** and configure the fields **Purchase Contract Amount Approval Limit**, **Unlimited Purchase Contract Approval**, and **Purchase Contract Approver ID** according to your needs.

A purchase contract administrator – typically a controller – initiates the process by either sending one contract or a batch of contracts to the approver, who then approves, rejects, or forwards the contracts. In each approval, the approver can add comments for the controller to consider.

## Additional approval functionality

Note that the following approval functionality is only available for purchase contracts when the Document Capture Document Approval module is active and purchase contract approval is enabled.

* Force approval and approval sharing.
* Additional fields on the **Purchase Contract** card:
  * **Approval by** - specifies the users who are part of the approval flow for the document.
  * **Approval Comments** - specifies the last comment added to this document. You can use lookup to show all comments.
* Additional fields on the **Purchase Contracts** page:
  * **Approval by** - specifies the users who are part of the approval flow for the document.
  * **Comments** - shows if any approval comments exist for the purchase contract.

* Additional actions on the **Purchase Contract** card:
  * **Force Approval** - forces the approval of the purchase contract, bypassing the approval flow.
  * **Comments** - opens the **Approval Comments** page.

* Modified actions on the **Purchase Contract** card:
  * **Approvals** - opens the **Purchase Contract Approval Request Entries** page, which has functionality such as **Add Approver** and **Forward**.

* When you reject an approval, the **Approval Comment** page is opened. This allows you to see previous approval comments and add a rejection comment.

* The forward functionality has three options:
  * **Approve & Forward**
  * **Forward without approval**
  * **Forward and send the document back to me after approval**

> [!TIP]
> As an alternative to using the {{search}} icon as described in the guides below, both the approvers and the approval administrator can navigate through the approval process using the following Cues in the **Purchase Contracts** Cue group in the Microsoft Dynamics 365 Business Central Role Center:
>
> * **All** - covers all contracts and provides an overview for all users.
> * **Approval Due** - covers contracts with the **Next Approval Date** set to the current date or any date before it.
> * **Approval Needed** - covers contracts with the **Approval Status** set to **Approval Needed**.
> * **Pending Approval** - covers contracts with the **Approval Status** set to **Pending Approval**.

## To set up an approval administrator

To force approvals, you must be set up as an approval administrator. To do this:

1. Search ({{search}}) for and select **Continia User Setup**.
1. In the list of Continia users, click the ID of the user that you want to make an approval administrator. This opens the **Continia User Setup Card**.
1. On the **General** FastTab, enable the **Approval Administrator** setting.

## To send a single contract for approval

As an approval administrator, you can send a contract for approval by following these steps:

1. Search ({{search}}) for and select **Purchase Contracts**.
1. In the list of contracts, select the one that you want to send for approval.
1. On the action bar, click **Approve** > **Send Approval Request**.

This sends the contract for approval, and the **Status** field on the **Approvals** FastTab changes to **Pending Approval**.

## To send a batch of contracts for approval

As an approval administrator, you can send a batch of contracts for approval by following these steps:

1. Search ({{search}}) for and select **Purchase Contracts**.

1. On the action bar, click **Home** > **Send Approval Request Batch** to open the **Send purchase contracts for approval** page.

1. On the **Filter: Purchase Contract Header** FastTab, the **Next Approval Date** filter is added and prefilled with the date range **..[today]**, which means that all contracts that haven't yet been reviewed and whose **Next Approval Date** has been exceeded are sent for review in one batch. If necessary, change the prefilled date range.

1. **Optional:** To add another filter, click **+ Filter**.

1. **Optional:** To run the batch report at a later time, click **Schedule...**, and then select a start date/time and an expiration date/time. You can also enter a date formula, which autofills **Earliest Start Date/Time**.
   
   > [!NOTE]
   > If you select **Next Run Date Formula**, you must enter a formula in the form of a whole number followed by **D** (days), **WD** (weekdays), **W** (weeks), **M** (months), **Q** (quarters), or **Y** (years) – for example, **2W** (two weeks). For more advanced formulas, you can also use the mathematical symbols + and –, or you can enter the letter **C** (current) as a prefix to any of the previously mentioned time units – for example, **CM+10D** (current month plus ten days).
   
1. Click **OK** when you're done.

This sends all contracts within the specified date range for approval in one batch, and the **Approval Status** field on the **Approvals** FastTab changes to **Pending Approval** for each of the contracts.

## Automatic update of approval status
If you make a change to one or more of the following header fields, the status of a purchase contract is automatically set to **Approval Needed**:

* Vendor No.
* Purchaser Code
* Currency Code
* Price Type
* Invoicing Period Code
* Contract Start Date
* Contract End Date
* Auto Approve Within Variance
* Approval Frequency
* Approval Freq. Date Formula

If you make a change to one or more of the following line fields, the status of a purchase contract is also automatically set to **Approval Needed**:

* Type
* No.
* Price Type
* Currency Code
* Quantity
* Unit Cost
* Amount
* Status
* Prices Incl. VAT
* Amount Incl. VAT
* Start Date
* End Date
* Invoicing Period

>[!NOTE]
>Deleting an active purchase contract line also triggers the change in approval status.

## To cancel a contract approval request

To cancel an approval request that you've initiated, follow these steps:

1. Search ({{search}}) for and select **Purchase Contracts**.
1. In the list of contracts, select the one whose approval you want to cancel.
1. On the action bar, click **Approve** > **Cancel Approval Request**.

On the **Purchase Contract** page, the **Approval Status** field on the **Approvals** FastTab changes from **Pending Approval** to **Approval Needed**.

## To submit a contract approval

Once a contract has been sent to you for approval by an approval administrator, you can approve the contract. You can do this in either Business Central or the Continia Web Approval Portal.

### Using Business Central

To submit an approval using Business Central:

1. Search ({{search}}) for and select **Purchase Contracts**.
1. In the list of contracts, in the **No.** column, click the number of the contract that you want to approve. This opens the **Purchase Contract** page.
1. Review the contract.
1. On the action bar, click **Request Approval** > **Approve**.

This approves the request, and the **Approval Status** field on the **Approvals** FastTab changes to **Released**.

### Using the Web Approval Portal

To submit a review using the Web Approval Portal:

1. Sign in to the Web Approval Portal.
1. On the **Purchase** tab, click **Contracts** to open the **My Pending Approvals** page.
1. In the list of contracts for approval, select the one that you want to approve.
1. Approve the contract.
1. In the text field in the upper-right corner, enter your comments and click **Save** when you're done. Repeat this step if you have additional comments.
1. On the action bar, click **Submit Approval**.

This sends your approval to the purchase approval administrator. Also, In Business Central, on the **Purchase Contract** page, the **Status** field on the **Approval** FastTab changes to **Approval Submitted**.

## Related information

[Creating purchase contracts](@DC-86)  
[Creating contract invoices](@DC-88)  
[Approving contract invoices](@DC-89)  
[Viewing the Purchase Contracts Archive](@DC-90)  