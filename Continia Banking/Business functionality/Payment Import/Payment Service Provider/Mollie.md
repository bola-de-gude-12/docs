---
title: Mollie
date: 06-02-2025
description: Describes how to set up Mollie as a Payment Service Provider in Continia Banking.
id: CB-176
lang: en
---

# Mollie

> [!IMPORTANT]
>
> Available for version 26.0.0.0 or higher.

Mollie is an online payment platform that facilitates payments between individuals and businesses. With Continia Banking, you can use the PSP integration feature to send payment data between Mollie and Microsoft Dynamics 365 Business Central.



## File name

mollie [YYYY-MM].csv



## File format

CSV

## External payment reference field

ID

## Default rules

To be able to separate fees and other charges from Mollie invoices, by default, the Mollie PSP Rule Template applies the following rules:

| Rule name             | Description                                   |
| --------------------- | --------------------------------------------- |
| MOL                   | The invoice fees.                             |
| Transaction Type: FEE | The transaction fees, VAT,  and Reservations. |

> [!WARNING]
>
> We recommend not to edit the default Rule template as this template is created and maintained by Continia, and your changes will be overwritten during updates. If you want to add rules that aren't provided by Continia, you can add these to the PSP agreement.





