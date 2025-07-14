---
title: Printing extended financial reports in Continia Finance
date: 08-10-2024
description: How to print extended financial reports in Continia Finance.
id: CF-116
lang: en
---

# Printing Extended Financial Reports
This article describes how to print extended financial reports, be it to have a focused and more detailed view of the report within Continia Finance or to print it to a PDF or actual paper.

## To print extended financial reports
To print an extended financial report:

1. Choose **Extended Financial Reports** and then select the **Financial Report** dropdown menu to set the desired report, such as REVENUE.

2. As well as the standard options provided by Microsoft Dynamics 365 Business Central, the following options are available:

   **Layout**

   * Column definition - specifies the name of the column layout used for the report, such as period or net change.

   **Show**

   * Show Company - specifies whether the company's name or display name should be used.

   * Show Error - specifies if the report should include information related to errors, such as divisions by zero.
   * Show Account Schedule Setup - if enabled, the first page shows the setup of the account schedule and the column layout.
   * Print the field Structure instead of the field Row No. - if enabled, the structure field is printed instead of the row number field. The structure field can then be used to print the balance position.
   * Show Accounts Detail - if enabled, the underlying accounts of a total line appear below the respective total line in the printout.
   * Show System Accounts - if enabled, postings are grouped in separate accounts – based on the respective source account (customer, vendor, or bank account) and shown in separate lines. This feature is only available if the **Separate Receivables and Payables** setting is enabled in the row definition.
   * Use Detailed Export from Row Definition - if enabled, detailed lines are only exported for row definition lines where the field **Export Details** is set.
   * Prevent Export of Accounts with No Entries - specifies whether accounts without entries should be included in the report.
   * Check Plausibility - specifies if the system should check if all G/L accounts are included in the financial report or if any G/L accounts have been included twice. To include blocked accounts, the **Include Blocked Accounts** setting must be activated as well. Note that contra asset accounts must always be specified twice – both as assets and as liabilities.
   * Include Blocked Accounts - specifies if blocked G/L accounts should be included in the plausibility check.


You can then select how to share or print the report. Alternatively, you can select **Preview & Close** to preview the report.