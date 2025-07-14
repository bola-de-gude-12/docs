---
title: Switching posting types in Continia Finance
date: 24-10-2024
description: How to switch the posting type of an account or item in Continia Finance.
id: CF-124
lang: en
---

# Switching Posting Types

This article describes the **Switch Posting Type Sales/Purchase** feature, which lets you post sales within a purchasing document using the sales posting type – and within a sales document using the purchasing posting type.

Switching a posting type is useful when a sale to a customer, for example, involves a refundable deposit. This deposit could be related to a pallet on which the goods sold are delivered, consignment stock, reusable packaging, etc.

## To switch the posting type of a G/L account or item
The steps below cover the process to enable the posting type switching of a G/L account, but it's also possible to enable it for an item.

To switch the posting setup of a G/L account:

1. Choose the {{search}} icon, enter **VAT Posting Setup**, and then choose the related link.

2. In the action bar, select **+New** to create a VAT posting setup.

3. Populate the fields on the **General**, **Sales**, and **Purchases** FastTabs according to your needs.

4. On the **Continia Finance** FastTab, enter the desired dates for the **Valid From** and **Valid Until** fields – if needed. Then, enable the **Switch Posting Type Sales/Purchase** setting.

   >[!TIP]
   >If you already have a VAT posting group set up for the switching, select the corresponding checkbox under the **Switch Posting Type Sales/Purch.** column on the **VAT Posting Setup** page.

6. Choose the {{search}} icon, enter **Chart of Accounts**, and then choose the related link.

7. Select the G/L account to be used for the switching. Alternatively, you can create an account for this purpose.

   >[!NOTE]
   >Make sure that the selected G/L account or item has the **VAT Prod. Posting Group** field set to the posting group for which you enabled the **Switch Posting Type Sales/Purch.** setting.

## To use a switched G/L account or item in a transaction
The steps below cover the process to use a switched G/L account in a transaction, but it's also possible to use an item.

With the G/L account configured accordingly, you can now make use of it in appropriate transactions. This article uses a sales invoice as an example.

1. Choose the {{search}} icon, enter **Customers**, and then choose the related link.
2. In the action bar, select **New Document** > **Sales Invoice**.
3. Populate the required fields accordingly, including the information related to the sold item(s).
4. In the **Lines** section, add a line. Select G/L account under **Type** and, under **No.**, select the account configured in the section above.
5. To verify the setup, select **Post** >  **Preview Posting**. Two separate VAT entries related to the sales invoice should be visible – one for the sale and one for the purchase.

   >[!NOTE]
   >The **Line Amount Excl. VAT** field must have a negative value for the line item related to the switched G/L account, otherwise it's calculated incorrectly. If the value under the **Quantity** field is negative, the **Line Amount Excl. VAT** is automatically converted to negative too.