---
title: Mollie
date: 03-02-2023
description: Describes how to set up Mollie as a PSP.
id: PM-322
lang: en
---

# Mollie

> [!IMPORTANT]
>
> Available for version 5.3.0.0 or higher.

Mollie is an online payment platform that facilitates payments between individuals and businesses. With Payment Management, you can use the PSP integration feature to send payment data between Mollie and Microsoft Dynamics 365 Business Central.



## File Name

mollie [YYYY-MM].csv



## File Format

CSV

## External Payment Reference Field

ID

> [!NOTE]
>
> If the ID field contains a value, the External Payment Reference value is taken from the ID field. However, if the ID field value starts with "MOL," it is excluded from reconciliation, and the G/L account specified in the rules is applied instead.

## Default Rules

To be able to separate fees and other charges from Mollie invoices, by default, the Mollie PSP Rule Template applies the following rules:

| Rule name             | Description                                   |
| --------------------- | --------------------------------------------- |
| MOL                   | The invoice fees.                             |
| Transaction Type: FEE | The transaction fees, VAT,  and Reservations. |

> [!WARNING]
>
> We recommend not to edit the default Rule template as this template is created and maintained by Continia, and your changes will be overwritten during updates. If you want to add rules that aren't provided by Continia, you can add these to the PSP agreement.



## Related information

[Importing PSP payments](@PM-299)

[Adding a Payment Service Provider](@PM-298)



