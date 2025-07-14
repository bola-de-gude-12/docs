---
title: bol.com
date: 23-11-2022
description: Describes how to set up bol.com as a PSP.
id: PM-302
lang: en
---

# bol.com

> [!IMPORTANT]
>
> Available for version 5.2.0.0 or higher.

bol.com is currently the biggest marketplace for a wide range of products in the Netherlands and Belgium. With Payment Management, you can use the PSP integration feature to send payment data between bol.com and Microsoft Dynamics 365 Business Central.



## File Name

Detailspecificatie factuur

> [!IMPORTANT]
>
> Because the bol.com settlement file doesn't indicate currency, you must enter EUR in the Default Currency Code field in the PSP Agreement. See the [Adding a Payment Service Provider](@PM-298) article for more information.

## File Format

Excel

## External Payment Reference Field

Bestelnummer

> [!NOTE] By default, the value from the Excel F column ”Bestelnummer” is taken. However, if this field is empty, the G/L account selected as the type must be used.

## Default Rules

To be able to separate fees and other charges from bol.com invoices, by default, the bol.com PSP Rule Template applies the following rules:

| Rule name                            | Description                                                  |
| ------------------------------------ | ------------------------------------------------------------ |
| Pick & pack kosten                   | The pick and pack fees cover picking the item from storage and packaging it for shipment. |
| Correctie pick & pack kosten         | The correction applied to the previously charged pick and pack fees. For example, if a shipment is lost. |
| Verzendkosten                        | The shipping costs.                                          |
| Correctie verzendkosten              | The correction amount that is applied to the previously charged shipping costs. For example, if a shipment is lost. |
| Commissie                            | For each item you sell on bol.com, you pay a commission, consisting of a fixed amount and a percentage of the selling price. |
| Correctie commissie                  | The correction applied to the previously charged commission. For example, if a customer returns an item. |
| Bijdrage aan retourzegel(s)          | The fee charged for return labels used by a customer to send a return shipment to you. |
| Voorraadkosten                       | The fee charged (costs per day and per EAN) for storing items you sell at a bol.com distribution center. |
| Onverkoopbare voorraadkosten         | The fee charged for stock located in the bol.com distribution center that can't be sold. |
| Compensatie zoekgeraakte artikel(en) | The fee paid for product that got lost.                      |
| Correctie(s)                         | A (manual) correction that does not belong to an invoice line. |

>  [!WARNING]
>
> We recommend not to edit the default Rule template as this template is created and maintained by Continia, and your changes will be overwritten during updates. If you want to add rules that aren't provided by Continia, you can add these to the PSP agreement.



## Related information

[Importing PSP payments](@PM-299)
[Adding a Payment Service Provider Agreement](@PM-298)

