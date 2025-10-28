---
title: Setting up job queues in Document Capture
date: 26-08-2025
description: Information on job queues and the activities that can be automated via them.
id: DC-16
lang: en
---

# Setting up job queues

Continia Document Capture uses the standard Microsoft Dynamics 365 Business Central job queue functionality to optimize business processes and automate repetitive tasks. Through the task scheduler, you can view, create, and modify jobs that execute specific codeunits or reports in the background.

You can schedule these jobs to run either once or on a recurring basis, which provides flexibility in task management. For general information on how to work with job queues, see [Use job queues to schedule tasks](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks) (Microsoft article).

>[!IMPORTANT]
>To set job queues, users need a full permission set and can't have any security filter limitations.

In Document Capture, job queues can be set up for the following recurring activities:

<br>

| Activity | Description |
| --- | --- |
| **Importing documents** | You can have documents imported automatically on a regular basis. <br><br> To do this using a job queue, follow the [Microsoft guide](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks), using codeunit 6085669 **CDC Run Doc. Importer from JQ**. |
| **Batch-registering documents** | It's possible to register all documents in the document journal that are OK and for which there are no warnings or errors. <br><br> To batch-register documents using a job queue, follow the [Microsoft guide](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks), using report 6085580 **CDC Batch Register Documents**. |
| **Automatic document matching** | Documents can be matched automatically in bulk on a recurring basis. <br><br> To do this using a job queue, follow the [Microsoft guide](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks), using codeunit 6086022 **CDC Batch Match Documents** |
| **Sending status emails to approvers** | Document Capture can send reminder emails to users who need to approve one or more documents. <br><br> To send such emails to approvers using a job queue, follow the [Microsoft guide](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks), using codeunit 6085712 **CDC Purch. Approval E-Mail**. |
| **Batch-posting purchase invoices** | You can have all purchase invoices with the status **Released** posted in bulk. <br><br> To post purchase invoices using a job queue in Microsoft Dynamics NAV 2018 or later, follow the [Microsoft guide](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks), using report 497 **Batch Post Purchase Invoices**. For older versions, run report 6085585 **CDC Batch Post Purch. Invoices**. |
| **Batch-posting purchase credit memos** | Similarly to the above, Document Capture can automatically post all purchase credit memos with the status **Released** in bulk. <br><br> To post purchase invoices using a job queue in Microsoft Dynamics NAV 2018 or later, follow the [Microsoft guide](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks), using report 498 **Batch Post Purch. Credit Memos**. For older versions, run report 6085586 **CDC Batch Post Purch. CMs**. |
| **Sending status emails to document assignees** | Document Capture can send reminder emails to users who have been assigned any number of documents. <br><br> To send such emails using a job queue, follow the [Microsoft guide](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks), using codeunit 6086020 **CDC Send Delegation Email**. |
| **Batch-assigning documents** | Document Capture can be set up to assign documents to users in bulk. <br><br> To do this using a job queue, follow the [Microsoft guide](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks), using codeunit 6086021 **CDC Batch Delegate Documents**. |
| **Sending status emails to contract approvers** | You can set up Document Capture to send reminder emails to users who need to approve one or more purchase contracts. <br><br> To send such emails using a job queue, follow the [Microsoft guide](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks), using codeunit 6225182 **CDC Review E-mail**. |
| **Sending status emails to category managers** | You can set up Document Capture to send status emails to admins who need to register one or more open documents. <br><br> To send such emails using a job queue, follow the [Microsoft guide](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks), using report 6085589 **CDC Send Status Email to Category Managers**. |
| **Data maintenance** | You can set up Document Capture to perform data maintenance on a regular basis. <br/><br/>To do this using a job queue, follow the [Microsoft guide](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-job-queues-schedule-tasks), using codeunit 6086081 **CDC Data Maintenance Mgt**. |

> [!IMPORTANT]
> **Specifically for document import:** Note that you shouldn't run document import queues too often. The process is I/O- and CPU-intensive, and running it too often is likely to result in locking issues and a general decline in the NAV Service Tier performance, especially when many documents are imported at the same time. 
> 
> Conversely, running document import queues too rarely may result in the accumulation of very large numbers of documents that take a long time to import – clogging up the system and blocking it for other users and processes when the queue is finally run. If you receive large quantities of documents, you may want to schedule document import to take place outside of business hours.
> 
> The optimal interval between queue runs depends entirely on your specific business setup, not least in terms of incoming document volume. It's recommended that you fill out **No. of Minutes between Runs** on the **Recurrence** FastTab with a value that reflects your particular environment (e.g.: 60 minutes).

> [!NOTE]
> Job queues sometimes fail, for example due to interrupted communication with an essential external resource that's become unresponsive – eventually resulting in an error status. To avoid this, fill out the fields **Maximum No. of Attempts to Run** and **Rerun Delay (sec.)** on the **General** FastTab.
>
> For example, if you use Continia Cloud OCR for document import, network resources may be unavailable from time to time. To mitigate this, it's recommended that you set **Maximum No. of Attempts to Run** to 10 times.
