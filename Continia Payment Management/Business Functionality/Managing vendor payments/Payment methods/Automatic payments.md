---
title: Automatic Payments
description: How to directly post purchase documents for automatic payment methods.
date: 22-11-2021
id: PM-297
lang: en
---

# Automatic Payments

Payment Management lets you post purchase documents for automatic payment methods directly to the vendor. This way, the payment entry is automatically posted on the vendor and the posted purchase document is balanced out. These payments will not display in the Payment Journal and are not addressed by reconciliation suggestions. To do this, you must add a payment method for direct payments and change some general settings on the vendor card. 

## To set up a payment method for direct payments

Continia lets you set up a payment method to deal with direct payments such as for example the PBS (Payment Business Service) functionality for directly debiting an account for the amount agreed upon between the customer, the supplier, and the bank.

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Methods**, then select the related link. 

2. On the **Payment Methods** page, from the Action menu, select **New** > **New**.

3. Enter information for the following fields:

   | Field                      | Description                                                  |
   | -------------------------- | ------------------------------------------------------------ |
   | Code                       | Enter a code to identify the payment method. For example, *PBS* if you want to add a method for Direct Debit payments in Denmark. |
   | Payment Method Description | Enter a description for the payment method.                  |
   | Balance Account Type       | Select the account type the entries are posted to.           |
   | Balance Account No.        | Select the bank account number that the balancing entry of a posted sales or purchase document is posted to. |

   

## To set up a vendor to allow direct posting

Once you installed a payment method for direct payments, you can set up a vendor to allow the direct posting of purchase documents.

1. Use the ![Search for page or report](/images/search_small.png) icon and search **Vendors**, then select the related link. This will open the list of vendors.

2. Access the vendor card for which you want to allow direct posting. On the vendor card, navigate to FastTab **Payments**, and in the **Payment Method Code** field, enter the payment method for direct payments. 

   > [!NOTE]
   >
   > As automatic payments are most likely not meant for international use, consider setting all posting fields to Domestic. To do so, navigate to the FastTab **Invoicing**, and in the **Posting** section, set all fields to Domestic.

   With this setup, purchase documents for the created payment method will be posted directly and will not appear in the payment journal. 

   > [!TIP] 
   > 
   > If you use the procedure described in this article, the due date will be the same as the posting date. If you want the posting date and due date to be different, you must select the payment method MANUAL when posting the purchase document. Then, the item is included in the payment journal but not in the file to the bank. When the journal is posted, the due date will be correct.
