---
title: Email notifications 
date: 25-06-2025
description: How to set up, customize, and send status and reminder emails
id: EM-297
lang: en
---

# Email notifications

Ensure approvers are notified by email when they need to approve, reject, or cancel documents in Expense Management or in the Continia Web Approval Portal. You can notify approvers manually or automatically using job queues, and you can customize the outgoing notification emails.

## Pre requisites

Before Expense Management can send notification emails, you must first configure an email account.
To configure an email account with Expense Management:

1. In Expense Management, search for {{search}} **Set up email**.
1. Follow the on-screen instructions of the assisted setup guide to configure the email account.

## Send status emails manually

You can send status emails ad-hoc to all approvers that have pending approval requests whenever you need to notify them about documents pending their approval. Each status email includes a table listing all documents pending their approval and a link to the approval client which details all of their remaining approval requests for the day. 

Prior to sending out status emails, ensure all email recipients are set up so they can approve documents in Expense Management or in the Web Approval Portal, see [Expense user setup for Expense Management](@EM-36).

To manually send status emails:

1. Search for {{search}} **Send Status email to Approvers**. 
1. Click **Send Status email to Approvers (Expense Management)**. 

The approval client then displays all remaining approval requests not yet handled for the day. 

To determine when to send out additional notifications, Expense Management logs when a status email is sent to an approver. The first status email of the day (manual or automatic), contains all documents pending approval from the approver. Any subsequent emails sent to the approver that day are for new approval requests that were added after the first email was sent.

## Send status emails using job queues

By design, Expense Management doesn't support standard Microsoft Dynamics NAV/Business Central notifications. However, you can send status emails to approvers automatically using job queues.

To have Expense Management send status emails to approvers automatically:

1. Work through the procedure in [Setting up Job Queues](@EM-65).
1. In the **Object ID to Run** field, enter codeunit 6086313 to set up a status email job queue.
1. Set the recurrence rate to run, every 10-15 minutes.

The codeunit only sends out notification emails whenever a new approval entry has been created. This ensures approvers are always up to date with new approval entries. In case of no new approval entries, no email is sent for 24 hours.

Each status email includes a table listing all documents pending their approval and a link to the approval client which details all of their remaining approval requests for the day. 

Prior to automating status emails, ensure all email recipients are set up so they can approve documents in Expense Management or in the Web Approval Portal. For more information, see [Expense user setup for Expense Management](@EM-36).

## Customize notification emails

You can customize elements of emails sent to approvers, such as the default subject line and the text they contain.

To customize notification emails:

1. Search for {{search}} **Expense Management Setup**.

1. You can change the subject line of notification emails, under **Email** > **Reminder Email**.

1. Click **Approval Email Subject**, then enter the text for the email subject.

### Import custom templates
You can import a custom HTML template on the action bar.

   1. Click **Actions** > **Email** > **Import Approval Template**.
   1. Open the HTML template you want to import.
   1. When you create a custom template, you must keep the two keywords #DOCUMENTS# and #APPROVALFORMLINK# as Expense Management replaces them with a list of all relevant documents for approval and a link to the relevant approval client.

   > [!TIP]
   > Your Expense Management installation package includes a status email HTML template. You can edit and use it as a basis for your own custom template. Go to: [drive]\Support Files\Document Capture\Other. 

### When to use the default template
If you don't import your own custom HTML template, Expense Management will use the default template, which is hardcoded in a text variable in the CEM Expense Approval E-mail codeunit. 

If a custom template has been previously been imported but you want to use the default template instead, you can delete the imported template.

To delete an imported template:

1. On the **Expense Management Setup** page, on the action bar, click **Actions** > **Email** > **Delete Approval Template**, (only visible if a template has been imported).
1. A dialog box asks if you want to delete the template. Click **Yes** to delete the previously imported template and revert to the default.

## Related information

For further information relating to this article, see:

[Expense user setup for Expense Management](@EM-36)

[Setting up job queues](@EM-65)

