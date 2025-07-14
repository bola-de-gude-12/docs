---
title: Worldline
date: 03-02-2023
description: Describes how to set up Worldline as a PSP.
id: PM-337
lang: en
---

# Worldline

> [!IMPORTANT]
>
> Available for version 6.2.0.0 or higher.

Worldline is a payment and transactional services company. With Payment Management, you can use the PSP integration feature to send payment data between Worldline and Microsoft Dynamics 365 Business Central.



## File Name

The filename varies.

## File Format

Excel

> [!IMPORTANT]
>
> After you [select the Worldline file for import](@PM-299), in the **Name/Value** dialog box, select **4 Payout Details** and select **Ok**. Continia then converts the file and sends the data to Continia online, making it possible to import the data to the Cash Receipt Journal in Microsoft Dynamics 365 Business Central.



## External Payment Reference Field

TRANSACTION REF

> [!NOTE]
>
> By default, the value of the TRANSACTION REF field in the payout details G column is taken.

## Default Rules

To be able to separate fees and other charges from Worldline invoices, by default, the Worldline PSP Rule Template applies the following rules:

| Rule name       | Description                               |
| --------------- | ----------------------------------------- |
| TRANSACTION FEE | The transaction fee charged by Worldline. |

> [!WARNING]
>
> We recommend not to edit the default Rule template as this template is created and maintained by Continia, and your changes will be overwritten during updates. If you want to add rules that aren't provided by Continia, you can add these to the PSP agreement.



## Related information

[Importing PSP payments](@PM-299)

[Adding a Payment Service Provider](@PM-298)



