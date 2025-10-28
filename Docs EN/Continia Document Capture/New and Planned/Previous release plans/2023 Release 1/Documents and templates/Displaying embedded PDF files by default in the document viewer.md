---
title: Displaying Embedded PDF Files by Default in the Document Viewer
date: 28-11-2024
description:  
id: DC-293
lang: en
---

# Displaying Embedded PDF Files by Default in the Document Viewer

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Displaying embedded PDF files by default in the document viewer | {{checkmark}} Mar 2023 | {{checkmark}} Apr 2023 |

## Business value
Having embedded PDF files displayed by default in the document viewer saves you the trouble of having to find them manually yourself using the drop-down menu for every imported XML document. If you prefer to view PDF attachments rather than original XML files in the document journal, the introduction of this feature will certainly make your life easier.

## Feature details
A new setting, **Show Embedded PDF as Default**, will be added to the **Template Card** for XML master templates. If you enable this, the document viewer in the document journal will by default display any PDF file that has been embedded within an imported XML file instead of displaying the original XML.

If a file in any other format than PDF has been embedded in the imported XML, it won't be displayed by default. In such cases, the document viewer will then display the original XML instead.

For more information, see [Overview of the document journal](@DC-71#overview-of-the-document-journal).