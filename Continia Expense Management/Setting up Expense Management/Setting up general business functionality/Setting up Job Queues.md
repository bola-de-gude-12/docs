---
title: Setting up Job Queues in Expense Management 
date: 13-11-2024
description: Learn how to set up and manage job queues in Expense Management.  
id: EM-65
lang: en
---
# Setting up Job Queues

Automating regular tasks like synchronization can save significant time. Job queues enable you to automate these processes, running tasks automatically in the background, while still allowing for manual synchronization when needed. This article explains how to set up and manage job queues in Expense Management to automate tasks like synchronizations, approvals, and reminders. It covers a list of [the available job queues](@EM-278), using the [**Job Queue Setup** page to create and manage entries](#to-use-the-job-queue-setup-page) to manage job queues, adjust schedules, and provides step-by-step instructions for [configuring job queues and managing their schedules on the **Job Queue Entry Card**](#to-set-up-job-queues). For general information on working with job queues in Business Central, refer to [Microsoft's article on job queues](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks).

## To use the job queue setup page

To simplify the process of setting up and managing recurring tasks, you can use Expense Management's **Job Queue Setup** page. This page gives administrators direct access to the default codeunits to quickly create and manage job entries, like synchronizations and approvals, without needing to manually find job codes for each task.

To use the job queue setup page to manage job queues:

1. Use the {{search}} icon, search for **Expense Management Setup** and select the related link.
2. On the action bar, select **Setup > Job Queue Setup**. 
3. On the **Job Queue Setup** page, select **Schedule al**l on the action bar if you want to reset all codeunits to the default settings.
4. The fields on the **Job Queue Setup** page give you access to the default codeunits and allows you to customize their schedule as needed. You can add a new job queue and modify the settings of running job queues such as the task’s start time, frequency, or recurrence. After making your adjustments, select **Restart** to apply the changes and activate the codeunit. The following fields are available:
   | Field              | Description                                                  |
   | ------------------ | ------------------------------------------------------------ |
   | Continia Online    | Select *Schedule now* or select the current value to get direct access to the Job Queue Entry card for codeunit 6086305 CEM Online Synch. Mgt. with which you can manage the synchronization with Continia Online. |
   | Field Dependencies | Select *Schedule now* or select the current value to get direct access to the Job Queue Entry card for codeunit 6086569 CEM Update Field Dependencies. |
   | Approval Email     | Select *Schedule now* or select the current value to get direct access to the Job Queue Entry card for codeunit 6086313 CEM Expense Approval Email. This codeunit lets you schedule the sending of approval email messages. |
   | Reminder Email     | Select *Schedule now* or select the current value to get direct access to the Job Queue Entry card for codeunit 6086314 CEM Reminder Email. This codeunit lets you schedule the sending of reminder email messages. |
   | Status Report      | Select *Schedule now* or select the current value to get direct access to the Job Queue Entry card for codeunit 6086353 CEM Send Status Report. This codeunit lets you schedule the sending of status reports. |



## To set up job queues

As indicated above, you can use job queues to schedule and run many different tasks and processes. The setup procedure is always the same – only the codeunits/reports are different.

To set up a job queue, follow these steps:

1. Choose the {{search}} icon, enter **Job Queue Entries**, and then choose the related link.
1. In the action bar, select **New** to open the **Job Queue Entry Card**. Alternatively, go the the **Expense Management Setup** page and select **Setup** > **Job Queue Setup** and select a field to open the Job Queue Entry Card.  
1. On the **Job Queue Entry Card,** on the **General** FastTab, go to **Object Type to Run** and select the relevant type, depending on whether you're running a codeunit or a report.
1. In the field **Object ID to Run**, enter the relevant codeunit/report.
1. In **Earliest Start Date/Time**, specify the earliest date and time to start running the job queue. When you've picked or entered a date, the **Earliest Start Date/Time** field is autofilled with the default time of day, but you can change this if necessary.
1. On the **Recurrence** FastTab, specify the recurrence rate of the job queue (if any) by enabling the recurrence toggle for each of the days you want it to run. Fill out the remaining fields on the **Recurrence** FastTab as needed.
1. In the action bar, select **Set Status to Ready** to start the job queue.

> [!NOTE]
> Job queues sometimes fail, for example due to interrupted communication with an essential external resource that's become unresponsive, eventually resulting in an error status. To avoid this, we recommend that you fill in the fields **Maximum No. of Attempts to Run** and **Rerun Delay (sec.)**, which are located on the **General** FastTab. Note that you may have to select **Show more** for these fields to become visible.

