---
title: Handling freight amounts when matching to a purchase order in Document Capture
date: 15-10-2025
description: How to configure and capture freight amounts when matching purchase invoices to purchase orders.
id: DC-230
lang: en
---

# Handling freight amounts when matching to a purchase order

When matching a purchase invoice to a purchase order in Continia Document Capture, it's possible to capture a freight amount from the document that is not in the original purchase order – so the total invoice amount can be paid. This is supported in two ways:

* If matching and updating the purchase order, Document Capture can add a freight line to the purchase order without having to reopen and reapprove the purchase order.
* If matching the order and creating the invoice, the freight charge isn't added to the purchase order – but it can be added as a line on the registered purchase invoice.

>[!NOTE]
>If you're capturing invoices without matching to purchase orders, see [Automatic assignment of item charges](@DC-137).

## To configure the freight amount

If you've just added the **Freight Amount** field to the desired template, the field is configured by default – allowing for the remaining part of this article. If the **Freight Amount** was already present in your template:

1. Search ({{search}}) for and select **Document Categories**.
2. Click the code of the relevant document category – in this case **PURCHASE** – to open the document journal.
3. Open the desired document by clicking its number under the **No.** column.
4. On the document card, click the three dots (...) by the **Freight Amount** field to open the template field card.
5. Under the **Purchase** FastTab, set the **Transfer Amount to Document** field to **Always**.
6. If the freight amount is included in the amount excluding. VAT, set the **Subtract from Amount Field (On Registration)** field to **AMOUNTEXCLVAT**. Otherwise, make sure the **Subtract from Amount Field (On Registration)** field is empty.

## To capture the freight amount

After [training Document Capture to locate the freight amount in the template](@DC-110):

1. On the document card, click **Template** > **Accounts for Amounts** on the action bar.
2. Set the **Account Type** of your **Freight Amount** field to either **G/L Account** or **Item**.
3. Configure the **Account No.** accordingly.
4. On the action bar, click **Template** > **Template Card**.
5. Configure the following settings:

   * **Invoice Reg. Step 1** - set it to **Match & Update Order** or **Match Order & Create Invoice**. If you select **Match Order & Create Invoice**, enable **Copy Matched Header Dimensions**.

   * **Invoice Reg. Step 2** - set it to **Release**.

   * **Autorun Perform Match** - set it to enabled.

   * **Match Invoice** - set it to either **Receipt Only** or **Order Only**.

6. **Optional**: to match on the line level, set the **Match Order No.**, **Match Item No.**, **Match Quantity**, and **Match Unit Cost** fields to **Yes - always**.
7. On the action bar, click **Home** > **Recognize Fields**. If there are no errors to address, click **Register**.

### If using Match & Update Order

If you set **Match & Update Order** as **Invoice Reg. Step 1**, the quantity to invoice is updated on the purchase order and an extra line for the freight is added to the order.

* If you created an item charge line, assign it, post the receipt for the item charge, and post the invoice quantities for the purchase order.
* If you created a G/L line, post the receipt for the G/L line and then post the invoice quantities for the purchase order.

### If using Match Order & Create Invoice

If you set **Match Order & Create Invoice** as **Invoice Reg. Step 1**, you should see the matched lines from the receipt and an extra line for the freight on the invoice.

* If you created an item charge line, assign it and then post the invoice.
* If you created a G/L line, post the invoice.

>[!NOTE]
>If the freight amount appears as a line item instead of a header field, use a rule in the related **No.** column to exclude the freight line. For example, enter <>Freight in the **Rule** field of the template field card **No.** if it contains the word 'Freight'. Also, set **Caption is Mandatory** to **True** in the **Freight Amount** field and blank out the **Stop Lines Recognition** field.
