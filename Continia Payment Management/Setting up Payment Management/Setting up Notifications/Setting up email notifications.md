---
title: Setting up Email Notifications
description: How to set up email templates for sending payment notifications
date: 22-11-2021
id: PM-22
lang: en
---

# Setting up Email Notifications

When notifying your vendors about payments and being notified by the bank, your vendors can also be notified by email. Payment Management comes with a default email template. If needed, you can modify the template and define the information to include in the email.

> [!IMPORTANT]
> 
> Email setup must be completed before you can send emails from Business Central to your vendors. Setting up SMTP email is part of standard Microsoft Dynamics 365 Business Central. Read more information about how to set up SMTP email on Microsoft Docs [Set up Email](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-how-setup-email). 

For information on how to send and manage payment notifications from the payment journal, see [Managing Payment Notifications](@PM-197).



## To edit email templates

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Notification Setup**.
1. On the payment notification setup page, on the action bar, select **Email Template** > **Email Template Setup**.
   This opens the **Email Template Mapping** page with the current email template setup. 
1. On the action bar, select **Edit list** to edit the list of information used in the email template.
1. The table with email information consists of two columns: In the left column, select the table name from which you want to map information to the email template. In the right column, select a value that should be part of the email template.
1. Use the [Additional functionality](#additional-functionality) to manage the template setup.
1. When you have finished the setup, close the setup page.
> [!TIP]
>
> Use the email example to the right of the screen to get a preview of the email notification using the given email template setup.



## Additional functionality

| Field | Description |
| --- | --- |
| Insert Company Logo | Enable the **Show company logo** setting to on if you want the company logo to be included in the email notification. |
| Attach Report ID | From the drop-down box, select the report you wish to attach as a pdf file to the email notification. |
| Standard Remittance Report Selection | Switch to on if you want to attach the standard report for remittance to the email notification. |
| Insert Email Closing | Switch to if you want to add "Best regards" to the email notification automatically. |
| Email Closing Name | Enter the name that you want to display after "Best regards" in the email notification. If the **Insert Email Closing** setting is enabled and the **Email Closing Name** field is left empty, the name of the logged-in user will display. |
| Send a Test Mail | To receive a test email to validate the outcome of the email template setup, on the action bar, select **Send Test Mail**. |
| Update Email Template | To import potential updates to the template, on the action bar, select **Update Template**. |
| Load Default Settings | To restore the default settings for the e-mail template, on the action bar, select **Load default settings**. |



## To define the language for the email template

The Payment Management supported languages for email templates include **ENU** (US English), **DAN** (Danish), **NLD** (Dutch), and **NOR** (Norwegian).

The language used for email notifications will be determined by the language code defined on the vendor card. If no language code is specified on the vendor card, the language code on the payment notification setup will be used. Finally, if no language code has been defined on the vendor card or on the payment notification setup, the default language code will be **ENU**.

To set up a vendor-specific or default language code for email templates, see the following description:

- **Vendor-specific language code**: To define a vendor-specific language code for email notifications, use the ![Search for page or report](/images/search_small.png) icon and search for **Vendors**. On the vendor card, on the **Address & Contact** FastTab, in the **Language Code** field, choose the language code to use for email notifications for the given vendor. 
- **Default language code**: To define a default language code for email notifications, use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Notification Setup**. On the **Payment Notification Setup** page, in the **Default Email Notification Language Code** field, choose the default language code to use for email notifications. 



## To set up a job queue for sending email notifications

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Notification Setup**.
1. On the **Payment Notification Setup** page, on the **Payment Notification** FastTab, in the **Default Notification Method** field, select **Bank & Email** to send payment notifications by email.
1. In the **Email Sending method** field, select **Job Queue**.
1. Choose the **Job Queue Settings** to access the Payment Management default job queue for sending email notifications. This opens the list of job queues.

   > [!WARNING] 
   >
   > Avoid manually configuring job queues as it could lead to improper functionality. Instead, always use corresponding actions.
1. In the object ID **6216231**, with the **CPM Send Notice Email Job** object, verify that the status is set to **Ready**. If the status is not set to **Ready**, you can change the status by selecting the **Set Status to Ready** action in the action bar.
   > [!NOTE]
   >
   > To view or edit the job queue setup navigate to the action bar and select **Edit**. To edit the job queue setup, the status of the job queue must be set to **On Hold**. This is done from the action bar. For information on setting up task queue entries, see Microsoft Docs [You can use task queues to schedule tasks](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks).

You can see the completed job queues in **Log Entries** located on the action bar.

In case of issues running the job queue, or if the job has stopped unexpectedly, you can access the potential error messages from the **Show Error** action located on the action bar. 



## Related information

[Set up Email](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-how-setup-email) (Microsoft article)  
[Managing Payment Notifications](@PM-197)  
[Supported Countries and Languages](@PM-54)  
[You can use task queues to schedule tasks](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks) (Microsoft article) 



