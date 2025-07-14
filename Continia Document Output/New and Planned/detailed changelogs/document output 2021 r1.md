---
title: Detailed Changelog for Continia Document Output 2021 R1
description: Detailed Changelog for Continia Document Output 2021 R1
date: 11-06-2021
id: DO-5
lang: en
---

# Detailed Changelog for Continia Document Output 2021 R1

This article lists all new features and bug fixes for each version of Continia Document Output.

> [!IMPORTANT]
> This version of Document Output is no longer supported. As a consequence of this, Continia will no longer correct any errors appearing in this version, and no further service packs relating to the version will be released. For supported versions of Document Output, see [Software Lifecycle Policy and Continia Document Output On-Premises](@DO-42).

> [!TIP]
> As a Continia partner, you can be notified of new Document Output versions and service packs whenever they're released. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360005355319-Receive-a-notification-upon-new-Document-Output-releases) in the Continia PartnerZone (only available to partners).

## Document Output 2021 R1 Service Pack 5
*Released: June 29, 2021*  
*App version: 4.5.0.1*  
*FOB version: 4.05.01*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Moved Page 61775395 to 61775396 in On Premise |
| General Application | DO now deletes statement journal line after opening and sending mail. |
| General Application | In DO setup you can now set report ID for Picking and put away lists. |
| General Application | On CDO Customer Setup FlowField “Customer Name” is changed from 50 to 100. |
| General Application | DO now deletes statement journal line after opening and sending mail. |
| Platform and Technology | You can now choose protocol in DO SMTP Setup. (TLS 1.1,TLS 1.2, TLS 1.3) |
| Platform and Technology | New event OnFindReportID, to manually override the Report to print/save. |
| Platform and Technology | **XML Export**: Automatic Setup of ISO codes, Unit of Measure Codes |
| Platform and Technology | **XML Export**: Developer guide: How to use Events, shows how to implement additional Payment Methods, or to embed files in XML etc. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | CDN AccessByPermission on Customer Setup Card |
| General Application | If there where any changes in tables before printing local in BC 15 and forward, print failed with COMMIT error. |
| General Application | The error, You can only use "Combine Documents to one PDF" on tables with one field in primary key. Is changed to message instead of error. Because this works for some partners. |
| General Application | When sending e-doc and recipients was blank, DO tried to print the document. |
| General Application | On unhandled invoices and credit memos, print was not filtered correct. When e-mail recipient was blank. |
| General Application | **XML Export**: Use of GLN/EAN now works in general |
| Country and Regional | **XML Export**: Country Codes are automatically set in files |
| Country and Regional | **XML Export**: Export functionality issues fixed in localized versions |

## Document Output 2021 R1 Service Pack 4
*Released: June 9, 2021*  
*App version: 4.0.0.4*  
*FOB version: 4.04*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Batch to copy Templates, did not include merge fields when copying from another Company. |
| General Application | New event OnGetReportParameters. |
| General Application | When using DO Queue, DO now finds the printer name with the user ID that puts the record in queue. |
| General Application | New Reply activity on NAV/BC e-mail. |
| Country and Regional | Check for valid Country Code, when downloading templates. |
| General Application | New Pro Forma Invoice template. |
| General Application | New Filters on Unhandled Posted Invoice and Credit Memo You can now Filter on  E-Mail, Print and E-Document. |
| General Application | E-Mail/Print statements used wrong function to find Recipients. |
| Platform and Technology | Changed code for BC Cloud. Temp files are moved to BLOB fields. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Customer Setup  Batch, now includes "Output Profile". |
| General Application | Missing permissions for Log Attachment. |
| General Application | CU 6175273 Was not updated, to use new code to e-mail. |
| General Application | If template was set to print only, there was no attachment when opening the mail. |
| General Application | When copying attachment file from Outlook, the filename was wrong. |
| General Application | From  Name did not work any more. |
| General Application | Recipients on Payment Journal Remittance Advice, did not always show. |

## Document Output 2021 R1 Service Pack 3
*Released: May 5, 2021*  
*App version: 4.0.0.3*  
*FOB version: 4.03*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | New Event OnGetRecipientsFromTemplateLine |
| General Application | It is now possible to set E-Document File Name on Template Lines. |
| General Application | E-Mail log can now be moved to File System instead of database. (On Premise Only) |
| General Application | Delete old e-mail log, now only deletes the e-mail from the log. Not the log itself. |
| General Application | Include Document Attachments in mail From BC 13 and forward. |

## Document Output 2021 R1 Service Pack 2
*Released: April 27, 2021*  
*App version: 4.0.0.2*  
*FOB version: 4.02*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | It was not  possible to select Report Layout on Template Lines. |
| General Application | Filter on E-Mail Log FactBox on Service Credit Memo was wrong! |
| General Application | If ( or ) was used in primary keys on Customer etc. opening  E-Mail/Print Statment could not open. |
| General Application | MergeField in Apps failed on validation of Table No. Table Relation changed. |
| General Application | When PDF was saved to document folder. Background pdf and merge pdf was not included |
| Platform and Technology | E-Mail was saved in a hidden log. E-Mail Log FacBox showed Hidden logs. Hidden filer on E-Mail Log Page can be cleared. |

## Document Output 2021 R1 Service Pack 1
*Released: April 19, 2021*  
*App version: 4.0.0.1*  
*FOB version: 4.01*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Document and Templates | Include Document Attachments in mail From BC 13 and forward. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | DO Actions on Factbox in Quote, Order etc. is disabled and moved to Ribbon, because values are not always saved on lines. (Only Apps) |
| General Application | Mail was not saved in log from Document Output Monitor |
| General Application | When opening html e-mails in NAV/BC and message is collapsed (not shown) on e-mail page, you could not send the e-mail. |
| Platform and Technology | When PDF was saved to document folder. Background pdf and merge pdf was not included |
| Platform and Technology | Moved Page 61775395 to 61775396 in On Premise |




<style>
  .content table tr td:nth-child(1) {
    width: 200px;
  }
</style>