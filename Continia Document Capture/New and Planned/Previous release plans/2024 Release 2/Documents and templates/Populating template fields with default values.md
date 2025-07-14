---
title: Populating template fields with default values
date: 31-03-2024
description:
id: DC-312
lang: en
---

# Populating template fields with default values

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Populating template fields with default values | {{checkmark}} Sep 2024 | {{checkmark}} Oct 2024 |

## Business value

If an imported document is missing a field value but this value is available elsewhere – for example, in the **Vendor Card** – you may be surprised not to find it in the document journal. With this feature, this will no longer be the case, as the feature will automatically insert default values into template fields that would have otherwise been empty.

## Feature details

Currently, if no document-specific value is captured in a template field for an imported document, no value is displayed for that field in the document journal. With the implementation of this feature, Continia Document Capture will automatically populate the relevant template field with the default value from the applicable card instead of leaving the field empty.