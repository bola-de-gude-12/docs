---
title: Detailed Changelog for Continia Payment Management 2023 R1
description: Changelog containing an overview of all new updates, features, and hotfixes for Continia Payment Management 2023 R1
date: 20-03-2023
id: PM-325
lang: en
---

# Detailed Changelog for Continia Payment Management 2023 R1

This article lists all new updates, features, service packs, and hotfixes for Continia Payment Management 2023 R1.  

> [!TIP]
> As a Continia partner, you can be notified of new Payment Management versions and service packs whenever they're released. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360011738679-Receive-a-notification-upon-new-Payment-Management-App-releases) in the Continia PartnerZone (only available to partners).

## Payment Management 2023 R1, Service Pack 2, hotfix 4

*Released: September 13, 2023*  
*Online version: 6.2.4.163391*   
*Supported Business Central version: 2023 Release Wave 1 (BC22)*  

> [!IMPORTANT]
> This changelog provides [important information](#section-heading) for Business Central Cloud customers who use reports in email notifications.

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | We have resolved the issue that was overwriting the Status Level on Danske Bank after updating the setup, ensuring it retains its original value. | 48888 |
| Payment and Cash Receipts | In Payment Approval workflows with Batch approval, an issue allowed Payment journal lines to be added after sending the approval request but before approval, resulting in the journal getting locked until the request was canceled. We have resolved this issue. | 47396 |
| Payment and Cash Receipts | We have resolved the issue where email notifications were only functioning for vendor payments but not for employees or customers. | 49373 |
| Payment and Cash Receipts | We have addressed the issue that prevented the correct transfer of G-account information during the posting of invoices in specific setup configurations. | 49468 |
| Platform and Technology   | <a id="section-heading"></a> Due to the deprecation of report layout handling in BC, an event previously utilized by Payment  Management has also been deprecated.  <br />Important information for Business Central Cloud customers using reports in email notifications: To ensure a successful update to the latest version and continued access to report layout functionality, BC cloud users must take action by activating the "New Microsoft  Word report rendering platform" feature. | 49474 |
| Statement Intelligence    | We have resolved a filtering issue with bank account reconciliation, specifically addressing the "Show  Matched Bank Account Ledger Entries" and "Show all Bank Account  Ledger Entries" actions. | 48182 |
| Statement Intelligence    | We have have resolved the issue that restricted the matching of batch payments in Rabobank to just one entry at a time. Now, it efficiently identifies multiple matches in a single run. | 48322 |
| Statement Intelligence    | We have fixed the issue that caused filter overflow due to incorrect formatting of the EndToEndID from specific banks. | 48421 |

## Payment Management 2023 R1, Service Pack 2, hotfix 3

*Released: July 17, 2023*  
*Online version:  6.2.3.104580*   
*Supported Business Central version: 2023 Release Wave 1 (BC22)*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Implemented enhancements in the payment export functionality to minimize the occurrence of duplicate payments in the event of communication timeouts with banks through web service integration. The payment status displays [Uncertain](@PM-89) when we have not received confirmation from the bank. | 48049 |

### Bug fixes

| Functional area         | Description                                                  | ID    |
| ----------------------- | ------------------------------------------------------------ | ----- |
| General Application     | An issue was identified where the Payment Method Code, Bank Giro No., and Plus Giro No. were not properly transferred from the vendor to the purchase document during creation. This bug specifically affected the SE (Sweden) localization. The bug has been resolved, ensuring the necessary information is correctly transferred. | 48032 |
| Platform and Technology | Improved file import capability to handle files delivered in Base64 encoding. | 48215 |
| Statement Intelligence  | Resolved an issue where the "Renumber Document Nos." action was not functioning correctly in the Cash Receipt Journal when the lines were created through Statement Intelligence. | 48030 |
| Statement Intelligence  | Fixed the issue that caused inaccurate matching when reconciling an account that also existed as a vendor in the system. | 48050 |



## Payment Management 2023 R1, Service Pack 2, hotfix 2

*Released: July 17, 2023*  
*Online version:  6.2.2.95609*   
*Supported Business Central version: 2023 Release Wave 1 (BC22)*

### Bug fixes

| Functional area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Fixed an error when posting or exporting direct debit collections. | 48091 |



## Payment Management 2023 R1, Service Pack 2, hotfix 1

*Released: July 4, 2023*  
*Online version:  6.2.1.94477*   
*Supported Business Central version: 2023 Release Wave 1 (BC22)*

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Resolved permission error when posting Direct Debit.         | 48067 |
| Payment and Cash Receipts | A bug was identified in the Payment Journal, where the status of journal lines was not being updated from "Processing" to "Paid" as intended. This issue has been resolved, ensuring that the status is accurately reflected in the Payment Journal. | 48066 |

## Payment Management 2023 R1, Service Pack 2

*Released: June 29, 2023*  
*Online version:  6.2.0.89519*   
*Supported Business Central version: 2023 Release Wave 1 (BC22)*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Addition to Rabobank: now matching the functionality already available in other leading banks, the ability to manage multiple accounts with different currencies under the same IBAN, utilizing Rabobank's own API. | 45730 |
| Payment and Cash Receipts | Introduced a custom payment reference field in the Payment Service Provider module, matching the External Payment Reference in the PSP file. | 46399 |
| Payment and Cash Receipts | Added code unit 6216318 CPM Suggest Vendor Payments, to automatically suggest vendor payments for the specific payment journal. | 46294 |
| Payment and Cash Receipts | Added functionality and fields to manage batch payments for Rabobank and ABN AMRO. | 45974 |
| Payment and Cash Receipts | Added an event for Create Employee and  Vendor suggestions in the Payment Journal | 46512 |
| Payment and Cash Receipts | Added support for entries with missing document type when suggesting customer payments. | 46764 |
| Payment and Cash Receipts | Customer Card now includes additional fields for alternative customer information, offering flexibility for customer payments. | 47392 |
| Payment and Cash Receipts | Added an action in the PSP Cash Receipt Journal that allows updating the posting date for selected journal lines. | 47978 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Fixes error causing posting date calculation not to work on vendor payment request page. | 47660 |
| Payment and Cash Receipts | Addressed an issue caused by Microsoft's change in standard filtering, allowing for manual summarization even when encountering invalid conditions. | 47778 |
| Statement Intelligence    | Fixes error in reconciliation rules when Search from Right is used. | 47599 |
| Statement Intelligence    | Fixes issue preventing import of multiple statements using MT940 format. | 46708 |

## Payment Management 2023 R1, Service Pack 1, hotfix 2

*Released: June 6, 2023*  
*Online version:  6.1.2.66467*   
*Supported Business Central version: 2023 Release Wave 1 (BC22)*

### New or changed functionality

| Functional area          | Description                                    | ID    |
| ------------------------ | ---------------------------------------------- | ----- |
| Payment and Cash Receipt | Enhanced support account-to-account transfers. | 47519 |

### Bug fixes

| Functional area        | Description                                                  | ID    |
| ---------------------- | ------------------------------------------------------------ | ----- |
| Statement Intelligence | Addressed missing permission bug in optimized bank account reconciliation posting. | 47514 |
| General Application    | Resolved automatic approval issue in Document Capture workflow when the requester is the same as the approver. | 47517 |
| Statement Intelligence | Implemented additional UTC check when retrieving transactions from Rabobank. | 47518 |
| General Application    | Fixes issue with Fixed Regulatory Reporting permission bug on purchase. | 47536 |

## Payment Management 2023 R1, Service Pack 1, hotfix 1

*Released: May 25. 2023*  
*Online version:  6.1.1.53635*   
*Supported Business Central version: 2023 Release Wave 1 (BC22)*

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Resolves the problem of retrieving the Bank System during payment export for Rabobank and Bizcuit customers. | 46781 |
| Platform and Technology   | Addresses a permission issue that could cause documents using a Word layout to fail. | 46691 |

## Payment Management 2023 R1, Service Pack 1

*Released: May 18, 2023*  
*Online version: 6.1.0.47368*   
*Supported Business Central version: 2023 Release Wave 1 (BC22)*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Support for FI Reference Nos. in Statement Intelligence.     | 45219 |
| General Application       | Vendor Payment Suggestions now allow the usage of a specified Posting date while still identifying Payment Discounts in the calculation. | 46295 |
| General Application       | Improved search functionality by enabling matching of the entire notification line during searches. | 46296 |
| General Application       | Deletion of Rabobank authentication now automatically cleans up associated Bank and Bank Account records. | 46519 |
| General Application       | Implemented a feature to generate a new signup link every time the assisted setup for Rabobank is initiated. | 46668 |
| Payment and Cash receipts | Accurate display of payment discount tolerance on Vendor and Customer application pages. | 43767 |
| Payment and Cash receipts | New functionality to recalculate the journal line amount after application. | 43769 |
| Payment and Cash receipts | If a preferred Mandate ID is not specified, the system will now automatically use the Mandate ID linked to the Preferred Bank Account. | 46086 |
| Payment and Cash receipts | In the PSP Agreement, you can specify a tolerance for the number of days posting days can deviate when using Extended Search. | 46204 |
| Payment and Cash receipts | Enhanced Payment Entry creation by adding support for publishers, allowing the handling of additional Account Types. | 46673 |
| Payment and Cash receipts | The Bank Account Statement File Format BAI is added to the Bank Card. | 46981 |
| Statement Intelligence    | Introducing functionality that enables the [configuration of dimensions for Bank Account reconciliation rules](@PM-37#to-add-dimensions-to-bank-account-reconciliation-rules). | 44378 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Error in the Rabobank integration could cause the updated access token to be rolled back, resulting in a loss of connection. | 46526 |
| General Application       | Error in the assisted vendor setup if the preferred bank account does not exist. | 46795 |
| General Application       | Date dialog error in the payment journal after integrating Rabobank Direct. | 47202 |
| Payment and Cash receipts | Improved performance when suggesting payments performance with limit notification enabled. | 45979 |
| Payment and Cash receipts | Improved performance for Purchase Journal and Purchase document validation. | 46454 |
| Payment and Cash receipts | Enhancement in Cash Receipt Journal: Introducing No. Series check, ensuring accurate numbering. In case of discrepancies, renumbering is required and can be performed automatically or manually as preferred. | 46522 |
| Payment and Cash receipts | Incorrect Fee line amount when the Fix Exch. Rate Amount is in currency format. | 46468 |
| Payment and Cash receipts | Applies to ID not cleared from entries when suggesting vendor payments. | 46521 |
| Payment and Cash receipts | Addressed an issue by adding the missing tag in the in-house file, resolving rare error occurrences. | 46567 |
| Payment and Cash receipts | Error in the bank account cash receipt file format.          | 46692 |
| Platform and Technology   | Optimized the validation process for purchase documents.     | 46418 |
| Statement Intelligence    | A new setting has been introduced in Troubleshooting to optimize the performance of standard posting in scenarios where there are a few bank account statement lines but a large number of bank account ledger entries. | 46155 |

## Payment Management 2023 R1, Hotfix 2

*Released: May 10, 2023*  
*Online version: 6.0.2.0*   
*Supported Business Central version: 2023 Release Wave 1 (BC22)*

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash receipts | Fixes issue in payment export through Bizcuit caused by multiple accounts with the same IBAN. | 46691 |

## Payment Management 2023 R1, Hotfix 1

*Released: May 1, 2023*  
*Online version: 6.0.1.0*   
*Supported Business Central version: 2023 Release Wave 1 (BC22)*

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Fixes permission issue causing documents using word layout to potentially fail. | 46691 |
| Payment and Cash Receipts | Fixes issue with getting Bank System Code Argument during payment export for Rabobank and Bizcuit customers. | 46781 |

## Payment Management 2023 R1

*Released: April 1, 2023*  
*Online version: 6.0.0.0*   
*Supported Business Central version: 2023 Release Wave 1 (BC22)*



### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Improved functionality when creating purchase documents using G-Accounts. | 45196 |
| General Application       | Added functionality allowing the use of manual up- and download of files on individual bank accounts, related to a bank using direct communication. | 39836 |
| Payment and Cash Receipts | Added the possibility to apply filters to ledger entries when creating payment suggestions. | 44710 |
| Payment and Cash Receipts | Added a new setting in PSP Agreement to set a tolerance day for posting day if Extended Search is used. | 46204 |
| Platform and Technology   | Added functionality to enable having multiple accounts with the same IBAN in different currencies when using direct communication through Bizcuit. | 40655 |
| Platform and Technology   | Support for Continia Notifications.                          | 43797 |
| Platform and Technology   | Removed CPM Payment Method Code from purchase and sales and moved to standard payment method code instead. | 45292 |
| Platform and Technology   | Added functionality to allow Expense Management to add additional Payment Notification for payments covering multiple expenses giving a better overview for payment of settlements. | 45690 |
| Platform and Technology   | Added event to enable partners to expand on the Payment Reference Search Rules when matching Bank Account Ledger Entries. | 46156 |
| Statement Intelligence    | Additional improvements for estimating the ending no. in No. series when doing bank account reconciliations. | 43623 |
| Statement Intelligence    | Added functionality to improve the assignment of statement numbers. | 43976 |
| Statement Intelligence    | Improved matching capabilities for bank account reconciliation lines containing multiple unique references for matching sales documents or bank account ledger entries. | 45221 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Payment Method Code not transferred to purchase document.    | 44934 |
| Payment and Cash Receipts | Unexpected behavior summarizing payment suggestions for customers. | 43399 |
| Payment and Cash Receipts | Bal. Account Type set to "Bank Account" in the purchase journal when entering a vendor no. <br />The Bal. Account No. now has the default value "G/L Account" | 45903 |
| Payment and Cash Receipts | Slow performance when suggesting payments with the Limit notification setting enabled. | 45979 |
| Payment and Cash Receipts | Setting Bank Export Data as *Imported to Company* when using the action "Delete and set as Imported" in the Cash Receipt Journal. | 46141 |
| Payment and Cash Receipts | Unable to update importing status if Import File Format on Bank Account was set to *Text*. | 45825 |
| Statement Intelligence    | The standard filter setting on the posting date for entries shown in the Bank Account Ledger Entries subpage on the Bank Account Reconciliation page. | 45591 |



<style>
  .content table tr td:nth-child(1),
  .content table tr td:last-child {
    width: 210px;
  }

  .content table tr td:last-child {
    width: 75px;
  }
</style>