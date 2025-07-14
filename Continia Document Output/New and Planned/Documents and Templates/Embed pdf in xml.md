---
title: Embed PDF in XML
date: 03-12-2024
description: 
id: DO-40
lang: en
---

# Embed PDF in XML

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| Embed PDF in XML | {{checkmark}} Sep 19 2024 | {{checkmark}} Oct 2024 |

## Business value

Electronic invoicing is progressively becoming mandatory in many countries, both for B2G and B2B. Even though many companies are capable of receiving invoices in a supported XML format, there's still a desire to view invoices as a PDF. This can be achieved by embedding a PDF copy of the posted invoice into the XML files to be sent electronically, which is what this new feature in Document Output will deliver.

## Feature details

Embedding a PDF in an XML file has been supported, using event subscribers, for some time in Document Output, but an increased demand of making this a standard feature has defined this feature development. 

In the first version of this feature, it will be possible to mark the result of a report layout generated PDF to be embedded. If the feature is successful, it might be extended to allow embedding additional files in the future, which will also require functionality to assess XML file sizes.

Read about how to use this functionality in [Output Profiles](@DO-74).
