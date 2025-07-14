---
title: Defining Payment Notification Method
description: Information on how to define the payment notification method for notifying vendors about payments.
date: 24-02-2021
id: PM-23
lang: en
---

# Defining Payment Notification Methods

When sending vendor payments to the bank, you can notify your vendors that the payments have been completed. This can be done via the bank and by email. In the payment notification, you can add information about which invoices are included in a summarized payment.

When you complete the assisted [Payment Management General](@PM-2) setup guide, you can define how to notify your vendors. 

You can set up the parameters for notifying vendors at several places in Microsoft Dynamics 365 Business Central. Payment Management uses a hierarchy to determine which notification settings to apply to the payment. You can see the hierarchy for using the notification method in the following table.

| Level in hierarchy | Notification settings defined on... |
| --- | --- |
| 1 | Purchase Document |
| 2 | Vendor Card |
| 3 | Payment method |
| 4 | Vendor's preferred bank account |
| 5 | Payment Notification Setup |

For information on how to send and manage payment notifications from the payment journal, see [Managing Payment Notifications](@PM-197).



## To set up default payment notifications

1. Select the icon ![Search for page or report](/images/search_small.png), enter **Payment Notification Setup**, and then select the related link. This will open the page with default settings for payment notifications. 

1. To edit the settings, navigate to the page header and select the pencil. The following table lists the fields you can edit:

   | Field                               | Description                                                  |
   | ----------------------------------- | ------------------------------------------------------------ |
   | Default Notification Template       | Select the default notification template that should be used for payments that do not have a payment notification template defined. The template includes information about **Recipient Reference Template**, which information to include in the **Payment Notification Template**, and if the notification should be compressed.<br/>You can see all the available payment notification templates in the table at the bottom of the page with an example of how the notification will look. |
   | Default Notification Method         | Select whether notifications should be sent to your vendor only by the bank, or if you want to send the notification using both bank and email. If you choose **Bank & Email**, please refer to the article [Set Up Email Notifications](@PM-22). |
   | Limit Notification Size             | Enable **Limit Notification Size** to split summarized payments that exceed the notification limit. If this setting is not enabled, it is required that the notification method must be **Bank & Email**, as the full notification, for notifications that exceed the limit, can only be sent by email. |
   | Bcc Email for Payment Notifications | Enter your own company email if you want to receive all payment notification emails that are sent to your vendors. This will give you an overview of all sent notifications. |
   | Email Sending Method                | define when the notification should be sent by email. I you chose to send email notifications using the job queue, you can go to the job queue settings to specify the recurrence of the job queue. |
   | Send Email on Posting Date          | Enable to send email notifications about when a payment is due based on the posting date if a job queue is set up. |
   | Default Email Notification          | Enter a language code that will control which language layer to use when creating notifications. If the field is left empty, the language layer for notifications will be English, unless otherwise stated directly on the vendor |

   

## To set up a notification on vendor cards

To define payment notification settings for a vendor:

1. Use the {{search}} icon and search for **Vendors**, then select the related link. This opens the list of vendors. 
1. In the vendor list, select the vendor.
1. On the **Payments** FastTab, in the **Notification** section, enter the relevant information for payment notifications.
   > [!NOTE]
   > 
   > **Recipient Email** is required in order to notify the vendor by email.



## To set up a notification on payment methods

To define payment method notifications:

1. Use the {{search}} icon and search for **Payment Methods**, then select the related link. This opens the list of payment methods.
1. In the payment method list, select the payment method.
1. Fill in the **Default Notification Template** and **Notification Method**.



## To set up a notification on vendor bank accounts

1. Use the {{search}} icon and search for **Vendors**, then select the related link. This opens the list of vendors.
1. In the vendor list, choose the vendor, for whom you want to define payment notification settings.
1. In the action bar choose **Related** > **Vendor** > **Bank Accounts** and select the bank account.
1. On the **Payment Management** FastTab, fill in the **Notification Template** and the **Notification Method**.



## Related information

[Set up Email Notifications](@PM-22)  
[Managing Payment Notifications](@PM-197).

