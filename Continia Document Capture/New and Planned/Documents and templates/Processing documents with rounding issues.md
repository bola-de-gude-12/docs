---
title: Processing documents with rounding issues
date: 30-09-2025
description:
id: DC-469
lang: en
---

# Processing documents with rounding issues

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Processing documents with rounding issues | {{checkmark}} Sep 2025 | {{checkmark}} Oct 2025 |

## Business value

Currently, when users encounter small VAT differences between the vendor’s invoice and Business Central’s calculation, users need to manually address these issues in the created purchase invoice. To ease this process, the option to automatically correct the rounding will be added Document Capture.

## Feature details

A setting will be added to the **General Ledger Setup**. If enabled, this setting will automatically correct the created invoice if the values set in **Maximum Allowed Difference Excl. VAT** and **Maximum Allowed Difference Incl. VAT** allow for it.

For more information, see [Configuring purchase documents](@DC-139).
