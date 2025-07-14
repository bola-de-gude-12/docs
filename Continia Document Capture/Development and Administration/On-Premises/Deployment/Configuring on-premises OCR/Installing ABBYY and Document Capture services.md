---
title: Installing ABBYY and Document Capture Services
date: 05-07-2021
description:  
lang: en
---

# Installing ABBYY and Document Capture Services
The overall Continia OCR service consists of two essential elements:
* [the ABBYY FineReader Engine](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/installing-abbyy-and-document-capture-services#the-abbyy-finereader-engine)
* [the Continia Document Capture Service](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/installing-abbyy-and-document-capture-services#the-document-capture-service)

In the sections below, you can find an outline of each of these services, along with details on how to install them.

##The ABBYY FineReader Engine
When you use OCR on-premises, the ABBYY FineReader Engine carries out the actual OCR-processing of your imported documents. Only install this if you're *not* using Continia Cloud OCR. The application can be installed either on a server or on the computer that does the actual scanning.

To install the ABBYY FineReader Engine, follow these steps:

1. Run setup.exe from the root of the software directory to open the installer.
1. In the installer, select **ABBYY FineReader** > **Install**.
1. When the installation is complete, the ABBYY FineReader license manager is launched. Select **Activate License**, enter your serial number (SN), and follow the on-screen instructions to activate the license.

> [!NOTE]
> The FineReader Engine license can only be activated for one computer at a time. If you're using a software key, you can only deactivate and reactivate the license twice. After this, you must have it unlocked for any extra activations. This process can take several days and must be requested by your Continia partner.

##The Document Capture Service
The Document Capture Service is responsible for downloading emails and for monitoring incoming files that need to be OCR-processed. Only install this if you're *not* using Continia Cloud OCR. The service interacts with the FineReader Engine, and both services must be installed on the same computer. The Document Capture Service is installed as a Windows service called “Document Capture” and runs in a few key directories that must be configured after installation.

> [!IMPORTANT]
> When you upgrade the Document Capture Service to a newer version, you must also export the OCR configuration files. If you fail to do so, new features that depend on settings in the OCR configuration files won't work as expected (such as the import of emails using EWS or the creation of PNG image files).

To install the Document Capture Service, follow these steps:

1. Run setup.exe from the root of the software directory to open the installer.
1. In the installer, select **Document Capture Service** > **Install**.
1. When the installation is complete, the Document Capture Configuration Manager is launched. Configure each of the settings as needed.
   > [!IMPORTANT]
   > The path that's entered in **PDF files for OCR** must be identical with the path you enter in the **PDF File Path for OCR** field during the [on-premises OCR setup](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/configuring-on-premises-ocr#setting-up-on-premises-ocr) (step 6).
   >
   > Likewise, the path that's entered in **OCR-processed Files for NAV** must be identical with the path you enter in the **File Path for OCR-processed files** field during the [on-premises OCR setup](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/configuring-on-premises-ocr#setting-up-on-premises-ocr) (step 7).
1. If you place one or more folders on another computer, you must specify a valid domain user account with access to all folders.
1. Start the Document Capture Service.

> [!NOTE]
> In the Document Capture Configuration Manager event log, you can find the latest Document Capture entry. You must make sure that there are no errors when you start the service.

## Related information
[Configuring On-Premises OCR](Configuring on-premises OCR.md)  