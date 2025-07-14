---
title: Detailed Changelog for Continia Payment Management 2024 R1
description: Changelog containing an overview of all new updates, features, and hotfixes for Continia Payment Management 2024 R1
date: 01-10-2024
id: PM-393
lang: en
---

# Detailed Changelog for Continia Payment Management 2024 R1

This article lists all new updates, features, service packs, and hot fixes for Continia Payment Management 2024 R1. 

> [!TIP]
> As a Continia partner, we can notify you of new Payment Management versions and service packs whenever we release them. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360011738679-Receive-a-notification-upon-new-Payment-Management-App-releases) in the Continia PartnerZone (only available to partners).

## Payment Management 2024 R1 Service Pack 2, Hotfix 9

*Release date, online: September 24, 2024*  
*App version: 24.2.9*

| Functional area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Enhanced error handling for Rabobank account connections by adding functionality to save the bank's response when the account status is not ready. This allows for better troubleshooting by storing the output in the file archive for review when connection issues occur. | 59439 |

## Payment Management 2024 R1 Service Pack 2, hotfix 7 and 8

*Release date, online: September 12, 2024*  
*App version: 24.2.8*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Platform and Technology   | Update the handling of the Yapily refresh token.             | 59335 |
| Payment and Cash Receipts | Added checks in Validate triggers to fill missing BG and PG information in the Payment Journal. | 57112 |
| Platform and Technology   | Fix for handling of address for bulk payments through Yapily. | 58115 |
| Payment and Cash Receipts | Added functionality to create Payment Notifications when a Balance Account or Payment Method is defined. | 59185 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Statement Intelligence    | Matching on reversed lines occurred with an empty Transaction ID field. A check has been implemented to prevent matching on blank values. | 58824 |
| Payment and Cash Receipts | A fix has been implemented to update the payment method description when the Payment Method Code is selected. | 58861 |

## Payment Management 2024 R1 Service Pack 2, hotfix 6

*Release date, online: August 19, 2024*  
*App version: 24.2.6*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Platform and Technology   | Improved handling of address information for bulk payments processed through Yapily. | 58115 |
| Payment and Cash Receipts | Added functionality to include the Journal Batch ID in payment journal lines when suggesting payments. | 58307 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Enhanced the ability to deactivate Payment Approval Workflows. | 58403 |
| Payment and Cash Receipts | Introduced functionality to delete reversal lines generated during the Bank Account Reconciliation process. | 58625 |
| Statement Intelligence    | Resolved issue with merging statement lines that caused errors in Statement Intelligence matching. | 58624 |

## Payment Management 2024 R1 Service Pack 2, hotfix 5

*Release date, online: July 23, 2024*  
*App version: 24.2.5*

### Bug fixes	

| Functional area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | The issue with refreshing the Rabobank token has been fixed. | 57514 |

## Payment Management 2024 R1 Service Pack 2, hotfix 4

*Release date, online: July 18, 2024*  
*App version: 24.2.4*

### New or changed functionality

| Functional area            | Description                                                  | ID    |
| -------------------------- | ------------------------------------------------------------ | ----- |
| Payments and Cash Receipts | Enhanced company information for Bank Giro.                  | 57814 |
| Platform and Technology    | Customers experienced delays and long wait times when opening pages due to unnecessary bank account verification checks. This issue was caused by a missing check in the Payment Management Setup, which performed verification even when bank account verification was not activated. This has now been resolved | 57703 |
| Statement Intelligence     | Lines can now be deleted on the reversal page.               | 57891 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Fixed check on Bank system Code when updating Payment Information ID during status update. | 57896 |
| Payment and Cash Receipts | Settings where missing for the Payment Receipt Import. This has now been resolved. | 57900 |

## Payment Management 2024 R1 Service Pack 2, hotfix 3

*Release date, online: July 16, 2024*  
*App version: 24.2.3*

### New or changed functionality

| Functional area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | On the Direct Debit setup, you can now select **Compress File** to compress the manual direct debit file when exporting from a Direct Debit collection. | 57792 |

### Bug fix

| Functional area        | Description                                                  | ID    |
| ---------------------- | ------------------------------------------------------------ | ----- |
| Statement Intelligence | Solves problem of inconsistent payment identification in account statements, impacting payment matching in payment management. | 53819 |

## Payment Management 2024 R1 Service Pack 2, hotfix 2

*Release date, online: July 15, 2024*  
*App version: 24.2.2*

### New or changed functionality

| Functional area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | The Direct Debit collection now allows for the simultaneous rejection of multiple entries. | 57791 |
| General Application | When setting up direct debit, you can now select **Compress File** to compress the manual direct debit file during export from Direct Debit collection. | 57792 |
| General Application | You can now batch process direct debits with manual communication when exporting from the Direct Debit collection. | 57793 |

### Bug fixes

| Functional area        | Description                                                  | ID    |
| ---------------------- | ------------------------------------------------------------ | ----- |
| Statement Intelligence | Fixed an issue with inconsistencies in payment identification within account statements. | 53819 |

## Payment Management 2024 R1 Service Pack 2, hotfix 1

*Release date, online: July 9, 2024*  
*App version: 24.2.1*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Using the `revoketoken` action now also deletes authentication in Business Central. | 57575 |



## Payment Management 2024 R1 Service Pack 2

*Release date, online: June 28, 2024*  
*App version: 24.2.0*

### New or changed functionality

| Functional area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Added a tile in the Role Center for an overview of unverified bank accounts. | 55225 |
| General Application | A new Changelog page has been added to provide an overview of the verification history for all bank accounts, including those of customers, vendors, and employees. This page includes sorting and filtering options, simplifying the review of account changes for audits and approvals. | 56855 |
| General Application | Introduced a job queue to refresh tokens, reducing expired token issues in the direct communication with Rabobank. | 57289 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Platform and Technology   | Fixed an issue where an event subscriber incorrectly triggered a license check. | 56903 |
| Payment and Cash Receipts | Fixed an issue where the cash receipt format set to *Text* on the bank account card did not override the format setting on the bank card. This ensures the correct format is used for cash receipt imports. | 57073 |
| Statement Intelligence    | Fixed an issue where statement lines with blank descriptions were incorrectly merged when search text in merge rules was empty. | 57111 |
| Payment and Cash Receipts | Fixed incorrect variables in labels for payment suggestions for consolidated customers/vendors. | 57205 |
| Payment and Cash Receipts | Fixed an issue where the **Message to Recipient** field was not properly auto-filled when suggesting customer payments. | 57272 |
| Payment and Cash Receipts | Implemented a fix to enable processing of entries with the document type *Payments* for suggesting customer refunds. | 57273 |
| General Application       | Improved logging for bank account updates and creations using `.insert()` | 57317 |
| General Application       | Made minor UX improvements to the Modulus dropdown on the bank account card. | 56988 |



## Payment Management 2024 R1 Service Pack 1, hotfix 2

*Release date, online: June 4, 2024*  
*App version: 24.1.2*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | With the recent update to Yapily for exporting bulk payments, a new filter based on the posting date has been introduced. Now, only transactions sharing the same posting date can be exported together as a bulk. | 56775 |

## Payment Management 2024 R1 Service Pack 1, hotfix 1

*Release date, online: June 3, 2024*  
*App version: 24.1.1*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Implemented automation for voiding payments in the Payment journal after bank rejection. | 56698 |
| Payment and Cash Receipts | Performance enhancement for approving payment lines in the Payment journal. | 56711 |
| Payment and Cash Receipts | Added dimensions to the General Reconciliation Rules, enabling customers to add dimensions to their rules. | 56712 |
| Statement  Intelligence   | The `OnAfterFilterBankAccountLedgerEntry` event has been added in Statement Intelligence to allow sorting and filtering of the Bank Account Ledger Entries before they are reconciled. | 56691 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Resolved an issue where creating a journal line from a suggestion using the Create Journal Lines button resulted in an error. | 56714 |
| Statement  Intelligence   | Corrected a problem where the Statement Intelligence setup did not initialize properly, causing non-default split characters to be ignored. | 56713 |





## Payment Management 2024 R1 Service Pack 1

*Release date, online: May 30, 2024*  
*App version: 24.1.0*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Addressed a rounding issue when calculating G-Account amounts during invoice payments, which could cause errors due to discrepancies when rounding amounts such as 0.005 to 0.01. The G-Account amount is now saved with two decimals to prevent these errors. Additionally, functionality has been implemented to prevent double payments of G-Account amounts. | 55397 |
| Payment and Cash Receipts | Added support for processing entries with document type payment when suggesting customer payments. | 55026 |
| Payment and Cash Receipts | Fixed an issue in the CSV import for the PSP module that caused the import to fail if the file had been opened and saved by a user. | 55528 |
| Payment and Cash Receipts | Added functionality allowing users to change the modulus check used in the Payment Reference Mask, now supporting Modulus 11 and 731, enhancing the capabilities of the cash receipt journal. | 55661 |
| Payment and Cash Receipts | Improved background task performance and reduced unnecessary bank account verification checks to address performance issues. The timeout parameter for background tasks has been reduced. Additionally, a check for active approval and verification notifications has been introduced to minimize redundant verification status checks. | 56521 |
| Statement Intelligence    | Validation of the creditor identifier for Direct Debit Collections has been implemented and an error will be displayed in the FactBox if it is missing. | 45666 |
| Statement Intelligence    | Added functionality to allow user to adjust number of Direct Debit Entries in a collection. The Default value can be set on the Direct Debit Setup page, but the value can always be adjusted on the request page. | 56140 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Fixed an issue with Rabobank payment status updates, ensuring that payments spread over longer periods are correctly updated. | 56503 |
| Payment and Cash Receipts | Resolved an issue where the temporary Applies-To ID on customer ledger entries was not cleared after suggesting customer payments. | 56611 |
| Statement  Intelligence   | Resolved an issue with inconsistencies in the payment identification returned in account statements, affecting only certain banks. These inconsistencies have resulted in challenges in accurately matching payments created within payment management systems. | 53819 |



## Payment Management 2024 R1, hotfix 2

*Release date, online: May 1, 2024*  
*Release date, on-premises: May 6, 2024*  
*App version: 24.0.2*

### New or changed functionality

| Functional area         | Description                                                  | ID    |
| ----------------------- | ------------------------------------------------------------ | ----- |
| Platform and Technology | Implemented a minor fix to ensure correct date formatting when importing transactions from Yapily. | 55270 |

## Payment Management 2024 R1, hotfix 1

*Release date, online: April 23, 2024*  
*Release date, on-premises: April 26, 2024*  
*App version: 24.0.1*

### New or changed functionality

| Functional area         | Description                                                  | ID    |
| ----------------------- | ------------------------------------------------------------ | ----- |
| General Application     | Implemented telemetry to track matching statistics accurately in bank account reconciliation. | 54976 |
| Statement  Intelligence | Implemented functionality for Rabobank to update Payment Journal line status based on statement lines. | 54973 |

### Bug fixes

| Functional area        | Description                                                  | ID    |
| ---------------------- | ------------------------------------------------------------ | ----- |
| General Application    | Adjusted SE Organization number validation to accept the format for Swedish suppliers. | 55062 |
| General Application    | Resolved permission issue in Bank Account Reconciliation module when Payment Management is inactive. | 54842 |
| Statement Intelligence | Corrected ABN Payment Identification Search Rules to ensure accurate matching. | 54974 |

## Payment Management 2024 R1

*Release date, online: April 2, 2024*  
*Release date, on-premises: April 11, 2024*  
*App version: 24.0.0*

>  [!NOTE]
>
> With its 2024 spring release, Payment Management will make a version leap from 7.00 to 24.00, meaning that versions 7.00–23.00 don't exist and never will. This was done in order to align the versioning of Payment Management with that of Microsoft Dynamics 365 Business Central.

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Incorporated minor updates to the signup process for Handelsbanken Global-Online. | 54418 |
| Payment and Cash Receipts | Introduced a new feature enabling the setup of job queues for posting payment journals based on payment status. See the [Suggesting and processing payments](@PM-90#to-post-payments-automatically) article for more information. | 53820 |
| Payment and Cash Receipts | Implemented functionality for bank account verification, restricting user approval for self-made changes. See the [Enabling bank account verification](@PM-350) article for more information. | 53821 |

### Bug fixes

| Functional area        | Description                                                  | ID              |
| ---------------------- | ------------------------------------------------------------ | --------------- |
| Statement Intelligence | Fixed an error that occurred when manually applying entries during bank account reconciliation. The error was related to JIT loading, and it has now been resolved. | 54426 and 48597 |


<style>
 .content table tr td:nth-child(1),
 .content table tr td:last-child {
  width: 210px;
 }

 .content table tr td:last-child {
  width: 75px;
 }
</style>