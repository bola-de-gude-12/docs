---
title: Setting up cost types in Continia Banking
description: How to define cost type codes for payment methods and vendors
date: 22-04-2025
id: CB-237
lang: en
---

# Setting up cost types

When managing payments that include fees, it's essential to determine who will bear the costs associated with payment processing or service fees. This can be controlled using cost type codes. By specifying these codes, you can clearly define whether the customer or vendor will be responsible for these charges. The cost type code can be set up either [on the payment method](#to-set-the-cost-type-code-on-a-payment-method) or directly [on the vendor](#to-set-the-cost-type-on-a-vendor)  in Business Central. If a cost type is defined on the vendor, it overrides the one on the payment method. If the vendor’s cost type is left blank, the system will fall back to using the payment method's setting. On a purchase order, changing the vendor number will update the cost type according to the vendor’s settings. Therefore, if you define the cost type on the payment method, you can leave it blank on the vendor—unless you want to explicitly override it.

Once set up, when suggesting vendor payments, and selecting a payment method filter, the system first checks the vendor card for a defined cost type. If none is set, it then uses the cost type from the payment method. On the payment card or payment journal, you cannot override the cost type defined on the vendor card. If you attempt to manually change the cost type and then modify the payment method, the system will reset the cost type - reapplying the one from the vendor or payment method, depending on availability.

## Available cost types

Continia Banking comes with the following cost type codes:

| <span style="white-space: nowrap;">Cost type code</span> | Description |
| --- | --- |
| *Blank* | No cost type handling is applied. |
| Shared | Fees are split between you and the vendor. |
| Creditor | All fees are paid by the vendor. |
| Debtor | All fees are paid by you as the customer.            |
| Service level                                            | Fees are allocated according to pre-agreed service level arrangements. |



## To set the cost type code on a payment method

Define the cost type code on the payment method to standardize fee allocation across all transactions using that method. This ensures consistent cost handling, automatically applying the code whenever the payment method is used.

1. Search ({{search}}) for and select **Payment Methods**.
1. In the list of payment methods, select the payment method for which you want to define **Cost Type Code**.
1. In the **Cost Type Code** column, select the cost type code that should be applied per default when using the given payment method.

The cost type code has now been defined for the payment method and will per default be used for payments with this payment method. 



## To set the cost type code on a vendor

You can define a default cost type code for each vendor, which overrides the payment method setting if both are specified. Setting the cost type on the vendor record allows for customized fee allocation according to individual vendor agreements.

1. Search ({{search}}) for and select **Vendors**.
1. In the list of vendors, navigate to the vendor for which you want to define the cost type and open the vendor card.
1. On the vendor card, on the **Payments** FastTab, in the **Cost Type** field select the cost type code that should be applied per default when using the given payment method.

The cost type code has now been defined for the vendor and will per default be used when paying the vendor.

