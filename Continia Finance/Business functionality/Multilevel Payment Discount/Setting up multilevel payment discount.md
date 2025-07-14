---
title: Setting up Multi-level Payment Discount in Continia Finance
date: 15-10-2024
description: Learn more about setting up different levels of discounts.
id: CF-103
lang: en
---

# Setting up Multi-level Payment Discount

The Multi-level Payment Discount module in Business Central enables you to create payment terms for sales and purchase documents with discounts based on different payment dates. This article describes how to activate and set up the module.

To set up the Multi-level Payment Discount module using the assisted setup:

1. Choose the {{search}} icon, enter **Assisted Setup**, and select the related link.
2. In the **Continia Finance** section, select **Set up Multi-Level Payment Discount**.
3. The wizard helps you define at least one payment term. For a description of the fields shown here, see the table below.

To set up the Multi-level Payment Discount module manually:

1. Choose the {{search}} icon, enter **Multi-Level Pmt. Discount Setup**, and select the related link.

2. On the **Multi-level Pmt. Discount Setup** page, turn on the **Enable Multi-Level Pmt. Discount Setup** setting to enable the module. 

3. In the action bar, select **Payment Terms** to specify the default payment discount settings.

4. On the **Payment Terms** page, in the action bar, select **New** to add a payment term.

5. Enter information for the following fields:

   | Field                         | Description                                                  |
   | ----------------------------- | ------------------------------------------------------------ |
   | Code                          | Specifies a code to identify the payment terms. E.g.: 45D(15D). |
   | Due Date Calculation          | When you create an invoice with this payment term code, this formula is used to calculate the due date. E.g.: 45D. |
   | Discount Date Calculation     | Specifies the formula to calculate the payment date when payment terms include a discount. You can define up to four additional discount date calculations, besides the default one. E.g.: 5D, 10D, 15D, and 30D. |
   | Discount %                    | Specifies the payment discount percentage you want to grant for a specific level. You can define up to four additional discount levels, besides the default level. E.g.: 10, 8, 6, and 4. |
   | Calc. Pmt. Disc. on Cr. Memos | Select this checkbox to ensure that payment terms, including payment discount, cash discount, cash discount date, and due date are taken into account in credit memos. |
   | Description                   | Describes the payment terms.                                 |
   | Value Date Calculation        | Specifies a formula for determining the value date. If you enter a value date formula, the system calculates the due date and payment discount data by adding the value date formula to the document date. |

6. Your payment term with a multi-level discount is now ready to be used.

<style>
 .content table tr td:nth-child(1) {
 width: 230px;
 }
 .content table tr td:nth-child(2) {
 width: 570px;
 }
</style>
