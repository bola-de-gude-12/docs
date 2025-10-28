---
title: eDocument validation
date: 18-08-2025
description:
id: DC-466
lang: en
---

# eDocument validation

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| eDocument validation | - | Nov 2025 |

>[!NOTE]
>This feature will be released as part of a service pack in November 2025.

## Business value

This release will feature significant improvements to the validation of eDocuments – both prior to posting and, optionally, in their XML representations.

## Feature details	
Select fields will be validated prior to the posting of business documents, making users aware of missing or incomplete data that’s actually required.

Currently, detailed validation of XML files (i.e.: schematron validation) is performed in the connected network after the document is sent. Continia aims to have that validation in place in Business Central before the document is sent, reducing the amount of time involved in handling ill-formed documents.
