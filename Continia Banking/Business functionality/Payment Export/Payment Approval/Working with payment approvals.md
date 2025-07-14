---
title: Working with Payment Approval Workflows in Continia Banking
date: 08-10-2024
description: Describes how you can make approval requests and manage those requests.
id: CB-28
lang: en
---

# Working with Payment Approvals

Payment Approval workflows can be created for Continia Banking-enabled payment journals and set up to require approval of either the payment journal batch combined or the individual lines. If a Payment Approval workflow has been created for a payment journal, all payments must be sent for approval before they can be sent to the bank. 

## To request an approval

To request or cancel the approval for a journal batch or line:

1. Search ({{search}}) for and select **Payment Journals**.
2. If the payment journal has been set up with Journal Line Approval, in the payment journal, select the relevant lines. The lines must have the status "Valid" before you can send them for approval.
3. Select **Prepare** > **Send Approval Request**. If the payment journal has been set up with Journal Batch Approval, all the lines will be combined into one approval request. 
4. The status of the lines changes to "Pending Approval." 
5. To cancel an approval request, select **Prepare** > **Cancel Approval Request**. The status changes back to "Valid." 

> [!IMPORTANT]
>
> If you have sent an approval request for the journal batch, you can't add any extra lines until the batch has been approved and posted. 



## To approve or manage pending approval requests 

You can access an overview of the requests pending your approval from the Role Center. Unless you have admin permissions, you can only handle approval requests assigned to yourself. Depending on the setup, you'll also receive an email notification about requests pending your approval. 

To view and manage approval requestse:

1. Search ({{search}}) for and select **Payment Requests to Approve**.

   > [!NOTE]
   >
   > If you are using either the Accountant, Bookkeeper, or Business Manager role, you can access this overview directly from the Role Center, under **Pending Approvals** > **Requests to Approve**. 

3. In the list, select the approval requests you want to manage, and select one of the following actions in the action menu.
   -  **Approve**: Approve the selected payments. The status of the relevant lines in the payment journal changes to "Approved."
   -  **Reject**: Reject the selected requests. The status of the relevant lines in the payment journal changes to "Rejected Approval."
   -  **Delegate**: Forward the selected requests to a specific user with or without approval. When you delegate an approval request, any approval limit is disregarded so that you can delegate approval requests to any user set up on the **Approval User Setup** page. 
   -  **Open Record**: View the related payment details in the payment journal.
   -  **Comments**: Add a comment about the approval request before you process it. If you delegate the approval request to a different user, this will be added as a comment. The comment is visible for all other approvers. 

4. To view all requests, including the approved and rejected requests, in the action menu, select **Actions** > **View** > **All Requests**.

## To handle a rejected line

If an approval request has been rejected, you can correct it, validate it and send a new approval request.

To handle a rejected line:

1. Search ({{search}}) for and select **Payment Journals**.
2. Make the relevant changes to the line.
3. Select **Prepare** > **Validate Payments**. This changes the status of the line to Valid.
4. To send a new approval request, select **Prepare** > **Send Approval Request**.

> [!IMPORTANT]
>
> When you select **Validate Payments**, be aware that all the payment lines will be validated – not just the selected line.



## To view and manage sent approval requests

From the Role Center, users who have sent an approval request from a payment journal can access an overview of the requests, their status, and if they are overdue.

> [!TIP]
>
> Consider using the Bookkeeper role for an overview of the most important Continia Banking features. With this role assigned, the Role Center view contains most tasks for handling day-to-day financial tasks, such as creating, paying, and approving invoices.


To view and manage requests sent for approval:

1. Search ({{search}}) for and select **Payment Approval Entries**.
	 > [!NOTE]
	>
	> If you are using either the Accountant, Bookkeeper, or Business Manager role, you can access this overview directly from the Role Center, under **Payment Approvals** > **Requests Sent for Approval**. 
1. In the list, select the approval requests you want to manage, and select one of the following options:
   -  **Delegate**: Forward the selected requests to a specific user with or without approval. When you delegate an approval request, any approval limit is disregarded so that you can delegate approval requests to any user set up on the **Approval User Setup** page. 
   -  **Record**: View the details of the related payment in the payment journal.
   -  **Comments**: Add a comment about the approval request before you process it.  If you delegate the approval request to a different user, this will be added as a comment.  This comment is visible for all other approvers.

> [!TIP]
>
> Users with the Admin or SUPER permission set assigned, can view details and delegate all payment approval requests sent from all payment journals.





