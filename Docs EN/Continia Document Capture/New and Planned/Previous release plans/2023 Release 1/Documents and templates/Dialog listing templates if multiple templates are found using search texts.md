---
title: Dialog Listing Templates if Multiple Templates Are Found Using Search Texts
date: 28-11-2024
description:
id: DC-299
lang: en
---

# Dialog Listing Templates if Multiple Templates Are Found Using Search Texts

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Dialog listing templates if multiple templates are found using search texts | {{checkmark}} Mar 2023 | {{checkmark}} Apr 2023 |

## Business value

By allowing you to choose the correct template from a list, this feature will provide added user control when it comes to the identification of templates using search texts. Until now, Continia Document Capture has always automatically selected the template with the first identified search text, but now you'll be in charge whenever the identified templates include more than one search text.

## Feature details

When you're using [search texts to identify a document template](@DC-109) and multiple templates are found, a dialog that allows you to select the right one will be displayed. This will only happen when fields are recognized in a single document – not on document import and not when you select multiple documents in the document journal. 

The dialog will only be displayed if the identified templates include more than one search text. If multiple templates with only one search text are found, existing functionality will prioritize which one to use based on where in the document that search text is located. In such cases, the template for which the matching search text is identified first (at the top of the document) will be used.