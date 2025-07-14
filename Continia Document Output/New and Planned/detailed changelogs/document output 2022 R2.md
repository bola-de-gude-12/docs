---
title: Detailed Changelog for Continia Document Output 2022 R2
description: Detailed Changelog for Continia Document Output 2022 R2
date: 06-02-2025
id: DO-39
lang: en
---

# Detailed Changelog for Continia Document Output 2022 R2

This article lists all new features and bug fixes for each version of Continia Document Output.

> [!TIP]
> As a Continia partner, you can be notified of new Document Output versions and service packs whenever they're released. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360005355319-Receive-a-notification-upon-new-Document-Output-releases) in the Continia PartnerZone (only available to partners).

## Document Output 2022 R2 Service Pack 5
*Released: January 24, 2025*  
*Fob version: 7.05.*  

### New or changed functionality

| Functional area         | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Delivery Netowrk | Updated to support ZUGFeRD and XRechnung for valid documents as of January 2025. |

## Document Output 2022 R2 Service Pack 4, hotfix 1
*Released: February 5, 2025*  
*App version: 7.4.1*  

### New or changed functionality

| Functional area         | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Delivery Netowrk | Updated to support ZUGFeRD and XRechnung for valid documents as of January 2025. |

## Document Output 2022 R2 Service Pack 4

*Released: April 14, 2023*  
*App version: 7.4*  
*Continia Core: 7.2.0.173895*  
*Continia Delivery Network: 4.3.1.182428*  
*Cloud version: 7.4.0.197459*  

### New or changed functionality

| Functional area         | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Documents and Templates | “Quote No.” and “On Hold” have been added to Unhandled Sales and Purchase Orders (Visible=No). |
| General Application     | Tiles were changed from 'run' to 'runmodal' to open a page in edit mode, and new sales tiles were added. |
| General Application     | The Role Center now has new purchase tiles.                  |
| General Application     | New page for Default filters is added.                       |
| General Application     | Added "Send as e-doc" to Issued Reminder FactBox             |

### Bug fixes

| Functional area         | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Documents and Templates | The mail was not being saved in the log from Monitor, but this issue has been resolved now. |
| Documents and Templates | The refactoring issue related to finding recipients and sending Document Output Email has been fixed. |
| Documents and Templates | The "CDO Web Service E-Mail Log" has been updated with *CreateEmailLogEntry* changed to External. |




## Document Output 2022 R2 Service Pack 3

*Released: February 17, 2023 (SP2 HF versions 7, 8 and 9 were only released to cloud and are included in this release)*  
*App version: 7.3.0*   
*FOB version: 7.03*  
*Continia Core version: 7.1.0.95811*  
*Continia Delivery Network: 4.2.1.137518*  
*Cloud version: 7.3.1.168685*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | New option to import templates from multiple countries. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Send Action is now only enabled if there are recipients on email. |
| General Application | Report Layout Lookup when using Report Selection on template (fixed). |
| General Application | When running Setup Wizard it failed in a Try function with LOCKTABLE (fixed). |
| Platform and Technology | Azure App (Office 365): could not send to customers with multiple recipients. |
| Platform and Technology | Azure App (Office 365): Missing cc and bcc on new Azure mails (Office 365). |
| Platform and Technology | Use the senders User id to find From Address when sending from queue (used the service user before). |
| Documents and Templates | When running email jobs, the “Template Code” was not used in all code paths. |
| Documents and Templates | When deleting or renaming templates, the table “E-Mail Templ. Line Report” is now updated. |

## Document Output 2022 R2 Service Pack 2, hotfix 6
*Released: January 31, 2023 (hotfix versions 4 and 5 have been skipped to match release version with cloud release)*  
*App version: 7.2.6.0*  
*Cloud version: 7.2.6.148611*  
*Continia Core version: 7.1.0.95811*  
*Continia Delivery Network: 4.2.1.137518*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Setup Wizard starts Job Queue if you have permission. |
| General Application | User id changed from code 20 to 50 in “CDO Queue Entry.GertPrinterName". |
| General Application | Fixed Base64 error when sending test mail. |
| Documents and Templates | Email/Print Statement was showing incorrect figures. |

## Document Output 2022 R2 Service Pack 2, hotfix 3
*Released: January 20, 2023*  
*App version: 7.2.3.0*  
*Cloud version: 7.2.4.141273*  
*Continia Core version: 7.1.0.95811*  
*Continia Delivery Network: 4.2.1.137518*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | If sending method was set to DO SMTP, the mail was not sent. |
| General Application | Field “Print Timeout (sec)” was missing in CDO setup table from BC18 and forward. |
| Documents and Templates | Document Output Customer Setup was deleted when running email/print statement. |
| Documents and Templates | Field “Print Timeout (sec)” was missing in CDO setup table from BC18 and forward. |

## Document Output 2022 R2 Service Pack 2, hotfix 2
*Released: January 19, 2023*  
*Cloud and app version: 7.2.2.0*  
*FOB version: 7.02.02 (FOB version not released yet)*  
*Continia Core version: 7.1.0.95811*  
*Continia Delivery Network: 4.2.1.137518*

>  [!NOTE] The FOB version has not been released yet but is expected to be released shortly.

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | New Customer Card for email/print statements from customer card. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Save .eml file in log when using Outlook. |
| General Application | Could not send with SMTP in BC versions 18-21. |
| General Application | SMTP Code was missing in email log. |
| Delivery Network | DK: Onboarding Page could not register using DK:GLN. |

## Document Output 2022 R2 Service Pack 2, hotfix 1
*Internal release, never published*

## Document Output 2022 R2 Service Pack 2
*Released: January 2, 2023*  
*Cloud and app version: 7.2.0.0*  
*FOB version: 7.02*  
*Continia Core version: 7.1.0.95811*  
*Continia Delivery Network: 4.2.0.111472*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Platform and Technology | New Office 365 Mail integration (sending mails with a web API) (OAUTH 2.0). |
| Platform and Technology | UTH-8 handling of HTML templates. |
| General Application | Name change in Doc. Output FactBox to Document Output FactBox. |
| Documents and templates | Separate background PDF for first and last page. |
| Documents and templates | New templates for Purchase Return. |
| Documents and templates | New Merge Field, User Full Name. |
| Documents and templates | New ZUGFeRD functionality. |
| Documents and templates | New option to define different report selection per email template line. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Missing commit on open email from Statement Journal. |
| General Application | Printed Statement from statement journal was not deleted. (Recipients =’’). |
| General Application | Did not find the correct report layout when using report selection with more reports. |
| General Application | Fixed problem with saving PDF to document folder. |
| General Application | Automatic statement fixed an endless loop with LM as Date formula. |

## Document Output 2022 R2 Service Pack 1
*Released: November 16, 2022*  
*Cloud and app version: 7.1.0.0*  
*FOB version: 7.01*  
*Continia Core version: 7.0.0.35523*  
*Continia Delivery Network: 4.0.0.35521*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | New filters added on Email/Print Statement. |
| General Application | Unhandled Pages filter updates. |
| General Application | New templates for Purchase Return. |
| General Application | Better error handling when creating PDF files. |
| General Application | Activation check before running setup wizard. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Error on print when report id = 0 on template. |
| General Application | Edoc did not always show in email address. |
| General Application | Missing report selections when using lookup on Email Template. |
| General Application | Fixed problem with saving PDF to document folder. |

## Document Output 2022 R2
*Released: October 3, 2022*  
*Cloud and app version: 7.0.0.0*  
*FOB version: 7.00*  
*Continia Core version: 7.0*  
*Continia Delivery Network: 4.00/4.0.0.0*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Password protect PDF. When sending emails, it is now possible to password protect attached PDF files with a user-defined password. This feature can’t be used in combination with Sign PDF or use of background PDFs. |
| General Application | Create PDF/A for Output profiles. In order to generate a PDF in the format ZUGFeRD (DE) or Factur-X (FR), this PDF file type is required. |
| General Application | New page for downloading country templates. |
| General Application | Templates can now use report selections. This means that Document Output templates now automatically use changes made in the standard report selection without changing the report on the template. |
| General Application | New DLL files download. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Preserve links when using a background PDF. Before this fix, background PDFs would deactivate the links in documents. |
| General Application | Email/Print Statement page opened with errors from customer when filters were set. |



<style>
  .content table tr td:nth-child(1) {
    width: 200px;
  }
</style>