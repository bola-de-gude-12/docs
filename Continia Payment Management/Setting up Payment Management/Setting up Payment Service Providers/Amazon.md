---
title: Amazon
date: 23-11-2022
description: Describes how to set up Amazon as a PSP.
id: PM-301
lang: en
---

# Amazon

> [!IMPORTANT]
>
> Available for version 5.2.0.0 or higher

Selling on Amazon is an easy way to reach millions of potential buyers. With Payment Management, you can use the PSP integration feature to send payment data between Amazon and Microsoft Dynamics 365 Business Central.



## File Name

The Amazon settlement report. The name of the file is different for every marketplace.

## File Format

XML

## External Payment Reference Field

OrderID 

## Default Rules

To be able to separate fees and other charges from Amazon invoices, by default, the Amazon PSP Rule Template applies the following rules:

| Rule name                                              | Description                                                  |
| ------------------------------------------------------ | ------------------------------------------------------------ |
| Tax                                                    | Amount of sales tax paid as a part of the transaction.       |
| Shipping                                               | The shipping costs.                                          |
| ShippingTax                                            | The VAT portion of the shipping cost credit.                 |
| Commission<br/>                                        | The commission fee is based on the product category.         |
| RefundCommission<br/>                                  | When Amazon reimburses you for a customer refund, Amazon determines the amount of the order-related fees credited back to you and the amount of such fees that Amazon retains, based on the product line of the item and the amount of the order. |
| FBAPerUnitFulfillmentFee<br/>                          | Fee charged per unit sold for items that Amazon fulfills.    |
| ShippingChargeback<br/>                                | If Amazon takes care of the shipping (FBA), they withdraw the shipping cost fee the customer paid you. |
| CouponRedemptionFee<br/>                               | The fee is charged when a coupon on the item is redeemed.    |
| AdvertisingTransactionDetails<br/>                     | The fee for advertising on Amazon.                           |
| Inbound Transportation Fee<br/>                        | The inbound transportation fee is the payment for shipping your products to FBA warehouses using Amazon’s partnered shipping. |
| Inbound Transportation Program Fee<br/>                | Fee for the FBA inbound transport program (applies if you send the goods to the shipping center using an Amazon transport partner) |
| Transaction Type: STORAGE_RENEWAL_BILLING<br/>         | Fee for long-term storage.                                   |
| Transaction Type: STORAGE_FEE<br/>                     | This is the fee charged for storing your items in the Amazon Fulfillment Center. |
| Transaction Type: REVERSAL_REIMBURSEMENT<br/>          | Refunds with shipping by Amazon. For example: if the customer wants to return a product, customer service will reimburse the customer first and collects the amount from you. However, you will get this money back if the customer does not return the item. |
| Transaction Type: PREVIOUS_RESERVE_AMOUNT_BALANCE<br/> | The amount withheld from your previous settlement and released on your current one. |
| Transaction Type: COMPENSATED_CLAWBACK<br/>            | FBA fee charged for incorrect reimbursements.                |
| Transaction Type: CURRENT_RESERVE_AMOUNT<br/>          | The amount withheld from orders until seven days after the latest estimated delivery date. |
| Transaction Type: COMMINGLING_VAT                      | VAT-related fee for acquiring a product from another FBA seller. |

> [!WARNING]
>
> We recommend not to edit the default Rule template as this template is created and maintained by Continia, and your changes will be overwritten during updates. If you want to add rules to that aren't provided by Continia, you can add these to the PSP agreement.



## Related information

[Importing PSP payments](@PM-299)

[Adding a Payment Service Provider](@PM-298)





