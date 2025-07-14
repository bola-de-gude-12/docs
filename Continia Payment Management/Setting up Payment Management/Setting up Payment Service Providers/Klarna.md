---
title: Klarna
date: 03-02-2023
description: Describes how to set up Klarna as a PSP.
id: PM-309
lang: en
---

# Klarna

> [!IMPORTANT]
>
> Available for version 5.3.0.0 or higher.

Klarna is a 'buy now, pay later' service founded in Sweden in 2005. With Payment Management, you can use the PSP integration feature to send payment data between Klarna and Microsoft Dynamics 365 Business Central.

## File Name

The [Klarna settlement report](https://docs.klarna.com/settlement-reports/#fields-description-detailed-type).

## File Format

CSV



For Continia to convert the CSV file correctly, it is important not to change the first ten fields in the file. This means that you must keep the following fields in the same column and row:

* type

* capture_date

* sale_date

* order_id

* short_order_id

* capture_id

* merchant_reference1

* merchant_reference2

* amount

* posting_currency

## External Payment Reference Field

order_id

## Default Rules

To be able to separate fees and other charges from Klarna invoices, by default, the Klarna PSP Rule Template applies the following rules:

| Rule name                    | Description                                                  |
| ---------------------------- | ------------------------------------------------------------ |
| FEE                          | Service fee charged by Klarna for the related sale transaction. |
| RETURN                       | Refund that is registered to indicate that the customer has returned the goods. |
| COMMISSION                   | Percentage commission paid by Klarna.                        |
| CORRECTION                   | Manual corrections.                                          |
| HOLDBACK                     | The amount is used as a rolling reserve, which covers for future refunds or other security reasons. |
| RELEASE                      | The amount reduces the rolling reserve (the opposite of a holdback). The credit Klarna set apart for a merchant gets released and paid back to the merchant. |
| CREDIT                       | Miscellaneous credit that is described in the field detailed_type. |
| CHARGE                       | Miscellaneous charge that is described in the field detailed_type. |
| REVERSAL_MERCHANT_PROTECTION | Net-amount of the order value (incl. consumer VAT), credited by Klarna for merchant protection. The amount reduces the total_reversal_amount. |

> [!WARNING]
>
> We recommend not to edit the default Rule template as this template is created and maintained by Continia, and your changes will be overwritten during updates. If you want to add rules that aren't provided by Continia, you can add these to the PSP agreement.



## Related information

[Importing PSP payments](@PM-299)

[Adding a Payment Service Provider](@PM-298)

