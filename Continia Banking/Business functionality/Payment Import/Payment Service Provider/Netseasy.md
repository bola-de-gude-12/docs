---
title: NetsEasy
date: 06-02-2025
description: Describes how to set up NetsEasy as a Payment Service Provider in Continia Banking.
id: CB-179
lang: en
---

# NetsEasy

NetsEasy is a payment processing platform that facilitates secure and convenient payment acceptance for businesses. With Continia Banking, you can use the PSP integration feature to send payment data between NetsEasy and Microsoft Dynamics 365 Business Central.



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







