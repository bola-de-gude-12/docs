---
title: Support for Multi-Entity Management (MEM) by Binary Stream Software
date: 26-11-2024
description:
id: DC-263
lang: en
---

# Support for Multi-Entity Management (MEM) by Binary Stream Software

| Feature | Public preview | General availability online |
| --- | :-: | :-: | 
| Support for multi-entity management (MEM) by Binary Stream Software | {{checkmark}} Mar 2024 | {{checkmark}} Apr 2024 |

## Business value

This feature will allow you to use Continia Document Capture alongside [Multi-Entity Management](https://binarystream.com/products/D365BC-MEM/) (MEM) from Binary Stream Software in Microsoft Dynamics 365 Business Central. The introduction of a helper app to facilitate the coexistence of MEM and Document Capture ensures smooth document registration with no workflow interruptions and no additional manual action required, once everything has been set up.

## Feature details

To allow Document Capture to work together with MEM, Continia has developed the app "DC+MEM Dimension Helper", which will now be made widely available.

MEM is a popular extension that allows you to consolidate multiple legal entities into a single company within Business Central. The entities exist as dimensions in this single company, and these entity dimensions must be validated first when transactions are entered in Business Central.

Whenever you register a document, the helper app checks if MEM is installed and, if so, ensures that purchase and sales transactions are created in the right order (global dimension 1 first), in order to align with MEM's validation order. The app also changes the order in which header fields are validated and adds a prepopulated new field, **CDC Document No.**, to the purchase and sales header tables. In this way, compatibility with MEM's updated validation order is retained, and you won't receive any errors when you register documents.

The helper app supports the following types of transactions:

* Document categories: **PURCHASE**, **PURCHORDER**, and **SALES**
* Document types: Purchase orders, purchase invoices, purchase credit memos, purchase return orders, sales orders, and sales credit memos

For more information, see [Support for Multi-Entity Management (MEM) by Binary Stream Software](@DC-218).