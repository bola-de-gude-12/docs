---
title: The Purchase Order category in Document Capture
date: 19-05-2025
description: How to create and update purchase orders in Document Capture.
id: DC-136
lang: en
---

# The Purchase Order category

The Purchase Order category – PURCHORDER – enables you to automatically create and update purchase orders based on data recognized in another document (typically an order confirmation from a vendor). The purchase orders are created in Microsoft Dynamics 365 Business Central once you register them.

When a purchase order is created this way, the recognized data can be, for example, item numbers, price, and quantity – or virtually anything else that you might find relevant to capture in the document from the vendor. The updating of purchase orders, however, includes only a limited number of selected fields: **Vendor Order No.**, **Vendor Shipment No.**, **Promised Receipt Date**, **Quantity**, and **Direct Unit Cost**.

>[!NOTE]
>Although you can't add lines to an existing purchase order, you can update existing lines. Alternatively, you can create a different purchase order.

It's also possible to handle delivery notes in the Purchase Order category. This enables you to match vendor delivery notes to an open purchase order, update the **Quantity to Receive** field of the purchase order, and post the purchase receipt and/or an invoice.

All three processes – creation as well as updating and matching of purchase orders – are described in the sections below.

## To create a purchase order

To create a Business Central purchase order based on an imported document, such as an order confirmation:

1. Search ({{search}}) for and select **Document Categories**.

1. Select the **PURCHORDER** code to open the document journal for purchase orders.

1. In the list of documents, select the one that you want to use as a basis for the purchase order you're about to create.

1. If the document is related to a new vendor, make sure that there's a vendor and a template associated with it. If not, create the vendor by selecting **Vendor > Vendor Card** on the action bar and filling out the details. Document Capture will then create a copy of the related master template, and associate it with the new vendor.

1. On the action bar, click **Home** > **Recognize Fields** to capture the fields of the selected document.

1. Check that all required fields have been captured correctly, and if any warnings or error messages are displayed in the **Comments** section at the bottom. If something is wrong or missing, correct this manually. For example, to capture any unidentified field captions or values manually, see [Capturing header fields in a document](@DC-110).

1. Go to **[O]rder / [R]eceipt**, and check that the letter **O** is displayed in the **Value** column. If not, enter it manually, and then select **Enter**.

1. On the action bar, click **Template** > **Template Card** to open the template card.

1. On the **Purchase Orders** FastTab, go to **Order Reg. Step 1** and make sure that **Create Order** or **Create or Update Order** is selected.
   > [!NOTE]
   > If **Create or Update Order** is selected, Document Capture uses the **Our Order No.** or **Vendor Order No.** data to automatically determine whether to create a new order or update an existing one.

1. On the action bar, click **Home** > **Register** to register the new purchase order.

The purchase order is then created as a business unit in Business Central, ready for further processing.

## To update a purchase order

To update an existing purchase order:

1. Search ({{search}}) for and select **Document Categories**.

1. Select the **PURCHORDER** code to open the document journal for purchase orders.

1. In the list of documents, select the one whose data you want to use to update an existing purchase order.

1. On the action bar, click **Home** > **Recognize Fields** to capture the fields of the selected document.

1. Check that all required fields have been captured correctly and if any warnings or error messages are displayed in the **Comments** section at the bottom. If something is wrong or missing, correct this manually. For example, to capture any unidentified field captions or values manually, see [Capturing header fields in a document](@DC-110).

1. Go to **[O]rder / [R]eceipt**, and check that the letter **O** is displayed in the **Value** column. If not, enter it manually, and then select **Enter**.

1. On the action bar, click **Template** > **Template Card** to open the template card.

1. On the **Purchase Orders** FastTab, go to **Order Reg. Step 1** and make sure that **Update Order** or **Create or Update Order** is selected.
   > [!NOTE]
   > If **Create or Update Order** is selected, Document Capture uses the **Our Order No.** or **Vendor Order No.** data to automatically determine whether to create a new order or update an existing one.

1. On the action bar, click **Home** > **Register** to update the related purchase order.

The existing purchase order that matches the selected document is then updated with the data of the selected document.

## To update a purchase order based on a delivery note

To update an existing purchase order based on a delivery note:

1. Search ({{search}}) for and select **Document Categories**.

2. Select the **PURCHORDER** code to open the document journal for purchase orders.

3. In the list of documents, select the delivery note whose data you want to use to update an existing purchase order.

4. On the action bar, click **Home** > **Recognize fields** to capture the fields of the selected document.

5. Check that all required fields have been captured correctly and if any warnings or error messages are displayed in the **Comments** section at the bottom. If something is wrong or missing, correct this manually. For example, to capture any unidentified field captions or values manually, see [Capturing Header Fields in a Document](@DC-110).

6. Go to **[O]rder / [R]eceipt**, and check that the letter **R** is displayed in the **Value** column. If not, enter it manually, and then select **Enter**.

7. On the action bar, click **Template** > **Template Card** to open the template card.

8. On the **Purchase Orders** FastTab, go to **Receipt Reg. Step 1** and select **Update Order Receipt**.

9. **Optional:** If you also want to post the purchase receipt, go to the **Purchase Orders** FastTab, go to **Receipt Reg. Step 2** and select **Post Receipt** or **Post Receipt and Invoice** based on your preference.

   > [!NOTE]
   > If **Create or Update Order** is selected, Document Capture uses the **Our Order No.** or **Vendor Order No.** data to automatically determine whether to create an order or update an existing one.

10. On the action bar, click **Home** > **Match Lines**.

11. On the action bar, click **Perform Match**. Document Capture tries to find the matched items and update the columns **Matched Quantity** and **Total Matched Quantity**. 

12. On the action bar, click **Home** > **Register** to update the related purchase order.

This updates the **Qty. to Receive** field of the existing purchase order that matches the selected document and, depending on your setting in step 9, the receipt is posted.

## Related information

[Basic concepts in Document Capture](@DC-83)  
[Working with document categories](@DC-78)