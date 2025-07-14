---
title: Detailed Changelog for Continia Payment Management 2025 R1
description: Changelog containing an overview of all new updates, features, and hotfixes for Continia Payment Management 2025 R1
date: 27-05-2025
id: PM-407
lang: en
---

# Detailed changelog for Continia Payment Management 2025 R1

This article lists all new updates, features, service packs, and hotfixes for Continia Payment Management 2025 R1. 

> [!TIP]
> As a Continia partner, we can notify you of new Payment Management versions and service packs whenever we release them. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360011738679-Receive-a-notification-upon-new-Payment-Management-App-releases) in the Continia PartnerZone (only available to partners).

## Payment Management 2025 R1, Service Pack 2, hotfix 1

*Release date, online: 28 May, 2025*  
*App version: 26.2.1*

### New or changed functionality

| Functional Area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Added an error message to the job queue functionality to improve error handling. | 66513 |
| Payment and Cash Receipts | You can now disable the status update process during payment export. This is particularly useful for handling large volumes of transactions, where status updates can be time-consuming. Configure this option in the **Payment Journal Setup** page. | 66624 |

### Bug fixes

| Functional Area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Fixed an error that occurred when deactivating payment approval flows in the Payment Approval Setup assisted setup. | 66512 |
| Payment and Cash Receipts | Fixed an issue with approving on behalf of other approvers when using the **Required number of approvers** setting. | 66511 |

## Payment Management 2025 R1, Service Pack 2

*Release date, online: 8 May, 2025*  
*App version: 26.2.0*

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

## Payment Management 2025 R1, Service Pack 1

*Release date, online: 23 April, 2025*  
*App version: 26.1.0*

### New or changed functionality

| Functional Area         | Description                                                  | ID    |
| ----------------------- | ------------------------------------------------------------ | ----- |
| Platform and Technology | Improved performance of the `OnDelete`trigger for Payment Journal Lines. | 65776 |

### Bug fixes

| Functional Area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Fixed an issue where translations were not updated during setup import. | 65777 |

## Payment Management 2025 R1

*Release date, online: 10 April, 2025*  
*App version: 26.0.0*

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




<style>
 .content table tr td:nth-child(1),
 .content table tr td:last-child {
  width: 210px;
 }

 .content table tr td:last-child {
  width: 75px;
 }
</style>