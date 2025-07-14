---
title: Expense Management Automatic Creation of Digital Vouchers
date: 02-04-2024
description:
id: EM-214
lang: en
---

# Automatic Creation of Digital Vouchers

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Automatic creation of digital vouchers | {{checkmark}} Mar 2024 | {{checkmark}} Apr 2024 |

## Business value

In an increasing number of countries, organizations are required to provide documentation for all accounting entries by storing supporting electronic documents – known as *digital vouchers* – such as invoices and other business documents. For example, the new Danish Bookkeeping Act effectively requires Danish organizations that use Microsoft Dynamics 365 Business Central to have digital vouchers generated and transferred to **Incoming Documents** for storage.

Microsofts [enforced digital voucher functionality](https://learn.microsoft.com/en-us/dynamics365/business-central/across-how-setup-digital-vouchers) is very useful for this purpose, and this new Continia Expense Management feature supports and extends that functionality. With the feature, Expense Management can automatically create digital vouchers for incoming documents, so you don't have to manually attach files yourself.

## Feature details

A digital voucher is an electronic document that supports financial transactions. The feature ensures that digital vouchers are automatically created based on Expense Management files and then transferred to the **Incoming Documents** page for storage when you register a document. When you post a mileage or per diem, a tax report extract will be generated. This serves as a digital voucher for these documents.

For more information, see [Automatic Creation of Digital Vouchers](@EM-223).