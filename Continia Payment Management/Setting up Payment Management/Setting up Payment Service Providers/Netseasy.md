---
title: NetsEasy
date: 03-02-2023
description: Describes how to set up NetsEasy as a PSP.
id: PM-336
lang: en
---

# NetsEasy

> [!IMPORTANT]
>
> Available for version 7.0.0.0 or higher.

NetsEasy is a payment processing platform that facilitates secure and convenient payment acceptance for businesses. With Payment Management, you can use the PSP integration feature to send payment data between NetsEasy and Microsoft Dynamics 365 Business Central.



## File Name

PayoutDetails.csv



## File Format

CSV



## External Payment Reference Field

Order ID

## Default Rules

To be able to separate fees and other charges from NetsEasy invoices, by default, the NetsEasy PSP Rule Template applies the following rules:

| Rule name   | Description                                                  |
| ----------- | ------------------------------------------------------------ |
| PAYMENT FEE | Any general fee associated with the Nets MyNets payment service. It could include transaction fees, processing fees, or other charges applicable to the payment transactions. |

> [!WARNING]
>
> We recommend not to edit the default Rule template as this template is created and maintained by Continia, and your changes will be overwritten during updates. If you want to add rules that aren't provided by Continia, you can add these to the PSP agreement.



## Related information

[Importing PSP payments](@PM-299)

[Adding a Payment Service Provider](@PM-298)



