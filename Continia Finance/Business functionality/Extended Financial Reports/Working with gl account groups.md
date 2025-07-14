---
title: Working with G/L account groups in Continia Finance
date: 18-09-2024
description: How to create customized account groups.
id: CF-98
lang: en
---

# Working with G/L Account Groups	
This article describes the **G/L Account Groups** feature, which is part of the Extended Financial Reports module in Continia Finance.

The **G/L Account Groups** feature allows you to create account groups and link them with G/L accounts. It's similar to the **G/L Account Categories** feature built into Microsoft Dynamics 365 Business Central, though G/L account groups are more flexible because they can be fully customized.

Grouping similar accounts together helps you declutter financial data and better organize financial reports – such as balance sheets, profit-and-loss statements, and business analyses.

>[!NOTE]
>Extended financial reports were previously known as extended account schedules.

It's possible to create up to eight different account groups and use group codes to organize these accounts in different financial reports.

## Setup of G/L account groups

The setup of G/L account groups involves four steps, which are described below.

### To create G/L account group captions

The first step is to assign captions to the default account groups. Although this is optional, it makes it easier to identify your account groups when working on your chart of accounts and financial reporting pages.

To create G/L account group captions:

1. Choose the {{search}} icon, enter **Extended Financial Reports Setup**, and select the related link.
2.	On the **Account Groups** FastTab, enter captions to describe the purpose of each G/L account group required. For example, Balance Sheets for Annual Report.

### To add G/L account group codes
Next, you need to specify the codes used to organize the G/L accounts within each account group. You can create as many codes as needed, and each code can be assigned to multiple G/L accounts.

To add G/L account group codes:

1. Choose the {{search}} icon, enter **G/L Account Groups Setup**, and select the related link.
2.	In the **G/L Account Group** dropdown, select the G/L account group you want to edit.
3.	In the action bar, select **Edit List**.
4.	Select an empty line and enter the desired **Code** and **Description**. For example, BS101 and Income from Sales.

### To link a G/L account to a G/L account group code
With the captions, account groups, and codes in place, you can now connect G/L accounts with G/L account group codes.
To do so:

1.	Choose the {{search}} icon, enter **Chart of Accounts**, and select the related link.
2.	In the action bar, select **Edit List**.
3.	Under the column with the caption associated with the desired account group (for example, Balance Sheets for Annual Report), select the three dots to assign a G/L account group code to one or more accounts.

It's also possible to link a G/L account with a G/L account group when you're either creating or editing the G/L account itself. On the **G/L Account Card**, add the desired G/L account group codes to the relevant G/L account groups on the **Continia Finance** FastTab.

### To use G/L account groups in row definitions

Once you have set up G/L account groups, you can use the account group codes in the row definitions of financial reports. To do so:
1.	Choose the {{search}} icon, enter **Financial Reports**, and select the related link.
2.	Select the report you want to edit and, in the action bar, select **Edit Definitions** > **Edit Row Definition**.
3.	On the **(Financial Report) Row Definition** page, select the desired G/L account group under the **Totaling Type** column.
4.	Under the **Totaling** column, enter the desired G/L account group code or choose one from the list by selecting the three dots.
