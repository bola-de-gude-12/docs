---
title: The Sales Orders and Credit Memos category
date: 27-10-2025
description: How to create and update sales orders and credit memos in Document Capture.
id: DC-459
lang: en
---

# The Sales Orders and Credit Memos category

The Sales Orders and Credit Memos category – **SALES** – in Continia Document Capture enables you to automatically create and update sales orders and credit memos based on data recognized in another document (typically a purchase order from a customer). The sales orders and credit memos are created in Microsoft Dynamics 365 Business Central once you register them.

When a sales order is created this way, the recognized data can be, for example, order and delivery dates, item numbers and quantities – or virtually anything else that you might find relevant to capture in the document from the customer.

This article focuses on sales orders, but the instructions within also apply to credit memos.

## To create a sales order

To create a Business Central sales order based on an imported document:

1. Search ({{search}}) for and select **Document Categories**.

2. Click the **SALES** code to open the document journal for sales orders and credit memos.

3. In the list of documents, select the one you want to use as a basis for the sales order you're about to create.

4. If the document is related to a new customer, make sure that there's a template associated with it. If not, create the customer by clicking **Customer** > **Customer Card** on the action bar and filling out the details. Document Capture creates a copy of the related master template, and associates it with the new customer.

5. On the action bar, click **Home** > **Recognize Fields** to capture the fields of the selected document.

6. Check that all required fields have been captured correctly, and if any warnings or error messages are displayed in the **Comments** section at the bottom. If something is wrong or missing, correct this manually. For example, to capture any unidentified field captions or values manually, see [Capturing header fields in a document](@DC-110).

   >[!NOTE]
   >More often than not, capturing amounts isn't necessary because your prices and other amount-related values should come directly from Business Central. However, you can configure Document Capture to automatically transfer captured values to the sales order line created – overwriting the price listed on the related item card. This process also works for account types that lack prices.
   >
   >1. On the document card, click the three dots (...) next to a value under the **Unit Price** column on the **Lines** FastTab.
   >2. On the **Template Field Card** for the line field **Unit Price**, go to the **Field in Sales Line** field under the **Transfer Value to…** section and select the **Unit Price** option.

7. **Optional**: If needed, you can also perform manual or AI line recognition on sales orders. For more information, see [Capturing line fields in a document (line recognition)](@DC-147).

8. On the action bar, click **Home** > **Register** to register the new sales order.

The sales order is then created as a business unit in Business Central, ready for further processing.

## Related information

[Basic concepts in Document Capture](@DC-83)  
[Working with document categories](@DC-78)