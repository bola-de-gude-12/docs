---
title: Setting up reminder codes for email reminders
date: 08-07-2025
description: How to set up reminder codes for Expense Management email reminders
id: EM-329
lang: en
---

# Setting up reminder codes for email reminders
You can use reminder codes to create different levels of reminder emails that will be sent to expense users. Each level outlines the frequency of notifications sent and how many times they are sent. For example, you can set a maximum number of reminder emails to be sent to a user.

## Set up email reminders

It's important define your reminder codes.

To locate and set up reminder codes in Business Central:

1. Search for {{search}} **Reminder Codes**.
    > [!NOTE]
    > For older versions of NAV, go to: **Departments** > **Administration** > **Application Setup** > **Expense Management** > **Users & Approvals** > **Reminder Codes**. 
2. On the Reminder Codes action bar, click **Levels**.
3. Click **Edit List**.
4. For each entry add the relevant information from the following Reminder codes definitions table.

## Reminder codes definitions

Refer to the following table to better understand the information you need to set up reminder codes.

| **Field** | **Definition** |
| --- | --- |
| Expense Reminder Code | Identifies the reminder, for example, an *Employee* or *Manager*. You will see this code used on the **Continia User Setup Card** under **Expense Management** > **Expense Reminder Code**.<br>Fill in this field - if the field is left blank it will keep sending out reminders indefinitely. You must also assign the code to the user for the reminder to activate for the user (otherwise only a general reminder will be sent). |
| Max No. of Reminders | Specifies the maximum number of reminders to be sent. If you are using multiple levels, you must set the maximum for each level. <br>In a scenario where you combine multiple levels, reminders are sent at the frequency set for the level. After the maximum number of reminders is reached for a level, the functionality will continue by sending out reminders that obey the frequency and limit stated for the next level given. When it reaches the end of the levels specified, no further reminders are sent. |
| No.                  | This represents the reminder level. You can use multiple reminder levels to specify how often you want notifications sent. The following example uses five levels and has set different grace periods for each to ensure every possible scenario is covered: <ul><li>Reminder Level No. 1 - Has a grace period set to three days, so the first notification email is sent out after three days.</li><li>Reminder Level No. 2 - Has a grace period set to one day, so a reminder is sent daily.</li><li>Reminder Level No. 3 - Has a grace period set to every fourteen days, so a reminder is sent out every two weeks.</li><li>Reminder Level No. 4 - Has a grace period set to every twelve weeks, so a reminder is sent out quarterly.</li><li>Reminder Level No. 5 - Has a grace period set to 52 weeks, so a reminder is sent out annually.</li></ul>Based on the above example, you could set up a scenario that uses multiple levels (levels 1 and 2 for example). So the first notification is sent out after three days (Level 1), then is followed up with a daily reminder (Level 2) thereafter until the notifications sent reach the set maximum number of reminders limit. |
| Grace Period         | The period after which a reminder notification is sent/the next reminder level is calculated. It is good practice to specify a grace period for each level so the user is not spammed by emails. |
| Reminder Text        | The description appropriate for the reminder level. For example, it could describe the action you want the user to take for that reminder level, such as, "*Please complete your expenses as soon as possible*". |
| Reminder Level | Shows which reminder level is currently in use. |
| Dates | The system chooses a start date that is before the grace period begins. The start date is derived from the following fields: **Date Created** and **Document Date**/**Registration Date**/or (in the case of expenses, mileages, and per diems) **Departure Date**.<br>If one of the fields is empty, the date is taken from one of the other fields, and if no date is available then today's date is used. |

## Monitoring reminders
For a better overview, you can follow the progress of all the reminders that are being sent out by adding specific columns to the documents page of **Expenses**, **Mileages**, or **Per Diems**.

To add reminder overview columns:

1. Search for {{search}} **Settings**.
2. Click **Personalize**.
3. On the action bar, click **+Field**.
4. Under **Add Field to Page**, select the **Current Reminder Level** field and drag it to where you want it in the table. 
5. Select the **Next Reminder** field and drag it to where you want it in the table.
6. Click **Done**.


## Related information

For more information about reminder codes in Expense Management, see:

[Expense user setup for Expense Management](@EM-36)
