---
title: Detailed Changelog for Continia Document Output 2022 R1
description: Detailed Changelog for Continia Document Output 2022 R1
date: 09-04-2024
lang: en
---

# Detailed Changelog for Continia Document Output 2022 R1

This article lists all new features and bug fixes for each version of Continia Document Output.

> [!IMPORTANT]
> This version of Document Output is no longer supported. As a consequence of this, Continia will no longer correct any errors appearing in this version, and no further service packs relating to the version will be released. For supported versions of Document Output, see [Software Lifecycle Policy and Continia Document Output On-Premises](@DO-42).

> [!TIP]
> As a Continia partner, you can be notified of new Document Output versions and service packs whenever they're released. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360005355319-Receive-a-notification-upon-new-Document-Output-releases) in the Continia PartnerZone (only available to partners).

## Document Output 2022 R1 Service Pack 2, hotfix 2

*Released: August 26, 2022*  
*App version: 6.2.0.2*  
*FOB version: 6.02.02*  
*Continia Core 6.02*  
*Continia Delivery Network version: 3.02.3 / 3.2.0.3*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application |	From BC18 or later, Document Output apps are converted to Cloud apps. A new on-prem app can be installed to get file access. DO SMTP access. It also supports PDF manipulation with DLL instead of users having to use Continia Online for that. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application |	Fixed an error regarding the balance due merge field on templates. |
| General Application |	Fixed a bug regarding finding template for vendor remittance advice. |

## Document Output 2022 R1 Service Pack 2, hotfix 1

*Released: July 11, 2022*  
*App version: 6.2.0.1*  
*FOB version: 6.02.01*  
*Continia Core 6.02*  
*Continia Delivery Network version: 3.02 / 3.2.0.0*  


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application |	Permission error on unhandled page (Tiles) has been fixed. |
| General Application |	New permission set has been added to the App version from BC18. It includes permissions to pages, code units, and reports. |
| General Application |	New OnPrepareMail event has been added. The event can be used to modify the email subject and body. |

## Document Output 2022 R1 Service Pack 2

*Released: June 24, 2022*  
*App version: 6.2.0.0*  
*FOB version: 6.02.00*  
*Continia Core version: 6.02*  
*Continia Delivery Network version: 3.02 / 3.2.0.0*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application |	Factbox with Merge Fields on edit signature. |
| General Application | New CU for Setup Management CDO Setup Management. |
| General Application | New Pro Forma Invoice Actions on Sales Orders. |
| General Application | You can now add Reminder e-document codeunits to e-documents. |
| General Application | Append e-document to PDF (OnPremise only). |
| General Application | In DO Setup you can now check “Only use Output Profiles”, and you can convert the existing setup on Customer or Customer Template Setup to Output profiles. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application |	Remittance Report Fixes. |
| General Application |	Removed print from queue when recipient was empty. |
| General Application |	Error when using print/email all from issued reminders is fixed. |
| General Application | Combine Document can now handle tables with 20 fields in primary keys | 

## Document Output 2022 R1, hotfix 1

*Released: April 20, 2022*  
*App version: 6.1.0.1*  
*FOB version: 6.01.01*  
*Continia Core and Continia Delivery Network version: 3.01 / 3.1.0.0*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application |	New Picture Merge Field, and Format String on Template Merge Fields. |
| General Application |	Fixed CC and BCC Recipients now with merge fields. |
| General Application |	Email Template Management, CreatePDFDoc, fixed when ReportID is 0. |
| General Application |	Automatic Statement did not calculate balance with end date. |
| General Application |	Fixed error when creating log where storage type = File System. |
| General Application |	Improved email recipients page and check for valid email address. |
| General Application |	Improved use of Ship-To Code as email address. |
| General Application |	Added event OnGetLanguageCodeFieldNo to E-mail jobs. |
| General Application |	Limit count to 1000 on unhandled pages for better performance. |

## Document Output 2022 R1 Service Pack 1

*Released: April 1, 2022*  
*App version: 6.1.0.0*  
*FOB version: 6.01.00*  
*Continia Core and Continia Delivery Network version: 3.01 / 3.1.0.0*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application |	Better error handling when generating PDFs. |
| General Application | New Page for downloading country Templates. |
| General Application | Email signature implementation. |
| General Application | You can now show and Lookup on “From Address” on email in NAV/BC. |
| General Application | OAuth authentication is now an option in Document Output Service. |

## Document Output 2022 R1

*Released: March 1, 2022*  
*App version: 6.0.0.0*  
*FOB version: 6.00.00*  
*Continia Core and Continia Delivery Network version: 3.00 / 3.0.0.0*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application |	Assisted Setup re-designed. |
| General Application | New retry count on email queue, added max. retry count to DO Setup under general. |
| General Application | Added Purchase Invoice and Purchase Receipt to possible report selections. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Fixed a problem when opening an email from log where an Outlook template was used. |
| General Application | Table Email Recipients, change Clustered = No on Key2, for consistency between fob, apps and cloud. |
| General Application | Fixed logo attachment error from new logo merge field. Mail was sent with logo as ATT00001. |
| General Application | Fixed multiple places where Flowfield length was too short. |




<style>
  .content table tr td:nth-child(1) {
    width: 200px;
  }
</style>