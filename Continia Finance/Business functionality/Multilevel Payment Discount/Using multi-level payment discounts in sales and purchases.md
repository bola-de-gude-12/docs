---
title: Using multi-level payment discounts in sales and purchases in Continia Finance
date: 22-11-2024
description: How to use multi-level payment discounts in sales and purchase orders.
id: CF-130
lang: en
---

# Using Multi-level Payment Discounts in Sales and Purchases

This article describes how to use multi-level payment discounts in sales and purchase documents in Continia Finance.

These discounts can encourage early payments – which in turn reduce the administrative burden of chasing overdue invoices –, and also drive customer loyalty.

>[!NOTE]
>Before using multi-level payment discounts in sales and purchases documents, you need to enable multi-level payment discounts and add at least one payment term. For more information, see [Setting up Multi-level Payment Discount](@CF-103).

## To use multi-level payment discounts in sales documents
The example below uses a sales invoice, but similar approaches work across different sales documents.

To use multi-level payment discounts in sales invoices:

1. Choose the {{search}} icon, enter **Sales Invoices**, and then choose the related link.
2. On the **Sales Invoices** page, select **+New** to create a sales invoice.
3. Populate all the required fields, as well as the ones you need for this specific case.
4. On the **Invoice Details** FastTab, select a value from the **Payment Terms Code** dropdown menu.
5. When you're ready, select **Post** in the action bar.

When the document is posted, you can open the related entry to see an overview of the payment terms applied. To do so, select the 'i' icon at the top-right corner to expand the **Customer Ledger Entry Details** FactBox pane on the **Customer Ledger Entries** page.

## To use multi-level payment discounts in purchase documents
The example below uses a purchase order, but similar approaches work across different purchase documents.

To use multi-level payment discounts in purchase orders:

1. Choose the {{search}} icon, enter **Purchase Orders**, and then choose the related link.
2. On the **Purchase Orders** page, select **+New** to create a sales order.
3. Populate all the required fields, as well as the ones you need for this specific case.
4. On the **Invoice Details** FastTab, select a value from the **Payment Terms Code** dropdown menu.
5. When you're ready, select **Post** in the action bar.

When the document is posted, you can open the related entry to see an overview of the payment terms applied. To do so, select the 'i' icon at the top-right corner to expand the **Vendor Ledger Entry Details** FactBox pane on the **Vendor Ledger Entries** page.

>[!TIP]
>It's also possible to add a payment term to a customer or vendor card, under the **Payments** FastTab. This way, the payment term applies to every sales or purchase document corresponding to the customer or vendor.

## To apply entries with multi-level payment discounts

When you apply a payment related to a document with multi-level payment discounts, the payment date is used to calculate the correct discount. The example below uses the cash receipt journal, but a similar approach works on the general journal.

To apply entries with multi-level payment discounts:

1. Choose the {{search}} icon, enter **Cash Receipt Journals**, and then choose the related link.
2. On the **Cash Receipt Journals** page, populate all the required fields according to the related sales or purchase document.
3. Under **Amounts**, enter the required amount minus the discount valid for the posting date.
4. In the action bar, select **Home > Apply Entries**. Then, select the correct posted entry.
5. In the action bar, select **Set Applies to ID** to populate the fields in the posted entry with the values from the document in the journal.
6. The payment discount fields are automatically populated, according to the posting date and the selected payment terms code.

## See also

[Setting up Multi-level Payment Discount](@CF-103) 