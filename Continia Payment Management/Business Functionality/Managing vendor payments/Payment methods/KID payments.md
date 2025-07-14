---
title: KID Payments
description: Information on how to pay vendors with the payment method KID
date: 29-10-2021
id: PM-204
lang: en
---

# KID Payments

A KID number (Kunde ID, customer identification number) is a payment reference used for Norwegian account-to-account payments to identify the customer or vendor and the invoice paid. The length of a KID number can vary from 2-25 digits. Standard BC uses modulus 10 to calculate the last part of the KID number. 

The banks in Norway offer to store the KID number for each registered transaction (as additional information to name, address, and account number) to make it easier for companies to keep track of payments. 

> [!IMPORTANT] 
>
> The bank must approve an agreement about using the payment method KID before sending an invoice with KID. Otherwise, the online bank will reject the KID number and cancel the transaction.

## The general setup

When you import an account statement, Payment Management tries to match according to the setup in Sales & Receivables.

To view the default setup:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Sales & Receivables**, then select the related link. 
2. On the **Documents** FastTab, navigate to the **KID Setup** field. This field determines how to structure the KID reference. The options are:
   * Document No.
   * Document No. + Customer No.
   * Customer No. + Document No.
   * Document Type + Document No.
   * Document No + Document Type

3. Navigate to the **Document No. length** field to assign the default length for the document number in the KID number. For example, if you enter 10, the document number will be prefixed with zeros if the document number is not long enough. 
4. Navigate to the **Customer No. length** field to assign the default length to the customer number in the KID number.

You can also refer to the Payment Management mask setup that is used for matching OCR references when matching payment receipts. For more details, refer to the [Defining the Payment ID](@PM-92) article.



## To pay vendors with KID

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Vendors**, then select the related link. 
1. Open the relevant vendor card.
1. On the vendor card, navigate to the FastTab **Payments**.
1. In the field **Payment Method Code**, choose the payment method **KID** (KID Payment).
1. Fill in other relevant payment information such as **Preferred Bank Account Code** and **Balance Account No.**
   > [!NOTE]
   >
   > The vendor bank account must have been set up with **Bank Account No.**, **SWIFT Code**, and **IBAN**.

