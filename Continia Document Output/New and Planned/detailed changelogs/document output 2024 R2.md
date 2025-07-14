---
title: Detailed Changelog for Continia Document Output 2024 R2
description: Detailed Changelog for Continia Document Output 2024 R2
date: 04-03-2025
id: DO-194
lang: en
---

# Detailed Changelog for Continia Document Output 2024 R2

This article lists all new features and bug fixes for each version of Continia Document Output 2024 R2.

> [!TIP]
> As a Continia partner, you can be notified of new Document Output versions and service packs whenever they're released. To sign up for this service, go to [Receive a notification upon new Document Output releases](https://continia.zendesk.com/hc/en-us/articles/360005355319-Receive-a-notification-upon-new-Document-Output-releases) in the Continia PartnerZone (only available to partners).

> [!IMPORTANT]
> Currently, Document Output supports BC v14 and the three latest versions of Business Central. This will change with the release of Document Output 2025 R1 (26.00) in April 2025. **Document Output 2025 R1 (26.00) and all future versions from then on will only support the three latest versions of Business Central.**
> 
> **This version of Document Output – Document Output 2024 R2 (25.00) – is the last version with support for Business Central April 2019 (BC v14).**

## Document Output 2024 R2 Service Pack 2, hotfix 7
*Release date, online: March 03, 2025*  
*Release date, on-premises: March 05, 2024*  
*App version: 25.2.7*  
*Fob version: 25.02.07*  

### Bug Fixes

| Functional Area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | A new configuration option, **Generate Single Report**, has been added to the **Email Template Card**. This feature enables users to generate a consolidated report for all records that meet specified filter criteria, rather than generating individual reports for each record. | 64148 |

## Document Output 2024 R2 Service Pack 2, hotfix 6
*Release date, online: February 13, 2025*  
*App version: 25.2.6*  

### Bug Fixes

| Functional Area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | When an **Output Profile** was configured for printing only, it failed to queue a print job. | 64000 |
| Documents and Templates      | Previously, when a report selection contained multiple reports and the template was configured to display **Request pages**, the process failed if any of the reports included a write action, such as **Log Action**.<br><br>- When encountering a write action in one of the reports, the following error occurred:<br>- *The process cannot continue due to a write transaction.*<br><br>Now, the **Request page** is displayed up until the first write transaction, allowing the process to continue without interruption. | 64029 |

## Document Output 2024 R2 Service Pack 2, hotfix 5
*Release date, online: February 13, 2025*  
*App version: 25.2.5*  

### Bug Fixes

| Functional Area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | When using the **Email All** action in **Customer Statement Journal** to send customer statements, the PDF files of the statements were not attached to the emails. | 63771 |
| General Application | In certain scenarios, an error occurred during a **RunModal** operation within the **Template Card**. This issue arose due to an attempt to update a log entry that did not exist. When this situation occurred, the following error message was displayed: *Form.RunModal is not allowed in write transactions.* | 63776 |

## Document Output 2024 R2 Service Pack 2, hotfix 4
Internal release only

## Document Output 2024 R2 Service Pack 2, hotfix 3
*Release date, online: February 03, 2025*  
*Release date, on-premises: February 04, 2024*  
*App version: 25.2.3*  
*Fob version: 25.02.03*  

### Bug Fixes

| Functional Area | Description | ID |
| --- | --- | --- |
| General Application | When using **Output Profiles** and posting a sales or purchase document, the following error occurred:<br><br>*Sorry, the current permissions prevented the action. (TableData 112 Sales Invoice Header Modify: Continia Document Output)* | 63436 |

## Document Output 2024 R2 Service Pack 2, hotfix 2
*Release date, online: January 31, 2025*  
*Release date, on-premises: February 04, 2024*  
*App version: 25.2.2*  
*Fob version: 25.02.02*  

### Bug Fixes

| Functional Area       | Description | Id    |
|---|---|---|
| General Application   | When creating new documents from the **Customer Card** > **New Document** menu, the **Output Profiles** field was occasionally left unfilled. This issue has been addressed by implementing a fallback mechanism. Now, if the **Output Profile** is not specified on a document, it will automatically default to the **Output Profile** set in the **Customer** table. | 62689 |
| General Application   | On the **Unhandled Posted Service Invoices**, **Unhandled Posted Service Shipments**, and **Unhandled Posted Service Credit Memos** pages, setting a filter on the **Handled** field did not apply the filter correctly.<br>This issue occurred when users attempted to filter records based on the **Handled** status, expecting to view only those entries that matched the specified criteria. However, the filter was not applied, resulting in the display of all records regardless of their **Handled** status.<br>The filtering functionality has been corrected to ensure that when a filter is set on the **Handled** field, only records that meet the specified criteria are displayed. This allows users to effectively manage and review service documents based on their handling status. | 63179 |
| General Application   | The **Output Profile** was incorrectly assigned when posting an invoice document from an order. This issue occurred under specific circumstances where the system failed to recognize the correct profile settings.<br>The logic for assigning the **Output Profile** during the invoice posting process has been corrected. Now, when you post an invoice from an order, the system accurately assigns the appropriate **Output Profile** based on the predefined settings.<br>This fix ensures that the correct **Output Profile** is consistently applied, preventing potential mismatches and ensuring seamless document processing. | 63228 |

## Document Output 2024 R2 Service Pack 2, hotfix 1
*Release date, online: January 22, 2025*  
*Release date, on-premises: January 23, 2024*  
*App version: 25.2.1*  
*Fob version: 25.02.01*  

### Bug Fixes

| Functional Area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | An issue was identified when generating the reports, where users encountered an error message preventing the report from being created. This error occurred because request page filters weren't applied correctly. | 63053 |

## Document Output 2024 R2 Service Pack 2
*Release date, online: January 19, 2025*  
*App version: 25.2.0*  

### New or Changed Functionality

| Functional Area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | The **Output Profile** field was added to standard Business Central document pages. This enhancement allows users to see output settings directly from the document pages. | 60535 |
| General Application    | Enhanced functionality was implemented to allow users to hide the standard **Email** action on purchase documents in Business Central. This update provides greater flexibility in customizing the user interface. | 60632 |


### Bug Fixes

| Functional Area        | Description                                                  | ID    |
| ---------------------- | ------------------------------------------------------------ | ----- |
| Document and Templates | An issue was resolved where electronic documents were not generated for all documents when the **Combine** feature was used in an email template. This also fixes the issue where electronic documents were not all marked as Handled (DO) despite being sent. | 61407 |
| General Application    | When the **Open Email** action was used with the **Combine Documents** option enabled in the **E-Mail Template**, the system entered an infinite loop. | 60607 |
| General Application    | When attempting to import multiple email templates with multiple translations from a single file, the import process failed. | 60687 |
| General Application    | When new documents were created from **Customer Card** > **New Document**, the **Output Profiles** field was not populated in certain scenarios.A fallback mechanism to ensure the **Output Profile** in the **Customer** table is used when the **Output Profile** field is not filled on documents was implemented. | 62689 |

## Document Output 2024 R2 Service Pack 1, hotfix 2
*Release date, on-premises: January 13, 2025*  
*Fob version: 25.01.02*  

### Bug Fixes

| Functional Area        | Description                                                  | ID    |
| ---------------------- | ------------------------------------------------------------ | ----- |
| Document and Templates | The assisted setup has been enhanced to improve processing efficiency, particularly on legacy systems. It now sets the **Output Profile** only on posted documents that are not marked as handled. This change reduces unnecessary processing and accelerates the setup process by focusing only on relevant documents. | 62618 |

## Document Output 2024 R2 Service Pack 1, hotfix 1
*Release date, online: January 10, 2025*  
*App version: 25.1.1*  

### New or Changed Functionality

| Functional Area     | Description                                                  | Id    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | You can now apply filtering options to the **Update Output Profile on Documents** batch job. This enhancement allows users to specify criteria for selecting documents, thereby improving the efficiency and accuracy of the output profile updates. Users can filter based on various document attributes, such as **Document Type**, **Document Date**, and **Customer/Vendor No.**, ensuring that only relevant documents are processed. | 62428 |

### Bug Fixes

| Functional Area     | Description                                                  | Id    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Previously, when the **Setup Wizard** was executed multiple times, it inadvertently overrode the **Output Profile** settings across all documents. This issue occurred regardless of the initial configuration, leading to unintended modifications in document handling. The problem arose when users attempted to reconfigure settings using the **Setup Wizard**, causing the existing **Output Profile** to reset to default values. This has now been fixed, ensuring that the **Output Profile** remains consistent and unchanged when the **Setup Wizard** is used again. | 62418 |

## Document Output 2024 R2 Service Pack 1
*Release date, online: December 16, 2024*  
*Release date, on-premises: December 16, 2024*  
*App version: 25.1.0*  
*Fob version: 25.01*  

### New or Changed Functionality

| Functional Area | Description | ID |
| --- | --- | --- |
| General Application | Enhanced stability has been achieved when using Azure Blob Storage to store log data. This improvement addressed issues that previously led to intermittent failures during data storage operations, ensuring more reliable performance and data integrity. | 60361 |
| General Application | When a copy to a sandbox environment is performed, the **Azure Blob Container Name** is cleared. This change was implemented to prevent any unintended modifications to production data stored in Azure Blob Containers. | 62090 |

### Bug Fixes

| Functional Area | Description | ID |
| --- | --- | --- |
| General Application | When using the **Embed PDF in E-Document** functionality in **Output Profiles**, the following errors occurred:<br>- When the **Embed PDF in E-Document** functionality was disabled in the same session, sometimes a PDF was still embedded in the E-Document.<br>- When the **E-Mail** field in **Output Profiles** was set to **Xml (e-doc)**, the PDF document was sometimes still attached. | 60901 |
| General Application |Added the ability to include the **DO Output Profile** field in draft documents, such as **Sales Invoice**.<br>The **DO Output Profile** field was automatically populated with the code configured on the **Document Output Customer/Vendor Card**.<br>When the **DO Output Profile** field was active on the draft page, users could override the Output Profile without altering the customer settings.<br>The override was posted with the document and processed accordingly. | 61116 |
| General Application | In **Customer Statement Journal** > **Email All**, the action failed to attach certain PDF reports. | 61281 |
| General Application | When sending statements for the first time using the **Enhanced Automatic Statements** feature, the period dates for the statements were calculated incorrectly. | 61295 |
| General Application | When calculating the next sending date for **Automatic Statements** using weekday-based sending intervals, the date was sometimes calculated incorrectly. | 61431 |
| General Application | When an output profile was created with a specified **E-Document Setup Code**, the email action was incorrectly set to **PDF and XML (e-doc)**. This resulted in the document being emailed by default, which was not the intended behavior. The email action has now been changed to **Skip** to prevent automatic emailing. | 61584 |
| General Application | When users attempted to use the **Copy E-Mail Template Line** action in **E-Mail Template Card**, validation occasionally prevented the selection of a valid language/variant combination. | 61658 |
| General Application | When an email address exceeding 80 characters was entered in the **E-Mail** field within **E-Mail Recipients** > **<Location>**, the displayed value was truncated to 80 characters. | 61810 |
| General Application | An issue was resolved where incorrect documents were embedded in an e-document when sending multiple documents in a batch. | 62131 |

## Document Output 2024 R2, hotfix 4
*Release date: November 7, 2024*  
*App version: 25.0.4.231590*

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | Id |
| --- | --- |  --- |
| General Application | In the **Customer Statement Journal**, the **Email All** action did not attach some PDF reports.  | 61281 |
| General Application | When sending statements for the first time using the **Enhanced Automatic Statements** feature, the period dates for the statements were calculated incorrectly.  | 61295 |

## Document Output 2024 R2, hotfix 3
*Release date: November 6, 2024*  
*App version: 25.0.3.230586*

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | Id |
| --- | --- |  --- |
| General Application | For some tenants, it would sometimes revert any setup changes to the **Document Output Setup Card**.  | 61303 |

## Document Output 2024 R2, hotfix 2
*Internal release*

## Document Output 2024 R2, hotfix 1
*Internal release*

## Document Output 2024 R2

*Release date, online: October 1, 2024*  
*Release date, on-premises: October 23, 2024*  
*App: 25.0.0*  
*Fob version: 25.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Documents and Templates | Added Merge field functionality to Signature editor. This highlights the data field visually making it easier to build the desired signature. |
| Documents and Templates | Copy email template lines: Ability to copy all content of an email template line (including HTML Editor text) to help build a new variant of an email template line. |
| Documents and Templates | Automatic Documents: Updated user interface for handling statements, including a customer distribution calendar, based on the exact configuration per customer. This enables control of sent documents, as well as future document distribution. |
| Document and Templates | Added the possibility on Output Profiles to embed the PDF into the XMLs.  | 57642 |
| Document and Templates | New feature called Automatic Statements has been added, check webinars for more information.  | 58572 |
| Document and Templates | Added an action to Copy Line on Email Template Lines.  | 58749 |
| General Application | Aligned naming of multiple pages, especially lists, to the Microsoft naming convention.  | 58592 |
| General Application | Removed CDO from captions on pages.  | 58595 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | Id |
| --- | --- |  --- |
| Document and Templates | When editing a signature, merge fields incorrectly showed as %fields instead of a merge tag.  | 58877 |
| General Application | During recipient lookup where a field of type Guid is used the following error message is shown:<br><br><em>The value \<Guid\> is longer then the max value 16 Trying to set filter on field \<Field\> table \<Table\> From Table no. : _\<Table no. \>_ field no. _\<Field no. \> </em><br><br>An additional check for the Guid type has been added.  | 58640 |
| General Application | Fixed an issue where if multiple files was attached to an email, in rare cases, there could be artifacts in one of them.  | 59782 |


<style>
  .content table tr td:nth-child(1) {
    width: 200px;
  }
</style>