---
title: Validate sustainability values in document header and lines
date: 31-03-2025
description:
id: DC-436
lang: en
---

# Validate sustainability values in document header and lines

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Validate sustainability values in document header and lines | {{checkmark}} Mar 2025 | {{checkmark}} Apr 2025 |

## Business value

This validation check ensures that you're working with the right details when using Continia Document Capture and Continia Sustainability, saving you time and reducing the number of input errors.

## Feature details

When the settings under the **Purchase Document Posting** section of the related G/L Account Card or Item Card are specified, Document Capture will trigger a validation check. If the following field values don't correspond to these **Purchase Document Posting** settings, Document Capture will show a standard, configurable comment in the **Comments** section of the document journal and document card.

* Environmental Account Type
* Environmental Account No.
* Emission Type
* Emission Code
* Total Emission Quantity
* Emission Unit Code
* Emission Quantity
* Emission Unit Type

For more information, see [Tracking emissions in Document Capture with Continia Sustainability](@DC-232).
