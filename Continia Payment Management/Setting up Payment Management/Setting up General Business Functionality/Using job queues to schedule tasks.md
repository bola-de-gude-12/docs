---
title: Using job queues to schedule tasks in Payment Management
description: Overview of the Payment Management job queues
date: 03-10-2024
id: PM-324
lang: en
---

# Using Job Queues to Schedule Tasks

Payment Management uses the Business Central Job queue functionality to streamline business processes and process repetitive tasks automatically. A job queue uses the task scheduler to let you view, create, or modify jobs that are set to run specific codeunits in the background. You can set jobs to run one time or regularly. 

## Key considerations before working with job queues

Before you start working with job queues, the following must be taken into account:

* Delegated users lack the necessary permissions to start job queues. Please ensure the task is performed by a user with the proper permission assigned.
* Before activating job queues related to importing and reconciling bank statements, customers with Dutch and UK banks must import and reconcile the first bank account to enable the job queues.
* Only adjust the recurrence interval as needed, and avoid making other manual configurations to job queues. Changes beyond the recurrence interval can affect the functionality of the jobs or tasks triggered by the job queue.

## Available job queues

For an overview of all the existing jobs, select the search icon and search for Job Queue Entries.

Payment Management comes with the following default codeunits:

| Codeunit | <div style="width:250px"></div>Name | Description                                                  |
| -------- | ----------------------------------- | ------------------------------------------------------------ |
| 6216327  | CPM Update Pmt.Jnl.Line Status      | Updates the status line in the payment journal. By default, set to the recurring time interval of 60 minutes. <br />If, on the bank card, you select to update the payment journal line status automatically, it will run this Job queue on the selected time interval and update the status accordingly. See the [Managing Journal Lines](@PM-36) article for more information.<br />Bank card > **Advanced** > **Update Payment Journal Lines Status** field, and from the drop-down box, select *Automatic* |
| 6216279  | CPM Update Setup File               | Checks if there are any new setup files.                     |
| 6216305  | CPM Upgrade BankSystem/Bank         | Updates the bank system automatically.                       |
| 6216231  | CPM Send Notice Email Job           | Sends email notifications about payments. The payments must have been posted before a job queue can send them. Dependent on notification setup. See the [Setting up Email Notifications](@PM-22) article for more information. |
| 6216335  | CPM Import Payment Receipt JQ       | Automatic import of payment receipts (camt.053) to the cash receipt journal. See the [Importing Customer Payments](@PM-96#to-import-payments-automatically) article for more information. |
| 6216245  | CPM Curr. Exchange Rate Import      | Automatically imports the exchange rate. See the [Setting up Currency Exchange Rates](@PM-41#to-set-up-automatic-currency-exchange-rate-import) article for more details. |
| 6216310  | CPM Acc. Stmnt. Job Queue           | Automatically imports statement data to the bank export data. See the [Importing and Reconciling Bank Statements](@PM-48#to-import-bank-statements-automatically) article for more details. |
| 6216550  | CPM Aut. Import to Reconc           | Automatically imports data to the bank reconciliation journal. Dependent on the setup of bank account data. See the [Importing and Reconciling Bank Statements](@PM-48#to-import-bank-statements-automatically) article for more details.<br />To learn more about how bank statements are imported and handled in the job queue, see [Manage the import of bank statements](@PM-31#to-manage-the-bank-statement-import-method) |
| 6216318  | CPM Suggest Vendor Payment          | Automatically suggests vendor payments for the specific journal. See the [Suggesting and processing payments](@PM-90#to-suggest-vendor-payments-automatically) article for more information. |
| 6216364  | CPM Post Payment Journal JQ         | Automatically posts journals based on the status of the payment lines. See the [Suggesting and processing payments](@PM-90#to-post-payments-automatically) article for more information. |

