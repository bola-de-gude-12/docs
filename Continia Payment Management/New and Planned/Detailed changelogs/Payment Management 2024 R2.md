---
title: Detailed Changelog for Continia Payment Management 2024 R2
description: Changelog containing an overview of all new updates, features, and hotfixes for Continia Payment Management 2024 R2
date: 13-05-2025
id: PM-387
lang: en
---

# Detailed Changelog for Continia Payment Management 2024 R2

This article lists all new updates, features, service packs, and hotfixes for Continia Payment Management 2024 R2. 

> [!TIP]
> As a Continia partner, we can notify you of new Payment Management versions and service packs whenever we release them. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360011738679-Receive-a-notification-upon-new-Payment-Management-App-releases) in the Continia PartnerZone (only available to partners).

## Payment Management 2025 R1, Service Pack 7

*Release date, online: 8 May, 2025*  
*App version: 25.7.0*

### New or changed functionality

| Functional Area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Added the possibility to change the file name used for Handelsbanken. This should only be changed if the bank expects a different file name. If left blank, the default name from the bank system card will be used. | 66000 |
| General Application       | Introduced an [additional validation for Approval Administrators](@PM-256), requiring them to delegate approval requests before approving on behalf of others. This helps prevent unintended approvals. | 66203 |
| Payment and Cash Receipts | Enabled the ability to clear dimensions in the manual summarization process, and to combine dimensions as in Payment Suggestions. These settings can be configured on the **Payment Journal Setup** page | 66169 |

### Bug fixes

| Functional Area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Resolved an issue where a `Runmodal` error occurred when posting Direct Debit collection entries. | 66212 |
| Payment and Cash Receipts | Resolved an issue where modifying specific fields in the Payment Journal could unintentionally clear values due to validation logic in the `BuildNotification` procedure. | 65625 |
| Payment and Cash Receipts | Standardized the creation of Applies-to-ID for customer payments to align with the process used for Vendor Payments. | 66204 |

## Payment Management 2024 R2, Service Pack 5

*Release date, online: 3 April, 2025*  
*App version: 25.5.0*

### New or changed functionality

| Functional Area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Platform and Technology   | Added `GenJnlLine` as a parameter in the `OnAfterSetFilterToGetVendLedgEntries` event. | 64700 |
| Payment and Cash Receipts | Fixed an issue where customer statements failed to match in the Cash Receipt Journal. | 65263 |
| Payment and Cash Receipts | Fixed an issue where decimals were incorrectly processed during export. | 65305 |
| Payment and Cash Receipts | Added an OCR reference interface to externalize the procedure. | 65306 |
| Payment and Cash Receipts | Extended Force-Void functionality to support multiple lines. | 65307 |

### Bug fixes

| Functional Area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Corrected a translation for 7-3-1 Modulus in the NL localization. | 63109 |
| Payment and Cash Receipts | Fixed an issue where IBAN LookUp autofill prevented users from verifying their own changes on the bank account card. | 62176 |
| Payment and Cash Receipts | Added support for handling characters in the payment reference. | 62233 |

## Payment Management 2024 R2, Service Pack 4, hotfix 4

*Release date, online: 26 March, 2025*  
*App version: 25.4.4*

### New or changed functionality

| **Functional Area**       | **Description**                                              | **ID** |
| ------------------------- | ------------------------------------------------------------ | ------ |
| Payment and Cash Receipts | Fixed issue where timeouts when communicating with banks where not registered correctly, causing the status of payments to remain Valid after export. | 65132  |

## Payment Management 2024 R2, Service Pack 4, hotfix 2

*Release date, online: 14 March, 2025*  
*App version: 25.4.2*

### New or changed functionality

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| General Application | When setting up connection to Yapily, we now look at the token status before continuing the flow in Business Central. | 64615  |



## Payment Management 2024 R2, Service Pack 4, hotfix 1

*Release date, online: 7 March , 2025*  
*App version: 25.4.1*

### Bug fixes

| **Functional Area**       | **Description**                                              | **ID** |
| ------------------------- | ------------------------------------------------------------ | ------ |
| Payment and Cash Receipts | Implemented a fix for incorrect amount adjustments in the Payment Journal for Nordea customers. | 64267  |

## 

## Payment Management 2024 R2, Service Pack 4

*Release date, online: February 27 , 2025*  
*App version: 25.4.0*

### New or changed functionality

| **Functional Area**       | **Description**                                              | **ID** |
| ------------------------- | ------------------------------------------------------------ | ------ |
| Statement Intelligence    | Added functionality to disable the search for Customer Ledger entries during bank account reconciliation. | 64015  |
| Payment and Cash Receipts | Fixed issues with amount adjustments related to status updates on Payment Journal lines. | 63570  |
| Platform and Technology   | Added support for handling structured remittance for KID when summarizing payments. | 63808  |
| Platform and Technology   | Improved performance in application management.              | 64100  |
| Payment and Cash Receipts | Added an option to disable the use of matching bank ledger entries based on Payment Inf. ID, which is used in the Batch Payments matching process for some banks. This setting is available on the bank account card. | 64101  |
| Payment and Cash Receipts | Implemented functionality to add Related Party Name to the Description field if provided in the Bank Account Statement. This setting is available on the bank card. | 64105  |

### Bug fixes

| **Functional Area**       | **Description**                                              | **ID** |
| ------------------------- | ------------------------------------------------------------ | ------ |
| Payment and Cash Receipts | Fixed an error caused by missing permissions when updating status with fee lines. | 63600  |
| Payment and Cash Receipts | Resolved an issue with reusing a bank account code that had a changelog. | 63941  |
| Payment and Cash Receipts | Fixed a problem where the Account No exceeded the string length limit during bank account reconciliation and journal line creation. | 64070  |
| Payment and Cash Receipts | Corrected an issue where the Giro number was not added when suggesting payments in the Payment Journal. | 64102  |

## 

## Payment Management 2024 R2, Service Pack 3, hotfix 1

*Release date, online: February 17 , 2025*  
*App version: 25.3.1

### New or changed functionality

| **Functional Area**     | **Description**                                         | **ID** |
| ----------------------- | ------------------------------------------------------- | ------ |
| Platform and Technology | Added support for summarizing KID payment in TietoEvry. | 62515  |

### Bug fixes

| **Functional Area**       | **Description**                                              | **ID** |
| ------------------------- | ------------------------------------------------------------ | ------ |
| Platform and Technology   | Resolved an issue where a codeunit upgrade caused the Payment Management update to fail. | 63806  |
| Payment and Cash Receipts | Fixed an error triggered by subscribers modifying values on payment journal lines. | 63998  |

## 

## Payment Management 2024 R2, Service Pack 3

*Release date, online: February 2 , 2025*  
*App version: 25.3.0*

### New or changed functionality

| **Functional Area**       | **Description**                                            | **ID** |
| ------------------------- | ---------------------------------------------------------- | ------ |
| Payment and Cash Receipts | Improved the performance of Direct Debit Export processes. | 63425  |

### 



## Payment Management 2024 R2, Service Pack 2, hotfix 5

*Release date, online: January 21  , 2025*  
*App version: 25.2.5*

### New or changed functionality

| **Functional Area**    | **Description**                                              | **ID** |
| ---------------------- | ------------------------------------------------------------ | ------ |
| Statement Intelligence | Optimized performance for loading the Payment Journal by improving discount checks. | 62807  |

### Bug fixes

| **Functional Area**       | **Description**                                              | **ID** |
| ------------------------- | ------------------------------------------------------------ | ------ |
| Payment and Cash Receipts | Fixed an issue where the Payment Journal setup was not considered when using report settings for Payment Suggestions. |        |

## Payment Management 2024 R2, Service Pack 2, hotfix 4

*Release date, online: January 2, 2025*  
*App version: 25.2.4*

### New or changed functionality

| **Functional Area**       | **Description**                           | **ID** |
| ------------------------- | ----------------------------------------- | ------ |
| Payment and Cash Receipts | Improvements to summarizing KID payments. | 62515  |

 

## Payment Management 2024 R2, Service Pack 2, hotfix 3

*Release date, online: January 1, 2025*  
*App version: 25.2.3*

### New or changed functionality

| **Functional Area**       | **Description**                                         | **ID** |
| ------------------------- | ------------------------------------------------------- | ------ |
| Payment and Cash Receipts | Added support for summarizing KID payment in TietoEvry. | 62515  |



## Payment Management 2024 R2, Service Pack 2, hotfix 1, 2

*Release date, online: December 20, 2024*  
*App version: 25.2.1 and 25.2.2*

### New or changed functionality

| **Functional Area**     | **Description**                                              | **ID** |
| ----------------------- | ------------------------------------------------------------ | ------ |
| General Application     | Added an additional filter to procedures in Entry Application Management to avoid triggering on journal lines with other account types. | 62514  |
| Platform and Technology | Minor changes to improve performance when creating Payment Entries. | 62513  |

### 

## Payment Management 2024 R2, Service Pack 2

*Release date, online: December 13, 2024*  
*App version: 25.2.0*

### New or changed functionality

| **Functional Area**       | **Description**                                              | **ID** |
| ------------------------- | ------------------------------------------------------------ | ------ |
| General application       | Added the ability to validate individual lines in the journal instead of validating the entire journal. With a dropdown button, users can select and validate specific lines, improving efficiency and avoiding disruption to the current flow. | 61557  |
| General application       | Issues arose after extending the CPM functionality, specifically with the CPMContainsCPMGeneratedLines function. To resolve these issues and improve performance, filters have been implemented. | 61560  |
| Payment and Cash Receipts | A Microsoft error was causing the PSP date to malfunction, leading to a crash in BC. This issue has now been fixed. | 62138  |

### Bug fixes

| **Functional Area**       | **Description**                                              | **ID** |
| ------------------------- | ------------------------------------------------------------ | ------ |
| Payment and Cash Receipts | Applied a fix for the calculation of the G-Account amount on NL purchase invoices. | 61558  |
| Payment and Cash Receipts | Updating the status of a payment journal line triggers feelines creation based on Bank Export Charges. If LCY is used as the currency code, an error occurs stating the currency code does not exist. This issue has been fixed. | 61559  |
| Payment and Cash Receipts | A crash occurred when opening a validation error in the Payment Journal. The issue has been resolved. | 61638  |



## Payment Management 2024 R2, Service Pack 1, hotfix 1

*Release date, online: November 9, 2024*  
*App version: 25.1.1*

### New or changed functionality

| **Functional Area**       | **Description**                                              | **ID** |
| ------------------------- | ------------------------------------------------------------ | ------ |
| Payment and Cash Receipts | Fixed an issue with the `BuildNotification` function, which previously prevented users from changing the Balance Account or Recipient Bank Account in the Payment Journal due to triggers on the `OnAfterValidate` event. | 61060  |

## Payment Management 2024 R2, Service Pack 1

*Release date, online: October 24, 2024*  
*App version: 25.1.0*

### New or changed functionality

| **Functional Area**       | **Description**                                              | **ID** |
| ------------------------- | ------------------------------------------------------------ | ------ |
| General Application       | Dependencies have been migrated to SE Core.                  | 60692  |
| Payment and Cash Receipts | BG/PG fields now pull information from the vendor if the Payment Method Code is missing on the vendor ledger entry and **Use Payment Information from vendor** is set to *Yes*, ensuring accurate data population. | 54809  |
| Payment and Cash Receipts | To reduce incorrect cash receipt matches, an option to enforce a Document Number match has been added to the bank account card. | 60478  |
| Payment and Cash Receipts | Enhanced functionality now includes credit memo handling to improve transaction processing for selected banks. | 60694  |

### Bug fixes

| **Functional Area**       | **Description**                                              | **ID** |
| ------------------------- | ------------------------------------------------------------ | ------ |
| General Application       | The Role Center tile now correctly displays the number of payments and reconciliation lines. | 60498  |
| Payment and Cash Receipts | Fixed the Manual/Direct export check to correctly reference the Direct Debit Export field. | 60477  |
| Payment and Cash Receipts | Existing bank transactions without a payment type can now have the payment type assigned retroactively. | 30812  |

## Payment Management 2024 R2

*Release date, online: October 1, 2024*  
*App version: 25.0.0*

### New or changed functionality

| **Functional Area**       | **Description**                                              | **ID** |
| ------------------------- | ------------------------------------------------------------ | ------ |
| General Application       | Implemented a new Bank Export data structure to improve the handling of charges. | 43968  |
| Payment and Cash Receipts | Improved handling of charges when updating the Payment Journal status. | 43969  |
| Payment and Cash Receipts | The system now includes a check to prevent the summarization of purchase invoices that are linked to payments involving G-accounts. | 59009  |
| Statement Intelligence    | Added the opportunity to disable the search for closed customer ledger entries in the bank account reconciliation on Statement Intelligence setup. | 59748  |
| Statement Intelligence    | Extended the reversal posting feature to allow users to choose selected lines or all lines for posting of reversals. | 59749  |




<style>
 .content table tr td:nth-child(1),
 .content table tr td:last-child {
  width: 210px;
 }

 .content table tr td:last-child {
  width: 75px;
 }
</style>