---
title: Setting up Expense Reminder Codes
date: 21-03-2025
description:   
lang: en
---
# Setting up Expense Reminder Codes

You can easily configure Continia Expense Management to send out reminders to any expense user who needs to carry out a task for a document. This could, for example, be a credit card transaction that needs to be finalized or an expense that has been rejected by an approver and therefore must be dealt with by the expense user.

> [!NOTE]
> This functionality is only for expense users, *not* for approvers. It's very commonly – but not exclusively – used in connection with expenses that are created automatically from company credit card transactions and need to be completed by the relevant expense users.

The actual activity of sending reminder emails is executed by the codeunit **6086314 CEM Reminder Email**. For more information, see [Setting up Job Queues](@EM-65).

To set up expense reminder codes, follow these steps:

1. Choose the {{search}} icon, enter **Continia User Setup**, and then choose the related link.
1. In the list of users, in the **Continia User ID** column, select the user that you want to set up expense reminder codes for. The **Continia User Setup Card** opens.
1. On the **Expense Management** FastTab, go to **Expense Reminder Code** and select the three dots on the right side of the field to open the **Reminder Codes** page.
1. Do one of the following:
   * In the list of codes, select one of the existing ones (select the line of the code, not the code itself).
   * Create a new code: In the action bar, select **New**, enter a name for the new code, and then select **Enter** or exit the field. In the **Max No. of Reminders** column, specify the maximum number of reminders you want to be sent out for this code.
1. In the action bar, select the tree dots, and then select **Levels** to open the **Reminder Levels** page.
1. In the **No.** column, specify the level of the reminder by entering an integer. As the **No.** column determines the order in which reminder emails are sent out, the first level is typically labeled **1**, and any subsequent levels are then labeled with consecutive numbers (**2**, **3**, etc.).
1. In the **Grace Period** column, enter the amount of time that should pass before a reminder email is sent out at this level.
   > [!TIP]
   > Your entry must be a [date formula](https://learn.microsoft.com/en-us/dynamics365/business-central/ui-enter-date-ranges#use-date-formulas). As regards the start date of each grace period, see [Grace period start dates](#grace-period-start-dates) below.
1. In the **Reminder Text** column, enter a text that can be used internally to identify the level.
1. Repeat steps 6-8 for any additional reminder levels you want to add, and then close the page to return to the **Reminder Codes** page.
1. Make sure that the code you've created or customized is selected in the list, and then select **OK** to close the page.

The selected reminder code is now added to the **Expense Reminder Code** field on the **Continia User Setup Card**, and the user you selected in step 2 of the guide will receive reminder emails according to your setup.

## Grace period start dates

In the table on the **Reminder Levels** page, the date formula you enter in the **Grace Period** column for a certain level specifies the amount of time that should pass before a reminder email is sent out at this level. For the first level, this is calculated from a start date that's derived from one of the following fields:

* **Date Created**
* **Document Date**/**Registration Date**/**Departure Date** (for expenses, per diems, and mileages)

If one of these fields is empty, the other one is used. If both fields have a date value, the earlier date is used. And if both fields are empty, **TODAY** (the current date) is used.

The above applies only to the first level in the table. For subsequent levels, the amount of time that should pass before a reminder email is sent out is calculated from the time when the previous reminder was sent.