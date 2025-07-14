---
title: Worldline
date: 25-03-20225
description: Describes how to set up Worldline as a Payment Service Provider in Continia Banking.
id: CB-180
lang: en
---

# Worldline

> [!IMPORTANT]
>
> Available for version 26.0.0.0 or higher.

Worldline is a payment and transactional services company. With Continia Banking, you can use the PSP integration feature to send payment data between Worldline and Microsoft Dynamics 365 Business Central.

## File Name

The filename varies.

## File Format

Excel

> [!IMPORTANT]
>
> After you [select the Worldline file for import](@CB-209), in the **Name/Value** dialog box, select **4 Payout Details** and select **Ok**. Continia then converts the file and sends the data to Continia online, making it possible to import the data to the Cash Receipt Journal in Microsoft Dynamics 365 Business Central.



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



