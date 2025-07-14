---
title: Detailed Changelog for Continia Banking 2024 R2
description: Changelog containing an overview of all new updates, features, and hotfixes for Continia Banking 2024 R2
date: 14-07-2025
id: CB-150
lang: en
---

# Detailed changelog for Continia Banking 2024 R2

This article lists all new updates, features, service packs, and hotfixes for Continia Banking 2024 R2. 

> [!TIP]
> As a Continia partner, we can notify you of new Continia Banking versions and service packs whenever we release them. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/21731056669458-Receive-a-notification-upon-new-Continia-Banking-releases) in the Continia PartnerZone (only available to partners).

## Continia Banking 2024 R2, Service Pack 9

*Release date, online: July 11, 2025*   
*App version: 25.9.0*

### New features

| Functional Area | Description                                                  | ID    |
| --------------- | ------------------------------------------------------------ | ----- |
| Payment Import  | General improvements to messages, error handling, and confirmation dialogs in the Import app. | 66794 |
| Payment Export  | Added support for specifying the approver ID type for non-Danish/Nordic approvers who cannot use a social security number. A new type field has been implemented for `AMLApproverIdentifier` and `AMLApprover2Identifier`, and is included in the in-house file. Supported types include SOSE (Social Security Number) and NIDN (National ID Number); additional types can be added if needed. Both Approver ID Type and Approver ID must be filled in for the values to be exported. | 66666 |
| Payment Export  | Added support for maintaining the Sender ID - interpreted as the Organization ID (OrgId) - on the bank record for cross-border payments. This is required in scenarios where the Sender ID differs from the VAT Registration No. currently used from Company Information. A new OrgId field has been introduced on the bank (search for Banks). | 67351 |
| Payment Import  | **Preview**: Added support for importing multiple bank account statements into the same reconciliation journal. Imports can be grouped by aggregation period and automated via job queue. Enable the feature in Continia Feature Management. See [Importing multiple bank statements](@CB-245) for details. | 44209 |
| Payment Import  | Added an **Import** button to the Payment Reconciliation Journal, allowing direct import of data into the bank transaction table for processing. | 67577 |

### Bug fixes

| Functional Area     | Title                                                        | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| Payment Export      | Fixed an issue where the **Payment Reference** field on the purchase invoice could not be cleared if it was initially populated from the vendor's payment reference template. It is now possible to clear both the payment reference template and the payment reference fields on the purchase invoice, regardless of the vendor settings. | 67155 |
| Payment Export      | Fixed an issue where switching from Advanced to Normal mode in the payment journal broke the **Suggest Vendor Payments** feature. | 67348 |
| Payment Import      | Fixed the transaction error for CSV import.                  | 67545 |
|                     |                                                              | 67089 |
| Payment Export      | Fixed tooltip error for the **Send Email on Posting Date** feature. | 67116 |
| Payment Export      | Fixed issue where the **Show Customers/Vendors/Employees** feature was not working on the Remittance Advice Setup Check page. | 67122 |
| Payment Export      | Fixed issue preventing posting of invoices with a zero amount. | 67176 |
| Payment Import      | Fixed an error in `GetProprietaryBankTransactionCodeIssuer` where strings longer than 20 characters caused a failure. | 67284 |
| Payment Export      | Fixed an issue where the Payment Suggestions tile on the Advanced Role Center incorrectly counted already posted suggestions. | 67366 |
| General Application | Fixed issue with missing permissions for inserting retention policies during activation. | 67415 |

## Continia Banking 2024 R2, Service Pack 8

*Release date, on-premises: June 27, 2025*   
*Version: 25.8.0*

### New functionality

| Functional Area | Title                                                        | ID    |
| --------------- | ------------------------------------------------------------ | ----- |
| Payment Export  | The Remittance Advice Email was added to the Retention Policy. The policy is set to manual, so users must activate it before use. | 66289 |
| Payment Export  | If you use **Find Entries** in standard processes, the Remittance Advice Email entry is now integrated to provide direct access. | 66290 |
| Payment Export  | Added a new feature to help users identify and resolve issues with missing remittance advice emails. Accounts, Email Setups, or Document Setups will be checked to provide information about wrong setups. For more information, see [Reviewing remittance advice setups](@CB-246). | 65876 |
| Payment Export  | Created a new Remittance Advice Outbox to allow users to see all sent and unsent remittance advices from Banking. Users can now resend emails or change recipients. For more information, see [Working with the remittance advice outbox](@CB-249). | 65877 |
| Payment Export  | Added a filter for Banking Export batches.                   | 66736 |
| Payment Export  | Added functionality to manually summarize lines in the Payment Journal. You can now run the Payment Suggestion without summarizing per account. After lines are created, select lines and use **Actions** > **Functions** > **Summarize Payments**. The system will consider summarizing setup and explains failures (e.g., posting dates differ or dimension values don't match). | 60909 |
| Payment Export  | Added the option **Bank & PDF** to Remittance Handling. This option creates a PDF using standard document output, so browser defaults determine how the file is handled. For more information, see [Working with the remittance advice outbox](@CB-249). | 65878 |
| Payment Export  | A new notification alerts users about unsent remittance advice emails. Notifications are shown on: Payment Journals, Direct Debit Journals, and Payment Suggestions. | 66436 |
| Payment Import  | Added new publisher event `OnAfterFilterSearchRule` for codeunit 71554206 "CTS-PI Match Search Rules". | 65989 |
| Payment Import  | Added new publisher event `OnBeforeStartMatchingPaymentReconciliation` for codeunit 71554177 "CTS-PI Match Reconciliation". | 65986 |
| Payment Import  | Added new publisher events `OnBeforeModifyGenJournalLine` and `OnBeforeModifyBankGenJournalLine` for codeunit 71554184 "CTS-PI Bank Recon Appl Entries". Also added `OnBeforeUpdateTempGenJournalLine`. | 65988 |
| Payment Import  | Added new publisher event `OnBeforeStartMatchingBankAccReconciliation` for codeunit 71554177 "CTS-PI Match Reconciliation". | 65978 |
| Payment Import  | Added support for viewing posted reversed transactions from returned Direct Debits. The feature can be enabled in the Continia Feature Management Page. See [Introducing direct debit returns](@CB-241) | 66141 |
| Payment Import  | Added support for matching returned Direct Debits. The system will automatically identify and reverse matching transactions. The feature can be enabled in the Continia Feature Management Page. See [Handling direct debit returns](@CB-243) | 61504 |
| Payment Import  | Added support for reversing transactions based on returned Direct Debits. The feature can be enabled in the Continia Feature Management Page. See [Handling direct debit returns](@CB-243) | 61505 |
| Payment Import  | Support for Direct Debit Return Reasons added. Return reason descriptions are now visible. The feature can be enabled in the Continia Feature Management Page. See [Understanding return reason codes](@CB-241) | 61501 |
| Payment Import  | Support for handling Direct Debit Returns added to reconciliation. See Continia Docs for more information. The feature can be enabled in the Continia Feature Management Page. See [Handling direct debit returns](@CB-243) | 44147 |



### Bug fixes

| Functional Area     | Title                                                        | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Updated error messages to include the URL and improved ETag retrieval logic. | 67114 |
| Payment Export      | The Bank Account selection from Payment Posting Setup was not implemented correctly. Also, a missing filter for the payment method has been added. If at least one entry exists in the setup, the internal Bank Account No. field becomes visible. The system then retrieves the balance account accordingly. | 66931 |
| Payment Import      | Long text entries are now split to prevent truncation during import of CAMT statements. | 66829 |
| Payment Export      | Improved error message clarity when no entries are found for the payment balance account. | 66742 |
| Payment Import      | When the full amount is entered in the **Applied Amount** field on the **Review** or **Apply Entry** page, an actionable error is triggered, if payment discount is still possible. The **Remaining Payment Discount Possible** is set to zero and a full application without applying any payment discount can be posted. | 66271 |
| Payment Import      | Importing CSV file with double delimiters now is allowed.    | 59576 |



## Continia Banking 2024 R1, Service Pack 7, hotfix 1

*Release date, online: May 20, 2025*   
*App version: 25.7.1*

### New functionality

| Functional Area           | Title                                                        | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Added functionality to reset stuck payment approvals in transfer processes. | 66388 |



### Bug fixes

| Functional Area | Title                                                        | ID    |
| --------------- | ------------------------------------------------------------ | ----- |
| Payment Export  | Fixed issue where the job queue status was incorrectly set to *On-Hold*. Also resolved the error when users without activation permissions could create job queues. | 66405 |
| Payment Export  | Fixed intermittent error during posting preview. This issue occurred in document renumbering cases. | 65611 |
| PSP             | Updated the PSP Header Card functionality to allow bulk updates. When selecting multiple lines, actions like changing *Imported to Company* can now be applied to all. | 65626 |
| PSP             | The Payment Service Provider field is now auto-filled when selecting a number in the PSP Agreement column from the PSP overview. | 65627 |
| PSP             | Fixed the issue where the External Reference field did not function correctly in Customer Ledger Entries. | 65985 |

## Continia Banking 2024 R2, Service Pack 7

*Release date, online: May 9, 2025*   
*App version: 25.7.0*

### New functionality

| Functional Area     | Release Notes                                                | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Previously, all bank accounts were shown in the Payment Allocations. The list is now filtered to display only specific payment allocation accounts. | 65512 |
| Payment Export      | Added [cost type](@CB-237) to the Purchase Order page, so it is now possible to edit it there as well. | 65485 |
| Payment Export      | Customer, vendor, and employee templates were extended with payment-related fields relevant to Continia Banking. | 65891 |
| Payment Import      | Improved the assignment of the Last Statement No. when creating a Bank Account Reconciliation or Payment Reconciliation. | 64610 |
| Payment Import      | Improved assignment of Balance Last Statement on Bank Account Reconciliation or Payment Reconciliation when importing a bank account statement. | 64942 |
| Payment Export      | Added [cost type](@CB-237) to Payment Method, so it's no longer necessary to define the cost type for all vendors. | 65484 |
| Payment Export      | Created a job queue to update status in the payment journal. | 65954 |
| Payment Export      | Changed Applies-To ID generation in Payment Export to use a unique reference to avoid confusion when multiple lines exist with the same document number. | 65947 |
| Payment Export      | Resolved an issue in the standard No. Series functionality where non-sequential document numbers during posting could prevent the Last Document No. from being saved correctly. | 53845 |
| Payment Import      | Added support for split rules [using a percentage](@CB-216). | 65290 |
| Payment Import      | Enhanced creation of split rules to prevent creating a rule with an empty Code. | 65288 |

### Bug fixes

| Functional Area | Release Notes                                                | ID    |
| --------------- | ------------------------------------------------------------ | ----- |
| Payment Export  | Fixed two issues in Payment Allocation handling. First, changes to fields like cost type on the main allocation header were not transferred to the linked header. Second, while editing lines, only certain fields (e.g., Payment Description) should be editable - amounts should not be changed. | 65492 |
| Payment Export  | Fixed an issue where using Edit Payment Suggestion from the Payment Journal did not update all relevant fields and tables as expected. | 65804 |
| Payment Export  | Resolved an issue where the selection filter in Payment Export did not function correctly. | 65818 |
| Payment Export  | Fixed an error occurring when a USD bank account was set up in the Payment Balance Account Setup but the payment used an empty currency code (LCY = Euro). The system now allows creating lines without a balance account, but the user must manually enter the required information. | 65319 |
| Payment Export  | Fixed an issue that caused an error when the allowed remittance line length was set to 0, while the number of allowed remittance lines was greater than 0. | 66046 |
| Payment Export  | Fixed an issue where PAIN.008 (Direct Debit) files could not be sent using direct communication through Konfipay, despite the bank account being configured for direct communication. | 66015 |
| Payment Export  | You can now [edit, add, or remove dimensions in Advanced Mode](@CB-240). If Summarize per account is enabled, use the existing action on the Payment Card. If not, use the new action on the subpage to access and edit dimensions per line. | 63449 |
| Payment Import  | Fixed a bug that caused a runtime error during Related Party matching when the address information contained special characters. | 65800 |
| Payment Import  | The document type Invoice is no longer used for applying entries. Instead, the document type Refund is used. | 65632 |
| Payment Import  | In search and split rules, the document type can only be selected when the account type is G/L Account. | 65633 |

## 

## Continia Banking 2024 R2, Service Pack 6, hotfix 1

*Release date, online: April 23, 2025*   
*App version: 25.6.1*

### Bug fixes

| Functional Area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Fixed an error during payment status updates when exporting files with multiple sender accounts. | 65533 |
| Payment Export      | Fixed an issue where updating the payment method code via assisted setup didn't update related vendor or customer bank accounts. | 65350 |
| Payment Export      | Changing **Amount to Pay** to zero in the payment suggestion line now correctly unapplies the line, as zero-amount lines cannot be paid. | 65787 |
| Payment Export      | Corrected the displayed amount in remittance advice when discounts are applied. | 65848 |
| Payment Export      | Improved filtering before validation to prevent validating lines in unrelated journals. | 65789 |
| Payment Export      | Fixed an issue where the wrong Creditor No. was used in Advanced Payment Suggestion. | 65862 |
| Payment Import      | The transaction text for a split rule’s additional child line is now also used during posting in the payment reconciliation journal. | 65344 |
| Payment Import      | The system now shows a warning for incomplete Payment Reference Rules if the Domain Code, Family Code, or Sub-Family Code are not fully filled out. | 65590 |
| Payment Import      | Fixed an issue where using **Remove Match** on the Bank Acc. Reconciliation page didn't update the Reconciliation Status or delete the related Payment Application Proposal. | 65318 |

## 

## Continia Banking 2024 R2, Service Pack 6

*Release date, online: April 2, 2025*  
*App version: 25.6.0*

### New functionality

| Functional Area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Added the product name to pages that share names with other apps. | 64667 |
| General Application | Added a Learn Link to Continia Hub and a Welcome video after completing Bank Account Setup. | 65322 |
| Payment Export      | Added support for [importing camt.054 files](@CB-163) in the payment journal to update payment status to paid and get updated currency exchange rates. | 62745 |
| Payment Export      | The Payment Inf. ID will now be a unique identifier instead of using the first End to End ID. This information will be transferred to all referenced entries, such as Bank Ledger Entry, G/L Entry, Customer Ledger Entry, and Vendor Ledger Entry. The End to End ID will also be transferred to detect related entries. | 64930 |
| Payment Export      | [German regulatory reporting](@CB-210) is now integrated into banking export. You can set up the necessary information in the reporting setup to create reporting entries, which will be transferred to the Z4 file. | 63405 |
| Payment Export      | You can enable Payment Allocations from the Continia Feature Management page. Currently, it supports allocating partial invoice amounts to alternative vendor bank accounts. | 63795 |
| Payment Export      | Added [AML support](@CB-211) for Nordea Corporate Access.    | 62469 |
| Payment Export      | The external document number is now displayed in the payment suggestion lines for vendor payments. | 64307 |
| Payment Export      | Added support for Norway’s Anti-Money Laundering (AML) Act, allowing identity information to be included in payments using the standard approval flow. This enables banks to track payment initiators. | 62468 |
| Payment Export      | Added an option to specify an [alternative beneficiary](@CB-218) in customer/vendor bank accounts. This information will be transferred into the file instead of using vendor/customer account details. | 63801 |
| Payment Export      | Added the Applied Entry Currency Code to the list of Applied Entries, accessible from the Payment Suggestion list. | 64868 |
| Payment Import      | Matching Bank Account Ledger Entries on posting date and amount is now available. The setting can be enabled on the [Banking Import Setup](@CB-14). | 44151 |
| Payment Import      | Added support for [Split Rules](@CB-213) using a Search Text or a Fixed Amount. The feature can be enabled through Continia Feature Management. | 44144 |
| Payment Import      | The label for Invalid Regex when testing Payment Reference Rules on the Payment Reference Rule Card Page now clearly states that the issue is due to the Validation Pattern Code. | 63196 |
| Payment Import      | Removed the Line Filter Dialog page in Bank Account Reconciliation. Previously, this dialog appeared when invoking actions like Set Manual Line, Remove Manual Line, Create Manual Journal, Create Journal Lines from Search Rule, and Transfer Differences. The dialog has been removed to simplify functionality, and the actions now use the selection filter of the bank statement lines sub-page instead. | 63650 |
| Payment Import      | Added the PSP Module to enable file [import from third-party Payment Service Providers (PSPs)](@CB-209) such as eCommerce marketplaces and payment services. Customer payment files can now be imported directly from the PSP into the cash receipt journal. | 55833 |
| Payment Import      | Cleaned up pages in the Import App and removed obsolete elements. | 63966 |
| Payment Import      | Added a Payments to Import quick filter for CAMT54 on the Bank Transactions - Continia Banking page. | 64409 |
| Payment Import      | Added a Payments to Import cue for CAMT54 on the Import Activities page in the Role Center. | 64410 |

### Bug fixes

| Functional Area | Description                                                  | ID    |
| --------------- | ------------------------------------------------------------ | ----- |
| Payment Export  | The default language code in banking export setup (used for remittance advice creation) previously only applied to the filename. Now, the remittance content is also translated accordingly. | 64980 |
| Payment Export  | The **Validate Payments** action in Payment Suggestion is now only active if **Validate Advanced Payment Suggestions** is enabled in Banking Export Setup. | 64147 |
| Payment Export  | Fixed an issue where new errors related to incorrect posting dates in payment suggestions triggered a general error message but were not displayed in the FactBox. | 64008 |
| Payment Export  | All approval entries are now deleted when using **Force Void Payment** in the Payment Journal. | 64113 |
| Payment Export  | Fixed an issue in advance payment suggestions where the sender bank account was not recognized for FIK payments. | 65218 |
| Payment Export  | Fixed an issue where updated rejected payments could still be processed. | 65345 |
| Payment Export  | Fixed an issue where **Amount to Pay** did not work for remittance templates when using standard payment suggestions. | 64741 |
| Payment Export  | Removed Denmark-specific functionality that added leading zeros to Bank Branch No. or Bank Account No. on bank accounts, vendor bank accounts, and customer bank accounts. | 63007 |
| Payment Export  | Previously, if you entered a **Preferred Bank Account Code** on a vendor or customer card, it was impossible to remove it without encountering an error. This issue has been resolved, allowing you to clear the **Preferred Bank Account Code** without receiving the *Bank Account does not exist* error. | 64602 |
| Payment Export  | Fixed an issue where payments with a manual payment method were incorrectly included when exporting or sending payments to the bank. | 64628 |
| Payment Export  | Ensured that the mandate ID always matches the related bank account. Selecting a mismatched mandate will now trigger an error in Direct Debit Journal, Advanced Mode Payment Suggestion, Customer Ledger Entry, and Sales Invoice. | 65128 |
| Payment Export  | Fixed an issue where remittance sending was not correctly executed when using the job queue. | 65130 |
| Payment Export  | Ensured that alternative information fields for vendors/customers are always used together. If alternative information is set up, only those fields are used, and original fields are ignored. | 63410 |
| Payment Export  | Fixed a validation error in the Create Payment action on the vendor ledger entries page, which previously caused a Bank Account No. not found issue. | 63457 |
| Payment Export  | Added support for 731 validation for payment references exceeding 19 characters. | 65117 |
| Payment Export  | The standard action for regulatory reporting codes in the Norwegian version is now hidden when using a banking export journal. | 65311 |
| Payment Export  | Fixed an issue with the Credit/Debit indicator in Payment Status Entry. | 65352 |
| Payment Export  | Fixed an issue in advanced mode where remittance information could not be added to payments. A new action is now available on Payment Suggestion Lines to access remittance information when payments are not summarized. If payments are summarized, the action should be used on the Payment Suggestion Header instead. | 64563 |
| Payment Export  | Fixed an issue where running the Security Setup only displayed one Payment Journal Batch instead of all available batches. | 65073 |
| Payment Import  | Fixed an issue where Banking Import fields and actions were not displayed after Business Central logged out due to inactivity. They are now properly restored after re-login. | 65264 |
| Payment Import  | Bank Account Reconciliation Lines are now updated accordingly when a search rule is deleted. | 63703 |



## Continia Banking 2024 R2, Service Pack 5

*Release date, online: March 10, 2025*   
*App version: 25.5.0*

### New functionality

| Functional Area | Description                                                  | ID    |
| --------------- | ------------------------------------------------------------ | ----- |
| Payment Import  | The automatic matching now correctly matches batch payments made from Banking when a Payment Batch ID is used. | 60660 |
| Payment Import  | Added a new sub-group on the Banking Import Setup for fields related to importing payments (CAMT54) into the Payment Reconciliation Journal. | 62998 |
| Payment Import  | Added a total for **Transferred Difference Amount** on the **Payment Application Review** page and **Apply Ledger Entries** page. | 63770 |
| Payment Import  | When assigning an account to a search rule, the dimensions from the account are now transferred to the search rule. | 63983 |

### Bug fixes

| Functional Area         | Description                                                  | ID    |
| ----------------------- | ------------------------------------------------------------ | ----- |
| Payment Export          | The dynamics validation now applies to all editable fields on the payment suggestion card. | 63143 |
| Payment Export          | Fixed an issue where the Payment Suggestion was marked as posted despite open headers due to deletions in the general journal. This occurred in summarized payments due to a missing filter, which has now been corrected. | 63989 |
| Payment Export          | Fixed an issue where remittance information was not correctly updated when using the edit functionality in advanced mode, causing validation errors. | 64366 |
| Payment Import          | Fixed an error where the Bank Account Reconciliation Page did not update correctly when creating a new bank account reconciliation with only one bank account. | 63701 |
| General Application     | Improved Role Center performance.                            | 64350 |
| Payment Export          | Fixed an issue where, in some cases, the **Payment Status** changed from rejected unintentionally. | 64388 |
| Platform and Technology | Added support for the **Demo Scenarios** page in the Demo App. | 64577 |
| Payment Import          | Fixed an issue in Bank Account Reconciliation where a custom posting description was not assigned to journal lines when creating a manual journal line. | 63626 |
| Payment Import          | Fixed an issue where the Document Type field was left blank when using the Transfer Difference to Account action in Bank Account Reconciliation. | 63699 |
| Payment Import          | Fixed an error in the calculation of the difference amount when creating manual journal lines in Bank Account Reconciliation. | 63211 |
| Payment Import          | Fixed an issue where dimensions from a Search Rule were not assigned to the Bank Account Reconciliation Line. | 63357 |
| Payment Import          | The Show Reconciliation Line Details action was incorrectly placed on the General Journal Page. It has now been moved to the **Lines** tab. | 63950 |
| Payment Import          | Fixed an issue where dimensions were deleted when using the **Apply To Account** action in the Payment Reconciliation Journal. | 63424 |
| Payment Export          | Fixed an issue where clicking **Update Status** after exporting a payment in the Payment Journal did not change the status correctly. It now changes to Processing after the first click and Paid after the second click. | 62565 |
| Payment Export          | Fixed an issue where the **Validate Payments** action on the Payment Overview had no effect. It is now working as expected. | 63990 |
| Payment Export          | Fixed an issue where the **Cost Type** was not transferred correctly to the General Journal Line when summarizing was used. Even though the Cost Type was present on the Payment Card, it was blank on the created journal line. | 64143 |

## Continia Banking 2024 R2, Service Pack 4

*Release date, online: February 14, 2025*   
*App version: 25.4.0*

### New functionality

| Functional Area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Refactored the **Validation Type** as an interface to improve modularity and maintainability. | 63203 |
| General Application | Added unit tests for validation codeunits to enhance code reliability and coverage. | 63513 |
| General Application | Implemented the use of the Core Management Interface for IBAN lookup to improve accuracy and efficiency. | 63564 |
| Payment Export      | Adjusted the **Move Payment Date** default setting for bank closing days. | 62050 |
| Payment Export      | Ensured that payment suggestions are only created when payments are actually generated. | 62569 |
| Payment Export      | Integrated the ability to switch between standard and advanced payment export modes at the journal batch level, ensuring flexibility in payment processing. For more information, see the [The Advanced Payment Suggestion Option](@CB-145) article. | 63197 |
| Payment Import      | Added a new action on the Bank Account Card Page to open the **Bank Acc. Reconciliations List Page**, allowing quick creation of new bank account reconciliations. | 61381 |
| Payment Import      | Modified the import process for CAMT.054 and CAMT.053 files to allow reimporting of lines into the Bank Transaction Line. For more information, see the [Enabling Reimport of Bank Statement Files](@CB-183) article. | 62833 |
| Payment Import      | Added posting group information to the **Match Details** FactBox on the **Payment Reconciliation Journal** Page and introduced a **Dimensions** FactBox for improved financial analysis. | 62891 |
| Setup Server        | Fixed and improved the import functionality for setup server files. | 61650 |
| Setup Server        | Improved the Setup Server Version Management by replacing the hardcoded version label in the CTS-CT ICoreMgt codeunit with a visible version display in the **Continia Banking Setup** card. Additionally, a new **Fetch Latest Setup Server Version** action has been added to the **Troubleshooting** section, allowing users to manually trigger an update from Continia Online, similar to the automatic update functionality in **Continia Banking Setup**. The action prompts users for confirmation before retrieving the latest version. | 61554 |

### Bug fixes

| Functional Area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Added usage registration for Posted Payment Reconciliation Journal lines to improve tracking and reconciliation processes. | 62500 |
| Payment Export      | Fixed an issue where a warning was missing in the **Suggestion Head** and **General Journal Line** when the **Remittance Information** exceeded the allowed length and could not be accurately represented. | 63408 |
| Payment Export      | Implemented a requirement for recipient bank account codes in the **Advanced Payment Suggestion** feature to ensure correct payment processing. | 63552 |
| Payment Export      | Fixed an issue where payment reference templates were not imported correctly. | 63553 |
| Payment Export      | Resolved an issue where the payment reference template lookup was not functioning as expected. | 63554 |
| Payment Import      | Fixed an issue where imported bank transaction files with no lines were not automatically marked as **Imported To Company**. | 63358 |
| Payment Import      | Fixed an inconsistency error in the payment reconciliation journal that occurred when a line applied to an entry resulted in an additional adjustment line. | 63590 |

## Continia Banking 2024 R2, Service Pack 3, hotfix 3

*Release date, online: February 6, 2025*   
*App version: 25.3.3*

### New functionality

| Functional Area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Improved the template structure to enhance usability and maintainability. | 62572 |

### Bug fixes

| Functional Area         | Description                                                  | ID    |
| ----------------------- | ------------------------------------------------------------ | ----- |
| General Application     | Updated the activation procedure to ensure it runs correctly when initiated from **Assisted Setups.** | 63363 |
| Payment Export          | Fixed an issue where invoking the Renumber Document Nos. action in the Payment Journal caused errors. | 60324 |
| Payment Export          | Prevented modifications to certain fields on posted purchase invoices, ensuring changes are only made through appropriate suggestions instead of directly editing posted documents. | 60522 |
| Payment Export          | Fixed a validation issue where selecting a non-banking-related payment method in **Sales and Purchase Documents** triggered an error unnecessarily. Validation is now turned off for non-banking-related payment methods. | 61401 |
| Payment Export          | Ensured that **Remittance Information Templates** are correctly applied when creating payment suggestions, instead of defaulting to values from the export setup. | 63141 |
| Payment Export          | Moved the **Move Regulatory Reporting Codes** action from the **Functions** menu to the **Related** menu for better organization. | 63201 |
| Payment Export          | Fixed an issue where **Regulatory Reporting Codes** were not transferred from the **Vendor Legal Entity** to the **Payment Suggestion.** | 63209 |
| Payment Export          | Relocated the **Rebuild Remittance Information** menu item from the **Related** section to **Actions** for better accessibility. | 63229 |
| Payment Export          | Resolved an issue where opening **Remittance Information** from an empty **Payment Journal** displayed remittance details from all open suggestions. Now, remittance info is only available when journal lines exist. | 63248 |
| Payment Export          | Replaced the outdated **Vendor Specific** setup with the new **Recipient Specific** setup. | 63409 |
| Payment Export          | Ensured **Regulatory Reporting Descriptions** do not exceed the bank's allowed character length. | 63459 |
| Payment Import          | Fixed an inconsistency error that occurred when manually applying accounts after using the **Apply To Account** action. | 63169 |
| Payment Import          | Resolved an issue in the **Payment Reconciliation Journal** where applying an account manually caused the **Apply To Account** action to overwrite all selected lines with the first line's account. | 60506 |
| Payment Import          | Fixed incorrect debit/credit signs on **General Journal Lines** when an **Account Type/No.** was also a **Bank Account,** particularly in **Bank Account Reconciliation.** | 63452 |
| Platform and Technology | Fixed an issue where **Bank Connect Certificate Updates** failed for certain banks. | 63514 |
| Platform and Technology | Resolved an issue where the **Pmt. Entry Val. Map. Direct** setting caused validation errors in **Nordea Manual Exports.** | 63538 |

## Continia Banking 2024 R2, Service Pack 3, hotfix 2

*Release date, online: January 23, 2025* 
*App version: 25.3.2*

### Bug fixes

| Functional Area | Description                                                  | ID    |
| --------------- | ------------------------------------------------------------ | ----- |
| Payment Export  | If a general journal line is deleted, related banking records will also be deleted, even if Banking is not activated. This issue has been fixed. | 61899 |
| Payment Export  | The account types G/L Account and Bank Account are no longer available in the payment suggestion card as they were not needed. | 62104 |
| Payment Export  | Fixed an issue where manually entered amounts in the advanced payment suggestion were not transferred to the journal when no entry application was applied. | 62765 |
| Payment Export  | Fixed duplicate remittance information when compression was activated and the first line was too long. Also resolved an issue where deleted journal lines left remittance entries in the background, preventing incorrect data from affecting other processes. | 62967 |
| Payment Export  | Fixed an issue where the **Send remittance advice** option prevented the deletion of a payment suggestion after transferring it to the general journal. | 63000 |
| Payment Export  | Fixed an issue where the status in the **Suggestion Card** changed to partially posted even when fully posted, rendering the suggestion unusable. | 63015 |
| Payment Export  | Fixed an issue where Customer/Vendor Bank Account Names longer than 50 characters could not be processed. | 63010 |
| Payment Export  | Fixed an error when running **Suggest Vendor Payments** with Vendor Ledger Entries using Payment Method FIK71 while the Vendor was set up for BTD. Now, Recipient Bank Account No. is not filled for such cases. | 63016 |
| Payment Export  | If summarizing is not activated, credit memos are included in the suggestion but are not marked as To be Paid. This prevents errors in payment files due to mismatched amounts. | 62778 |
| Payment Import  | Handling of LCY rounding differences has been added to the payment reconciliation journal to prevent inconsistency errors. | 62791 |
| Payment Import  | Fixed an issue where posting difference lines with applied entries in the payment reconciliation journal caused inconsistency errors. | 62904 |

## Continia Banking 2024 R2, Service Pack 3, hotfix 1

*Release date, online: January 14, 2025* 
*App version: 25.3.1*

### New functionality

| Functional Area | Description                                                  | ID    |
| --------------- | ------------------------------------------------------------ | ----- |
| Payment Import  | Fixed an issue where the applied amount was doubled in the Payment Reconciliation Journal line. | 62531 |
| Payment Import  | Resolved a bug where posting a foreign currency (FCY) vendor on account in the Payment Reconciliation Journal resulted in an incorrect amount. | 62538 |

## Continia Banking 2024 R2, Service Pack 3

*Release date, online: January 13, 2025*   
*App version: 25.3.0*

### New functionality

| Functional Area | Description                                                  | ID    |
| --------------- | ------------------------------------------------------------ | ----- |
| Payment Export  | Investigate Create Payment action on Employee Ledger Entries. | 63458 |

### Bug fixes

| Functional Area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Fixed issue preventing manual communication for certain Danish banks using BEC, Bankdata, or SDC. | 61182 |
| General Application | Created CSV Import Interface.                                | 61371 |
| General Application | Fixed formatting validation error for values used in later validations. | 61631 |
| General Application | Separated CSV app from Import app.                           | 61372 |
| General Application | Prevented bank requests with empty fields in Bank Account Setup. | 61834 |
| Payment Export      | Fixed error when changing the Payment Method Code in advanced mode using Edit Payment Suggestion. | 61967 |
| Payment Export      | Fixed issue where Validate Payments in Payment Suggestion Overview was not working correctly. | 62102 |
| Payment Export      | Streamlined SEPA Mandate ID behavior when exporting payments from Direct Debit journals. Now checks Ignore Exp. Number of Debits before closing mandates. | 62133 |
| Payment Export      | Bank Closing Days Wizard did not allow entering single bank closing days. | 62441 |
| Payment Export      | Lookup was not working on Suggest Customer, Vendor, and Employee Payments reports for various templates. | 62457 |
| Payment Export      | Fixed issue where an empty PlusGirot Payment entry field overwrote BankGirot values. | 62574 |
| Payment Export      | Fixed issue where updating the posting date on the suggestion card did not update the record. | 62581 |
| Payment Import      | SEPA DD Amendment history was not being created for Journal lines. | 62288 |
| Payment Import      | CSV-Port Wrong Posting date issue.                           | 62343 |
| Payment Import      | Importing file to File Archive and processing.               | 55862 |
| Payment Import      | Automatic matching now supports batch payments using Payment Information ID (PmtInfId). Feature enabled in Continia Feature Management Page. | 47787 |
| Payment Import      | Fixed issue in Danish localization when applying vendor ledger entries in bank account reconciliation with both Creditor No. and Recipient Bank Account specified. | 62479 |
|                     |                                                              |       |

## Continia Banking 2024 R2, Service Pack 2, hotfix 2

*Release date, online: January 2, 2025*  
*App version: 25.2.2*

### Bug fixes

| Functional Area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Fixes issue with VAT No validation in the Assisted Setup for SEB Direct communication. | 62431 |

## Continia Banking 2024 R2, Service Pack 2, hotfix 1

*Release date, online: December 20, 2025*  
*App version: 25.2.1*

### New functionality

| Functional Area | Description                                                  | ID    |
| --------------- | ------------------------------------------------------------ | ----- |
| Payment Export  | Added a filter for already posted Bank Accounts from List.   | 61492 |
| Payment Import  | Show **Payment Reference Rules Page** when enabling the setting on the Banking Import Setup. | 61880 |

### Bug fixes

| Functional Area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Fixed a recursive infinity loop issue.                       | 62330 |
| General Application | Fixed the problem where it was impossible to create a validation entry. | 62175 |
| Payment Export      | Fixed problem where the wrong Payment Amount was shown if the payment currency was changed. Added a new field to show the amount in the Payment Currency. | 61510 |
| Payment Export      | Fixed an error in the Assisted Setup Set up Recipient Payment Information when a preferred Bank Account was filled in Customer setup. | 62080 |
| Payment Import      | The filter on account is no longer cleared after manually applying an entry on the payment application review page. | 62350 |

## Continia Banking 2024 R2, Service Pack 2

*Release date, online: December 13, 2024*   
*App version: 24.4.0 and 25.2.0*

### New or changed functionality

| Functional Area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Expanded the character limit for the **Expression** field from 250 to 2000 for enhanced validation and entry flexibility. | 61142 |
| General Application | The requester's name is now added to requests for missing banks in the **Bank Account Setup** page. | 61783 |
| Payment Export      | Search functionality for single payments has been introduced in the suggestion list. | 45999 |
| Payment Export      | Added functionality to enter single payment information directly in purchase or other financial documents. | 46001 |
| Payment Export      | A new report has been integrated for payment suggestion lists. Although not yet available in the menu, it will be released soon. | 60974 |
| Payment Export      | Added the ability to enter single payment information directly in the General Journal Line. | 46000 |
| Payment Import      | A new preview feature enables the import of CAMT.054 files into the Payment Reconciliation Journal, available through the **Continia Feature Management** page. | 55923 |
| Payment Import      | Added Payment Reference Rules as a preview feature in Banking Import, allowing users to define rules for payment references and match ledger entries in reconciliations. | 60668 |
| Payment Import      | Introduced the first edition of regulatory reporting codes.  | 60689 |
| Payment Import      | A preview feature was added for Matching with Payment References, allowing rule-based reconciliation using the **Continia Feature Management** page. | 60720 |
| Payment Import      | Default regular expressions for Payment Reference Rules have been added to Banking Import as a preview feature. These expressions support Swiss QR and FIK references and can be enabled via the **Continia Feature Management** page. | 60746 |
| Payment Import      | During import, statements without lines will be marked as imported for the company reconciliation, skipping these invalid entries. | 61900 |

### Bug fixes

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| General Application | Resolved a setup job queue failure caused by unsupported bank accounts during configuration. | 62048  |
| General Application | Fixed an issue that caused job queue creation to fail during activation, specifically when using delegated admin access. | 61785  |
| Payment Export      | Validation backtracking issue has been resolved when using Payment Entry Value Mapping. | 60757  |
| Payment Export      | The inactive **Remittance Advice** field in SDCISO20022 is no longer retained for value mappings. | 61024  |
| Payment Export      | Resolved an issue where the reverse discount date function didn't work for summarized payments after deleting a Payment Journal Line. This now correctly restores the discount date for summarized payments. | 61041  |
| Payment Export      | Fixed an issue where the Minimum Posting Date was not updating correctly when using the Update Posting Date feature on Payment Suggestion Lines. | 61348  |
| Payment Export      | Resolved visibility issues for the **New Bank Account** and **Bank Account Verification Status** fields in the Direct Debit Journal and the Payment Journal. | 61462  |
| Payment Export      | Addressed an unresolved error in the Direct Debit Journal where the Currency Code could not be summarized per account. | 61490  |
| Payment Export      | Fixed an error in purchase documents when selecting a vendor bank account for the **Pay-to Vendor Bank Account No.** field. | 61809  |
| Payment Export      | Corrected an issue in the **Edit Payment Suggestion** function where changing the Posting Date caused default values to populate the **Recipient Bank Account** and **Direct Debit Mandate ID** fields. | 61949  |



## Continia Banking 2024 R2, Service Pack 1, hotfix 1

*Release date, online: November 20, 2024*   
*App version: 24.3.0 and 25.1.1*

### Bug fixes

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| General Application | Fixed an issue causing the Customer Bank Account to not update correctly during the IBAN lookup process. | 60418  |
| General Application | Fixed the Bank Branch Number lookup issue in assisted setup for bank account configurations (Denmark only). | 61219  |
| General Application | Implemented a check to prevent the insertion of empty bank information records. | 61297  |
| Payment Export      | Fixed an issue where Payment Suggestion would incorrectly modify the discount date on ledger entries when **Find Payment Discount** or **Always Discount** was not set. | 61040  |
| Payment Export      | Resolved an issue where the original discount date was not correctly restored for summarized payments after deleting Payment Journal Lines. | 61041  |
| Payment Export      | Resolved an issue where manual payments did not correctly update their status during payment suggestions. | 61181  |
| Payment Export      | Added functionality to handle cases where both the Creditor No. and recipient bank account are set on the General Journal Line for DK localization. | 61296  |

## Continia Banking 2024 R2, Service Pack 1

*Release date, online: November 17, 2024* 
*App version: 24.3.0 and 25.1.0*

### New or changed functionality

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| General Application | Optimized handling of validation sets and added `AssistEdit` for field format adjustments. | 60209  |
| General Application | Added `ReadIsolation` handling to improve data integrity within the Banking module. | 58663  |
| Payment Export      | Added default validation values for payment export processes. | 60761  |
| Payment Export      | Implemented logic to use a vendor's default cost type if none is present on the vendor ledger entry. | 60790  |
| Payment Export      | Introduced drilldown functionality in the **Payment Overview** page. | 60826  |
| Payment Export      | Extended the assisted setup to easily enable the **Allow Summarizing Payments** option without manual edits. | 60922  |
| Payment Export      | Enhanced payment suggestions to show the already paid amount in advanced mode, with the ability to add the field through personalization. | 60933  |
| Payment Export      | Introduced the ability to create new payment heads for individual entries. | 60969  |
| Payment Export      | Integrated a basic report for **Payment Suggestion Lists** into banking, though it is not yet available in the main menu. | 60974  |
| Payment Export      | Enhanced miscellaneous remittance handling.                  | 59747  |
| Payment Import      | Enabled the setup of proprietary bank transaction code issuers for specific bank systems, which can be imported during bank account setup. | 60501  |
| Payment Import      | Introduced transformation rules to convert text based on substring logic, primarily used with proprietary bank transaction codes. | 60492  |
| Payment Import      | Made minor improvements to translations of captions, tooltips, and actions in Danish for Payment Import functionality. | 52163  |
| Payment Import      | Improved alignment of footer fields between Bank Statement Lines and Bank Account Ledger Entries on the Bank Reconciliation Page. | 59676  |
| Payment Import      | Added sub-groups on the Bank Transaction Card Page for better organization of fields. | 59941  |
| Payment Import      | Added functionality to convert proprietary bank transaction codes for specific bank systems using transformation rules. This setup is accessible from Banking Import Setup. | 60258  |
| Payment Import      | Created a table and page to manage Default Statement Description Templates for specific bank systems. | 60486  |
| Payment Import      | Added default bank statement description templates for Deutsche Bank on the setup server. | 60490  |
| Payment Import      | Added the ability to set up Default Bank Statement Description Templates, enabling different templates based on specific bank systems. These templates are imported and assigned during assisted bank account setup. | 60485  |
| Payment Import      | Enabled the creation of Banking-specific transformation rules for text conversion using substring logic. Rules are applicable for proprietary bank transaction codes. | 60493  |
| Payment Import      | Added a transformation rule to extract specific characters from text for use with proprietary bank transaction codes. | 60499  |
| Payment Import      | Added a proprietary bank transaction code issuer for Deutsche Bank with issuer code *DK* on the setup server. | 60502  |

### Bug fixes

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| Payment Export      | Improved direct debit suggestion logic to ensure invalid mandates are not suggested, while allowing manual selection with status information. | 60543  |
| Payment Export      | Corrected payment suggestion validation to account for differences between summarized and non-summarized payments. Header values alone are no longer used. | 60994  |
| Payment Export      | Fixed incorrect handling of the Sender Reference Template, ensuring it is properly applied. | 61154  |

## Continia Banking 2024 R2, hotfix 3

*Release date, online: October 24, 2024*   
*App version: 24.2.3 and 25.0.3*

### New or changed functionality

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| Payment Export      | Direct Debit Export corrected to separate DirectDebit B2B and Core in different files. | 59927  |
| Payment Export      | Addition of an `OnValidate` trigger for the **Batching Allowed** option in Bank System Payment Method. | 60565  |
| Payment Import      | The Import App's usage registration now logs the Statement Type to show the origin of journal lines and provide insights into the statement types users are utilizing. | 59133  |

### Bug fixes

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| Payment Export      | Resolved an issue where the master account number set up in Continia Finance wasn't used in payment suggestions due to an incorrect search function. | 60331  |
| Payment Export      | Fixed an issue where attempts to format a field value caused an error during journal line validation. | 60340  |
| Payment Export      | Enabled direct debit features without requiring manual activation in the banking export setup. | 60382  |
| Payment Export      | Fixed an error in Direct Debit account linking payments where a positive vendor amount triggered a validation error, requiring the amount to be less than zero. | 60468  |
| Payment Export      | Payment summarization when processing account linking or association payments is now enforced. | 60536  |
| Payment Export      | Fixed the `OnAfterStartActivation` event to function correctly with OnPrem environments. | 60552  |
| Payment Export      | Resolved an issue related to summarization of vendors with associations, even if summarization at the vendor level is deactivated. | 60579  |
| Payment Export      | Corrected the calculation for the QR check digit.            | 60588  |
| Payment Export      | Resolved a QR check digit issue that was preventing accurate QR code functionality. | 60624  |
| Payment Export      | Fixed an issue where related information remained visible in the payment overview of open suggestions after posting, due to a missing status change in the posting process. | 60894  |
| Payment Export      | Corrected an error in structured remittance creation, ensuring proper handling when both payment and document references are used. | 60898  |
| Payment Export      | Addressed an error in payment suggestions caused by the presence of both the Creditor No. and Recipient Bank Account on Vendor Ledger Entries (specific to DK). | 60918  |
| Payment Import      | Removed the **MT940** option from the **Statement Type Filter** field on the **Search Rule** page. | 60519  |
| Payment Import      | Fixed an issue where the **Suggest Lines** action in the Bank Acc. Reconciliation didn’t update the reconciliation status to **Completed** when **Match Automatically** was used afterward. | 60704  |
| Payment Import      | Added a missing filter for the **Active line** and **Selected lines** options to prevent lines from other statements from being processed in the Bank Acc. Reconciliation. | 60505  |
| Payment Import      | An invalid search rule already assigned to a Bank Acc. Reconciliation Line can now be finalized. A line marked as **Search Rule invalid** allows the user to modify the search rule. Error message will no longer appear if lines have a status of **Unsolved** or **Search Rule invalid**. | 60520  |

## Continia Banking 2024 R2, hotfix 1 and 2

*Release date, online: October 3 and 8, 2024*   
*App version: 24.2.1, 24.2.2 and 25.0.1, 25.0.2*

### New or changed functionality

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| Payment Export      | Implemented the ability to add the Charge Bearer (<ChrgBr>) at the Transaction Information level, required for cases such as DACH BTI. The Charge Bearer on Payment Information level will now be cleared when set at the transaction level to ensure correct export. | 60201  |



## Continia Banking 2024 R2

*Release date, online: October 1, 2024*   
*App version: 24.0.0 and 25.0.0*

### New or changed functionality

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| General Application | Continia Banking has been released for BC v24 and BC v25, including [localizations for DK, SE, DE, CH, and AT](@CB-56). For more information, see the [Business Functionality](@CB-144) article. | NA     |



<style>
 .content table tr td:nth-child(1),
 .content table tr td:last-child {
 width: 210px;
 }

 .content table tr td:last-child {
 width: 75px;
 }
</style>