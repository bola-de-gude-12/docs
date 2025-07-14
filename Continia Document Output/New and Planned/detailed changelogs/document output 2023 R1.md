---
title: Detailed Changelog for Continia Document Output 2023 R1
description: Detailed Changelog for Continia Document Output 2022 R2
date: 07-09-2023
id: DO-76
lang: en
---

# Detailed Changelog for Continia Document Output 2023 R1

This article lists all new features and bug fixes for each version of Continia Document Output 2023 R1.

> [!TIP]
> As a Continia partner, you can be notified of new Document Output versions and service packs whenever they're released. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360005355319-Receive-a-notification-upon-new-Document-Output-releases) in the Continia PartnerZone (only available to partners).

## Document Output 2023 R1 Service Pack 2, hotfix 2

*Released: September 7, 2023*  
*App version: 8.2.2*  
*Continia Core: 8.2.0.357209*  
*Continia Delivery Network version: 5.2.0.356855*  
*Cloud version: 8.2.2.158664*

### New or changed functionality

| Functional area         | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Documents and Templates | New table for Recipients setup or Template. You can now have a prioritized list on how to find the recipient on a template.           |
| General Application     | Sets Output Profiles on Customers and Vendors to EMAIL. |
| General Application     | New events on Export and Import XML. |

### Bug fixes

| Functional area         | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Documents and Templates | Fixed double request page on Print PDF. |
| Documents and Templates | Fixed Vendor on delete subscriber. |
| General Application     | Permission sets fixed. |

## Document Output 2023 R1 Service Pack 2, hotfix 1
*Internal release, never published*

## Document Output 2023 R1 Service Pack 2

*Released: September 1, 2023*  
*App version: 8.2*  
*Continia Core: 8.2.0.357209*  
*Continia Delivery Network version: 5.2.0.356855*  
*Cloud version: 8.2.0.152538*

### New or changed functionality

| Functional area         | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Documents and Templates | Filter on “Use as attachment” on report selection.           |
| Documents and Templates | Introduced the capability to set a new end date for signatures. |
| Documents and Templates | Implemented a new table to configure recipients in templates. This feature empowers users to establish a prioritized recipient hierarchy. |
| General Application     | Integrated a fresh setup option that enables skipping mail processes when customers/vendors lack output profiles. |
| General Application     | Addition of a new Event: "OnBeforeGetOutputProfile"          |
| Delivery Network        | The Delivery Network is now added to Document Output Role Center. |

## Bug fixes

| Functional area         | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Documents and Templates | To ensure that email jobs do not process incomplete records, the record is locked. |

## Document Output 2023 R1 Service Pack 1, hotfix 2

*Released: July 7, 2023*  
*App version: 8.1.2*  
*Continia Core: 8.1.0.273509*  
*Continia Delivery Network version: 5.1.0.270381*  
*Cloud version: 8.1.2.96542*

### New or changed functionality

| Functional area         | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Documents and Templates | When downloading templates, the default language will be German for Austria (AT) and Switzerland (CH). If the country is not supported, the default language is W1. |
| Documents and Templates | The "From Address" will be displayed when the User Setup is selected on a template. |
| General Application     | Printer selection has been improved by storing and providing access to related service information (configuration, printers, and so on.) in BC. |
| General Application     | A new event called "OnBeforeCreateAndSendMail" has been added. |
| General Application     | New events have been introduced: "OnBeforeEDoc()", "OnAfterEDoc()", "OnAfterPrint()", and "OnLogCreated()" |

### Bug fixes

| Functional area         | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Documents and Templates | The email recipient field in the E-mail recipients table has been changed from a limit of 80 characters to 250 characters. |
| Documents and Templates | An issue has been fixed where PDF files could contain e-document data. |
| Documents and Templates | Improvements have been made regarding finding recipients and sending Document Output emails. |
| General Application     | The Warehouse FactBox on a sales order now checks for read permission on Warehouse Employee. |
| General Application     | An email template line record has been added to the Event Publisher "OnBeforeCreateDocumentExt." |



## Document Output 2023 R1 Service Pack 1, hotfix 1

*Released: June 20, 2023*  
*App version: 8.1.1*  
*Continia Core: 8.1.0.273509*  
*Continia Delivery Network version: 5.1.0.270381*  
*Cloud version: 8.1.0.79512*

### New or changed functionality

| Functional area         | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| General Application     | Added functionality to skip emails when enabling a Participant code (Delivery Network) in Output. |
| Documents and Templates | Introducing a new filter option to use attachments on report selection. |

### Bug fixes

| Functional area         | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Documents and Templates | Fixed an issue where Remittance Email did not function correctly from vendor ledger entries. |
| Documents and Templates | Resolved a problem where the with and without email filter did not work on email remittance. |
| Documents and Templates | Improved the process of identifying recipients and sending Document Output emails. |
| General Application     | Included an email template line record to the Event Publisher (BeforeCreateDocumentExt.) |
| General Application     | Variant Codes longer than 20 characters will be truncated to 20 characters. |



## Document Output 2023 R1 Service Pack 1

*Released: June 7, 2023*  
*App version: 8.1*  
*Continia Core: 8.1.0.27359*  
*Continia Delivery Network version: 5.1.0.270381*  
*Cloud version: 8.1.0.67569*

### New or changed functionality

| Functional area         | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| General Application     | Skipped documents are now logged as *skipped* for easy tracking. |
| General Application     | Added a new function *get FixedRecipients* to the CDO email code unit. |
| General Application     | Introduced new events: *OnBeforeDocumentIsProtected* and *OnAfterCreateDocument* |
| General Application     | Users utilizing Azure Application (Office 365) can now use read and delivery receipts for requests. |
| General Application     | Email logs can now be stored as Azure Blobs for improved storage efficiency. |
| Documents and Templates | Added a new feature called *Disable Combine Documents* on template lines. |
| Documents and Templates | Introduced two new FactBoxes on the Template Card: *Attachment* and *Log*. |
| Documents and Templates | The Purchase and Service Orders FactBoxes now have new post and handle functionality |

### Bug fixes

| Functional area         | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Documents and Templates | Address lookup issue with the "From" field is solved, and recipients are now properly displayed in the "cc" and "bcc" fields on the Email page. |
| Documents and Templates | Unable to set the request page when using Report Selection on a template. |
| Documents and Templates | Multiple reports in the report selection caused Open Documents to create two documents. |
| General Application     | The sending method was not included when resending an email from a log. |

## Document Output 2023 R1, hotfix 3

*Released: May 10, 2023*  
*App version: 8.0.3*  
*Continia Core: 8.0.0.222572*  
*Continia Delivery Network version: 5.0.0.208932*  
*Cloud version: 8.0.3.37574*

### New or changed functionality

| Functional area     | Description                                                  |
| ------------------- | ------------------------------------------------------------ |
| General Application | It is now possible to use plain text as the body of an email. |
| General Application | New PDF dll for BC22.                                        |

### Bug fixes

| Functional area         | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Documents and Templates | Preserve links when using Background PDF.                    |
| Documents and Templates | Could not set the request page when using Report Selection on a template. |
| General Application     | Do not send an e-doc when opening an email.                  |
| General Application     | Delete the CDO Vendor Setup when a Vendor is deleted.        |
| General Application     | Several table options are replaced by enums.                 |
| General Application     | CDO Report Selection Usage now uses enums.                   |

## Document Output 2023 R1, hotfix 2

*Internal release, never published*

## Document Output 2023 R1, hotfix 1

*Internal release, never published*

## Document Output 2023 R1

*Released for online: April 3, 2023*  
*Released for on-premises: April 14, 2023*  
*App version: 8.0.0.0*   
*Continia Core version: 8.0.0.200319*  
*Continia Delivery Network: 5.0.0.200319*  
*Cloud version: 8.0.0.200509*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | New feature enabling email template lines to define whether attachments should be included as one combined file, a zip/pfd file, or as individual attachments (single files). |
| Documents and Templates | Automatic invoice discount calculation if set in sales setup. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | New Customer Card for email/printing statement from Customer Card. |
| General Application | Removed Text 1024 limit on merge fields. |
| General Application | Could not Open/send mail if the source table had more fields with the same caption as the field(s) in primary key. |
| General Application | Show correct From address on Email Page. |
| Documents and Templates | Refactoring regarding finding recipients and sending Document Output email. |
| Documents and Templates | Allow multiple email addresses on one line in email recipients. |



<style>
  .content table tr td:nth-child(1) {
    width: 200px;
  }
</style>