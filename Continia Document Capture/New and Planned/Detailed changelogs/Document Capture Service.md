---
title: Detailed changelogs for the Continia Document Capture Service
date: 19-08-2025
description:  
id: DC-133
lang: en
---

# Detailed changelogs for the Continia Document Capture Service

This article lists all the changes that have been carried out for the Continia Document Capture Service and all related service packs.

> [!TIP]
> As a Continia partner, you can be notified of new Document Capture versions and service packs whenever they're released. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360005355079-Receive-a-notification-upon-new-Document-Capture-releases) in the Continia PartnerZone (only available to partners).

> [!IMPORTANT]
> When you upgrade the Document Capture Service to a newer version, you must also export the OCR configuration files. If you fail to do so, new features that depend on settings in the OCR configuration files won't work as expected (such as the import of emails using EWS or the creation of PNG image files).

## Document Capture Service 26.02

*Released: August 19, 2025*

### Bug fixes

| Functional area | Description                                                  | ID   |
| --------------------------------------------------------- | ------------------------------------------------------------ | ---- |
| Platform and Technology |Prior to this, incoming ZUGFeRD and PDF files could receive the same filename in some cases. |68329|

## Document Capture Service 26.01

*Released: August 4, 2025*

### Bug fixes

| Functional area | Description                                                  | ID   |
| --------------------------------------------------------- | ------------------------------------------------------------ | ---- |
| Platform and Technology |Improved the handling of ZUGFeRD documents with multiple files. |62470, 66926|
| Platform and Technology |Due to a bug introduced in version 26.00, the retrieval of emails from EWS was failing in some cases. |67871|
| Platform and Technology |Removed the ability to recognize documents from scanners. |-|

## Document Capture Service 26.00

*Released: June 18, 2025*

### Bug fixes

| Functional area | Description                                                  | ID   |
| --------------------------------------------------------- | ------------------------------------------------------------ | ---- |
| Platform and Technology |Updated to .NET 8.0. |-|
| Platform and Technology |The x86 version of the service has been deprecated. Now, only the x64 version is supported. |-|

## Document Capture Service 25.02

*Released: February 18, 2025*

### Bug fixes

| Functional area | Description                                                  | ID   |
| --------------------------------------------------------- | ------------------------------------------------------------ | ---- |
| Platform and Technology |When extracting XML from a ZUGFeRD PDF, the email file was given an incorrect name. |62692|
| Platform and Technology |Upgraded NuGet packages to fix vulnerabilities. |-|

## Document Capture Service 25.01

*Released: December 10, 2024*

### Bug fixes

| Functional area | Description                                                  | ID   |
| --------------------------------------------------------- | ------------------------------------------------------------ | ---- |
| Platform and Technology |Prior to this, barcodes could not contain new lines or carriage returns. |61272|

## Document Capture Service 25.00

*Released: October 1, 2024*

### New or changed functionality

| Functional area | Description                                                  | ID   |
| --------------------------------------------------------- | ------------------------------------------------------------ | ---- |
| Platform and Technology |Added support for Google Workspace accounts (Gmail) using service accounts. To switch from AppPassword to service account, add a GoogleServiceAccount.json file to the category input directory. |57325|
| Platform and Technology |Added support for the Microsoft Graph API. To switch from EWS to Microsoft Graph, add an MsGraphEmail (no extension, no content) file to the category input directory. |57325|
| Platform and Technology |The x86 version of the Document Capture Service is no longer supported, now only x64 is supported. ||
| Platform and Technology |Preventing incorrect, double encoding of XML special characters (such as '>' in FIK codes). ||

## Document Capture Service 24.01

*Released: August 7, 2024*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID   |
| --------------------------------------------------------- | ------------------------------------------------------------ | ---- |
| Platform and Technology                                   | Better sanitization of XML values from emails, such as removing invalid characters. |      |
| Platform and Technology                                   | Support for ABBYY FineReader Engine 12.6 (downloaded separately). |      |

## Document Capture Service 24.00

*Released: April 11, 2024*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | The version number has been syncronized with the Document Capture version number. |
| Platform and Technology | Added "EmlInbox" and "EwsInbox" to categories, so that raw .eml files can be processed without the actual inbox. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | Fixed a user interface bug to enable the service to start after being stopped manually. This only applies when the program is started directly from the .exe file – not when you run it as a windows service. |
| Platform and Technology | Fixed a bug where the content type **multipart/related** was spelled incorrectly as **multipart/relatid**. Related work items: 54398 |

## Document Capture Service 12.02
*Released: December 18, 2023*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | Fixed issue to avoid the service from shutting down while processing scanned images. Related work items: 52002 |

## Document Capture Service 12.01
*Released: December 4, 2023*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | Embedded XML files have been sanitized for invalid characters. Some of these started with a *zero-width no-break space* character but were otherwise valid. |
| Platform and Technology | PDF files that fail during embedded XML checks will no longer block other PDF files from being processed. |

## Document Capture Service 12.00
*Released: October 2, 2023*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | Updated the Abbyy FineReader Engine from 12.5.15.0 to 12.5.15.7. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | Fixed issue where the Abbyy FineReader Engine would fail with "Internal program error" and refer to Type3FakeFontFile.cpp for some PDF files. |
| Platform and Technology | Fixed issue where the engine would fail with "IPE: EnumConverterFT.h" in the error message. |
| Platform and Technology | Added support for "profile.reset.ini", which can be used to reset the "profile.ini" settings to default values. |

## Document Capture Service 11.02
*Released: July 13, 2023*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | Fixed issue with attachments that are processed from the **Temp** folder. |
| Platform and Technology | When a document fails during import, any generated TIFF and PNG files are now automatically removed. |
| Platform and Technology | When a file is locked, a message is now logged in the application log. |

## Document Capture Service 11.01
*Released: May 1, 2023*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | Fixed issue with missing email information when processing PDF files containing restrictions. |
| Platform and Technology | When the maximum number of pages to OCR is set to 0, we will fall back to the default value of 200 pages. |
| Platform and Technology | Fixed issue with PDF files not getting moved to the **Error** folder when an error occurred at some point following the OCR process. |


## Document Capture Service 11.00
*Released: March 27, 2023*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | EWS Client now supports subfolders. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | Invalid characters in attachment file names resulted in an error. |
| Platform and Technology | Updated Configuration Manager with new Continia branding. |

## Document Capture Service 10.02
*Released: February 8, 2023*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | Resize issue when PDF pages did not share the exact image resolution. |
| Platform and Technology | If an error occurs during service start-up, it will be displayed in the Configuration Manager. |
| Platform and Technology | If a TIFF file cannot be generated, an error will be raised. |

## Document Capture Service 10.01
*Released: November 24, 2022*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | An error during e-mail download resulted in re-download of the entire e-mail batch. |
| Platform and Technology | Attachments without a file-extension will now be OCR processed if the files content-type is *application/pdf*. |
| Platform and Technology | Attachments on e-mails with digital signature were not OCR processed. |
| Platform and Technology | Long e-mail subject resulted in failed processing. |
| Platform and Technology | Attachments starting with the letters LOG triggered an internal logging function. |

## Document Capture Service 10.00
*Released: October 7, 2022*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | Installing Windows Service as "Automatic" and with a dependency to ABBYY FineReader engine if present. | |
| Platform and Technology | Email attachments will have unique timestamps. | |
| Platform and Technology | Automatically changes License if multiple licenses available and one runs out of pages. | |
| Platform and Technology | AutoCorrectOrientation has been disabled per default. | |
| Platform and Technology | Correct skew on TIFF files. | |
| Platform and Technology | All processed xml documents contain detailed version of which ABBYY version was used (e.g. 12.5.6.12). | |

## Document Capture Service 9.00
*Released: March 1, 2022*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | Updated to .Net Framework 4.7.2. | |
| Platform and Technology | Emails with no recipient can be processed. | |
| Platform and Technology | Validation of EWS configuration. | |
| Platform and Technology | Access restrictions will be removed from PDF files if configured. | |
| Platform and Technology | Updated Configuration Manager to display DC service version. | |
| Platform and Technology | Updated referenced third-party libraries. | |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | Fixed issue with duplicated documents. | |

## Document Capture Service 8.01
*Released: October 1, 2021*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology |We have updated the ABBYY Installer to contain a newer version of ABBYY (12.5.6.12).<br>The full changelog of the ABBYY version can be read here:<a href="https://www.abbyy.com/finereader-engine-downloads/windows/">https://www.abbyy.com/finereader-engine-downloads/windows/</a><br><br>As we have only changed the ABBYY component, we have not changed the version number of the installed Continia Document Capture for NAV - Service (x64). the version number is still 8.00.|27260|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Documents and Templates|When capturing a value, sometimes the value is captured twice in the same field and separated by a space. E.g., the amount on the invoice was &quot;15.65&quot;, but the value captures was &quot;15.65 15.65&quot;. The issue has been corrected in ABBYY 12.5.|24795|

## Document Capture Service 8.00
*Released: September 1, 2021*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| Documents and Templates | With the release of Document Capture 2021 R2 (8.00), we have limited the number of pages that can be processed to a maximum of 500 pages. | 23518 |
| Platform and Technology | Fixed an issue where the OCR Service, in some cases, did not process email attachments if the email was signed. | 23961 |

## Document Capture Service 7.00
*Released: April 9, 2021*   

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
|  Technology | Fixed an issue in the Document Capture Service when downloading attachments from email accounts using EWS. When the error occurred, emails for the relevant document category were not processed. The event log displayed the following: <ul><li>Unable to cast object of type 'Microsoft.Exchange.WebServices.Data.ItemAttachment' to type 'Microsoft.Exchange.WebServices.Data.FileAttachment'".</li></ul> |
|  Technology | Fixed an issue where the Document Capture service failed when running EWS and checking an email with no attachments. |
|  Technology | We have updated the ABBYY Installer to contain a newer version of ABBYY (12.4.7.63). The full changelog of this version can be read here: [Changelog for ABBYY FineReader Engine 12 for Windows](https://www.abbyy.com/media/29524/release_notes_fre12_win_r4u3.pdf) |

## Document Capture Service 6.50.02
*Released: November 23, 2020*   

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Technology | Fixed an issue where the Document Capture service would use the PDF file to create the png-files used for showing the document pages in the web client. However, that behavior was not correct, as the OCR processing is based on a skew-corrected version of the document. This issue could cause the process of manually capturing values in the web client to produce unexpected results. <br><br> The service has now been changed to obtain the correct coordinates aligned with the web client's visual presentation. |

## Document Capture Service 6.50
*Released: October 27, 2020*   

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Technology | We have changed the installer for the Document Capture OCR Service, as we saw issues where the 6.05 installer would not upgrade the files in the program folder. The contents of the installer are the same as for 6.05, so if you have installed 6.05 and experience no issues, it is not necessary to install this update. However, if you experience problems processing PDF-files (version 2.0), we recommend uninstalling the 6.05 service and installing this version. |

## Document Capture Service 6.05
*Released: August 5, 2020*   

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Technology | We have corrected an issue with Pdf 2.0 files that would cause the service to enter an infinite loop. |
| Technology | We have corrected an issue where QR codes would produce invalid characters, making the files impossible to import into the document journal. |

## Document Capture Service 6.04
*Released: June 3, 2020*   

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Technology | We have added support for capturing the full content of QR barcodes in the Document Capture OCR service. |
| Technology | When using an older version of the Document Capture OCR Service, the PNG files of a document was not created. Therefore, when the document was split, merged, or move to another company, a corrupted/empty PNG file was created. When viewing the document using the Web Client, a blank document was shown. |

## Document Capture Service 6.01
*Released: February 13, 2020*   

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Technology | With version 12 of the ABBYY service, text in some documents was recognized wrongly. The recognition parameters have been altered to fix this issue in the new version of the on-premises OCR service. |

<style>
  .content table tr td:nth-child(1) {
    width: 35px;
  }
  .content table tr td:nth-child(2) {
    width: 500px;
  } 
  .content table tr td:nth-child(3) {
    width: 35px;
  }
</style>