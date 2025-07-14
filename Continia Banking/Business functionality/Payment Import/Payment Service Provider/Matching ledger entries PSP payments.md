---
title: Matching ledger entries with PSP payments
date: 28-03-2025
description: Describes how to match customer ledger entries with PSP imported payment lines in Continia Banking.
id: CB-182
lang: en
---

# Matching ledger entries with PSP payments

To enable the matching of ledger entries with payment lines imported from a payment service provider (PSP), you must configure specific settings for the **External Payment Reference** field. This configuration is done when running the **PSP Agreement Setup**.

The **External Payment Reference** field is included in sales documents and customer ledger entries, allowing it to be matched with the corresponding reference field specified in the imported file. Successful reconciliation occurs when these two fields contain identical values. By accurately specifying the relevant fields or columns for each PSP, Continia Banking ensures precise reconciliation based on the payment references provided within the file.

To apply the External Payment Reference field settings:

1. Search ({{search}}) for and select **PSP External References Rules**. Alternatively, use the PSP Agreement Setup assisted setup. 
2. To add a new External Reference Rule Template, select **New**.
3. Enter information for the **Template Code** and **Template Description** fields. 
4. Click the three dots on the far right to access the **Field Selection** page, where you can choose from various fields to include in external reference information. For example, include the **External Reference Number** and click **OK**.
5. Click the three dots next to the record in the **Field Selection Text** field to access the **Template Field Properties** page where you can configure more detailed settings. For example, set **Length** to **10** and **Place After** to **0** to ensure the sales header always contains ten digits.

Once you have set up the PSP, the PSP agreement, and the external reference rules, your ledger entries pages will display a **PSP External References** FactBox. This FactBox provides details such as the **PSP code** and the **External Payment Reference** from which the entry originates.

Additionally, in the **Cash Receipt Journal**, after configuring the PSP integration, you can **[import PSP payments](@CB-209)** using the designated import functionality. This allows reconciliation of payments with outstanding invoices based on external references. 
