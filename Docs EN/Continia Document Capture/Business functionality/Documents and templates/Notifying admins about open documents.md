---
title: Notifying admins about open documents in Document Capture
date: 15-10-2025
description: How to configure email notifications for admins in Document Capture.
id: DC-158
lang: en
---

# Notifying admins about open documents

You can send emails to designated admins (such as accounts payable managers) to notify them that there are documents that need to be registered in Continia Document Capture. To send these notification emails – also known as status emails –, you must first [set up an admin as a category manager](#to-assign-category-managers) (one per document category) and then make sure that [the emails are sent either manually automatically](#to-send-status-emails).

You can also [set up a number of customized reminder emails](#to-set-up-reminder-emails) at different levels of urgency, based on how long the individual documents have been in the document journal. For each level, you can enter a specific text that emphasizes the increasing importance of registering the documents. Reminder emails with your entered texts are then sent to the assigned admin at specified intervals until the documents have been registered.

> [!NOTE]
> Note that, although both the setup and the functionality of this type of notification are very similar to those of [approval notifications](@DC-26), these are two different types of notification emails that are sent at different stages in the overall document process.

## To assign category managers

To set up an admin as a category manager, who will receive notification emails about unregistered documents, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the category that you want to set up a category manager for. For example, the **PURCHASE** category (the category line, not the code).
1. On the action bar, click **Edit** to open the **Document Category** page.
1. On the **General** FastTab, go to **Category Manager**.
1. In the dropdown menu, select the user who is to be notified about open documents.
1. Close the **Document Category** page, and repeat steps 2-5 for any additional categories you want to set up category managers for.

The selected user(s) will now be notified of documents that are pending registration in the document journal, provided that you [make sure that status emails are sent](#to-send-status-emails) either manually or automatically.

## To set up reminder emails

Once you've assigned one or more category managers, you can set up one or more customized reminder emails for the recipients to take action. To set up reminder emails:

1. Search ({{search}}) for and select **Open Document Reminder Email Setup**.
1. On the action bar, click **New** to create a new reminder email entry.
1. In the **Level** column, specify the level of the reminder by entering a whole number. As the **Level** column determines the order in which reminder emails are sent out, the first level is typically labeled **1**, and any subsequent levels are then labeled with consecutive numbers (**2**, **3**, etc.).
1. In the **Due Date Calculation** column, enter the amount of time that should pass before a reminder email is sent out at this level. This is calculated from the moment the document is imported.
   > [!NOTE]
   > Your entry must be a whole number followed by **D** (days), **WD** (weekdays), **W** (weeks), **M** (months), **Q** (quarters), or **Y** (years) – for example, **2W** (two weeks). For more advanced formulas, you can also use the mathematical symbols + and –, or you can enter the letter **C** (current) as a prefix to any of the previously mentioned time units. For example, **CM+10D** (current month plus ten days).
1. **Optional**: To send copies of reminder emails to other users, either enter or select the ID of that user in the **Send CC to User ID** column.
1. In the **Email Subject** column, enter the text to be displayed in the subject line of all reminder emails sent at this level.
1. **Optional**: To customize the body text of any of the reminder emails, select the relevant reminder level, go to the action bar, select **Beginning Text** and/or **Ending Text**, and enter the text you want to have displayed in the body of all reminder emails sent at this level.
   
   > [!TIP]
   > Any text entered under **Beginning Text** is displayed at the top of the email, above the table of documents pending registration. Any text entered under **Ending Text** is displayed at the bottom of the email, below the table of documents.

## To send status emails

Status emails can be sent either manually by you or automatically using job queues. Both methods are described below:

**To send status emails manually**:

1. Search ({{search}}) for and select **Send Status Email to Category Managers**.
1. Click **OK**.

Status emails will now be sent to the category managers you've assigned.

**To send status emails automatically using job queues**, follow these steps:

1. Search ({{search}}) for and select **Send Status Email to Category Managers**.
1. Click **Schedule**.
1. Fill out the fields as needed. For more information, see [Scheduling a report to run later or periodically](https://learn.microsoft.com/en-us/dynamics365/business-central/ui-work-report#ScheduleReport) (Microsoft article).

Status emails will now be sent to the category managers you've assigned, in accordance with your specified settings.

> [!NOTE]
> You can also set up the job queue from the **Job Queue Entries** page. For more information on how to do this, see [Setting up job queues](@DC-16).

## Related information

[Email notifications](@DC-26)  