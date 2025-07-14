---
title: Detailed Changelog for Continia Document Output 2021 R2
description: Detailed Changelog for Continia Document Output 2021 R2
date: 21-01-2022
lang: en
---

# Detailed Changelog for Continia Document Output 2021 R2

This article lists all new features and bug fixes for each version of Continia Document Output.

> [!IMPORTANT]
> This version of Document Output is no longer supported. As a consequence of this, Continia will no longer correct any errors appearing in this version, and no further service packs relating to the version will be released. For supported versions of Document Output, see [Software Lifecycle Policy and Continia Document Output On-Premises](@DO-42).

> [!TIP]
> As a Continia partner, you can be notified of new Document Output versions and service packs whenever they're released. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360005355319-Receive-a-notification-upon-new-Document-Output-releases) in the Continia PartnerZone (only available to partners).

## Document Output 2021 R2 Service Pack 3

*Released: February 4, 2022*  
*Cloud and app version: 5.3.0.0*  
*FOB version: 5.03*  
*Continia Core version: 5.02*  
*Continia Delivery Network: 2.03/2.3.0.0*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Output profile for OIOUBL format added (file export only). |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | If you don't have access to the table shown in the tile, the role center fails. Fixed by Access By Permission on Unhandled page for Role Center. |
| General Application | Improved performance log. |
| General Application | Max. email per minute on CDO Setup, for BC18 and later. |
| General Application | CDN AccessByPermission on Customer Setup Card. |
| General Application | Fixed problem when importing more than one template line. |
| General Application | Setting Engine to Excel or Work on template did not work. |
| General Application | New HTML editor 2.0.4.0. |

## Document Output 2021 R2 Service Pack 2

*Released: November 30, 2021*  
*App version: 5.2.0.0*  
*FOB version: 5.02.00*  
*Continia Core version: 5.01*  
*Continia Delivery Network: 2.2.0.0*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Fixed error in version number in “About Continia Document Output”. |
| General Application | From address was filled out in log. |
| General Application | Support of standard pager “Email Account” from BC18 and forward. |
| General Application | New events OnBerforeInsertSignature, OnGetReportSelection - OnGetReportIDFromTable - OnGetReportSelectionFromTable - OnSetRecipientsSetCustomeFilter - OnEMailRecipientsField - OnLookupSetFilter. |

## Document Output 2021 R2, hotfix 1

*Released: October 21, 2021*  
*App version: 5.1.0.2*  
*FOB version: 5.01.02*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Error when “No. Printed” when sending e-docs. |
| General Application | On Table Statement Journal Line, Customer Name is changed from 50 char to 100 char. |
| General Application | When running e-mail jobs the “Template Code” was not used in all code paths. |
| General Application | Standard filter on unhandled pages were language dependant. |
| General Application | HTMLEditor 2.0.2 did not support Danish letters æøå. This has been fixed. |

## Document Output 2021 R2 Service Pack 1

*Released: October 4, 2021*  
*App version: 5.1.0.0*  
*FOB version: 5.01.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | BC 19 support |
| General Application | Option to zip attachments |
| General Application | New HTML Editor 2.0.2 |
| General Application | Now possible to delete multiple attachments on e-mail page |
| General Application | New zip function on mail Attachment factbox |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Fix in template selection when using variant and language code |
| General Application | Fix editable on Merge Fields Table No. |
| General Application | Fixed bug sending automatic statement from Job Queue |

## Document Output 2021 R2

*Released: September 1, 2021*  
*App version: 5.0.0.0*  
*FOB version: 5.00.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application |	New Reply activity on NAV/BC e-mail. |
| General Application | It is now possible to lookup and see “From Adress” on e-mail in NAV/BC. |
| General Application | New HTML Editor 2.0.1. |
| General Application | New Picture Merge Field, and Format String on Merge Fields. |
| General Application | Signatures is now used on default templates. |
| General Application |	New “From E-Mail Address Field” on templates. |
| General Application | “From E-Mail Address” is added to Log. |
| General Application |	New sales and purchase blanket order templates. |
| General Application |	Easy setup wizard – With option for Full or Custom setup. |
| General Application. | XML Export: It is now possible to export Service documents in both the PEPPOL and XRechnung electronic documents format |
| General Application | XML Export: Documents with Prices Including VAT can now be exported. |
| General Application | XML Export: Improved Codeunit 6086231 CTS-CDN XML Library so that it can be used to customize the content of the PEPPOL or XRechnung electronic documents. |
| Platform and Technology | XML Export: Introduced a new Event Publisher OnBeforeCreatePaymentMeans which can be used to setup FIK Payment values. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | XML Export: In some cases when trying to send a document via PEPPOL Network, the following error was thrown: “You are trying to send a network document (xxxxxx) to customer xxxxxxx, who is not registered in the network.” |
| General Application | XML Export: In some cases when trying to send a document via PEPPOL Network, the following error was thrown: “Unable to convert from Microsoft.Dynamics.Nav.Runtime.NavXmlNode to Microsoft.Dynamics.Nav.Runtime.NavXmlElement.” |
| General Application | XML Export: When trying to create a PEPPOL or XRechnung document the following error was thrown: “The length of the string is xx, but it must be less than or equal to 10 characters.” |
| General Application | XML Export: A PEPPOL or XRechnung document was not created correctly when using Reverse Charge VAT setup. |




<style>
  .content table tr td:nth-child(1) {
    width: 200px;
  }
</style>