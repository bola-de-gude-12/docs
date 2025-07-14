---
title: PayPal
date: 03-02-2023
description: Describes how to set up PayPal as a PSP.
id: PM-307
lang: en
---

# PayPal

> [!IMPORTANT]
>
> Available for version 5.3.0.0 or higher.

PayPal is an online payment platform that facilitates payments between individuals and businesses. With Payment Management, you can use the PSP integration feature to send payment data between PayPal and Microsoft Dynamics 365 Business Central.



## File Name

The Paypal [monthly statement report](https://developer.paypal.com/docs/reports/online-reports/monthly-statement/). 



## File Format

CSV

For Continia to convert the CSV file correctly, it is important not to change the first ten fields in the file. This means that you must keep the following fields in the same column and row:

* Date
* Time
* Time Zone
* Description
* Currency
* Gross
* Fee
* Net
* Balance
* Transaction ID
* From Email Address
* Name
* Bank Name
* Bank Account
* Shipping and Handling Amount
* Sales Tax
* Invoice ID
* Reference Txn ID

## External Payment Reference Field

Invoice ID

> [!NOTE]
>
> If the Invoice ID has a value, the default External Payment Reference value is taken from that field. However, if the Invoice ID field is empty, the G/L account specified in the rules is applied instead.

## Default Rules

To be able to separate fees and other charges from PayPal invoices, by default, the PayPal PSP Rule Template applies the following rules:

| Rule name                    | Description                                                  |
| ---------------------------- | ------------------------------------------------------------ |
| Fee                          | Amount of fees associated with the transaction.              |
| Shipping and handling amount | Amount paid for shipping and handling as a part of the transaction. |
| Sales tax                    | Amount of sales tax paid as a part of the transaction.       |
| Transaction type: FEE        | For transactions without an invoice ID.                      |

> [!WARNING]
>
> We recommend not to edit the default Rule template as this template is created and maintained by Continia, and your changes will be overwritten during updates. If you want to add rules that aren't provided by Continia, you can add these to the PSP agreement.



## Related information

[Importing PSP payments](@PM-299)

[Adding a Payment Service Provider](@PM-298)



