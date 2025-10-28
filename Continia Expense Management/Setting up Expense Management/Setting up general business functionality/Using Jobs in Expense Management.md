---
title: Using jobs and job tasks
description: Learn how to assign expenses to specific jobs and tasks.  
date: 24-07-23
id: EM-170
lang: en
---

# Using projects and project task numbers

For all document types, you can determine which fields are visible to expense users within the Expense Mobile App and the Expense Portal. In addition to the default fields, you can include other fields, such as Project No. (projects/jobs) and Project Task No. (the project/job task number). Use the Project No. and Project Task No. fields to assign expenses to specific jobs and tasks:

*  **Project No.** - is the field for jobs. For example, if you want to assign expenses to a specific job, that refers to a particular project, task, or assignment undertaken by an individual or a team within an organization. It represents a work effort that requires resources and may have associated costs.
* **Project Task No.** - is the field for job tasks. For example, if you want to specify expenses that are related to sub-activities in completing a job. These tasks can be the individual steps or actions required to complete the job. Each task may have its own associated costs, such as materials, labor, or external services.

## Add project numbers and project task numbers

To add a Project No. and Project Task No. for an expense:

1. Search for {{search}} **Configured Fields**.

2. On the action bar, click **Per Diem**, **Mileage**, **Expense**, or **Expense Report**. The default for the expense type now displays. 

3. In the **Fields Code** column, select an empty cell and click **New**.

4. From the drop-down list, click **Project No.** or **Project Task No.**

## Use project billable or non-billable fields for project numbers and project task numbers
The document is automatically marked as billable if you add a **Project No.** and **Project Task No.** field. In Business Central, on the Expense Card, the **Job Line Type** is set to "Billable". This feature is useful when the job needs to be invoiced to the final customer, allowing a consultancy company, for instance, to invoice the job instead of bearing the costs. However, if the job is not intended for further invoicing, you can set the Job Line Type to **Budget**.

You can set the **Project Billable** field to default in the Expense Mobile App and Expense Portal. However, you can  only modify the **Job Line Type** field in Business Central. If you want to allow users in the app and portal to choose whether a document with a job and task assigned should be billable or not, you can add a field to the **Configured Fields**. This will enable users to edit the **Job Line Type** field directly in the app and portal.

To display the **Job Line Type** field in the Expense Mobile App and Expense Portal:

1. Search for {{search}} **Configured Fields**.

2. In the **Fields Code** column, select an empty cell and click **New**. 

3. In the drop-down list, click **Project Billable**. This action makes the field accessible on both the app and portal, with the default value being set to "False".

   In scenarios where the field should consistently default to "False" (non-billable), you can select the **Hide visibility by default** and **Editable** fields. This configuration hides the field while keeping its value as "False".

## Related information

For more information about jobs and tasks, see:

[The available job queues](@EM-278)

[Setting up job queues](@EM-65)

[Data maintenance using job queues for Continia Expense Management tables](@EM-205)