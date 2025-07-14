---
title: Using allocation accounts
date: 05-03-2025
description:
id: DC-226
lang: en
---

# Using Allocation Accounts

This article describes how allocation accounts work in Continia Document Capture.

Allocation accounts is [a standard Microsoft Dynamics 365 Business Central feature](https://learn.microsoft.com/en-us/dynamics365/business-central/finance-allocate-revenue-costs) that allows you to split costs between two or more G/L accounts or dimensions within a company. This is useful because costs can't always be directly linked to a specific department, for instance.

When recognizing fields, it's possible to set **Allocation Account** as the **Type** on the header level, and as the **Translate to Type** on the line level. You can then set an account number in **No.** or **Translate To No.**, and define how the captured amounts or quantities are split across different destination accounts on the **Allocation Account** page.

>[!NOTE]
>**Allocation Accounts** must be configured with the fixed account types, rather than variable. Otherwise, the amounts involved are distributed evenly across accounts – instead of proportionally, according to the configuration of the allocation account. Also: it's not possible to match order lines with the account type set to **Allocation Account**; and the destination account type **Inherit from parent** isn't supported.

For example, an allocation account can be configured to equally split amounts invoiced by a certain vendor between the Content and Marketing departments (i.e.: 50% and 50%). Another account can be configured to allocate 80% of the bill from an Internet service provider as a broadband subscription, while the remainder is allocated as a mobile subscription.

To test a configured allocation, select **Test Allocation** on the action bar on the **Allocation Account** page. You're then presented with the **Allocation Account Preview**, which uses data from the selected document to show how the amount in the document will be split.

When registering documents, purchase lines with the **Allocation Account** type are automatically expanded to the underlying account types using the standard function **Generate Lines From Allocation Account Line**, which is available on the standard purchase document pages.

>[!NOTE]
>The validation of the **Total Amount Incl. VAT**/**GST** isn't done when using allocation accounts. This is due to the fact that Business Central doesn't calculate the VAT/GST amount on documents containing lines with allocation accounts.