---
title: Using Jobs and Job Tasks
description: Learn how to assign expenses to specific jobs and tasks.  
date: 13-07-23
id: EM-170
lang: en
---

# Using Jobs and Job Tasks

For each document type, it is possible to determine the specific fields visible to expense users within the Expense App and the Expense Portal. In addition to the default fields, you can include other fields, such as jobs. To assign expenses to specific jobs and tasks, you can add the following fields:

*  **Jobno** - field for jobs. For example, if you want to assign expenses to a specific job, that refers to a particular project, task, or assignment undertaken by an individual or a team within an organization. It represents a distinct work effort that requires resources and may have associated costs.
* **Task** - field for job tasks. For example, if you want to specify expenses related to sub-activities involved in completing a job. These tasks can be the individual steps or actions required to accomplish the overall objective of the job. Each task may have its own associated costs, such as materials, labor, or external services.

## To add jobs and tasks

To add Jobno and Task for an expense:

1. Select the {{search}} icon, enter **Configured Fields**, and then select the related link.

2. On the action bar, select the **Per Diem**, **Mileage**, **Expense**, or **Expense Report**. The default for the expense type now display. 

3. In the **Fields Code** column, select an empty cell and select **New**.

4. From the drop-down list, select **Jobno** or **Task**. 

## To use billable or non-billable for jobs and tasks
The document is automatically marked as billable if you add a **Jobno** and **Task** field. In Business Central, on the Expense Card, the **Job Line Type** is set to *Billable*. This feature is useful when the job needs to be invoiced to the final customer, allowing a consultancy company, for instance, to invoice the job instead of bearing the costs. However, if the job is not intended for further invoicing, you can set the Job Line Type to **Budget**.

The **Billable** field can be configured by default in the Expense App and Expense Portal. However, the **Job Line Type** field can only be modified in Business Central. If you want to allow users in the app and portal to have the ability to choose whether a document with a job and task assigned should be billable or not, you can add a field to the **Configured Fields**. This will enable users to edit the **Job Line Type** field directly in the app and portal.

To display the **Job Line Type** field in the Expense App and portal:

1. Select the {{search}} icon, enter **Configured Fields**, and then select the related link.

2. In the **Fields Code** column, select an empty cell and select **New**. 

3. From the drop-down list, select **Billable**. This action makes the field accessible on both the app and portal, with the default value being set to *False*.

   In scenarios where the field should consistently default to *False* (non-billable), you can select the **Hide visibility by default** and **Editable** fields. This configuration hides the field while keeping its value as *False*.