---
title: Detailed Changelogs for old versions of Continia Document Output
date: 04-06-2020
description: Detailed Changelogs for old versions of Continia Document Output
id: DO-4
lang: en
---

# Detailed Changelogs for old versions of Continia Document Output

This article lists all new features and bug fixes for each version of Continia Document Output.

## Document Output v3 Service Pack 2, hotfix 6
*Released: February 9, 2021*  
*Version: 3.2.6.0*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Document Output Cloud using BC Mail Accounts |
| General Application | New Test recipient on Document Output Setup. That works for all templates. |
| General Application | Document Ouput Cloud, local print from Print Queue now possible. |
| Platform and Technology | Updated Unhandled Cues |
| Platform and Technology | New event OnBeforeSendMail Event is called before mail is sent with smtp |

## Document Output v3 Service Pack 2, hotfix 5
*Released: February 3, 2021*  
*Version: 3.2.5.0*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Platform and Technology | If running from web client print now always uses service tier. |
| Platform and Technology | Contact name in table CDO E-Mail Recipients is changed from 50 to 100 characters. Because from BC version 14 contact name was changed from 50 to 100 characters on standard contact table. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | When you clicked E-Mail Log on Unhandeld Issued Reminders, e-mail recipients opened. |
| Document and Templates | If signature had more then one picture, creating a mail with that signature failed. |
| Platform and Technology | Report ID was not returned from Custom Layout on Customer or Vendor |
| Platform and Technology | When creating new merge field Web Clients stopped with strange error. |

## Document Output v3 Service Pack 2, hotfix 4
*Released: January 29, 2021*  
*Version: 3.2.4.0*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Document and Templates | Option on send code to email pdf, xml or both, only FOB versions. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | You could not edit filters on Unhandled Sales Quote, Order and Invoices, when opened from role center. |
| Document and Templates | Lookup on Report Layout on Template Lines did not work in all versiones. |
| Platform and Technology | Roles where missing on new tables. |

## Document Output v3 Service Pack 2, hotfix 3
*Released: January 21, 2021*  
*Version: 3.2.3.0*  

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Document and Templates | UTF-8 handling of HTML templates. |
| Document and Templates | Option on send code to email pdf, xml or both |
| Platform and Technology | Updated Unhandled Cues |

## Document Output v3 Service Pack 2, hotfix 1
*Released: December 16, 2020*  
*Version: 3.2.1.0*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | New “Send Codes” used to specify e-mail, print, and e-doc for customers. New “E-Doc. Send Codes”, where you can specify Codeunits to validate, export and deliver e-docs. |
| General Application | The Print/E-Mail all functions are now enabled. |
| General Application | The Open E-Mail under Print/send on Purchase orders are now enabled. |
| General Application | New Export Folder and Caption flowfields on E-Doc Send Codes |
| Documents and Templates | Pictures and icons are now visible on the HTML Template. |
| Documents and Templates | E-mail signature implementation |
| Platform and Technology | New Print queue for BC cloud. |
| Platform and Technology | Changed code for BC Cloud. Temp files are moved to BLOB fields. |
| Platform and Technology | Table relation on Codeunit field in E-Documents Send Codes. |
| Platform and Technology | If running from web client print now always uses service tier. |
| Platform and Technology | New Event OnSaveDoc. |
| Platform and Technology | From name added to SMTP. |
| Platform and Technology | New Electronic Document Response codeunit. |
| Country and Regional | Added the following countries: Czech Republic, Brazil, Finland, Ireland, Italy, Hungary, Iceland, Mexico, South Africa. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Resend from the log now works. |
| Documents and Templates | Fixed issue regarding multiple attachments on a template line. |
| Documents and Templates | Import of templates could fail with C/AL error. Fixed with missing COMMIT. |
| Platform and Technology | CU 6175282 CDO MergeFIeld Value Finder, could fail on salesperson where the code > 10 chararters. |
| Platform and Technology | Report Request Page could fail with reportid = 0. |
| Platform and Technology | OnGetRecipients event was not always called. |

## Document Output v3 Service Pack 1
*Released: June 17, 2020*  
*Version: 3.10*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | E-mail signature implementation |
| Platform and Technology | New Codeunits for handling XML and HTTP |
| General Application | Page CDO Unhandled, now uses default filters from the unhandled pages. |
| General Application | E-Mail log now includes print, e-doc and combined docs. |

### Bug fixes


| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | If Document Folder was blank on E-Mail Template Header "Do Not Save to Document Folder" did not work. |

## Document Output v3, hotfix 2
*Released: May 13, 2020*  
*Version 3.02*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Log is now always created. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | You could not attch files to HTML templates. |
| Platform and Technology | When opening HTML e-mail with image, it failed to insert image. |
| General Application | Merge Fields with Type Codeunit showed tableno. and name. |
| Documents and Templates | When using Template Variant without Dimensions FindTemplate did not always find the correct template. |
| General Application | General fix. |

## Document Output v3, hotfix 1 
*Released: April 26, 2020*  
*Version: 3.01*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Log is now always created. |
| General Application | New HTML editor version 1.0.1, now whit drag and drop files in Web Clients. |
| Platform and Technology | New “Send Codes” used to specify e-mail, print, and e-doc for customers. New “E-Doc. Send Codes”, where you can specify Codeunits to validate, export and deliver e-docs. |
| General Application | E-Mail log now includes print, e-doc and combined docs. |
| Documents and Templates | You can now use the CustBalanceDue merge field in templates with the following tables: Sales Header Sales Shipment Header Sales Invoice Header Sales Cr.Memo Header Return Receipt Header Reminder Header Issued Reminder Header Finance Charge. |
| General Application | New Unhandled Remittance Advice page. |
| Platform and Technology | Gmail SMTP port is changed from 465 to 587. |
| General Application | From BC and forward the std. E-mail buttons is not used for CDO. |
| General Application | New Vendor Setup table. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | You could not export templates from web clients. This is now fixed. |
| Platform and Technology | The handle description in the doc. output fact boxes like, e-mail, print, skip etc. was wrong if the customer did not have an e-mail address and skip was chosen. |
| Platform and Technology | "C/AL functions limited during write transactions” error when printing statements. |
| Platform and Technology | If "Send Always with Outlook" was checked, and the e-mail was sent with Queue, it failed with a Client callback error. Now it gives the correct error. |
| Platform and Technology | If using a different from e-mail account in Outlook, the mail address was required with the correct uppercase and lowercase letters. |
| Platform and Technology | Jobs Quote did not open/send. |
| Documents and Templates | Unhandled Sales/Purchase Quote, Sales/Purchase Order and Sales/Purchase Invoice had wrong Card Page ID. Resulted in error when clicking New, View or Edit. |
| Documents and Templates | When using the new Codeuint 6175303 Document Output to open/send e-mail it did not fid the correct language template. |

## Document Output v3
*Released: January 23, 2020*  
*Version: 3.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Platform and Technology | New Extension "Document Output 365" for Business Central 15.0. |
| General Application | Save PDF button on all unhandled pages. |
| Platform and Technology | GdPicture updated to Version 14.0.0.77. |
| General Application | Merge Fields Improved with: Event Finding Value from Related Tabels. |
| General Application | New Activation wizard. Setup Wizard improvements. |
| General Application | New HTML editor. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | Exporting and Importing Templates did not include all fields. |
| General Application | General fix. |



<style>
  .content table tr td:nth-child(1) {
    width: 200px;
  }
</style>