---
title: Business Identification Fields for Determining Document Vendors
date: 28-11-2024
description:
id: DC-307
lang: en
---

# Business Identification Fields for Determining Document Vendors

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Business identification fields for determining document vendors | - | {{checkmark}} Oct 2023 |

## Business value

For each purchase document that's sent to Continia Document Capture, it's essential to correctly identify the vendor that sent it, so that the right template can be assigned and field recognition can be carried out correctly. This feature will improve the accuracy and overall performance of this vendor identification process through the use of identification templates.

## Feature details

To identify the vendor who sent a given document, Document Capture uses a number of different strategies. The most efficient one of these is typically to attempt to identify a VAT registration number in the document and then search through the vendor table for a vendor with a corresponding VAT registration number.

This method isn't always successful though, for example because not all incoming documents even include VAT registration numbers in the first place. For that reason, the identification template will now be expanded to allow Document Capture to search for multiple additional business identification fields used across different localizations. The following identification fields will be included:

* VAT registration number
* Enterprise number
* ABN number
* Registration number

In addition to this, the number of identification inaccuracies that result from the use of unnecessary characters (such as spaces, dots, and slashes) will now be greatly reduced, as Document Capture will clean up the search values before searching through vendor tables for matching business identification fields.

For more information, see [Finding the Document Source and Template](@DC-109).