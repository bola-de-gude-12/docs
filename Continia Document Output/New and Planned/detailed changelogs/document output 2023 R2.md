---
title: Detailed Changelog for Continia Document Output 2023 R2
description: Detailed Changelog for Continia Document Output 2023 R2
date: 11-03-2024
id: DO-132
lang: en
---

# Detailed Changelog for Continia Document Output 2023 R2

This article lists all new features and bug fixes for each version of Continia Document Output 2023 R2.

> [!TIP]
> As a Continia partner, you can be notified of new Document Output versions and service packs whenever they're released. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360005355319-Receive-a-notification-upon-new-Document-Output-releases) in the Continia PartnerZone (only available to partners).

## Document Output 2023 R2 Service Pack 1, hotfix 4

*Released: March 11, 2024*  
*Continia Core: 9.1.0.257458*  
*Continia Delivery Network version: 6.1.3.317447*  
*Cloud version: *9.1.4.344592*  

Only released to app and cloud.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | Improved UI specifically on Email Templates. |
| Documents and Templates | Fixed permission on table 297 Issued Reminder Header in 6175307 CDO Electronic Document Mgt. |
| Documents and Templates | Did not find statement recipients on Customer Card. |
| Documents and Templates | Fixed error where the combine per vendor did not work on vendor remittance advice. |

## Document Output 2023 R2 Service Pack 1, hotfix 3

*Released: February 6, 2024*  
*Continia Core: 9.1.0.257458*  
*Continia Delivery Network version: 6.1.2.306483*  
*Cloud version: 9.1.3.310561*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Periodic display error when filtering on page Fields (With Relation). |
| General Application | Did not find statement recipients on Customer Card. |

## Document Output 2023 R2 Service Pack 1, hotfix 2

*Released: February 6, 2024*  
*App version: 9.1.2*  
*Continia Core: 9.1.0.257458*  
*Continia Delivery Network version: 6.1.2.306483*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | French language fixed for uploading files. PDF, certificate etc. |
| General Application | Permission error on Document Output log, when showing factbox. |
| General Application | On E-mail/print statement page, filtering on automatic statements was not working. |
| General Application | Document Output tables that should not be synchronized between companies as master data, is now blocked with an error (example could be log tables etc. |
| General Application | New Event on e-mail/print statement page. |
| General Application | hen building DO extensions, min and max object range was missing in app json. |
| General Application | When opening DO mails from the menu bar, GetView(true) is changed to GetView(false) to avoid problems, when using local languages. |
| Documents and Templates | It was possible to send emails without attachments from automatic statements. |
| Documents and Templates | With the Document Output On-Premise App, embed file (XML) to PDF did not work. |

## Document Output 2023 R2 Service Pack 1

*Released: January 20, 2024*  
*App version: 9.1*  
*Continia Core: 9.1.0.257458*  
*Continia Delivery Network version: 6.1.0.256840*  
*Cloud version: 9.1.1.296607*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | Option to combine (merge) documents to one email, or have multiple files in one email. |
| Documents and Templates | Search field on Field lookup on Merge Fields. |
| Documents and Templates | Error when sending all mails from statement journal. |
| Documents and Templates | Customer Setup records with no output profile was not converted to customer table extension on upgrade. |
| Documents and Templates | It was possible to search for the old Page Customer Setup List 6175318 (obsolete). |
| Documents and Templates | Fixed several special character display bugs (e.g. æøå). |

## Document Output 2023 R2, hotfix 5

This hotfix is only released to the cloud version of Document Output.

*Released: December 15, 2023*  
*Continia Core: 9.0.0.181397*  
*Continia Delivery Network: 6.0.2.230418*  
*Cloud version: 9.0.5.249204*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Fixed a Delivery Network dependency needed to run the Demo Portal. |

## Document Output 2023 R2, hotfix 4

*Released: November 20, 2023*  
*App version: 9.0.4.0*   
*Continia Core: 9.0.1.185245*  
*Continia Delivery Network: 6.0.0.230418*  
*Cloud version: 9.0.4.235568*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | You can now set request page on reports on template line. |
| Documents and Templates | Output Profile problem introduced with DO 9.0.3 has now been fixed. |

## Document Output 2023 R2, hotfix 3

*Released: November 14, 2023*  
*App version: 9.0.3.0*   
*Continia Core: 9.0.1.185245*  
*Continia Delivery Network: 6.0.0.222462*  
*Cloud version: *9.0.3.227561*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Platform and Technology | Move logs as a background task and improved the process. |
| Platform and Technology | Action Remittance advise on Payment Journal moved to Document Output group. |
| Platform and Technology | Output Profile added to Customer and Vendor Template. Moved Customer and Vendor setup table to table extensions. (BC19 and later). |
| General Application | Removed Text250 limit on merge field codeunit. Added function SetValue to the record. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Fixed issue where all Output Profiles were set to skip on App upgrade. |
| General Application | Local print did not work on remittance advice. |
| General Application | Automatic statements generated wrong end date when there were periods without statement. |

## Document Output 2023 R2, hotfix 2

*Internal release only*  

## Document Output 2023 R2

*Released: October 10, 2023*  
*App version: 9.0.1.0*   
*Continia Core: 9.0.1.185245*  
*Continia Delivery Network: 6.0.0.181398*  
*Cloud version: 9.0.0.181486*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | Factbox on email Templates, showing email recipient lookup options, Log and Attachments. |
| General Application | Enhanced Output Profile functionality on Document Output Setup and more profiles added. |
| General Application | More email recipient flexibility, for locating the recipient email address through a prioritized list. |
| General Application | Integration to Azure BLOB Storge for log backup. |
| General Application | Automatic AL Extensions in Custom-made email templates. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Fixed several missing language captions. |

<style>
  .content table tr td:nth-child(1) {
    width: 200px;
  }
</style>