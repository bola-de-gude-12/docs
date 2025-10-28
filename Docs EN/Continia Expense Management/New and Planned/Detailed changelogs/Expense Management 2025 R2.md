---
title: Detailed changelog for Continia Expense Management 2025 R2
date: 10-10-2025
description: List of features and bug fixes for each version of Expense Management 2025 R2
id: EM-359
lang: en
---
# Detailed changelog for Continia Expense Management 2025 R2
This article lists all of the new features, changes, and bug fixes for each version of Continia Expense Management 2025 R2.

> [!TIP]
> As a Continia partner, you can be notified of new Expense Management versions and service packs whenever they're released. To sign up for this service, go to [Receive a notification](https://continia.zendesk.com/hc/en-us/articles/360005316840-Receive-a-notification-upon-new-Expense-Management-releases) in the Continia PartnerZone.

> [!IMPORTANT]
> Expense Management 2025 R2 supports the following version of Microsoft Dynamics 365 Business Central: Business Central 2025 R2 (v27).

## Expense Management 2025 R2

*Pre-release date, online: September 8, 2025*  
*Release date online: October 1, 2025*  
*Release date on-premises: October 8, 2025*  
*App version: 27.0.0*  

### New or changed functionality

| Functional area | Description | ID |
| --- | --- | --- |
| General Application (Document Capture) | The **Continia Users** and **Continia User Setup** tables have been refactored and moved to the Continia Business Foundation app. Functionality specific to users has also been moved to separate apps:<ul><li>The **Approval Setup** has moved to the Continia Approvals app.</li><li>The **Web Portal Setup** has moved to the Continia Online Connector app.</li></ul>For more information, see [Important notice about refactoring in Document Capture and Expense Management](https://continia.zendesk.com/hc/en-us/articles/27530051601810-Important-notice-about-refactoring-in-Document-Capture-and-Expense-Management "https://continia.zendesk.com/hc/en-us/articles/27530051601810-important-notice-about-refactoring-in-document-capture-and-expense-management") (only available to partners). | 69908 |
| Credit Card Transactions | You can now customize how bank transaction postings appear in the general ledger by defining a description template. Instead of generic text, the template can include key transaction details, enabling faster reconciliation and improved clarity during audits. | 29474 |
| Document Approval | It is now possible to select and approve multiple entries simultaneously on the **Approval Entries – Expense Management** page. | 54462 |
| Document Approval | Custom filters applied on the **Approval Entries – Expense Management** page now remain active as users work with approval records. This enhancement improves usability by preserving filter context. In addition, the following procedures have been made available for external access, enabling better extensibility and integration:<ul><li>PutOnHold</li><li>RemoveOnHold in codeunit **CEM Approval Management**.</li><li> Forward in codeunit **CEM Approvals Bridge**</li> | 66088 |
| Expenses | Reminder emails previously failed to display merchant information when the **Description** field was empty, making it difficult to identify pending expenses. This has now been fixed. If no description is provided, the merchant name is now shown to help users identify which expenses require attention. | 67001 |
| Expenses | **Applied Purchase Document Type** and **Applied Document No.** are no longer visible for expenses attached to an Expense Report. The functionality was not supported from this level. | 67180 |
| Expenses | To enhance the integration between Expense Management and Document Capture, the system now automatically sends expenses for approval when the user selects **Process with Document Capture**. Additionally, expenses that have been sent to Document Capture will be automatically posted once they are approved. | 63252 |
| Expenses | Expenses now include an **External Document No.** field that will be used when posting. This enhancement gives users more flexibility to choose between values provided by **OCR**, the **Applied Document No.**, or the default posting value (such as _EXPENSE 123_), depending on their preferred setup and processing flow. | 65844 |
| Expenses | The following event publisher has been added to Codeunit 6086338 "CEM Settlement-Post". It provides an opportunity to adjust the VAT amount as necessary when posting Expenses:<ul><li><em> OnPostExpenseOnBeforeValidateVATAmount</em></li></ul> | 67569 |
| General Application | In the context of the **"3-Month Rule"**, in the German localization, **Addresses** are now searchable outside of the **Per Diem** context. | 64704 |
| General Application | The configurable messages related to **Invoice No.** and **Process with Document Capture** have been downgraded from **Warning** to **Information** level. | 68813 |
| General Application | The navigation available via Business Central’s **Explore more roles** feature has been restructured to provide a clearer and more comprehensive overview of Expense Management functionality. Related features are now grouped into logical sections—such as **Expense Reports**, **Transactions**, **Mileage**, **Per Diem**, and **Approval**—making it easier for users to navigate and understand the full scope of available capabilities. | 57715 |
| General Application | The **Tax Report** has been enhanced with additional per diem details, including destinations, meal allowances, and deductions. It now also includes **Payment Type** on expenses and displays associated document numbers.<br>Additionally, the report now supports filtering by a single document type, providing more precise reporting and analysis. | 67127 |
| General Application | Users can now assign specific projects and tasks to individual destinations, within per diems, on a daily basis. When multiple destinations with different projects are visited on the same day, the system posts separate **Job Journal** entries for each project, using the total daily amount per project. To support customization, new integration events have been added, to tailor the posting behavior to specific business needs. | 62098 |
| General Application | Procedure SetGlobalVars in report, **CEM Status Report** is now available for external access. | 64982 |
| General Application | When changing the **Posting Date** on an **Expense Report** that includes expenses or per diems in foreign currency, users are now alerted with the following message:<ul><li><em> _You have changed the Posting Date on the expense report, which might affect the exchange rates that are used for currency calculation on the expense report lines. __Please review the lines._</em></li></ul> | 68061 |
| General Application | The following changes have been applied to the Expense Management permission sets:<ul><li>CEM-ALL has been renamed to CEM BASIC</li><li>CEM-APPROVE has been renamed to CEM APPROVE</li><li>CEM-SUPER has been renamed to CEM ADMIN</li><li>CEM-NAVUSER has been renamed to CEM DOC. EDIT</li></ul>The renamed permission sets will be updated automatically during the upgrade.<br>For more information about the permission sets, see [Expense Management permissions](@EM-62). | 66519 |
| General Application | The integration to Continia Sustainability has been replaced with an integration to Microsoft Sustainability.<br/>If you were using Continia Sustainability:<br/><ul><li>A new setup must be created for the relevant expense types and sustainability dependencies</li><li>All existing expenses must be updated with the new sustainability accounts</li></ul> | 68070 |
| General Application | You can now import multiple expense users simultaneously from a Configuration Package without the need to confirm each user record individually.<br>When creating non-Business Central users in **Continia User Setup**, the following dialog will no longer be triggered when using the **Configurable Packages** module.<br><ul><li><em> <UserID> does not exist as a BC-user. Do you want to add the user anyway?</em></li></ul> | 55498 |
| General Application | Per diem destination visibility has been improved by displaying the destination **Country Name** when no specific destinations are entered for a day. | 64118 |
| General Application | The **Dataloen Employee** table has been refactored to support the expansion of the **Employee ID** field from 30 to 50 characters. This change aligns with upcoming requirements from Dataloen and ensures continued compatibility. Note! License update is required. | 69092 |
| General Application | Context-sensitive help links have been added to relevant **Expense Management** pages. These links provide direct access to matching articles on Continia Docs, making it easier for users to find guidance and support while working in the application. | 32762 |
| Mileages | It is now possible to set up environmental accounts on vehicles in Expense Management. This enables the collection of emissions data from mileage entries, supporting environmental reporting and analysis. | 66478 |
| Per Diem | When **Enable Per Diem Destinations** is set, the **Departure Country/Region** field is now automatically populated with the most recently used value during **Per Diem** creation. Manual override is still possible, and no additional setup is required to use this enhancement. | 64120 |
| Per Diem | On the **Per Diem Rate** page, meal values for **breakfast**, **lunch**, and **dinner** now display dynamically, based on your configuration:<br><ul><li> As **clean percentages** when defined as percentages of the total allowance</li><li> In **local currency with decimals** when using LCY values</li></li> In **foreign currency** when applicable</li> | 65790 |
| Per Diem | The **Per Diem Card** now displays full **country** and **region** names instead of codes, providing a more user-friendly experience. Users can enter the country name directly or select from a lookup list, with the system automatically matching partial entries. The underlying **code values** are still used for data integrity and compatibility. | 66919 |

### Bug fixes

| Functional area | Description | ID |
| --- | --- | --- |
| Document Approval | When using Danish language in the Business Central client, and filtering approval entries by **Document Type** on the **Approval Entries - Expense Management** page, the following error occurred when attempting to approve documents:<br><ul><li><em>Titlen Bilagstype er tvetydig mellem flere felter i tabellen Godkendelsespostering - Expense Management.</em></li></ul> | 68994 |
| Expenses | Expense validation has been enhanced to provide clearer feedback when the **Description** field is empty:<br>- An error is shown if the description is mandatory.<br>- A warning is shown if the description is optional.<br>Additionally, the display of the **Merchant** field has been standardized across all expense cards to improve UI consistency. | 66563 |
| Expenses | The **Employee Reimbursed** field in **Expense Report** is now automatically cleared when any sub-document payment is unapplied. | 68062 |
| Expenses | In the **Canada (CA) localization**, when a **Tax Group Code** was configured on an **Expense**, submitting or re-submitting the expense with **Allocations** caused Business Central to update the allocations in Continia Online with blank **Tax Group Code** values. This issue has now been fixed. The correct **Tax Group Code** is preserved during submission and synchronization. | 69133 |
| General Application | Previously, there was a bug when transferring expenses or mileages using **Move To Company**; Attached documents that were transferred with expenses or mileages between companies (that were configured with Azure blob storage) became inaccessible for the destination company. This issue has now been resolved and attachments remain accessible after the transfer. | 68840 |
| General Application | An expense document is now counted as usage as soon as it is created in Business Central. Previously, documents with the status, **Open**, were not counted until they were sent for approval, which could delay accurate usage tracking. Open expenses are now also included in the usage statistics. | 68776 |
| Per Diem | Resolved an issue where an incorrect **Settlement Line No.** was generated for Per Diems attached to Expense Reports. | 68038 |
| Per Diem | Validation has been added to prevent sub-rate minimum hours from being equal to or greater than the **Full Day Minimum Hours** threshold. This ensures logical consistency in per diem calculations and prevents overlapping or conflicting rate conditions. | 67210 |
