---
title: VAT entries overview
date: 30-09-2024
description: How to access and use the VAT entries overview.
id: CF-115
lang: en
---

# VAT Entries Overview
This article describes the **VAT Entries Overview** in Continia Finance.

The **VAT Entries Overview** is part of the **Extended Financial Reports** module in Finance. It shows a combined list of G/L account balances based on various criteria, provided that the account has at least one posting including VAT. If you use the [affiliation or filters features](@DC-113), the **VAT Entries Overview** can also display financial data from different companies.

To access the **VAT Entries Overview**:

1. Select **Extended Financial Reports** > **Reconcile**, then select **VAT Entries Overview**.
2. At first, the overview is empty. To populate it, select **Refresh Table** in the action bar.
3. On the **Options** FastTab, the following settings are available:
   * VAT Statement Template: Specifies the VAT statement template used to transfer the row number when running the **Refresh VAT Entries Accounting Review** report.
   * VAT Statement Name: Specifies the VAT statement used to transfer the row number when running the **Refresh VAT Entries Accounting Review** report.
   * Include Proof of VAT-Accounts: If enabled, the VAT accounts set up in the VAT statement are included.
   * Include VAT entries: Specifies the VAT entries that should be included in the report. For example, open and closed.
4. When you're satisfied with the configuration, select **OK**.
5. The overview is populated accordingly, allowing you to sort the data based on the many columns presented.

By clicking a value under the **Amount** or **VAT Amount** columns, you can see all entries in the related G/L account.

## See also
[Using Affiliations](@CF-113)<br>
[G/L Entries Overview](@CF-114)