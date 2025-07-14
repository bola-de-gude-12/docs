---
title: Managing Payment Notifications
description: Information on managing and sending payment notifications to your vendors from the payment journal.
date: 22-09-2021
id: PM-197
lang: en
---

# Managing Payment Notifications

After processing one or more payments, you can use payment notifications to inform your vendors about the payments. You can send these notifications through the bank or through both the bank and email, depending on your preference. For more information, see the [Defining Payment Notification Method](@PM-23) article. 

Notifications sent by the bank are sent when the payments have been processed in the bank. If you are notifying your vendors about payments via email, you must have defined the setup for email notifications and specified a recipient email. For more information, see the [Setting up Email Notifications](@PM-22) article.

You can see the payment notification details for a given payment line in the payment journal fact box **Payment Notification**.

## Sending email notifications

The bank will automatically send notifications to vendors, but if you've chosen to notify them via email as well, your payment notification setup will determine how the email is sent. There are three options for sending the emails, depending on your [payment notification setup](@PM-23):

- **On Post** - email notifications are sent when posting the payments in the payment journal.
- **Job Queue** - the job queue settings send email notifications. The payments must have been posted before a job queue can send them.  For information about job queue setup, see [Setting up Email Notifications](@PM-22#to-set-up-job-queue-for-sending-email-notifications).
- **Manually** - email notifications are sent from the payment journal by navigating to the action bar and selecting **Prepare** > **Send Email Notifications**. The payments must have been sent/exported before you can manually send the email notifications. 



## Managing unsent email notifications

You can access an overview of all unsent emails from the payment journal by selecting **Prepare** > **View Unsent Emails**. This will open the **Notification Email List** page with a filtered list of email notifications that have not been sent. If you wish to clear the filter and see all email notifications (both sent and unsent), you can select **Show All** in the action bar.

In some cases, email notifications aren't sent as expected. This can be the case if the job queue has not yet been processed or in case of errors in the job queue. To see the status of a given job queue, use the ![Search for page or report](/images/search_small.png) icon and search for **Job Queue Entries**, then select the related link. Another reason for unsent emails can be a missing or incorrect recipient email on the vendor card. Correct the recipient email on the vendor card; this will update the recipient email on the unsent email notifications. 

After having corrected any potential errors for unsent emails, you can manually execute the sending of the emails from the **Notification Email List** page by selecting **Send Mails**.



## To adjust a payment notification from the payment journal

To adjust a payment notification:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Journals**, then select the related link. 
1. Open the relevant journal and select a payment line for which the payment notification must be modified. 
1. On the action bar, select **Line** > **Notifications**. This will open the notification for the selected payment line.
1. Change the details for the payment notification as desired and close the page. You can see the updated information in the notification fact box.



## Restoring notifications

If you've changed the settings for email notifications, such as changing the language code or notification template, or if you have changed the notification on a payment line so that it no longer matches the default payment notifications settings, you can restore the payment notification so that it matches the current payment notification setup.

You can restore the payment notification in the payment journal by selecting a payment line, then navigating to the action bar and select **Line** > **Rebuild Payment Notification**. This will rebuild the payment notification for the selected line using the existing payment notification settings.

## Related information

[Defining Payment Notification Method](@PM-23)  
[Setting up Email Notifications](@PM-22)  

