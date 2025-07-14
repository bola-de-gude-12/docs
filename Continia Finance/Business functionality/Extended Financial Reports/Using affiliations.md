---
title: Using affiliations
date: 13-09-2024
description:
id: CF-113
lang: en
---

# Using Affiliations

This article describes the usage of affiliations in Continia Finance.

An affiliation is a relationship between two or more companies that are connected to each other for business purposes. If companies are affiliated in Finance, you have the option to see their combined data – such as G/L entries or VAT entries – in a single report.

## To connect companies as an affiliation

Before you can make use of this feature, you have to connect your companies as an affiliation:

1. Choose the {{search}} icon, enter **Extended Financial Reports Setup**, and then choose the related link.
2. On the **Affiliation** FastTab, enter a code in the **Affiliation** field. For example, AFF_01.
3. Next, select the company icon to open the **Available Companies** pane and switch to the company that you would like to affiliate with the current company.
4. Repeat steps 1 and 2, entering the same code you entered for the previous company. For example, AFF_01.

## To see combined data as a single report

Once your companies are configured as an affiliation, you can see their combined data in a single report. To do this:

1. Select **Extended Financial Reports** > **Reconcile**, then select either **G/L Entries Overview** or **VAT Entries Overview**.
2. In the action bar, select **Refresh Table** to open the related overview.
3. On the **Options** FastTab, enable the **From Affiliation** setting and make sure that the code in the **Affiliation** field is correct.
4. Select **OK** at the bottom of the page.

>[!NOTE]
>It's possible to achieve the same result by using the filters on the **Filter: Company** FastTab on the **Refresh G/L Entries Overview** and **Refresh VAT Entries Accounting Review**. Here you can also use an asterisk as a wildcard. For example, to include all companies with the word Cronus in their names, enter Cronus*.
