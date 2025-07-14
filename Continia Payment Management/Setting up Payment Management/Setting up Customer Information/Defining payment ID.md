---
title: Defining payment ID
description: How to define payment ID 
date: 11-06-2021
id: PM-92
lang: en
---

# Defining the Payment ID mask

A payment ID serves as a distinct identifier for customer payments. It allows you to associate a payment transaction with a specific sales invoice in your system. For Payment Management to correctly interpret the payment ID information, you need to establish a payment ID mask.

> [!TIP]
>
> If you are unsure about the length of the payment ID, you can import a FIK customer payment and count the characters in the payment reference to determine the appropriate length.



## To define a payment ID mask on bank accounts

You can define the payment ID mask directly on a bank account. If no payment ID mask is defined on the bank account, the [default Payment ID mask](#to-define-a-default-payment-id-mask) specified on the **Payment Management Setup** page will be used when managing the imported customer payments. 

To define a payment ID mask on a bank account:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Accounts**, then select the related link. 
1. Open the bank account card for which you want to define a payment ID mask, and on that card, navigate to the **Payment Receipt Import** FastTab, and in the **Payment ID Mask** field, specify the mask. The mask can be generated using the following characters: 
   * C=Customer no. 
   * D=Document no. 
   * M=Modulus check digit
   * T=Document type
   * X=Ignore



## To define a default payment ID mask

You can set up a default payment ID mask to catch all customer payments that don't have a mask defined for the bank account.

To define the default payment ID mask:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Management Setup**, then select the related link. This opens the Payment Management Setup page.

1. On the setup page, on the **Payment Receipt Import** FastTab, in the **Default Payment ID Mask** field, define the default mask which will be used to interpret the payments imported to the company bank accounts. You can generate the mask using the following characters: C=Customer no. D=Document no. M=Modulus check digit. T=Document type. X=Ignore. 

1. On the **Payment Receipt Import** FastTab, go to the **Modulus Type** field to select the appropriate modulus type for your payment processing needs.

   



## See Also

[Using the OCR Reference Interface](@PM-10)
