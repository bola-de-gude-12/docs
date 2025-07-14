---
title: Integrating Regulatory Reporting in Continia Banking
date: 01-04-2025
description: Learn how you can manage regulatory reporting for cross-border payments in Continia Banking.
id: CB-210
lang: en
---
# Introducing regulatory reporting

Some countries require the use of specific reporting codes for cross-border payments to ensure compliance with financial regulations. For example, in Germany, any amounts over €12,500 leaving the country must be reported to the Bundesbank. Similarly, in Sweden and Norway, payments exceeding 150,000 SEK and 100,000 NOK, respectively, must trigger a warning.  Continia Banking simplifies this process by providing predefined codes, validation handling, and the ability to configure these rules directly on the vendor, ensuring that the required regulatory reporting codes are also included in the exported payment file.

To view the regulatory reporting codes:

* Search ({{search}}) and select **Regulatory Reporting Codes** to access predefined codes. These codes are available in the system by default in Continia Banking.

To view a vendor's regulatory reporting codes:

* Open the vendor or customer card, and on the action bar, select **Related** > **Vendor** > **Regulatory Reporting Codes**. Assign regulatory reporting codes to a vendor card, and they will automatically apply to future purchase documents. The codes will be applied directly to the vendor’s purchase documents.

## Manual setups

The following manual setups allow you to customize and configure essential information for regulatory reporting. These setups help ensure that all relevant data is properly aligned with your reporting requirements:

* **Reporting Setup** - on this page, you can configure the **Reporting Type**, **Reporting Amount**, and **Company Number** (for German localizations, this number is provided by the Bundesbank). For example, in a German localization, if the **Reporting Amount** is set to €12,500. Any international payment exceeding this amount generates a reporting entry.
* **Regulatory Reporting** - on this page, you can add the **Code**, **Description**, and **Reporting Group**.



## Reporting groups

Continia Banking provides a pre-filled table of regulatory reporting codes and their groups, simplifying setup. Currently, the Group field categorizes transactions into Transit, Service, or Capital, which align with German bookkeeping standards. This feature provides a structured approach to managing and reporting regulatory information related to ledger entries. While Continia Banking currently focuses on Germany, we are working to expand regulatory reporting support to other regions.

For more information on reporting entries and regulatory reports, refer to the [Generating a regulatory report](@CB-220) article.

