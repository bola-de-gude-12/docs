---
title: Handling discounts
date: 01-10-2024
description:
id: DC-227
lang: en
---

# Handling Discounts

This article describes how to handle discounts in Continia Document Capture.

Although discounts are a standard Microsoft Dynamics 365 Business Central feature, using it requires manually populating either the **Invoice Discount Amount** or the **Invoice Discount %** fields.

Document Capture allows you to capture a discount amount in a document and automatically transfer it to the standard invoice discount fields.

## Capturing discounts

The instructions below assume that you've already added the **Invoice Discount Amount** field to the desired template – and that you know how to train Document Capture to locate values. For more information, see [Capturing Header Fields in a Document](@DC-110).

To capture a discount:

1. Search ({{search}}) for and select **Document Categories**.
2. Select the code of the relevant document category – in this case **PURCHASE** – to open the document journal.
3. In the document list, select the document that you want to register.
4. On the action bar, click **Home** > **Recognize Fields** and make sure that all values, including the discount, have been captured correctly.
   >[!NOTE]
   >By default, discounts are captured as negative amounts. If a captured discount already includes the minus sign, go to the **Invoice Discount Amount** template field card and disable the **Change Sign** setting on the **General** FastTab.
5. If there are no errors, select **Home** > **Register** to register the invoice.
6. On the **Purchase Invoice** page, check the values transferred to the **Invoice Discount Amount** and **Invoice Discount %** fields at the bottom of the **General** FastTab.
   >[!NOTE]
   >Discounts are subtracted from the **Amount Excl. VAT**.
   >
## Related information
[Handling Discrepancies, Including Partial Matching](@DC-63)