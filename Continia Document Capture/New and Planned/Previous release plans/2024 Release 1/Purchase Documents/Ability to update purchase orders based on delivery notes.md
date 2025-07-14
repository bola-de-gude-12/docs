---
title: Ability to Update Purchase Orders Based on Delivery Notes
date: 29-11-2024
description:
id: DC-345
lang: en
---

# Ability to Update Purchase Orders Based on Delivery Notes

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Ability to update purchase orders based on delivery notes | {{checkmark}} Mar 2024 | {{checkmark}} Apr 2024 |

## Business value

Currently, it's not possible to update existing purchase orders based on delivery notes. With this release, this much sought-after feature will be added, meaning that no more workarounds or manual updating will be needed to achieve this going forward.

## Feature details

The feature will enable you to use the data from delivery notes to update related purchase orders quickly and easily by matching the quantities of both types of documents. So if, for example, you ordered 20 units of an item but only received 15, the relevant fields of the purchase order will automatically be updated accordingly when you match it with the delivery note:

* **Qty. to Receive**: **5** (changed from **0**)
* **Quantity Received**: **15** (changed from **20**)

For more information, see [The Purchase Order Category](@DC-136).