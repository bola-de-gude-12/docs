---
title: Support for serial and lot numbers in the matching process
date: 11-12-2024
description:
id: DC-365
lang: en
---

# Support for Serial and Lot Numbers in the Matching Process

| Feature | General availability on-premises | General availability online | Public preview |
| --- | :-: | :-: | :-: |
| Support for serial and lot numbers in the matching process | {{checkmark}} Sep 1, 2020 | {{checkmark}} Oct 1, 2020 | - |

## Feature details
Support has been added for the partial matching of purchase receipt and return shipment lines with multiple tracking entries (that is, multiple lot or serial numbers). If a purchase receipt/return shipment contains items that haven't already been matched with or linked to any existing documents, the tracking entries of those remaining, non-matched items are automatically matched if they correspond to items on an incoming invoice or credit memo. This also applies to auto-matching.

When only one item is invoiced and there's more than one lot or serial number, you must perform the lot/serial number matching manually at item-tracking level before posting. You're notified in the comments section if manual action is required.