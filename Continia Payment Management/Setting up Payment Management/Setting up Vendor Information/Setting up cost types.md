---
title: Setting up cost types
description: How to define cost type codes for payment methods and vendors
date: 11-03-2021
id: PM-44
lang: en
---

# Setting up Cost Types

When making a payment that involves a fee, such as SEPA payments, the cost type code can define who should pay the fee. The cost type code can be defined on the payment method or directly on the vendor. 
> [!NOTE] 
>
> All payment methods to be used for foreign payments are, by default set up to have the cost type code **Shared**, as this is the most commonly used cost type.

Payment Management comes with the following cost type codes:

| <span style="white-space: nowrap;">Cost type code</span> | Description |
| --- | --- |
| *Blank* | If no cost type code is selected, costs and fees will not be considered for the purchase. |
| **Shared** | The costs will be shared between you and the vendor. |
| **Vendor** | All costs will be paid by the vendor. |
| **Customer**   | All costs will be paid by you as the customer. |
| **Swap Costs** | All costs will be exchanged between vendor and customer. This means that the vendor pays your costs, and you pay the vendor's costs. This cost type code is rarely used. |




## To set up cost type code on a payment method

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Methods**, then select the related link.
1. In the list of payment methods, select the payment method for which you want to define **Cost Type Code**.
1. In the **Cost Type Code** column, select the cost type code that should be applied per default when using the given payment method.

The cost type code has now been defined for the payment method and will per default be used for payments with this payment method.



## To set up cost type code on a vendor

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Vendors**, then select the related link.
1. In the list of vendors, navigate to the vendor for which you want to define **Cost Type Code**.
1. Open the relevant vendor card.
1. On the vendor card, on the **Payments** FastTab, in the **Cost Type Code** field select the cost type code that should be applied per default when using the given payment method.

The cost type code has now been defined for the vendor and will per default be used when paying the vendor.

