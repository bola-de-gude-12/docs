---
title: Job Queues available in Expense Management
date: 23-10-2024
description: The available job queues in Expense Management.  
id: EM-278
lang: en
---
# The Available Job Queues

In Expense Management, several recurring activities can be automated using job queues, such as synchronizing with Continia Online, sending approval and reminder emails, sending status reports, and updating field dependencies. The setup procedure for all these tasks is the same, differing only in the specific codeunit or report used.

For an overview of all the existing jobs, go the the **Expense Management Setup** page and select **Setup** > **Job Queue Setup**. Alternatively, select the search icon and search for Job Queue Entries. For more information about  job queues, refer to the [Setting up Job Queues](@EM-65) article. 

Expense Management comes with the following default codeunits:

| Codeunit | Name                          | Description                                                  |
| -------- | ----------------------------- | ------------------------------------------------------------ |
| 6086305  | CEM Online Synch. Mgt.        | Automates the synchronization with Continia Online to update the setup from Business Central and download documents submitted by expense users. |
| 6086313  | CEM Expense Approval Email    | Sends regular emails to approvers about pending documents for approval. This can be set to run daily, only if there are new documents to be approved. |
| 6086314  | CEM Reminder Email            | Sends reminder emails to expense users regarding pending documents. Reminders are configurable based on how many days should pass before sending an email. |
| 6086353  | CEM Send Status Report        | Sends a detailed status report of all documents claimed by a user, either posted or open. Customize the report details in the **Email** FastTab on the **Expense Management Setup** page. |
| 6086569  | CEM Update Field Dependencies | Validates field dependencies to prevent conflicts by running a consistency check. |
| 6225300  | CEM PCD Analyze Expenses      | Identifies recurring expenses and alerts the administrator when they're a good fit for automatic handling through a purchase contract. |

