---
title: Support for Full-Content QR Codes (e.g. Vendor Data) for the Swiss Market
date: 11-12-2024
description:
id: DC-267
lang: en
---

# Support for Full-Content QR Codes (e.g. Vendor Data) for the Swiss Market

| Feature | General availability on-premises | General availability online | Public preview |
| --- | :-: | :-: | :-: |
| Support for full-content QR codes (e.g. vendor data) for the Swiss market | {{checkmark}} Sep 1, 2020 | {{checkmark}} Oct 1, 2020 | - |

## Feature details
It's now possible to capture the full content of QR codes, which effectively means that you can import the content of QR codes containing vendor data and other long sections of text into Microsoft Dynamics 365 Business Central using Continia Document Capture. If the captured value contains more than the Business Central limit of 250 characters, only the first 250 characters will be displayed in the user interface, but you can retrieve the full value using **GetFullText** on the CDC Document Value table.

The feature has been deployed for the Swiss market but can also be made available to other markets. For more information, please contact your dedicated Continia partner. 

> [!NOTE]
> Note that in order to use this feature in the on-premises version of Business Central, you must update the on-premises Document Capture service to the latest version.