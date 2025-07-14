---
title: Adyen
date: 03-02-2023
description: Describes how to set up Adyen as a PSP.
id: PM-321
lang: en
---

# Adyen

> [!IMPORTANT]
>
> Available for version 5.3.0.0 or higher.

Adyen is an online payment platform that facilitates payments between individuals and businesses. With Payment Management, you can use the PSP integration feature to send payment data between Adyen and Microsoft Dynamics 365 Business Central.



## File Name

The Adyen Settlement details report

## File Format

CSV

For Continia to convert the CSV file correctly, it is important not to change the first 23 fields in the file. This means that you must keep those fields listed in the in the same column and row. For more details, see the [Settlement details report](https://docs.adyen.com/reporting/settlement-reconciliation/transaction-level/settlement-details-report#standard-columns) article on Adyen Docs.

## External Payment Reference Field

PSP Reference

> [!NOTE]
>
> By default, when the PSP Reference field contains a value and the type field is not set to *PaymentCost*, the default External Payment Reference value is taken from the PSP Reference field.

## Default Rules

To be able to separate fees and other charges from Adyen invoices, by default, the Adyen PSP Rule Template applies the following rules:

| Rule name         | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| Commission (NC)   | The commission fee that was withheld by the acquirer.        |
| Markup (NC)       | The fee charged by the acquiring bank.                       |
| Scheme Fees (NC)  | The fee charged by Visa/MC.                                  |
| Interchange (NC)  | The fee charged by the issuing bank.                         |
| Fee               | The transaction fee charged by Ayden.                        |
| PaymentCost       | Used only for Klarna payments, ELO payments, MasterCard personal payments, and Visa/Mastercard disputes. |
| MiscCosts         | Costs from externally settled payments that could not be matched with a specific transaction. |
| DepositCorrection | Withheld funds from the account due to a change in the required security deposit. |
| InvoiceDeduction  | Payment processing invoice that is credited/deducted from the account. |
| MatchedStatement  | Wire transfer from merchant booked in the account.           |
| ManualCorrected   | Manual adjustment by Ayden.                                  |
| Balancetransfer   | Balance transfer to or from subsequent payout batches in order to process negative payable/capture balances or for batches that could not have been paid out. |

> [!WARNING]
>
> We recommend not to edit the default Rule template as this template is created and maintained by Continia, and your changes will be overwritten during updates. If you want to add rules that aren't provided by Continia, you can add these to the PSP agreement.



## Related information

[Importing PSP payments](@PM-299)

[Adding a Payment Service Provider](@PM-298)

