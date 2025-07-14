---
title: Document matching improvements regarding units of measure
date: 01-04-2025
description:
id: 
lang: en
---

# Document matching improvements regarding units of measure

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Document matching improvements regarding units of measure | {{checkmark}} March 2025 | {{checkmark}} April 2025 |

>[!NOTE]
>This feature has been postponed to April 2025.

## Business value

By resolving the issues that exist with invoices matched against orders with differing units of measure (UOM), Continia Document Capture will streamline the matching process for users dealing with such UOM discrepancies.

## Feature details

A recurring problem for many organizations is the inability to match purchase invoices and purchase orders that have lines with the same line amount but with different units of measure (and different unit costs), as in the following example:

<br>

| Document line type | Item number | Quantity and UOM | Unit cost | Line amount |
| --- | --- | --- | --- | --- |
| Purchase order line | Item 1900-S | 12 pieces | $5.00 | $60.00 |
| Purchase invoice line | Item 1900-S | 2 boxes | $30.00 | $60.00 |

This feature will resolve any such issues and ensure a smooth reconciliation between invoices and orders, despite differences in units of measure and unit costs.

For more information, see [Enhanced line recognition](@DC-191#to-use-ai-line-recognition).