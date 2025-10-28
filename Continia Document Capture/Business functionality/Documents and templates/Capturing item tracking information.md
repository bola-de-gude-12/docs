---
title: Capturing item tracking information in Document Capture
date: 30-09-2025
description: 
id: DC-175
lang: en
---

# Capturing item tracking information

It's possible to capture item tracking data in Continia Document Capture, allowing for better inventory accuracy, traceability, compliance, and cost management. When the document is registered, captured information such as an item's warranty date is added to the created invoice – and you can then track the item directly in Microsoft Dynamics 365 Business Central.

You can use the following five fields for item tracking purposes:

* **Expiration Date**
* **Lot No.**
* **Package No.**
* **Serial No.**
* **Warranty Date**

>[!NOTE]
>If you don't see the above-mentioned fields, either import the configuration files or upgrade to the latest version of Document Capture.

For more information on item tracking, see [Track items with serial, lot, and package numbers](https://learn.microsoft.com/en-us/dynamics365/business-central/inventory-how-work-item-tracking) (Microsoft article).

## Considerations

At present, the capture of item tracking data is only possible:

* Within the **PURCHASE** category.
* When creating invoices.
* For PDF documents.
* With a single tracking point per line. That is, multiple package numbers or expiry dates in a single line – for example – can't be captured.

## Requirements

Before you can capture item tracking information in Document Capture, you need to:

1. [Enable line recognition](@DC-147) on the desired template.
2. [Add at least one of the following fields](@DC-241) to the desired template. These are the fields that define item tracking in Business Central.
   
   * **Lot No.**
   * **Package No.**
   * **Serial No.**

## To capture item tracking information

1. Search ({{search}}) for and select **Document Categories**.
2. Click the relevant document category code – in this case, **PURCHASE** – to open the document journal.
3. In the list of documents, select the desired document.
4. Make sure that at least one of [the required fields](#requirements) has a captured value.
5. On the action bar, click **Home** > **Register**.
