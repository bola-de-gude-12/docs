---
title: Using expense reports from your browser
date: 11-06-2025
description: Submit and review expense reports in the Expense Portal and Business Central
id: EM-294
lang: en
---
# Using expense reports from your browser

Keep track of your business expenses with an efficient expense report management tool that's intuitive to use and creates a more efficient workflow. Available online in Business Central and via the Continia Expense Portal

Features include: cash advance to report cash withdrawals, the option to pre-approve expense reports, comments visibility for every document included in a report all in one overview, and the option to open an expense in the expense report and view it in granular detail (rather than list view) on the Expense Document card. 

Get started by learning how to create and submit new expense reports, add existing entries to reports, and utilize key features such as improved comment visibility and warning notifications.

## Creating and submitting expense reports in the Continia Expense Portal

Expense users can create and submit expense reports using the Expense Portal. The expense reports are transferred through Continia Online to Business Central after synchronization. Typically, the Expense Portal is set to automatically synchronize with Continia Online using job queues.

To create and submit an expense report using the Expense Portal:

1. On the action bar at the top, click **Report**.
1. In the upper-left corner, click **New** to open the **Report** page.
1. In the **Description** field, enter a title for the report.
1. On the action bar, click to add a **New Expense**, a **New Mileage**, or a **New Per Diem**. To add a document you've already prepared:
   * Click **Add Existing Documents**.
   * On the **Select documents** page, choose the document you want to add.
   * In the bottom-right corner, click **Save and continue**.
1. For each of the expenses/mileages/per diems you add, fill in all necessary fields, then click **Save** in the upper-left corner.
1. On the **Report** page, you can:
   * Save the report to edit later – for example, if you want to add more expenses/mileages/per diems to the report before submitting it – on the action bar, click **Save**.
   * Delete the report – on the action bar, click **Delete**.
   * Submit the report for approval – on the action bar, click **Submit**.

Your report is now either saved, deleted, or submitted, depending on your preferences.

## Creating and submitting expense reports in Business Central

You can create expense reports in Business Central using the **Limit Document Visibility** setting on the **Continia User Setup Card**. This limits document visibility for a certain user to that user's own documents.

To create and submit an expense report in Business Central:

1. Search for {{search}} **Expense Reports**.

1. On the action bar, click **New** to open the **Expense Report Card**.

1. Under **Continia User ID**, enter or select the ID of the expense user whose expense report you're creating.

1. Under **Description**, enter a title for the report.

1. Add expenses, mileages, or per diems to the report (follow the steps below).

To add expenses:

   1. Under **Expenses**, click **New Line** to add a line to the table.
   1. Fill in the **Payment Type**, **Expense Type**, **Description**, and **Amount** fields, along with any other necessary fields.
   1. Attach a relevant file to the expense.
      1. On the Expenses, Mileage, or Per Diem action bar, click **Line** > **Attachments** to open the **Attached Files** page.
      1. On the action bar, click **Add** to open the **Select File** dialog.
      1. Add the file you want to attach, either **click here to browse** or drag the file straight from your file browser to the drag-and-drop area.
      1. The file is attached. Click **Close** to return to the **Expense Report Card**.
   1. To add more expenses, select a new line in the table and repeat steps 5b–5c.

To add mileages:
   1. Under **Mileage**, click **New Line** to add a line to the table.
   1. Fill in the **Purpose**, **From Address**, **To Address**, and **Total Distance** fields, along with any other relevant fields.
   1. Attach a relevant file to the mileage as you would for an expense in step 5.
   1. To add more mileages, select a new line in the table and repeat steps 6b–6c.

To add per diems:
   1. Under **Per Diem**, click **New Line** to add a line to the table.
   1. Fill in the **Departure Date/Time**, **Return Date/Time**, and **Description** fields, along with any other relevant fields.
   1. Click the **Amount** field to open the **Per Diem Details** page.
   1. On the action bar, click **Edit List** to make the list editable.
   1. For each of the date lines in the table, specify what allowances should be included in the per diem calculation by selecting the relevant boxes.
      > [!NOTE]
      > In the **Accommodation Allowance** column, you can't select the box for the earliest date in the top line, (even if there's only one date line in the table). You can only select the boxes for subsequent lines (if any).
   1. To add more per diems, click a new line in the table and repeat steps 7b–7e.

## Reviewing warnings in an expense report

Expense report warnings highlight issues that need to be resolved to ensure accuracy and completeness of your expense reports. The system-generated warnings include:

- Missing attachments for an expense
- A purchase contract that needs to be added

To review warnings in Business Central:

1. Search for {{search}} **Expense Reports**.
2. Review your list of expense reports, if there are any warnings the report line will have red writing.
3. Open the report and check the information is accurate and all necessary fields have been filled in. 
4. Check the comments of the report (they're directly visible on the document line within the expense report). Under **Expenses**, **Mileage**, or **Per Diem** > **Line**, click **Comments** to view comments for multiple documents from the report. This functionality allows you to quickly review all related comments without having to navigate to separate document lines.

## Linking fields between reports and individual documents

If you add one or more fields to the header of an expense report on the **Configured Fields** page, the individual documents of that report will automatically inherit the values of the fields you added (if you had added the same fields to the documents). This applies to both newly created documents and existing documents that you add to the report.

To add one or more fields to an expense report and to individual documents:

1. Search for {{search}} **Configured Fields**.
1. On the action bar, click **Home** > **Expense Report**.
1. To add one or more new fields:
   1. Under **Fields on Header**, click **New Line** to add a new line to the table.
   1. In the **Field Code** column of the new line, click in the field to open a dropdown menu.
   1. Either select a field from the dropdown menu, or enter a search phrase to find the field you want to add, then select the field from the menu to add it.
   1. To add any additional fields, repeat steps 3a–3c.
1. On the action bar, choose the type of expense document (**Expense**, **Mileage**, or **Per diem**) you want to add corresponding fields to.
1. Follow the instructions in step 3 to add the same fields as the ones you added to the expense report.
1. Repeat step 5 for any additional documents you want to inherit the values of your added fields.

Any document of the kind you set up will inherit the values of the fields you added to the expense report header after the document is added to an expense report or created from within an expense report.

For example, if you add the **Project No.** field to the expense report header and to the mileage header on the **Configured Fields** page, a corresponding **Project No.** field will be available for each expense report you create and for each mileage you add to an expense report. Then, when you select a **Project No.** field value for an expense report, this value will automatically be inherited by any mileage you create or add from within that report.

## Related information

For more information about creating, submitting, reviewing, or approving expense reports, see: 

[Overview of expense reports](@EM-44)

[Setting up pre-approval of expense reports](@EM-272)

[Setting up expense reports](@EM-306)

[Expense reports in the Expense Mobile App](@EM-326)
