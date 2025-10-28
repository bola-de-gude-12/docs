---
title: Email notifications 
date: 25-06-2025
description: How to set up, customize, and send status and reminder emails
id: DC-26
lang: en
---

# Email notifications

You can notify approvers by email when they need to carry out an approval action in Continia Document Capture or the Continia Web Approval Portal, such as approving, rejecting, or cancelling a document. It's possible to send this notification either [manually](#to-send-status-emails-manually) or [automatically using job queues](#to-send-status-emails-using-job-queues).

If necessary, you can [customize the actual emails](#to-customize-notification-emails) – and it's also possible to [set up reminder emails](#to-set-up-reminder-emails) to escalate the importance of having documents approved.

Before you can send notification emails, you must configure an email account using the assisted setup guide:

1. Search ({{search}}) for and select **Set up email**.
1. Follow the on-screen instructions to set up the email account.

## To send status emails manually

To manually notify approvers that there are documents pending their approval:

1. In the Role Center, go to **Continia Document Capture Activities**.
1. Under **Actions**, click **Send Status Email to Approvers**.

Emails are now sent to all approvers that have pending approval requests. Each email contains a table with all documents pending approval and a link to the approval client that the recipient has been [configured to use for approving documents](@DC-23#to-set-up-users-as-approvers) (either Document Capture or the Web Approval Portal). The approval client then displays all approval requests that haven't already been taken care of for that day.

> [!NOTE]
> When a status email is sent to an approver, this is logged by Document Capture, which uses the information to determine when to send out additional notifications. The first time the status-email process is run on any given day – whether manually or automatically using job queues –, an email containing all documents pending approval from the approver is sent to that approver. However, any subsequent process runs on the same day will only result in the sending of status emails to the approver if new approval requests involving that approver have been added since the first process run.

## To send status emails using job queues

It's also possible to have status emails sent to approvers automatically using job queues. For more information, see [Setting up job queues](@DC-16).

Each email contains a table with all documents pending approval and a link to the approval client that the recipient has been [configured to use for approving documents](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#to-set-up-users-as-approvers) (either Document Capture or the Web Approval Portal). The approval client then displays all approval requests that haven't already been taken care of for that day.

>[!TIP]
>To avoid duplicate notifications, it's recommended that you disable the standard Microsoft Dynamics NAV/Business Central notifications. Otherwise, both Document Capture and NAV/Business Central will notify approvers about the same approval requests.
>
>To disable the standard notifications:
>1. Search ({{search}}) for and select **Document Capture Setup**.
>2. On the **General** FastTab, under **Purchase Approval**, click the link in the **Status** field.
>3. On the **Document Capture Setup / Purchase Approval** page, turn off the **Enable Standard Notification** setting.

## To customize notification emails

To customize certain parts of the emails sent to approvers, including their default subject lines and the actual text they contain:

1. Search ({{search}}) for and select **Document Capture Setup**.
1. On the **General** FastTab, under **Purchase Approval**, click the link in the **Status** field.
1. On the **Document Capture Setup / Purchase Approval** page, under **Email Setup**, fill out the fields as needed.
1. **Optional**: To import a custom HTML template with, for example, different text and formatting than the default template, click **Status Email** > **Import Template** > **Choose** on the action bar and open the HTML template you want to import.
   
   > [!TIP]
   > The Document Capture installation package comes with a status email HTML template that you can edit and use as a basis for your own custom template. It can be found in: [drive]\Support Files\Document Capture\Other.
   > 
   > Note that if you do create your own custom template, you must keep the two keywords #DOCUMENTS# and #APPROVALFORMLINK#. When creating the notification email, Document Capture will replace these two keywords with a list of all relevant documents for approval and a link to the relevant approval client.
   
   > [!NOTE]
   > If you don't import your own custom HTML template, Document Capture will use the default template, which has been hardcoded in a text variable in the **CDC Purch. Approval E-Mail** codeunit. 
   > 
   > In case a custom template has previously been imported and you wish to use the default template instead, you can delete the imported template by following these steps:
   > 1. On the **Document Capture Setup / Purchase Approval** page, on the action bar, click **Actions** > **Email** > **Delete Template**.
   > 1. A dialog box asks if you want to delete the template. Click **Yes** to delete the previously imported template and revert to the default.

## To set up reminder emails

To add an extra level of urgency to the notification emails sent to approvers, set up one or more customized reminder emails.

Anything you enter when setting up reminder emails as described below – for example, the body text or subject lines of reminder emails – overwrites what you might have configured on the **Document Capture Setup / Purchase Approval** page.

To set up reminder emails:

1. Search ({{search}}) for and select **Approval Reminder Email Setup**.
1. On the action bar, click **New** to create a reminder email entry.
1. In the **Level** column, specify the level of the reminder by entering an integer. As the **Level** column determines the order in which reminder emails are sent out, the first level is typically labeled **1**, and any subsequent levels are then labeled with consecutive numbers (**2**, **3**, etc.).
1. In the **Due Date Calculation** column, enter the amount of time that should pass before a reminder email is sent out at this level. This is calculated from the moment the approval request is sent to the approver.
   > [!NOTE]
   > Your entry must be an integer followed by **D** (days), **WD** (weekdays), **W** (weeks), **M** (months), **Q** (quarters), or **Y** (years) – for example, **2W** (two weeks). For more advanced formulas, use the operators + and -, or enter the letter **C** (current) as a prefix to any of the previously mentioned time units – for example, **CM+10D** (current month plus ten days).
1. **Optional**: In the **Send CC to** column, specify if you want to have reminder email copies sent to the manager of either the current approver or the original approver.
1. **Optional**: In the **Send CC to User ID** column, enter the ID of any other user that you want to receive copies of reminder emails.
1. In the **Email Subject** column, enter the text to be displayed in the subject line of all reminder emails sent at this level.
1. **Optional**: To customize the body text of any of the reminder emails, select the relevant reminder level, go to the action bar, click **Beginning Text** and/or **Ending Text**, and enter the text you want to have displayed in the body of all reminder emails sent at this level.

	>[!NOTE]
	>Reminder emails are sent per document, not as a list including all documents that need to be approved. Keep this in mind when setting up reminder emails.

## Related information

[Continia User Setup for approvals](@DC-23)