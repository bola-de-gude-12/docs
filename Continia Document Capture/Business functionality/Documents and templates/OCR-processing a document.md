---
title: OCR-Processing a Document 
date: 17-06-2024
description:  
id: DC-145
lang: en
---

# OCR-Processing a Document 

Optical character recognition (OCR) is the process of extracting the textual content of a scanned image or PDF file and converting it into something that can be processed by a computer.

Whenever you receive a PDF document in Continia Document Capture, the document is automatically OCR-processed, which enables it to be imported into Document Capture for registration and further processing. For the actual OCR-processing, Document Capture uses some of the world's leading providers of OCR and document-scanning services. The actual OCR method depends on your environment, as outlined below.

## The technology behind

As regards the technology that's used to OCR-process incoming documents in Document Capture, the method depends on whether you have an online or an on-premises deployment:

**If you’re using Microsoft Dynamics 365 Business Central *online***, your default OCR method is Continia Cloud OCR. The Cloud OCR uses the [Azure AI Document Intelligence](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/overview?view=doc-intel-4.0.0) prebuilt [invoice model](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/concept-invoice?view=doc-intel-4.0.0).

**If you’re using Microsoft Dynamics NAV/Business Central *on-premises***, you can choose to use either on-premises OCR or Continia Cloud OCR. If you choose on-premises OCR, the process is carried out by the Continia OCR service, which consists of the Document Capture service (downloading emails and monitoring for incoming files for OCR-processing) and the [ABBYY FineReader Engine](https://www.abbyy.com/ocr-sdk/) (carrying out the actual OCR-processing of imported documents).

For more information on Continia Cloud OCR and how to set it up, see [Configuring Cloud OCR for NAV or Business Central on-premises](@DC-141).

For details on on-premises OCR and the Continia OCR service, as well as information on how to set these up, see [Configuring On-Premises OCR](/Continia Document Capture/Development and Administration/On-Premises/Deployment/Configuring on-premises OCR/Configuring on-premises OCR.md) and [Installing ABBYY and Document Capture Services](/Continia Document Capture/Development and Administration/On-Premises/Deployment/Configuring on-premises OCR/Installing ABBYY and Document Capture services.md). Relevant minimum requirements can be found under [OCR server requirements](/continia-document-capture/development-and-administration/on-premises/deployment/minimum-requirements#ocr-server-requirements) and [Firewall requirements](/continia-document-capture/development-and-administration/on-premises/deployment/minimum-requirements#firewall-requirements).

## The overall process

For every PDF document that's imported into Document Capture, the OCR engine will attempt to capture all characters and their positions. Using this OCR data, Document Capture can then locate all words and phrases in the document, which enables it to [search for captions and their corresponding values](/continia-document-capture/business-functionality/documents-and-templates/working-with-paper-and-pdf-documents#capturing-fields). In order to be able to display the scanned PDF document optimally in the user interface, along with all identified captions and values, Document Capture converts it into a TIFF file, as this is more manageable and easier to render. However, you can always retrieve the original PDF document via the action bar by selecting **Document** > **PDF File**.

For each identified caption, Document Capture will initially look for the value to the right of the caption, and if no value is found there, it will search for it immediately below the caption. If Document Capture fails to locate a value, or if it finds the wrong one, you can help it by [identifying the correct value manually](/continia-document-capture/business-functionality/documents-and-templates/working-with-paper-and-pdf-documents#working-with-field-captions-and-values). Once a value has been found – whether by Document Capture or by you – Document Capture registers the relative position of the caption and the value, and this is then used to identify the values of this caption in all future documents sent by the same vendor. The position of the caption itself is unimportant; only the relative position between the caption and the value is used.

## Related information

[Configuring Cloud OCR for NAV or Business Central on-premises](@DC-141)  
[Configuring On-Premises OCR](/Continia Document Capture/Development and Administration/On-Premises/Deployment/Configuring on-premises OCR/Configuring on-premises OCR.md)  
[Installing ABBYY and Document Capture Services](/Continia Document Capture/Development and Administration/On-Premises/Deployment/Configuring on-premises OCR/Installing ABBYY and Document Capture services.md)  
[Minimum Requirements for Using Continia Document Capture On-Premises](/Continia Document Capture/Development and Administration/On-Premises/Deployment/Minimum Requirements.md)  
[Working with Paper and PDF Documents](/Continia Document Capture/Business functionality/Documents and templates/Working with paper and PDF documents.md)  