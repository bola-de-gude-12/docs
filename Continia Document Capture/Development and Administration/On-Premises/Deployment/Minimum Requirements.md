---
title: Minimum requirements for using Continia Document Capture on premises
date: 26-03-2025
id: DC-135
lang: en
description: >-
  The minimum requirements and recommendations for using Document Capture in
  Business Central on premises.
---

# Minimum requirements for using Continia Document Capture on premises

This article describes the minimum requirements and recommendations for using Document Capture in Microsoft Dynamics 365 Business Central on-premises. Note that these minimum requirements are different from the ones relating to the online version of Business Central, which can be found in \[Minimum requirements for using Continia Document Capture]\(/Continia Document Capture/Getting Started/Frequently Asked Questions/Minimum Requirements/Overview.md).

> \[!IMPORTANT] As Document Capture is an integrated part of Business Central, the minimum requirements for Business Central also apply to Document Capture.

## Dynamics NAV Web client requirements

Document Capture only supports the Dynamics NAV Web client from Microsoft Dynamics NAV 2016 or later.

## Local scanner requirements

Document Capture supports the scanning of documents using a local desktop scanner connected to a computer. If you use a classic or RTC version of NAV/Business Central – i.e.: any version that's older than Business Central 2019 release wave 2 (BC v15) – you scan documents using the actual NAV/Business Central client.

> \[!IMPORTANT] When using the RTC client, you must install a version of the scanner driver that corresponds to the Microsoft Dynamics NAV version. For example, if you have the 32-bit version of Microsoft Dynamics NAV installed, you must install the 32-bit version of the scanner driver. Likewise, for the 64-bit version of Microsoft Dynamics NAV, you must install the 64-bit version of the scanner driver.

For BC v15 and later, you scan documents using the web client, which requires a separate Continia application to be installed as well as a TWAIN-compatible scanner. When you use the Business Central web client, both 32- and 64-bit versions of the Twain scanner driver are supported. However, note that 32-bit TWAIN scanner drivers are only supported in Document Capture 2021 R1 service pack 2 and later. For details on how to run the Document Capture Scanner Service as a 32-bit application, see [How to alter the Document Capture Scanner Service to run as a 32-bit application](https://continia.zendesk.com/hc/en-us/articles/360022114180-How-to-alter-the-Document-Capture-Scanner-Service-to-run-as-32-bit-application).

> \[!NOTE] When scanning multiple documents in one go, you must separate each of the documents with a blank page.

## OCR server requirements

In order to OCR-process documents, you need access to the OCR engine, which can be hosted on either a Continia server or your own local server. If you choose to access the engine via your own server, you must install both the Document Capture OCR service and the third-party ABBYY FineReader application on this server. Also, the additional server requirements listed below must be met.

> \[!NOTE] OCR-processing documents takes 4-6 seconds per page and is very CPU-intensive. You should consider this if the OCR applications mentioned above are installed on an existing server, as the OCR process may slow down other applications. This potential slowdown depends on the number of documents you need to process though – in many cases, there’s no problem at all.

Minimum hardware requirements:

* Operating system: Windows 2008 R2 Service Pack 1 or later
* CPU: 2 GHz; two or more cores recommended
* Memory: 8 GB minimum; 16 GB or more recommended
* Available disk space: 2 GB
* Microsoft Internet Explorer 8.0 or higher

Note that in order for the ABBYY engine to detect the correct fonts during OCR recognition, the fonts that are used in the processed documents must be installed first.

> \[!NOTE] ABBYY and the Document Capture Service don't support high availability/load balancing. If this is important to you, consider using Continia Cloud OCR instead, as this is designed for high availability.

## Internet requirements

Although it is possible to use Document Capture without a connection to the Internet, the following features are not available if you're using Business Central v22 and above while offline:

* [Split and merge](../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Deployment/@DC-80/)
* Document rotation
* Document previews in the document journal and on the document card\*

\* Depending on the version of Document Capture you migrated from.

## Email requirements

You import documents into Document Capture simply by sending them via email to a predefined email address hosted by Continia. See [Additional guidelines for using Continia Document Capture](../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Deployment/@DC-224/#technical-email-requirements) for technical requirements and things to note.

## PDF requirements

When you import PDF documents into Document Capture, it's recommended that you send each document as a separate PDF file. However, it’s possible to \[split a PDF file]\(/Continia Document Capture/Business functionality/Documents and templates/Splitting and merging documents.md) consisting of multiple documents automatically based on different criteria, for example based on barcode or invoice number.

The version of the PDF file must be PDF 1.7 or earlier, and it must conform to the PDF/A standard. Note that handwritten text isn't supported and is unlikely to be recognized well.

The following limitations also apply:

* Encrypted/password-protected PDF files are not supported.
* PDF files with electronic signatures may be processed successfully but are generally not supported.
* PDF files using the Adobe XML Forms Architecture (XFA) format are not supported.
* As of Document Capture Service 8.00, the maximum number of pages that can be processed for PDF files is 500.

To process files with any of the above properties, you must republish them as new PDF files. You can do this using, for example, **Microsoft Print to PDF**, which is available for free in Windows 10. Republishing the files as new PDFs will remove the added features and produce 'flat' PDF files with no interactive elements.

## Email server requirements

If an email server is configured and used for on-premises OCR, the email server must support IMAP or EWS.

> \[!NOTE] IMAP support for Exchange Online will be discontinued. For more information, see [Extension of the OCR service to support Exchange Web Services (EWS) instead of IMAP](../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Deployment/@DC-373/).

## Continia Web Approval Portal

The requirements for using the Continia Web Approval Portal with Business Central on-premises can be found \[here]\(Web Approval Portal Requirements On-Premises.md).

## Firewall requirements

The firewall must allow outgoing traffic on ports 80 and 443 (HTTPS) from the computer that performs the Continia Document Capture activation and downloads the Document Capture configuration and document files. For classic NAV clients, this is the actual computer that you’re using. For NAV RTC, it’s the computer running the NAV Service Tier.

To take full advantage of Document Capture during both setup and daily use, you must have access to the Internet. You may also have to configure the following firewall settings to activate Document Capture and to ensure that your setup is secure – but note that this is often not necessary.

> \[!IMPORTANT] If you – like most companies – allow all outgoing traffic from your clients and servers, you don't have to configure any firewall settings for outgoing traffic. However, if your policies for outgoing network traffic are restricted in any way, you must configure your firewall to allow the traffic below.

> \[!NOTE] All Continia resources are hosted in a Microsoft Azure environment. This means that the IP addresses associated with each domain name below are subject to change at Microsoft’s discretion. If the IP addresses do change, you can prevent sudden stop of all Internet-related functionality by allowing URL filtering rather than IP filtering.

\


From all NAV/Business Central client and server computers, you must allow outgoing traffic to the following addresses on the specified ports:

| Address                             | Port(s) | Direction | Environment |
| ----------------------------------- | ------- | --------- | :---------: |
| auth.continiaonline.com             | 443     | Outgoing  |  Production |
| demoauth.continiaonline.com         | 443     | Outgoing  |     Test    |
| license.continiaonline.com          | 443     | Outgoing  |  Production |
| demolicense.continiaonline.com      | 443     | Outgoing  |     Test    |
| codownloads.blob.core.windows.net   | 80, 443 | Outgoing  |     Both    |
| notification.continiaonline.com     | 443     | Outgoing  |  Production |
| demonotification.continiaonline.com | 443     | Outgoing  |     Test    |

\


When using on-premises OCR, you must allow outgoing traffic from the ABBYY FineReader/Document Capture service computer to the following addresses on the specified ports:

| Address                                                                     | Port(s)                                                                                       | Direction | Environment |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------- | :---------: |
| registration2.abbyy.com[<sup>1</sup>](<Minimum Requirements.md#footnote-1>) | 80, 443                                                                                       | Outgoing  |     N/A     |
| Your email server                                                           | 143 (unsecured IMAP) or 993 (secure IMAP)[<sup>2</sup>](<Minimum Requirements.md#footnote-2>) | Outgoing  |     N/A     |

\


***

1. The ABBYY activation server is located in Microsoft Azure (The Netherlands).
2. Please refer to our general documentation on this. You can find this in the Continia Document Capture software package, in the Documentation folder.

\


When using Cloud OCR, you must allow outgoing traffic from all NAV/Business Central client and server computers to the following addresses on the specified ports:

| Address                              | Port(s) | Direction | Environment |
| ------------------------------------ | ------- | --------- | :---------: |
| cdc.continiaonline.com               | 443     | Outgoing  |  Production |
| democdc.continiaonline.com           | 443     | Outgoing  |     Test    |
| cocloudocr.blob.core.windows.net     | 443     | Outgoing  |  Production |
| cocloudocrdemo.blob.core.windows.net | 443     | Outgoing  |     Test    |

\


When using the Continia Web Approval Portal hosted by Continia Software (www.continiaonline.com), you must allow incoming traffic from the following addresses and ports to the NAV/Business Central Web Services server:

| Address                                                         | Port(s)                      | Direction | Environment |
| --------------------------------------------------------------- | ---------------------------- | --------- | :---------: |
| EUN IP: 23.102.56.117 (Ireland, covering Northern Europe)       | SOAP service (default: 7047) | Incoming  |  Production |
| USC IP: 13.89.38.96 (Iowa, covering Central US)                 | SOAP service (default: 7047) | Incoming  |  Production |
| AUE IP: 23.101.213.2 (New South Wales, covering East Australia) | SOAP service (default: 7047) | Incoming  |  Production |
| DEMO IP: 40.118.71.119                                          | SOAP service (default: 7047) | Incoming  |     Test    |

\


When using the Continia Delivery Network, you must allow outgoing traffic from all NAV/Business Central client and server computers to the following addresses on the specified ports:

| Address                                     | Port(s) | Direction | Environment |
| ------------------------------------------- | ------- | --------- | :---------: |
| cdnapi.continiaonline.com                   | 443     | Outgoing  |  Production |
| codeliverynetworkprod.blob.core.windows.net | 80, 443 | Outgoing  |     Both    |

\


**If you’re using Continia Expense Management**, traffic to the following two URLs should also be allowed:

* cem.continiaonline.com – port 443 (production)
* democem.continiaonline.com – port 443 (test)

> \[!IMPORTANT] For all of the above, please make sure that no proxy server, antivirus software or the like is blocking your Internet access. Always consult the relevant IT department to ensure that this is in accordance with company rules and regulations.

## Add-in requirements

The minimum required version of .NET Framework for add-ins is version 4.

The drag-and-drop functionality can be used by anyone with a limited or Team Member license. Note that the drag-and-drop feature only works when you use a limited/Team Member license from Document Capture version 6.00 Service Pack 2 or later.

## Citrix and terminal-server requirements

Local scanning isn’t possible if Microsoft Dynamics NAV or Business Central is running from a Citrix or terminal server. Also, when Citrix is used, you may encounter certain performance issues if the Document Capture client components haven’t been installed correctly, for example if the client components haven't been made part of the Citrix image.

## Click Once requirements

When Click Once is used to distribute Microsoft Dynamics NAV or Business Central to clients, the Document Capture client components must be included in the Click Once basic image.

## Archive file server

Document Capture stores all files that are related to imported documents in an archive directory. This directory should be formatted as Windows (NTFS).

For this archive directory, you must set the security permissions listed below. Note that this goes for _all users_ when classic versions of Microsoft Dynamics NAV are used, and for the service account when a service tier is used:

* Modify
* Read & execute
* List folder contents
* Read
* Write

If you’re using a classic version of Microsoft Dynamics NAV and the selected directory is a network-shared folder, this folder must be accessible to all users.

## Azure Blob Storage

For newer versions of Microsoft Dynamics NAV/Business Central (NAV 2013 or later), Document Capture supports archiving of document files using Azure Blob Storage. For more information on Azure Blob Storage, including details on pricing and configuration, see [Azure Blob Storage](https://azure.microsoft.com/en-us/services/storage/blobs/) (Microsoft article).

In order for Azure Blob storage to work, the Dynamics NAV/Business Central service tier must be configured to use the TLS 1.2 security protocol. For further setup details, see \[Setting up Azure Blob Storage]\(/Continia Document Capture/Development and Administration/Setting up Azure Blob storage.md).

> \[!IMPORTANT] It's strongly recommended that you enable [blob soft delete](https://docs.microsoft.com/en-us/azure/storage/blobs/soft-delete-blob-overview) for your Azure Blob Storage accounts, as this allows you to restore any documents or files that were deleted or overwritten by accident.

> \[!CAUTION] It's crucial that Document Capture has full read/write/delete access to the relevant blob container. For example, configuring access policies with time-based retention isn't supported, and neither are immutability and legal hold.

Continia has no further minimum requirements for the use of Azure Blob Storage to store Document Capture files. For any specific questions or requests regarding Azure – including setup, subscription types, and general architecture – please refer to Microsoft.

## Continia File Service

The Continia File Service is built on .NET Core 6, which is supported on Windows Server Core 2012 or later. When you run the installer, .NET Core 6 is installed automatically.

## Additional guidelines

A number of other requirements and recommendations are relevant to mention, as they have an impact on how well Document Capture performs and how the app is used. For more information, see [Additional guidelines for using Continia Document Capture](../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Deployment/@DC-224/).

## Related information

\[Minimum requirements for using Continia Document Capture (Online)]\(/Continia Document Capture/Getting Started/Frequently Asked Questions/Minimum Requirements/Overview.md)\
\[Additional guidelines for using Continia Document Capture]\(/Continia Document Capture/Getting Started/Frequently Asked Questions/Minimum Requirements/Additional guidelines.md)\
\[Overview of business functionality]\(/Continia Document Capture/Getting Started/Business Functionality.md)\
\[Requirements for using Continia Web Approval Portal on premises]\(Web Approval Portal Requirements On-Premises.md)\
[Unsupported standard features](../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Deployment/@DC-134/)\
[Business Central website](https://dynamics.microsoft.com/business-central/overview/)\
[Microsoft's page on Azure Blob Storage](https://azure.microsoft.com/en-us/services/storage/blobs/)\
\[Setting up Azure Blob Storage]\(/Continia Document Capture/Development and Administration/Setting up Azure Blob storage.md)
