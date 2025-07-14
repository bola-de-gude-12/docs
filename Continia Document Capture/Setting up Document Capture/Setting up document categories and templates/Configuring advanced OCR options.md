---
title: Configuring advanced OCR options in Document Capture
date: 26-05-2025
description: How to configure advanced OCR settings in Document Capture.
id: DC-472
lang: en
---

# Configuring advanced OCR options

All PDF files imported into Continia Document Capture are OCR-processed in accordance with the settings applicable at the time of processing. The default settings apply if you make no adjustments, but it's possible to customize some of the more advanced settings to suit your needs. This article describes the customization process.

## To configure OCR settings

To configure how incoming documents are OCR-processed:

1. Search ({{search}}) for and select **Document Categories**.
1. Open the relevant document category. For example, to open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself), and then select **Edit** on the action bar.
1. On the **OCR Processing** FastTab, configure the settings as needed. For more information and recommendations, see [Details and recommended settings](#details-and-recommended-settings) below.

## Details and recommended settings

The table below contains a number of tips and recommendations for each of the fields you can customize using [the above guide](#to-configure-ocr-settings):

<br>

| Field | Details and recommendations |
| --- | --- |
| **Image Resolution** | In this field, you can enter the number of dots per inch (DPI) to be used by Document Capture when storing OCR-processed files as image files. The entered value must be at least 150 DPI – anything below this will return an error. <br><br>The higher the entered value, the better the resolution. However, note that very high values will result in correspondingly large image files that take a long time to load in the user interface. For this reason, we recommend that you select **300** DPI, which ensures good resolutions and acceptable file sizes.  |
| **Image Colour Mode** | Here, you can specifiy the color mode of the image files that all imported PDF files are converted into. You can choose between the following options: <ul><li><b>Black \& White</b>: Image files consisting of only black and white colors will be created and stored.</li><li><b>Gray</b>: Image files consisting of only grayscale tones will be created and stored.</li><li><b>Colour</b>: Image files consisting of all original colors will be created and stored.</li></ul> We advise against selecting the **Colour** option, as this will increase the size of the stored image files and consequently slow down image rendering. |
| **Max. number of pages to process per file** | This field allows you to specify how many pages should be OCR-processed for each imported file, enabling you to reduce the import time and thereby optimize the import process. The last three pages of any imported file is always processed, as they typically contain essential information. <br><br>Note that Document Capture imposes an overall limit of 500 pages on document import, meaning that no documents longer than 500 pages can be imported into Document Capture, regardless of what value you enter in this field.  |
| **OCR Languages** | In this field, you can add all the languages whose character sets should be recognized by Document Capture when OCR-processing incoming documents. <br><br>It's recommended that you limit the number of activated languages to the ones generally used in the documents you import (typically only your own native language and, if relevant, English), as enabling too many languages is likely to lower the overall quality of character recognition.<br/><br/>Note that this setting only applies to on-premises OCR installations. |
| **Process PDF files with XML files** | With this toggle, you can enable the import of XML files embedded in PDFs (such as ZUGFeRD, Factur-X, and XRechnung). For more information, see [Enabling the Import of PDF Files with Embedded XML Files (ZUGFeRD, XRechnung)](@DC-40). |

For information on the remaining customizable fields on the **OCR Processing** FastTab, which all relate to the automatic splitting of documents, see [Splitting documents automatically](/continia-document-capture/business-functionality/documents-and-templates/splitting-and-merging-documents#splitting-documents-automatically).
