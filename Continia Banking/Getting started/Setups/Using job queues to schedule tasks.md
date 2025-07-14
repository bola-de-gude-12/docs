---
title: Using job queues to schedule tasks
description: Overview of the Continia Banking job queues
date: 26-05-2025
id: CB-119
lang: en
---

# Using job queues to schedule tasks

Continia Banking uses the Business Central Job queue functionality to optimize business processes and automate repetitive tasks. Through the task scheduler, you can view, create, and modify jobs that execute specific codeunits or reports in the background. You can schedule these jobs to run either once or on a recurring basis, which provides flexibility in task management. For general information on how to work with job queues, refer to the [Microsoft documentation](https://learn.microsoft.com/en-gb/dynamics365/business-central/admin-job-queues-schedule-tasks).

## Key considerations before working with job queues

Before you start working with job queues, the following must be taken into account:

* Delegated users lack the necessary permissions to start job queues. Please ensure the task is performed by a user with the proper permission assigned.
* Only adjust the recurrence interval as needed, and avoid making other manual configurations to job queues. Changes beyond the recurrence interval can affect the functionality of the jobs or tasks triggered by the job queue.

## Working with the Continia Banking job queues

There are several places in the system in which you can create job queues.

To see an overview of all existing jobs:

* Search ({{search}}) for and select **Job Queue Entries**.

If you accidentally delete a job queue or want to reset the configuration, you can easily re-enable the job queues by following these steps:

1. Search ({{search}}) for and select **Continia Banking Setup**.
2. On the action bar, select **Actions** > **Troubleshooting**
3. On the **Troubleshooting** page, select **Actions** > **Re-enable Job Queues**.

> [!IMPORTANT]
>
> Delegated users lack the necessary permissions to start job queues. Please ensure the task is performed by a user with full administrative rights.
>

## The default codeunits

Continia Banking includes the following default codeunits:

| Codeunit | <div style="width:250px"></div>Name | Description                                                  |
| -------- | ----------------------------------- | ------------------------------------------------------------ |
| 71553647 | CTS-CB Update Setup                 | On the Continia Banking Setup page, the **Update Method** field determines whether bank and bank system updates occur automatically. If set to **Automatic**, the job queue entry CTS-CB Update Setup is created to handle updates. When new setup files are available, this job queue generates additional entries to ensure the setups are updated automatically.<br/><br/>The following job queue entries can be generated:<ul><li>CTS-CB Upgrade BankSystem</li><li>CTS-CB Upgrade Bank</li><li>CTS-PI Import Setup</li><li>CTS-PE Import Setup</li></ul><br />These job queue entries will run according to the time specified in the **Update Time** field. |
| 71553708 | CTS-CB Upgrade Bank                 | Updates the bank system automatically.                       |
| 71553646 | CTS-CB Upgrade BankSystem           | Downloads a bank system setup file to keep banks systems up to date. This job queue only displays when a new setup file is available. |
| 71554210 | CTS-PI Import Setup                 | Downloads an import setup file to keep the banking import setup up to date. |
| 71553905 | CTS-PE Import Setup                 | Downloads an import setup file to keep the banking export setup up to date. |
| 71553881 | CTS-PE Create Pmt. Sugg.            | Automatically suggests payments for the specific journal.<br />Job queues with the Object ID 71553881 (CTS-PE Create Pmt. Sugg. JQ) are designed to automate the creation of payment suggestions. Specifically, this job queue will process all Payment Suggestion Templates that meet the following criteria:<ul><li>The value in the **Job Queue ID** field matches the ID of the job queue.</li><li>The **Use For Job Queue** setting is enabled (set to True).</li></ul><br/>Templates meeting these criteria will be used to generate Payment Suggestions automatically. See the [Setting up Payment Suggestion Templates](@CB-89) article for more information. |
| 71553912 | CTS-PE Send Advice Email Job        | On the **Banking Export Setup** page, on the **Remittance** FastTab, the field **Email Sending Method** can be set to *Job Queue*. If this is set to *Job Queue*, the job queue CTS-PE Send Advice Email Job is created and remittance advice emails are sent automatically. See the [Configuring Export Settings](@CB-23) article for more information. |
| 71554352 | CTS-PI Bank Recon Imp JobQueue      | Creates and runs a job queue entry to import bank statements in the background when the **Import with Job Queue** option is selected on the **Import Reconciliation Setup** page. See the [Importing multiple bank statements](@CB-245) article for more information. |

