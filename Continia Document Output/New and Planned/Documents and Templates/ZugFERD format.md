---
title: ZugFERD Format (DE)
date: 27-03-2023
description:
id: DO-136
lang: en
---

# ZUGFeRD Format (DE)

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| ZUGFeRD format (DE) | - | {{checkmark}} Jan 2023 |

## Business value
This standardized electronic invoicing format is used in a number of countries, especially German-speaking ones, so being able to use ZUGFeRD will make invoicing in any country that's adapted it much easier. Companies can also use the ZUGFeRD format to send documents to those customers in Germany that are not yet ready to use the Peppol Bis3 format XRechnung, which is projected to become the dominant format for B2B invoicing in Germany.

## Feature details
ZUGFeRD is a PDF-A variant of a PDF attachment. It contains an embedded XML file with the same structured data from posted documents from Business Central as is used when a report is generated for a standard email template.

A new Output Profile for this new file format will define that attachments will be generated with the required settings for ZUGFeRD. The file type is still a PDF file, and it has to be sent as an attachment to an email.
