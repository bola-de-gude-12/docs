---
title: Document Output Setting up Job Queues
date: 17-05-2024
description:  
id: DO-44
lang: en
---
# Setting up Job Queues

Running tasks manually can be a time-consuming process. Job queues enable you to automate this process, as they can run automatically in the background. When you set up job queues, you can still run your tasks manually, if necessary.

It's important to note that job queues, which are standard Business Central functionality, and email jobs, which are Document Output functionality, are two different things. Job queue entries are used to schedule tasks, such as running a report or a codeunit. An email job on the other hand defines filters on email templates and records as well as timeframes for the execution of the email job. However, without a job queue entry an email job doesn't do anything. A particular Document Output job queue will run the Document Output codeunit that runs each of the email jobs and executes them, see below table.

In Document Output, the following recurring activities can be set up for any given job queue:

<br>

| Activity | Description |
| --- | --- |
| **Running email jobs automatically** | This job queue will run all enabled email jobs. <br><br>To run email jobs using a job queue, follow the [guide below](/continia-document-output/setting-up-document-output/setting-up-general-business-functionality/setting-up-job-queues#to-set-up-job-queues), using codeunit 6175283 **CDO NAV App.ServerE-MailJobMgt.** |
| **Sending statements automatically** | Document Output can send statements in fixed intervals using a job queue. <br><br> To send statements using a job queue, follow the [guide below](/continia-document-output/setting-up-document-output/setting-up-general-business-functionality/setting-up-job-queues#to-set-up-job-queues), using codeunit 6175297 **CDO Send Cust. Statement Mgt.** |

## To set up job queues

As indicated above, you can use job queues to schedule and run many different tasks and processes. The setup procedure is always the same – only the codeunits/reports are different.

To set up a job queue, follow these steps:

1. Choose the {{search}} icon, enter **Job Queue Entries**, and then choose the related link.
1. In the action bar, select **New** to open the **Job Queue Entry Card**.
1. On the **General** FastTab, go to **Object Type to Run** and select the relevant type, depending on whether you're running a codeunit or a report.
1. In the field **Object ID to Run**, enter the relevant codeunit/report (see the table above).
1. In **Earliest Start Date/Time**, specify the earliest date and time to start running the job queue.
1. When you've picked or entered a date, the **Earliest Start Date/Time** field is autofilled with the default time of day, but you can change this if necessary.
1. On the **Recurrence** FastTab, specify the recurrence rate of the job queue (if any) by enabling the recurrence toggle for each of the days you want it to run.
1. Fill out the remaining fields on the **Recurrence** FastTab as needed.
1. In the action bar, select **Set Status to Ready** to start the job queue.

> [!NOTE]
> Job queues sometimes fail, for example due to interrupted communication with an essential external resource that's become unresponsive, eventually resulting in an error status. To avoid this, we recommend that you fill in the fields **Maximum No. of Attempts to Run** and **Rerun Delay (sec.)**, which are located on the **General** FastTab. Note that you may have to select **Show more** for these fields to become visible.

## See also
[Microsoft's article on job queues](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks)  