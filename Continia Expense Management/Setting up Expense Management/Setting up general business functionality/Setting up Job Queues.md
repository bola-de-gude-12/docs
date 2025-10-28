---
title: Setting up Job Queues in Expense Management 
date: 24-07-2025
description: Learn how to set up and manage job queues in Expense Management.  
id: EM-65
lang: en
---
# Setting up job queues

Set up and manage job queues in Expense Management so you can save time by automating tasks and processes such as synchronizations, approvals, and reminders, as well as running tasks automatically in the background, while still allowing for manual synchronization when needed. 

On the Job Queue Entry Card of the Job Queue Setup page you can create and manage entries, manage job queues, and adjust schedules. For general information on working with job queues in Business Central, refer to [Use job queues to schedule tasks](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks) (Microsoft's article).



## Use the job queue setup page

To simplify the process of setting up and managing recurring tasks, you can use Expense Management's **Job Queue Setup** page. This page gives administrators direct access to the default codeunits to quickly create and manage job entries, like synchronizations and approvals, without needing to manually find job codes for each task.

To use the job queue setup page to manage job queues:

1. Search for {{search}} **Expense Management Setup**.
2. On the action bar, click **Setup > Job Queue Setup**. 
3. If you want to reset all codeunits to the default settings, on the **Job Queue Setup** page navigate to the action bar, and click **Schedule all**.
4. The fields on the **Job Queue Setup** page give you access to the default codeunits and allows you to customize their schedule as needed. You can add a new job queue and modify the settings of running job queues such as the task’s start time, frequency, or recurrence. After making your adjustments, click **Restart** to apply the changes and activate the codeunit. The following fields are available:
   | Field              | Description                                                  |
   | ------------------ | ------------------------------------------------------------ |
   | Continia Online    | Select *Schedule now* or select the current value to get direct access to the Job Queue Entry card for codeunit 6086305 CEM Online Synch. Mgt. with which you can manage the synchronization with Continia Online. |
   | Field Dependencies | Select *Schedule now* or select the current value to get direct access to the Job Queue Entry card for codeunit 6086569 CEM Update Field Dependencies. |
   | Approval Email     | Select *Schedule now* or select the current value to get direct access to the Job Queue Entry card for codeunit 6086313 CEM Expense Approval Email. This codeunit lets you schedule the sending of approval email messages. |
   | Reminder Email     | Select *Schedule now* or select the current value to get direct access to the Job Queue Entry card for codeunit 6086314 CEM Reminder Email. This codeunit lets you schedule the sending of reminder email messages. |
   | Status Report      | Select *Schedule now* or select the current value to get direct access to the Job Queue Entry card for codeunit 6086353 CEM Send Status Report. This codeunit lets you schedule the sending of status reports. |



## Set up job queues

As indicated above, you can use job queues to schedule and run many different tasks and processes. The setup procedure is always the same – only the codeunits/reports are different.

To set up a job queue:

1. Search for {{search}} **Job Queue Entries**.
1. On the action bar, click **New** to open the **Job Queue Entry Card**. Alternatively, go to the **Expense Management Setup** page, click **Setup** > **Job Queue Setup**, then select a field to open the Job Queue Entry Card.  
1. On the **Job Queue Entry Card,** under **General**, go to **Object Type to Run** and select the relevant type, depending on whether you're running a codeunit or a report.
1. In **Object ID to Run**, enter the relevant codeunit/report.
1. In **Earliest Start Date/Time**, specify the earliest date and time to start running the job queue. When you've picked or entered a date, the **Earliest Start Date/Time** field is auto filled with the default time of day, but you can change this if necessary.
1. Under **Recurrence**, specify the recurrence rate of the job queue (if any) by enabling the recurrence toggle for each of the days you want it to run. Fill in the remaining relevant fields under **Recurrence**.
1. On the action bar, click **Set Status to Ready** to start the job queue.

> [!NOTE]
> Job queues sometimes fail, for example due to interrupted communication with an essential external resource that's become unresponsive, eventually resulting in an error status. To avoid this, we recommend you fill in the fields **Maximum No. of Attempts to Run** and **Rerun Delay (sec.)**, which are located under **General**. You may have to select **Show more** for these fields to become visible.



## Related information

 [The available job queues](@EM-278)