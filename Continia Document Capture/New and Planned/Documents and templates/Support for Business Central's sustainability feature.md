---
title: Support for Business Central's sustainability feature
date: 30-09-2025
description:
id: DC-322
lang: en
---

# Support for Business Central's sustainability feature

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Support for Business Central's sustainability feature | {{checkmark}} Sep 2025 | {{checkmark}} Oct 2025 |

## Business value

By supporting Microsoft Dynamics 365 Business Central's sustainability feature, Document Capture allows you to allows you to capture various emissions data points on inbound purchase documents to calculate and track your company's greenhouse gas (GHG) emissions within Business Central.

## Feature details

The following header and line fields will be made available across all master templates in the purchase category in Document Capture:

* **Sustainability Account No.**
* **Fuel/Electricity***
* **Distance***
* **Custom Amount***
* **Installation Multiplier***
* **Time Factor***
* **Emission CO2**
* **Emission CH4**
* **Emission N2O**

The fields marked with an asterisk above, known as activity fields, won't be carried over from Document Capture templates to standard purchase invoices. Instead, Document Capture will automatically calculate the emission factor fields (i.e.: CO₂, CH₄, N₂O) in the document card – ensuring accurate and reliable sustainability data every time.

Fore more information, see [Capturing header fields in a document](@DC-110) and [Capturing line fields in a document (line recognition)](@DC-147).
