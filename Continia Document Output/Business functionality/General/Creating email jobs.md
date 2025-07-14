---
title: Creating Email Jobs
date: 05-12-2024
description:  
id: DO-48
lang: en
---

# Creating Email Jobs

In Document Output, email jobs are used to substitute manual execution of routine tasks with automation. The tasks associated with an email job will be sent to the **Document Queue** when the email job is run.

To create a new email job, follow these steps:

1. Choose the {{search}} icon, enter **Email Jobs**, and then choose the related link.	
1. In the action bar, select **New**.
1. In the new line, in the **Job No.** column, enter a descriptive name for the email job.
1. In the **Type** column, select **Email Template**.
1. In the **Email Template Code** column, select a template code.
1. Optional: In the **Table Filter** field, add filters to specify in detail which document to process.
   > [!WARNING]
   > Selecting **Disable Check for sent earlier** will resend the same emails continuously if no additional filters are applied.
1. Optional: In **Starting Time** and **Ending Time**, set an interval to limit a job to only run within a set timeframe regardless of how often the job queue entry is running. Individual days can be selected in which the job should be allowed to run. If none are selected, the job will run every day.
1. In the **Enabled** column, select the checkbox to enable the job.

Document Output is automatically configured with two standard email jobs:
* **Queue** dispatches all documents from the **Document Queue**.  
* **Delete-Log** will delete log entries in accordance with the settings on the corresponding email template.

>  [!TIP]
>  Using table filters will help you define conditions for email jobs. Common filter options are **Status**, **Posting Date**, **Document Type** and **CDO Handled**.  
<br>
<iframe src=https://player.vimeo.com/video/899483770?h=4769e64cc3&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479 width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" title="DO Learn_3b Automate email jobs"></iframe>

This video is part of the course [Get started using Document Output](https://learn.continia.com/get-started-using-document-output) on Continia Learn.

## See also
[Setting up Job Queues](@DO-44)