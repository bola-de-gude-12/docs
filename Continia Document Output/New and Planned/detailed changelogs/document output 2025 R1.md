---
title: Detailed Changelog for Continia Document Output 2025 R1
description: Detailed Changelog for Continia Document Output 2025 R1
date: 09-07-2025
id: DO-221
lang: en
---

# Detailed Changelog for Continia Document Output 2025 R1

This article lists all new features and bug fixes for each version of Continia Document Output 2025 R1.

> [!TIP]
> As a Continia partner, you can be notified of new Document Output versions and service packs whenever they're released. To sign up for this service, go to [Receive a notification upon new Document Output releases](https://continia.zendesk.com/hc/en-us/articles/360005355319-Receive-a-notification-upon-new-Document-Output-releases) in the Continia PartnerZone (only available to partners).

## Document Output 2025 R1 Service Pack 2
*Release date, online: July 2, 2025*  
*Release date, on-premises: July 4, 2025*  
*App version: 26.2*  

### New or Changed Functionality

| Functional Area | Description | ID |
|---|---|---|
| General Application | A new batch job has been added to update the **Handled** status on issued reminders. You can now run this batch job to automatically set the **Handled** field for reminders that meet specific criteria. | 67621 |

### Bug Fixes

| Functional Area | Description | ID |
|---|---|---|
| General Application | Whenever template line reports were used with multiple reports and **Show Request Page** was enabled, the following error occurred during write transactions: <ul><li><em>You cannot run the request page in a write transaction.</em></li></ul> The **Show Request Page** option is now automatically disabled when a template line report is executed within a write transaction. This prevents the error and ensures consistent processing of template lines with multiple reports. | 66848 |
| General Application | When a URL merge field was inserted by another merge field in the **Email Template** editor, the merge field was not replaced with the expected value during email generation. Instead, the merge field placeholder remained visible in the final email content. <br><br> This has now been fixed, and all nested merge fields, including URL merge fields, are correctly resolved and replaced with their corresponding values when generating emails. | 67037 |
| General Application | Fixed the following issues: <ul><li>When the **Save PDF** function was enabled on an email template, the request page was not displayed as expected. The request page now appears, allowing you to configure PDF saving options before sending emails.</li><li>The **Save PDF** function did not generate PDF files correctly for documents that had an output profile assigned for eDocuments but no output profile for other document types. PDF generation now works as intended in these scenarios.</li></ul> | 67164 |
| General Application | The font size value displayed in the email editor toolbar did not reflect the actual font size applied to the selected text.<br><br>This has now been fixed, and the toolbar now correctly shows the current font size of the selected content. | 67364 |

## Document Output 2025 R1 Service Pack 1
*Release date, online: May 26, 2025*  
*Release date, on-premises: May 28, 2025*  
*App version: 26.1*  

### New or Changed Functionality

| Functional Area | Description | ID |
| --- | --- | --- |
| General Application | The **Output Profiles** feature now includes a new option, **Fallback to Print**. This option can be enabled to automatically print documents when no email recipients are found during the email-sending process. By activating **Fallback to Print**, users ensure that documents are printed instead of being sent via email if recipient information is missing, thereby maintaining document delivery continuity. | 65788 |
| General Application | In the **Update Output Profile on Documents** batch job, the checkboxes will now default to **false**. This change ensures that users must actively select the checkboxes if they wish to update the output profile on documents, providing greater control and reducing the risk of unintentional updates. | 66343 |

### Bug Fixes

| Functional Area | Description | ID |
| --- | --- | --- |
| General Application | The **OnAfterCreateDocument** event, which previously did not trigger correctly when saving document PDFs, has now been fixed. This ensures that any custom logic tied to this event will execute as expected after a document PDF is created and saved. Users relying on this event for post-processing tasks can now expect consistent behavior. | 63993 |
| General Application | Support for **Hide Standard Mail Actions** and **Hide Standard Print Actions** has been expanded to additional pages extended by Document Output. This enhancement allows users to customize their interface by hiding standard mail and print actions on these newly supported pages, providing a more streamlined and tailored user experience. | 65938 |
| General Application | When using the **Open Email** action for documents associated with an output profile configured for printing, the system failed to generate a PDF document. This issue has now been resolved, ensuring that a PDF document is correctly created when the **Open Email** action is used, regardless of the output profile settings. | 66016 |
| General Application | When downloading an **Email Template Line** from **Continia Online**, the **Dimension Code** from the parent **Email Template Header** was not being assigned. This issue has been resolved, ensuring that the **Dimension Code** is now correctly inherited from the parent **Email Template Header** during the download process. | 66335 |
| General Application | The validation process for **Output Profiles** on both **Customer** and **Vendor** records has been updated to ensure better compliance with **Master Data Intercompany** scenarios. This enhancement addresses the need for consistent and accurate data management across intercompany transactions, reducing potential discrepancies and improving data integrity. Users involved in intercompany operations will now experience more reliable validation checks, ensuring that the **Output Profiles** align correctly with the master data requirements. | 66399 |
| General Application | When posting a partial **Sales Invoice** from a **Sales Order**, an incorrect **Output Profile** was assigned if the **Bill-to Customer No.** differed from the **Sell-to Customer No.** This issue has been resolved to ensure that the correct **Output Profile** is now applied in such scenarios. | 66449 |
| General Application | When the **Use reports for email attachments** checkbox was not selected, emails that did not contain any other PDF files were not sent. This issue has now been resolved, ensuring that emails are sent even if they do not include additional PDF attachments. | 66336 |

## Document Output 2025 R1, hotfix 3
*Release date, online: April 9, 2025*  
*Release date, on-premises: April 9, 2025*  
*App version: 26.0.3*  
*FOB version: 26.00.03*  

### Bug Fixes

| Functional Area | Description | ID |
| --- | --- | --- |
| General Application  | The combine functionality has been enhanced to work on standard pages as well. Users can now utilize the combine feature directly within standard page interfaces, ensuring a more seamless and integrated experience. | 65449 |
| General Application  | A potential issue has been resolved that could occur during the reinstallation of the Document Output app, version 25 and later, in the same database after it had been previously removed. This issue was specific to on-premises installations and could prevent the app from being installed correctly. | 65526 |
| General Application  | In unhandled unposted document pages, such as **Unhandled Sales Orders**, executing the **Print/Email All** action previously resulted in the following error:<br><br>- *The object has been run. Use the function CLEAR(Page)*<br><br>This issue occurred when attempting to print or email all documents simultaneously from these pages. The error has now been resolved, ensuring that the **Print/Email All** action functions correctly without triggering this message. | 65589 |

## Document Output 2025 R1, hotfix 2

Internal release.

## Document Output 2025 R1, hotfix 1

Internal release.

## Document Output 2025 R1
*Release date, online: April 1, 2025*  
*App: 26.0.0*  

### New or Changed Functionality

| Functional Area | Description | ID |
|---|---|---|
| Document and Templates | You can now translate **Email Templates** into different languages or adjust the tone of the email using Copilot. This functionality is accessible under **Edit Email Template** on the **Email Template** Card. It allows users to customize email communications to better suit their audience's language preferences or desired tone. Please note that this feature is currently in prerelease and will only be visible once it has been enabled in **Continia Feature Management**.                                                                                     | 63876 |
| General Application   | **Handled (DO)** functionality is now also added to Reminders.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | 60995 |
| General Application   | Enhanced the functionality for embedding documents in electronic documents to include attachments. The configuration for which documents to embed is determined by the settings in the **Output Profile** and is also influenced by the configuration of the template.                                                                                                                                                                                                                                                                                                                                                             | 61032 |
| General Application   | The fields **Log E-Mails** and **Keep E-Mail log for** on the **Email Template Card** now require users to have either the **SUPER** or **CDO-SUPER** permission set to edit them. This change ensures that only users with the appropriate level of access can modify these fields, enhancing security and control over email logging configurations.                                                                                                                                                                                                                                       | 61113 |
| General Application   | A new setup wizard was introduced to the **Automatic Period Statement** page. This wizard was designed to streamline the configuration process for the **Automatic Period Statement** and to provide clear guidance on how each setting in the table influences the dispatch of statements. To support this enhancement, the user interface on the **Automatic Period Statement** page was optimized for compatibility with the new wizard.                                                                                                                     | 61512 |

### Bug Fixes

| Functional Area       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | ID    |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| General Application   | When the **Open Email** action was used with the **Combine Documents** option enabled in the **E-Mail Template**, the system entered an infinite loop.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | 60607 |
| General Application   | Introduced the capability to hide the standard **Email** actions in Business Central for purchase documents.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | 60632 |
| General Application   | Email Template import would fail when importing multiple templates with multiple translations in a single file.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 60687 |
| General Application   | When an output profile with a specified **E-Document Setup Code** was created, the **Email Action** was changed to **Skip** instead of **PDF and XML (e-doc)**. This adjustment ensured that the document was not emailed by default.                                                                                                                                                                                                                                                                                                                                                                                             | 61584 |
| General Application   | When users attempted to use the **Copy E-Mail Template Line** action in the **E-Mail Template Card**, validation occasionally prevented the selection of a valid language and variant combination.                                                                                                                                                                                                                                                                                                                                                                                                                               | 61658 |
| General Application   | When an email address exceeding 80 characters was entered in the **E-Mail** field located in **E-Mail Recipients**, the displayed value was truncated to 80 characters.                                                                                                                                                                                                                                                                                                                                                                                                                                                         | 61810 |
| General Application   | In HTML email templates, URL-encoded characters were incorrectly replaced with merge fields. This issue has been addressed by introducing new placeholder behavior, which ensures that merge fields are correctly replaced within URLs without affecting URL-encoded characters.                                                                                                                                                                                                                                                                                                                                                 | 64287 |
| General Application   | In certain scenarios, an e-document log entry was not created as expected. This issue occurred when specific conditions were met during the e-document processing workflow. This has now been resolved, ensuring that an e-document log entry is consistently created in all relevant cases, thereby improving traceability and compliance.                                                                                                                                                                                                                                                                                     | 65028 |
| General Application   | In specific scenarios, an error occurred during the generation of the **Customer Calendar** for statements. This issue was triggered when particular weekdays were configured, and the adjustment spanned across month boundaries. The error has now been resolved, ensuring that the **Customer Calendar** can be generated without issues, even when adjustments involve crossing into a new month.                                                                                                                                                                                                                             | 65202 |
| General Application   | When an **Output Profile** is configured to send only e-documents and to embed document attachments in those e-documents, a PDF version of the document was attached to the email.                                                                                                                                                                                                                                                                                                                                                                                                                                               | 65275 |


<style>
  .content table tr td:nth-child(1) {
    width: 200px;
  }
</style>