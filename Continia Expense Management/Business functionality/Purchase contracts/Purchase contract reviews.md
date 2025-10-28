---
title: Expense Management Purchase Contract Reviews
date: 01-04-2023
description:  
id: EM-132
lang: en
---

# Purchase Contract Reviews

The review process is a central part of the Purchase Contracts module. The purpose of contract reviews is to ensure that one person in an organization – the reviewer – is responsible for periodically checking one or more of the organization's current contracts and making sure that they're up to date, renewed, cancelled, or modified, if necessary. You can assign different reviewers to different contracts or have one person review all contracts – whatever makes the most sense for your organization.

A purchase contract administrator – typically an accountant – will initiate the process by sending either one contract or a batch of contracts to the reviewer, who will then review the contracts and send them back to the accountant for verification and finalization. In each review, the reviewer can add extra lines, remove unused ones, and write review comments for the purchase contract administrator to consider.

The individual steps of the process are described in more detail in the sections below.

> [!TIP]
> As a useful alternative to using the {{search}} icon as described in the guides below, both the reviewers and the purchase contract administrator can easily navigate through the review process using the Cues in the **Purchase Contracts** Cue group on the Microsoft Dynamics 365 Business Central Role Center. The group contains the following four Cues:
> * **All**: Covers all contracts and provides a good overview for all users.
> * **Review Due**: Covers contracts whose **Next Review Date** is up to a week before today's date. This Cue is mainly intended for reviewers.
> * **Review Overdue**: Covers contracts whose **Next Review Date** is more than a week before today's date. This Cue is mainly intended for reviewers.
> * **Review Submitted**: Covers contracts that have been reviewed and returned by the reviewer. This Cue is mainly intended for the purchase contract administrator.

## To set up a purchase contract administrator

In order to be able to send contracts for review and carry out a number of other review actions, you must be set up as a purchase contract administrator. To do this, follow these steps:

1. Choose the {{search}} icon, enter **Continia User Setup**, and then choose the related link.
1. In the list of Continia users, select the ID of the user that you want to make a purchase contract administrator. This will open the **Continia User Setup Card**.
1. On the **General** FastTab, in the **Purchase Contracts** section, toggle the **Purchase Contract Administrator** switch.

This will make the selected user a purchase contract administrator capable of sending contracts for review and managing reviews in general.

## To send a single contract for review

> [!NOTE]
> Only purchase contract administrators can perform this action. To set up a purchase contract administrator, follow [the guide above](#to-set-up-a-purchase-contract-administrator).

As a purchase contract administrator, you can send a contract for review by following these steps:

1. Choose the {{search}} icon, enter **Purchase Contracts**, and then choose the related link to open the **Purchase Contracts** page.
1. In the list of contracts, select the one that you want to send for review.
1. In the action bar, select **Process** > **Start Review**.

This will send the contract for review, and the **Status** field on the **Review** FastTab will change to **Pending Review**.

## To send a batch of contracts for review

> [!NOTE]
> Only purchase contract administrators can perform this action. To set up a purchase contract administrator, follow [the guide above](#to-set-up-a-purchase-contract-administrator).

As a purchase contract administrator, you can send a batch of contracts for review by following these steps:

1. Choose the {{search}} icon, enter **Purchase Contracts**, and then choose the related link to open the **Purchase Contracts** page.
1. In the action bar, select **Process** > **Start Review Batch...** to open the **Send Purchase Contracts for Review** page.
1. On the **Filter: Purchase Contract Header** FastTab, the **Next Review Date** filter is added and prefilled with the date range **..[today]**, which means that all contracts that haven't yet been reviewed and whose **Next Review Date** has been exceeded will be sent for review in one batch. If necessary, change the prefilled date range.
1. **Optional:** If you want to add another filter, select **+ Filter**.
1. **Optional:** On the **Advanced** FastTab, enter any necessary restrictions to the batch report in terms of row generation time and/or maximum number of rows or documents.
1. **Optional:** If you want to run the batch report at a later time, select **Schedule...**, and then select a start date/time and an expiration date/time. You can also enter a date formula, which will then autofill **Earliest Start Date/Time**.
   > [!NOTE]
   > If you select **Next Run Date Formula**, you must enter a formula in the form of an integer followed by **D** (days), **WD** (weekdays), **W** (weeks), **M** (months), **Q** (quarters), or **Y** (years) – for example, **2W** (two weeks). For more advanced formulas, you can also use the mathematical symbols + and –, or you can enter the letter **C** (current) as a prefix to any of the previously mentioned time units – for example, **CM+10D** (current month plus ten days).
1. Select **OK** when you're done.

This will send all contracts within the specified date range for review in one batch, and the **Status** field on the **Review** FastTab will change to **Pending Review** for each of the contracts.

## To cancel a contract review

> [!NOTE]
> Only purchase contract administrators can perform this action. To set up a purchase contract administrator, follow [the guide above](#to-set-up-a-purchase-contract-administrator).

If, for some reason, you want to cancel a review that you've initiated, you can do this by following these steps:

1. Choose the {{search}} icon, enter **Purchase Contracts**, and then choose the related link to open the **Purchase Contracts** page.
1. In the list of contracts, select the one whose review you want to cancel.
1. In the action bar, select **Process** > **Cancel Review**.
1. A dialog appears, asking if you want to cancel the review. Select **Yes**.

This will cancel the review. Also, on the **Purchase Contract** page, the **Status** field on the **Review** FastTab will change from **Pending Review** to empty. 

## To submit a contract review

Once a contract has been sent to you for review by a purchase contract administrator, you can review the contract and submit your review back to the administrator. You can do this in either Business Central or the Continia Web Approval Portal, as described in the following two sections:

### Using Business Central

To submit a review using Business Central, follow these steps:

1. Choose the {{search}} icon, enter **Purchase Contracts**, and then choose the related link to open the **Purchase Contracts** page.
1. In the list of contracts, in the **No.** column, select the number of the contract that you want to review. This will open the **Purchase Contract** page.
1. Review the contract, and make any necessary changes.
1. When you've reviewed the contract, go to the **Review** FastTab, and select the **Comments** field.
1. On the page that opens, in the action bar, select **New** to add a comment line.
1. Under **Comment**, enter your review comments. The **Date** and **Name** fields will be autofilled.
1. Repeat steps 5-6 if you have additional comments, and then go back to the **Purchase Contract** page. Here, your comments will be displayed in the **Comments** field.
1. In the action bar, select **Process** > **Submit Review**.
1. A dialog appears, asking if you want to submit the review. Select **Yes**.

This will send your review to the purchase contract administrator, and the **Status** field on the **Review** FastTab will change to **Review Submitted**.

### Using the Web Approval Portal

To submit a review using the Web Approval Portal, follow these steps:

1. Sign in to the Web Approval Portal.
1. On the **Purchase** tab, select **Contracts** to open the **My Pending Reviews** page.
1. In the list of contracts for review, select the one that you want to review.
1. Review the contract, and make any necessary changes.
1. In the text field in the upper-right corner, enter your review comments, and select **Save** when you're done. Repeat this step if you have additional comments.
1. In the action bar, select **Submit Review**.

This will send your review to the purchase contract administrator. Also, In Business Central, on the **Purchase Contract** page, the **Status** field on the **Review** FastTab will change to **Review Submitted**.

## To finalize a contract review

> [!NOTE]
> Only purchase contract administrators can perform this action. To set up a purchase contract administrator, follow [the guide above](#to-set-up-a-purchase-contract-administrator).

As a purchase contract administrator, you can finalize a contract review by following these steps:

1. Choose the {{search}} icon, enter **Purchase Contracts**, and then choose the related link to open the **Purchase Contracts** page.
1. In the list of contracts, in the **No.** column, select the number of the contract that you want to finalize. This will open the **Purchase Contract** page.
1. Check the reviewer's contract changes and not least the review comments on the **Review** FastTab under **Comments**.
1. **Optional:** If something isn't quite right or you have questions for the reviewer, you can add a comment under **Comments** yourself, to let the reviewer know what's wrong or what you're unsure about. After this, return the contract to the reviewer by selecting **Process** > **Return to Reviewer**. In the dialog that appears, select **Yes**.
   > [!NOTE]
   > This will send the review back to the reviewer and change the **Status** field on the **Review** FastTab back to **Pending Review**. The reviewer can then check the administrator's comments, make any necessary changes, and resubmit the review as [described above](#to-submit-a-contract-review).
1. If, on the other hand, everything is in order, you can finish the review as follows: In the action bar, select **Process** > **Finish Review**.
1. A dialog appears, asking if you want to finish the review. Select **Yes**.

This will bring about five changes on the **Review** FastTab: It will clear the **Status** field to prepare for the next review cycle and update the **Next Review Date** field based on the review frequency that you've specified in the **Review** field. Also, any review comments you may have added will be displayed in the **Comments** field, **Last Date Reviewed** will be updated with today's date, and then your name will be displayed in **Last Reviewed by**.

## Related information

[Creating Purchase Contracts](@EM-131)  
[Approving Expenses Based on a Contract](@EM-133)  
[Viewing the Purchase Contract Archive](@EM-134)  