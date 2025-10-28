---
title: Automatic Checking of Line Item Prices
date: 29-11-2024
description:
id: DC-338
lang: en
---

# Automatic Checking of Line Item Prices

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Automatic checking of line item prices | {{checkmark}} Mar 2023 | {{checkmark}} Apr 2023 |

## Business value
With the implementation of this feature, you'll no longer have to check the item price of every single invoice line manually – Continia Document Capture will automatically do it for you, making it much faster and easier for you to process incoming invoices with no corresponding purchase orders.

## Feature details
A new switch, **Check Item Prices**, will be added to the **Template Card**. Enabling this switch will ensure that Document Capture automatically checks the item prices of all recognized lines in invoices that use the relevant template. If a recognized price differs from the item unit price, a warning will be displayed in the comments section of the document journal.

Prices will only be checked when line recognition has been enabled and when no related purchase orders exist. The feature will take into account whether or not any specific vendor purchase prices apply to the checked item numbers.