---
title: Using Dimensions on System Entries and Check VAT Key on a G/L Account
date: 19-09-2024
description: Learn how to use dimensions on system entries enable the Check VAT Key feature on a G/L account.
id: CF-31
lang: en
---

# Using Dimensions on System Entries and Check VAT Key on a G/L Account

In Business Central, dimensions are used to add additional context to transactions by categorizing entries with tags like departments, projects, or customer groups. These dimensions can then be used in reporting and analysis to gain more detailed insights into the business operations.

## Using dimensions on system entries

On each G/L Account Card, you have the following options to choose from in **Dimension for System Entries**:

* Gen. Jnl. Line (Always) - Always copy dimensions from the entered general journal line
* G/L Account (Always) - Copy dimensions from the default G/L account dimensions for system postings
* G/L Account (if empty Gen. Jnl. Line) - Copy dimensions from the default G/L account dimensions if no general journal line information is entered

These values are used for system postings, such as the **Adjust Exchange Rate**, to determine the dimensions in the postings.



## Enable **Check VAT Key** on a G/L account

With this feature enabled on a G/L account, the system checks the VAT key for all postings to this G/L account. If this key does not match that of the G/L account, an error message appears. Consequently, the corresponding G/L account is also checked during the shipping and invoicing of purchase and sales documents with items.

To enable **Check VAT Key** on a G/L account, follow these steps:

1. Go to the G/L Account Card for the G/L account for which you want to enable **Check VAT Key**.
2. In the **Continia Finance** FastTab, enable **Check VAT Key**.




<style>

 .content table tr td:nth-child(1) {

 width: 200px;

 }

 .content table tr td:nth-child(2) {

 width: 600px;

 }

</style>
