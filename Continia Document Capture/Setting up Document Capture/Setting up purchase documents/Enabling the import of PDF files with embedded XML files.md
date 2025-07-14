---
title: Enabling the Import of PDF Files with Embedded XML Files (ZUGFeRD, XRechnung) 
date: 01-07-2024
description: How to enable the import of PDF files with embedded XML documents into Document Capture 
id: DC-40
lang: en
---

# Enabling the Import of PDF Files with Embedded XML Files (ZUGFeRD, XRechnung)

For the German market, Continia Document Capture supports the import and processing of certain PDF files that have XML documents embedded in them, including the ZUGFeRD and XRechnung formats. 

Whenever such files are sent to the OCR service and imported into Document Capture, it's in fact the embedded XML documents that are extracted and processed, which happens automatically upon import. However, for each imported file, the original PDF is also attached to the document in the **XMLATTACH** document category.

> [!IMPORTANT]
> To process data inside extracted XML documents, you must import the XRECHNUNG-CII XML master and identification templates from either Continia Online or the Document Capture product package.

## To enable the import of embedded XML files

> [!NOTE]
> The following prerequisites and requirements must be met:
> * You must be running version 8 or later of the Document Capture service (OCR).
> * Specifically for on-premises deployments of Microsoft Dynamics NAV/Business Central: You must have an active license for the XML Import module in Document Capture.
> 
> For a list of currently supported formats, see [Supported Electronic Document Formats](/Continia Document Capture/Getting Started/Importing electronic documents/Supported Formats.md).

To enable the import of embedded XML files and configure the way incoming documents are OCR-processed in general, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Open the relevant document category. For example, to open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself), and then select **Edit** on the action bar.
1. On the **OCR Processing** FastTab, configure the settings as needed, and then turn on the **Process PDF files with XML files** toggle.

## Related information

[Importing Electronic Documents in Germany](/Continia Document Capture/Getting Started/Importing electronic documents/Germany.md)  