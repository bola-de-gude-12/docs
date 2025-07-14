---
title: More Available Payment Methods for XML Formats (FIK/OCR/KID/Bank Information)
date: 09-12-2024
description: 
id: DO-102
lang: en
---

# More Available Payment Methods for XML Formats (FIK/OCR/KID/Bank Information)

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| More available payment methods for XML formats | - | N/A |

> [!NOTE]
> The release of this feature has been postponed. A new release date has not yet been determined.

## Business value

The standard payment method for XML invoices from Document Output is making a bank transfer. There are many other options defined in the formats, and Document Output has so far used event subscribers to insert them. Document Output users have requested that more of the most frequently used methods be added directly to Document Output as a feature to make paying XML invoices even easier and quicker.

## Feature details

The feature will be implemented as a setup option defining which payment method should be used as default for electronic invoicing. The initial plan is to support FIK, OCR, KID and bank transfer options, but more options may be added later.