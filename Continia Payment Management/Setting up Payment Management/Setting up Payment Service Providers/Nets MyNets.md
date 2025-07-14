---
title: Nets MyNets
date: 03-02-2023
description: Describes how to set up Nets MyNets as a PSP.
id: PM-338
lang: en
---

# Nets MyNets

> [!IMPORTANT]
>
> Available for version 5.3.0.0 or higher.

Nets MyNets is a payment provider that offers various payment solutions and services. With Payment Management, you can use the PSP integration feature to send payment data between Nets MyNets and Microsoft Dynamics 365 Business Central.



## File Name

Nets.csv

## File Format

CSV

## External Payment Reference Field

If the line is 100 – the BATCH-NUMBER field is used, in documentation, it’s written that it’s “The reference number comes from the terminal or payment module.”
If the line is 110 or 120 – the TRANSACTIONS-NO field is used, in documentation, it’s written that it’s “Physical or cardholder-activated merchant: the terminal sends transaction serial numbers for individual transactions. Internet or moto: order numbers from PSP.”

## Default Rules

To be able to separate fees and other charges from Nets MyNets invoices, by default, the Nets MyNets PSP Rule Template applies the following rules:

| Rule name        | Description                                                  |
| ---------------- | ------------------------------------------------------------ |
| FEE              | Any general fee associated with the Nets MyNets payment service. It could include transaction fees, processing fees, or other charges applicable to the payment transactions. |
| SUBSCRIPTION FEE | A recurring fee charged for the subscription or ongoing usage of the Nets MyNets payment service. |
| ADJUSTMENT       | A modification or correction made to a payment or transaction. It could be an update to the transaction amount, a refund, or any other modification to rectify an error or discrepancy. |
| CHARGEBACK       | A chargeback occurs when a customer disputes a payment transaction and requests a refund from their bank or credit card issuer. In response to a chargeback, the funds are reversed and deducted from the merchant's account. The chargeback process is initiated to resolve payment disputes between customers and merchants. |

> [!WARNING]
>
> We recommend not to edit the default Rule template as this template is created and maintained by Continia, and your changes will be overwritten during updates. If you want to add rules that aren't provided by Continia, you can add these to the PSP agreement.



## Related information

[Importing PSP payments](@PM-299)

[Adding a Payment Service Provider](@PM-298)



