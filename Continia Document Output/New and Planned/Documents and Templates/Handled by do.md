---
title: Handled by DO
date: 28-06-2024
description: 
id: DO-31
lang: en
---

## Handled by DO

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| Handled by DO | - | {{checkmark}} Jun 2024 |

## Business value

Document Output helps monitor the number of posted documents which have not been printed or emailed. The print and email features in standard Business Central automatically use the “Printed no.” as the counter of handled documents.
This counter is also updated if you run a selected report layout to generate a PDF file. This may cause an accuracy problem, as Document Output can no longer be certain whether a document is, in fact, unhandled.

With the Handled by DO feature, you can be certain that documents are only counted if they have been processed by Document Output.

## Feature details

With this new feature in Document Output, you can add Output Profiles directly to posted documents by extending the field to the Business Central document. When the distribution method of a document has been determined, it's also possible to determine whether this distribution method has been in use or not. If the document's customer or vendor has no Output Profile, the document will not be handled by Document Output.

When you select an Output Profile for a customer or vendor in Document Output, that profile will automatically apply to all documents related to this customer or vendor.

You can find more information on this feature in the business functionality article [Handled by DO](@DO-112).

