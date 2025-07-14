---
title: Setting up search texts for a template in Document Capture
date: 27-06-2025
description: How to set up search texts as an identification method.
id: DC-108
lang: en
---

# Setting up search texts for a template

You can set up search texts either directly in a vendor template or from the document journal. Normally, you set up search texts in the document journal when processing documents – as this is typically where you find out that Document Capture hasn’t identified the correct vendor for a document.

To set up search texts for a template from the document journal, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Click the code of the relevant document category – for example, **PURCHASE** – to open the document journal.
1. In the document list, select the document whose template you want to add search texts to. Click the document line – not the number in the **No.** column, as this opens the document card.
1. Click the **Search Text** field for the chosen document line. To view the **Search Text** column, you may have to move right in the document list using the scroll bar (depending on your screen size).
1. For PDF documents, you can do one of the following:
   
   * Manually enter any free-text keyword(s) that you want to use as search text. 
   
   * Use existing text from the document image by left-clicking and holding the button to draw a blue box around the relevant text in the image (as when capturing template field values).
1. For XML documents, you must enter a free-text keyword manually – as capturing image text isn't an option.
1. To add more than one search text, click the three dots on the right of the **Search Text** field to open the **Template Search Texts** page.
1. Select a new line, and enter the new text in the **Search Text** column. Repeat this process for every additional text you want to add, and click **Close** when you're done.

>[!NOTE]
>If you add two or more search texts to a template, all of them must appear in the document at the same time for the vendor to be recognized.

Pay special attention to what words you use as search texts, as they could result in an incorrect vendor match if they’re not unique to a specific vendor. For example, if you’ve used the search text 'Freight' for the vendor DHL, Document Capture may also identify this word in documents from other vendors than DHL, such as UPS. This means that the same template is used for two different vendors, which is undesirable.

To solve this issue, make sure to use a search text that's unique to one specific vendor – such as their bank account number, their phone number, or even their address.

Alternatively, you can set up search texts on multiple templates. Then, if Document Capture finds a match in more than one template, a dialog box asks you to select the correct one. This only happens when fields are recognized in a single document – not on document import, and not when you select multiple documents in the document journal.

## Related information

[Finding the document source and template](@DC-109)  