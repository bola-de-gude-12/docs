---
title: Automatic archiving of purchase orders upon registration of updates
date: 24-12-2024
description:
id: DC-349
lang: en
---

# Automatic Archiving of Purchase Orders upon Registration of Updates

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Automatic archiving of purchase orders upon registration of updates | {{checkmark}} Sep 2024 | {{checkmark}} Oct 2024 |

## Business value

If a purchase order is updated by the vendor you sent it to, you may want to view the history of the order to see what it previously looked like. This is facilitated by this feature, which will enable you to track any purchase order changes and view earlier versions in a standard Microsoft Dynamics 365 Business Central archive.

## Feature details

With the feature, you'll be able to have your purchase orders archived automatically whenever you register any order updates made by a vendor. The feature will automatically archive the version of each purchase order that exists immediately before any vendor changes are applied. All archived order versions will be stored in the standard Business Central **Purchase Order Archive**.

Purchase orders will be archived automatically in the following scenarios, depending on the document category:

* **PURCHASE** category: When you register a Document Capture document as an invoice or a credit memo using the **Match & Update Order** or **Match & Update Return Order** registration options.
* **PURCHORDER** category: When you register a Document Capture document using the **Create or Update Order**, **Update Order**, or **Update Order Receipt** registration options.