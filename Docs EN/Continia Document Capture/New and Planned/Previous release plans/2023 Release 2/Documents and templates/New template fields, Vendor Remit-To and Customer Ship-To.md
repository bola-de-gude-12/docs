---
title: New Template Fields – Vendor Remit-To and Customer Ship-To
date: 29-11-2024
description:
id: DC-305
lang: en
---

# New Template Fields – Vendor Remit-To and Customer Ship-To

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| New template fields – **Vendor Remit-To** and **Customer Ship-To** | - | Oct 2023 |

## Business value

By adding two new fields to the PDF master template and making them available for selection straight from the document card before document registration, this feature will make it much easier for North American users to select remit-to and ship-to addresses for incoming purchase and sales documents in Continia Document Capture.

## Feature details

For the North American localization (NA), the following two template fields will be added to the PDF master template:

* **Vendor Remit-To** – added to the **PURCHASE** and **PURCHORDER** categories
* **Customer Ship-To** – added to the **SALES** category

The fields relate to standard Microsoft Dynamics 365 Business Central remit-to and ship-to fields, such as **Remit-to Code** and **Ship-to Code**. With the new fields, you'll be able to select alternative remit-to and ship-to addresses straight from the document card, in case the actual addresses differ from the default ones. This means that you'll no longer have to go through the hassle of first registering a document and then manually adding an address code to the registered document. Instead, the new functionality will allow you to do all this in a single operation from the relevant document card.