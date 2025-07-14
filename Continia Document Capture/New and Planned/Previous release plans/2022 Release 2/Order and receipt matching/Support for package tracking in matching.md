---
title: Support for package tracking in matching
date: 11-12-2024
description:
id: DC-371
lang: en
---

# Support for Package Tracking in Matching

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Support for package tracking in matching | - | {{checkmark}} Oct 2022 |

## Business value
*Use tracking by package number in reservation and tracking system* is a standard Microsoft Dynamics 365 Business Central feature that was introduced by Microsoft in 2021. By supporting this, Continia Document Capture now supports item tracking by package number, on the same level as lot and serial number tracking.

## Feature details
The feature is supported in order and receipt matching, for matching purchase receipt lines and return shipment lines.

Whenever an invoice is created from matched purchase receipt lines, any package number that's identified in the receipt is automatically transferred to the invoice.