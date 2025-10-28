---
title: Configuring On-Premises OCR in Document Capture
date: 10-01-2025
description: How to configure OCR in on-premises setups of Document Capture.
id: DC-150
lang: en
---

# Configuring On-Premises OCR
Optical character recognition (OCR) is the process of extracting the textual content of a scanned image or PDF file and converting it into something that can be processed by a computer.

If you’re using Microsoft Dynamics 365 Business Central online, your default OCR method is Continia Cloud OCR – which means that no additional configuration is required.

However, if you’re using Microsoft Dynamics NAV/Business Central on premises, you can choose to use either on-premises OCR or Continia Cloud OCR. The on-premises method is described in detail below, whereas you can find an in-depth description of Continia Cloud OCR in the article [Configuring Cloud OCR for NAV or Business Central on-premises](@DC-141).

>[!NOTE]
>If you use on-premises OCR, you must use File System as your storage type. For more information, see [Setting up Document Storage](@DC-3).

## Setting up on-premises OCR
When you use on-premises OCR, you won't be provided with a system-generated email address for document import as you do with Continia Cloud OCR. Instead, you must create and configure email addresses for each relevant document category in order to import your documents into Document Capture. You must also set up the OCR service and Document Capture, so that the imported documents can be OCR-processed and stored.

To set up on-premises OCR:

1. Ensure that you've imported the default Document Capture configuration.
1. Create and configure email addresses for each relevant document category. For more information, see [Creating and Configuring Email Addresses for Document Import](Creating and configuring email addresses for document import.md).
1. Install the ABBYY and Document Capture services. For more information, see [Installing ABBYY and Document Capture Services](Installing ABBYY and Document Capture services.md).
1. Search ({{search}}) for and select **Document Capture Setup**.
1. On the **Document Capture Setup** page, on the **General** FastTab, go to the **On-Premise OCR Storage** section.
1. In the **PDF File Path for OCR** field, specify a path to the folder where you want to store all scanned PDF documents. This folder corresponds to the **Pending OCR** cue in the **Continia Document Capture Activities** section of the Role Center.
   > [!IMPORTANT]
   > Note that the entered path must be identical with the path entered in **PDF files for OCR** during the [installation of the Document Capture service](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/installing-abbyy-and-document-capture-services#the-document-capture-service).
1. In the **File Path for OCR-processed files** field, specify a path to the folder where you want to store all OCR-processed PDF documents. This folder corresponds to the **Ready to Import** cue in the **Continia Document Capture Activities** section of the Role Center.
   > [!IMPORTANT]
   > Note that the entered path must be identical with the path entered in **OCR-processed Files for NAV** during the [installation of the Document Capture service](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/installing-abbyy-and-document-capture-services#the-document-capture-service).
1. In the **XML File Path** field, specify a path to the folder where you want to store all incoming XML documents (if any).
1. Choose the {{search}} icon, enter **Export OCR Configuration Files**, and then choose the related link. A dialog box confirms that a number of configuration files have been exported. Select **OK** to close it.

> [!NOTE]
> It's recommended to use [UNC paths](https://docs.microsoft.com/en-us/dotnet/standard/io/file-path-formats#unc-paths) when specifying folder paths as described above – for example, \\\\servername\share\DC\PDF\. Also, note that the service account that runs the Business Central service must have read, write, and delete permissions for the relevant folders.

## Related information
[Configuring Cloud OCR for NAV or Business Central on premises](@DC-141)  
[Creating and Configuring Email Addresses for Document Import](Creating and configuring email addresses for document import.md)  
[Installing ABBYY and Document Capture Services](Installing ABBYY and Document Capture services.md)  
[Microsoft article on UNC paths](https://docs.microsoft.com/en-us/dotnet/standard/io/file-path-formats#unc-paths)  