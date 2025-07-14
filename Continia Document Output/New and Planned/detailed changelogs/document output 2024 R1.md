---
title: Detailed Changelog for Continia Document Output 2024 R1
description: Detailed Changelog for Continia Document Output 2024 R1
date: 02-10-2024
id: DO-164
lang: en
---

# Detailed Changelog for Continia Document Output 2024 R1

This article lists all new features and bug fixes for each version of Continia Document Output 2024 R1.

> [!TIP]
> As a Continia partner, you can be notified of new Document Output versions and service packs whenever they're released. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360005355319-Receive-a-notification-upon-new-Document-Output-releases) in the Continia PartnerZone (only available to partners).

> [!IMPORTANT]
> Currently, Document Output supports BC v14 and the three latest versions of Business Central. This will change with the release of Document Output 2025 R1 (26.00) in April 2025. **Document Output 2025 R1 (26.00) and all future versions from then on will only support the three latest versions of Business Central**.
> 
> **The next version of Document Output – Document Output 2024 R2 (25.00) – will be the last version with support for Business Central April 2019 (BC v14)**.

## Document Output 2024 R1 Service Pack 2, hotfix 1

*Release date, online: September 26, 2024*  
*App version: 24.2.1*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | When generating multiple reports of different sizes (in bytes), merging could result in unexpected artifacts. This could result on random symbols show or duplicate report results. |

## Document Output 2024 R1 Service Pack 2

*Release date, online: August 30, 2024*  
*Release date, on-premises: August 30, 2024*  
*App version: 24.2.0*  
*FOB version: 24.02*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Bug when opening email and using request page and e-documents at the same time. |
| Delivery Network | All hotfixes from CDN 24.1.x, have now been included in this release. Read more [here](@DO-168). |

## Document Output 2024 R1 Service Pack 1, hotfix 9
*Release date: August 22, 2024*  
*App version: 24.1.9*  
*FOB version: 24.01.09*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Functions in Codeunit CDO Standard NAV Actions have been deleted, not in use anymore. |
| General Application | Service Order documents were not attached. |
| General Application | Permission error on moving log, when document type changed. |
| General Application | Update document record af e-doc. |
| General Application | New FlowFields on Email log, on Posted Sales Documents. |

## Document Output 2024 R1 Service Pack 1, hotfix 8
*Release date: June 26, 2024*  
*App version: 24.1.8*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | The newly added “Handled (DO)” field did not consider generated eDocument files (XML). |
| General Application | Codeunit E-mail Template Management version is now the same version for BC19 and 23 (upgrade issue). |

## Document Output 2024 R1 Service Pack 1, hotfix 7
*Release date: June 20, 2024*  
*App version: 24.1.7*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Update of Delivery Network code, to fix problem with XRechnung3.0. |

## Document Output 2024 R1 Service Pack 1, hotfix 6
*Release date: June 14, 2024*  
*App version: 24.1.6*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | “Handled (DO)” was not set when opening email or printed locally. |

## Document Output 2024 R1 Service Pack 1, hotfix 5
*Release date: June 12, 2024*  
*App version: 24.1.5*  

Only released in Business Central online.

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | Batch job to update Output profile on documents. |
| General Application | Setup Wizard updated to implement Handled (DO) and Email Sending method. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Record not up to date, when No. of E-Docs was updated. |
| General Application | Disabled Output Profile Update on App install. |

## Document Output 2024 R1 Service Pack 1, hotfix 4
Internal release only.

## Document Output 2024 R1 Service Pack 1, hotfix 3
*Release date: June 6, 2024*  
*App version: 24.1.3*  

Only released in Business Central online.

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | All unhandled pages now have No. Printed and Log as Importance = Additional. |
| General Application | Setup Wizard updated to implement Handled (DO) and Email Sending method. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Fixed issue where the E-mail button in the ribbon menu didn’t work when using report selection on the template (on e.g. sales invoice page). |
| General Application | Fixed issue where mails sent using Document Outputs Azure Office 365 Integration wasn’t saved in sent post. |
| General Application | Missing permissions on functions for new handled fields. |

## Document Output 2024 R1 Service Pack 1, hotfixes 1 and 2
Internal releases only.

## Document Output 2024 R1 Service Pack 1

*Release date, online: May 31, 2024*  
*Release date, on-premises: June 04, 2024*  
*App version: 24.1.0*  
*FOB version: 24.01*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | Functionality merging PDF using Continia Online PDF API is improved. |
| General Application | New field for counting of emails sent. Intended to be used instead of “No. Printed” on Documents. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | Progress bar fix, when logs were being moved. |
| General Application | General bugfixes regarding document creation. |
| General Application | Limited file upload filter to not contain “All files (*.*)”. |

## Document Output 2024 R1, hotfix 1

*Release date, online: May 3, 2024*  
*App version: 24.0.1*  

Only released in Business Central online.

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | Beta: Use SaveReportAsPDFInTempBlob on Report Selection. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | PDF Upload filter limited to only \*.pdf for the BackgroundPDF feature. |
| Documents and Templates | Email changed from text80 to text250 in the table E-Mail recipients. |
| General Application | Caption fixes. |
| General Application | Fixed issue where statement PDF was not added to the email when using “Email all” on the Customer Statement Journal page. |

## Document Output 2024 R1

*Release date, online: April 2, 2024*  
*Release date, on-premises: April 15, 2024*  
*App: 24.0.0*  
*Fob version: 24.00*  

> [!NOTE]
> With its 2024 spring release, Document Output will make a version leap from 9.00 to 24.00, meaning that versions 10.00–23.00 don't exist and never will. This was done in order to align the versioning of Document Output with that of Microsoft Dynamics 365 Business Central.

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | Templates updated to include new MergeTable showcase examples and updated Advertise logo. |
| Documents and Templates | Reorganized email template design for better UI and better standard BC appearance. |
| Documents and Templates | Updated HTML Editor. MergeFields are now presented as a marked text and not a %code. |
| Documents and Templates | Ability to exclude the Report PDF from email. |
| Documents and Templates | Use new Report Layout. |
| General Application | Added Factboxes to Email Template List, including direct link to HTML Editor. |
| General Application | Now possible to build a table in emails (MergeTable), which can organize Mergefields or add posted data lines from source document. |
| General Application | Ability to merge multiple attachments or send as separate files in same email. |
| General Application | The internal version of Document Output 2024 R1 has been updated to 24.00 (the internal version of Document Output 2023 R2 was 12.00). The change aims to align the Continia solution versions with those of Business Central, making it simpler for for Continia partners to tell which versions of the solutions are compatible. The synchronization is particularly crucial for the Continia Core and Continia Delivery Network extensions |
| General Application | Digital Voucher support in supported OnPremise version (BC14-BC22). |
| General Application | Better Azure Blob Storage error messages and action to test connection. |
| General Application | Simplified Output profile selection on Customer card. |
| General Application | Ability to choose Datacenter in Core. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | Missing statement PDF if Output  = Email in statement journal due to CalcFields in SendMail (Table 6175287). |
| Documents and Templates | Error when creating automatic statement where output = email. |
| Documents and Templates | Removed table-wrapper form generated table and added editable=”false” attribute instead. |
| Documents and Templates | Fixed typo and make UpdateFilterWithMark public on page 6175284 “CDO E-mail/Print Statement”. |
| Documents and Templates | Obsolete Customer Setup records need to be deleted so table do not need permissions. |

<style>
  .content table tr td:nth-child(1) {
    width: 200px;
  }
</style>