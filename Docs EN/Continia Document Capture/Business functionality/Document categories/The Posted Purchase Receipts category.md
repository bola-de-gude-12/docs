---
title: The Posted Purchase Receipts category in Document Capture
date: 18-09-2025
description: How to process documents imported into the Posted Purchase Receipts category.
id: DC-174
lang: en
---

# The Posted Purchase Receipts category

The Posted Purchase Receipts category – **PURCHRECPT** – in Continia Document Capture enables you to OCR-process receipts related to the purchase of goods or services (such as delivery notes or bills of lading), making them searchable.

When a purchase receipt is imported, this document category checks all recognized values and compares them to the **Vendor**, **Vendor Order No.**, and **Vendor Shipment No.** identification fields. [Each of these fields has a rating](@DC-81#calculating-confidence-scores), which can be edited on the **Identification Fields** page of the Posted Purchase Receipts category.

The resulting document is added to the original posted purchase receipt.

## To work with the Posted Purchase Receipts category

To process documents imported into the Posted Purchase Receipts category:

1. Search ({{search}}) for and select **Document Categories**.

2. On the **Document Categories** page, click the **PURCHRECPT** code to open the Posted Purchase Receipts category.

3. In the document journal, select the desired document and make sure that the **Purch. Rcpt. Header** field has picked up the correct value.

4. On the action bar, click **Home > Register** to register the document.

To see the registered document, you can either:

  * Search ({{search}}) for and select **Find entries**.
  * Add the **Documents** FactBox to the **Posted Purchase Receipt** page, which is hidden by default but can be revealed by clicking **Settings** ({{settings}}) > **Personalize** in the top-right corner of the page.
