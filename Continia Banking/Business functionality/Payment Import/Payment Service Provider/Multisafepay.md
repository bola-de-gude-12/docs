---
title: MultiSafepay
date: 04-03-2025
description: Describes how to set up MultiSafepay as a Payment Service Provider in Continia Banking.
id: CB-177
lang: en
---

# MultiSafepay

> [!IMPORTANT]
>
> Available for version 26.0.0.0 or higher.

MultiSafepay is a Netherlands-based payment platform offering end-to-end processing and acquisition services for European merchants. It provides online, in-person, and omnichannel payment solutions, helping businesses streamline their payment processes. With Continia Banking, you can use the PSP integration feature to send payment data between MultiSafepay and Microsoft Dynamics 365 Business Central.



## File Name

MultiSafePay Payout Report. The name of the file is different for every marketplace.



## File Format

Excel



## External Payment Reference Field

Order ID

## Default Rules

To be able to separate fees and other charges from MultiSafepay invoices, by default, the MultiSafepay PSP Rule Template applies the following rules:

| Rule name         | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| FEE               | Any general fee associated with the payment service, such as transaction fees, processing fees, or other applicable charges. |
| WALLET            | A rule for handling wallet-related transactions or balances. |
| MANUAL_CORRECTION | A rule for adjustments or corrections made manually to payment transactions. |
| AUTO-PAYOUT       | A rule for automatic payout processing.                      |

> [!WARNING]
>
> We recommend not to edit the default Rule template as this template is created and maintained by Continia, and your changes will be overwritten during updates. If you want to add rules that aren't provided by Continia, you can add these to the PSP agreement.





