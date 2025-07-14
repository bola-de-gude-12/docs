---
title: Detailed Changelog for Continia Payment Management 2023 R2
description: Changelog containing an overview of all new updates, features, and hotfixes for Continia Payment Management 2023 R2
date: 11-04-2024
id: PM-367
lang: en
---

# Detailed Changelog for Continia Payment Management 2023 R2

This article lists all new updates, features, service packs, and hotfixes for Continia Payment Management 2023 R2. 

> [!TIP]
> As a Continia partner, you can be notified of new Payment Management versions and service packs whenever they're released. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360011738679-Receive-a-notification-upon-new-Payment-Management-App-releases) in the Continia PartnerZone (only available to partners).

## Payment Management 2023 R2, Service Pack 2, hotfix 4

*Release date: April 11, 2024*  
*Online version: 7.2.4.0*  
*Supported Business Central version: 2023 Release Wave 2 (BC23)*

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Improved handling of batch and transaction statuses to prevent incorrect status setting from the Payment Information ID. | 54702 |

## Payment Management 2023 R2, Service Pack 2, hotfix 3

*Release date: April 4, 2024*  
*Online version: 7.2.3.0*  
*Supported Business Central version: 2023 Release Wave 2 (BC23)*

### New or changed functionality

| Functional area        | Description                                                  | ID    |
| ---------------------- | ------------------------------------------------------------ | ----- |
| Statement Intelligence | Improved reference matching now handles longer bank reference numbers by adjusting for discrepancies in length and deleting preceding zeroes when necessary, ensuring accurate reconciliation between statement lines and Customer Statement References. | 54539 |
| Statement Intelligence | Added a date selection dialog while creating a job queue for statement imports, enhancing clarity and ease of initiation when no statements have been imported previously. | 54591 |

### Bug fixes

| Functional area            | Description                                                  | ID    |
| -------------------------- | ------------------------------------------------------------ | ----- |
| Payments and Cash Receipts | Payments with later dates exported in the same file were not receiving a Paid status due to the register being marked as Done upon the reconciliation of the first lines. This has now been fixed | 54590 |

## Payment Management 2023 R2, Service Pack 2, hotfix 2

*Release date: March 21, 2024*  
*Online version: 7.2.2.0*  
*Supported Business Central version: 2023 Release Wave 2 (BC23)*

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Fixed issue In Validate Payment Method Code trigger to cause error in certain scenarios while doing batch posting of purchase documents. | 54131 |
| Payment and Cash Receipts | Resolved an issue with modulus 731 calculations, ensuring accurate validation of Payment References containing a 731-modulus check digit. | 53432 |
| Payment and Cash Receipts | Fixed a problem where the prefix functionality for matching entries based on Payment ID caused issues when matching on invoice numbers stated in the description or notification if non-numerical characters are used for the No. Series. | 53925 |
| Statement Intelligence    | Fixed issue causing documents containing initial split characters to not be matched correctly. | 54089 |
| Statement Intelligence    | Fixed issue in matching routine causing overflow when setting a filter on the Document No. | 54198 |

## Payment Management 2023 R2, Service Pack 2, hotfix 1

*Release date: March 13, 2024*  
*Online version: 7.2.1.0*  
*Supported Business Central version: 2023 Release Wave 2 (BC23)*

### New or changed functionality

| Functional area         | Description                                                  | ID    |
| ----------------------- | ------------------------------------------------------------ | ----- |
| Platform and Technology | Incorporated a modification to the existing event to incorporate Gen. Journal Line as a variable. This enhancement enables clearer identification of batches during event requests. | 46581 |
| Statement Intelligence  | Implemented support for the ACSC status code at the header level for ABN Amro. | 53998 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Implemented a change in PM 7.1.5 On-Prem based on a Customer Request to include the Transit No. field in the Vendor Bank Account, enhancing the completeness of vendor account information. | 53724 |
| Payment and Cash Receipts | Fixed a problem where applying Cash Receipt Journal Lines could cause issues when the journal was sorted, ensuring that all General Journal Lines affected by payments are updated correctly, even if they are sorted, preventing discrepancies during payment re-application. | 53948 |
| Statement Intelligence    | An error has been fixed that occurred when closing the Payment Identification Search Rule page without creating a rule. | 53843 |



## Payment Management 2023 R2, Service Pack 2

*Release date: February 20, 2024*  
*Online version: 7.2.0.0*  
*Supported Business Central version: 2023 Release Wave 2 (BC23)*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Updated the bank holiday list with an upgrade that removes Great Prayer Day. | 52924 |
| General Application       | Added support for looking up bank information based on UK sort codes. | 48861 |
| Payment and Cash Receipts | Improved functionality for handling Credit Transfer Register status used for status import on Dutch banks. | 47579 |
| Statement Intelligence    | Improved payment reference matching now handles preceding letters in number series, accommodating entries like DK-IN123456789. | 46802 |
| Statement Intelligence    | Introducing a new search rule for transaction reference identification within descriptions or additional information, to improve matching capabilities when using ABN Amro Direct. | 52785 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Implemented the Reset Approval Workflow for Line/Batch button on the Troubleshooting page to address instances where lines stuck in Pending Approval status due to workflow functionality issues can be reset. | 50352 |
| General Application       | Corrected the mishandling of ampersands in Import files for Payment Management, ensuring accurate processing and preventing data errors. | 52790 |
| General Application       | Addressed an issue where the Payment Method Description failed to update on the Customer Card. | 53177 |
| Payment and Cash Receipts | Resolved the issue where Payment Discount Tolerances were not being handled during the matching of entries in the Cash Receipt journal. | 52791 |
| Payment and Cash Receipts | Fixed a calculation error affecting amount calculation when applying for entries in various currencies to a journal line in a different currency. | 53178 |
| Platform and Technology   | Fixed issue causing an error when creating Vendor Bank Accounts in companies where Payment Management is not activated. | 52901 |

## Payment Management 2023 R2, Service Pack 1, hotfix 6

*Release date: January 11, 2024*  
*Online version: 7.1.6.0*  
*Supported Business Central version: 2023 Release Wave 2 (BC23)*

### Bug fixes

| Functional area         | Description                                                  | ID    |
| ----------------------- | ------------------------------------------------------------ | ----- |
| Platform and Technology | In version 7.1.5, a bug prevented sandbox environment creation. This issue has been resolved. | 52378 |

## Payment Management 2023 R2, Service Pack 1, hotfix 5

*Release date: January 8, 2024*  
*Online version: 7.1.5.0*  
*Supported Business Central version: 2023 Release Wave 2 (BC23)*

### New or changed functionality

| Functional area         | Description                                                  | ID    |
| ----------------------- | ------------------------------------------------------------ | ----- |
| General Application     | Added support for ING bank accounts with regular and savings accounts using the same IBAN and currency code. This update resolves issues previously encountered during account statement imports. | 52076 |
| Platform and Technology | In response to user feedback and to streamline sandbox creation within cloud environments, direct communication is now automatically disabled when creating a sandbox in a cloud environment. This adjustment prevents the accidental import of files from external sources, such as the bank, into the sandbox environment. | 52058 |

### Bug fixes

| Functional area          | Description                                                  | ID    |
| ------------------------ | ------------------------------------------------------------ | ----- |
| General Application      | Resolved an issue where notifications for unsupported payment methods were displayed despite the bank setup allowing them. Users will no longer receive unintended notifications for payment methods that are supported by their bank setup. | 48328 |
| Payment and Cash Receipt | Fixed issue causing Create Vendor Payment on the Vendor Ledger Entries list to fail under certain Payment Journal Setup configurations. | 52198 |
| Platform and Technology  | Fixed an issue where imported files didn't display regional letters correctly. We added a troubleshooting option to handle this problem after importing files. | 52100 |
| Platform and Technology  | The issue where manual file imports were failing because of hex characters present in the file has been resolved. Manual file imports will now process successfully without encountering this issue. | 52101 |
| Statement Intelligence   | Resolved an issue encountered during Statement imports where importing multiple statements led to an inaccurate update of the starting balance. This inconsistency caused reconciliation errors. | 52102 |
| Statement Intelligence   | Fixed issue where the Account Statement import job would fail due to missing statements. The update ensures job queue functions correctly even when no statements are present, preventing job failures. | 52197 |
| Statement Intelligence   | The issue with duplicate transactions while using ABN-AMRO has been resolved. | 52217 |

## Payment Management 2023 R2, Service Pack 1, hotfix 4

*Release date: December 18, 2023*  
*Online version: 7.1.4.0*  
*Supported Business Central version: 2023 Release Wave 2 (BC23)*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | We have updated our signup process for Continia Online to make it easier to identify customers in case of manual DNB signup. When signing up for DNB, customers are required to provide additional information to ensure KYC compliance. | 47553 |
| Payment and Cash Receipts | We have introduced an improvement for signing up an additional bank account with Rabobank. | 52020 |

### Bug fixes

| Functional area        | Description                                                  | ID    |
| ---------------------- | ------------------------------------------------------------ | ----- |
| General Application    | Fixed an issue that caused errors while posting journals in companies in which Payment Management is not activated | 50602 |
| Statement Intelligence | Resolved an issue where payment batches processed through Bizcuit didn't insert the ID in the PmtInfID, leading to the inability to identify bank ledger entries and resulting in inaccurate batch matching. | 51594 |
| Statement Intelligence | Statement Intelligence's overflow issue caused by Modulus validation on texts longer than 38 characters has been fixed. | 51601 |
| General Application    | Added a check to ensure customers are using the correct signup link for DNB and included a warning to prevent them from using it in unrelated companies. | 51820 |
| General Application    | The email address for signing up to Handelsbanken has been changed to Handelsbanken Sweden. | 51908 |
| General Application    | An issue has been fixed on the Unsent email page that was causing only vendor emails to be displayed. | 52004 |

## Payment Management 2023 R2, Service Pack 1, hotfix 3

*Release date: November 28, 2023*  
*Online version: 7.1.3.0*  
*Supported Business Central version: 2023 Release Wave 2 (BC23)*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Fixed issue causing Bank Account Verification to lock payments on giro type payments. | 51494 |

## Payment Management 2023 R2, Service Pack 1, hotfix 1 

*Release date: November 27, 2023*  
*Online version: 7.1.1.0*  
*Supported Business Central version: 2023 Release Wave 2 (BC23)*

> [!NOTE]
>
> hotfix 1 and 2 have been combined.

### New or changed functionality

| Functional area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Payment Management Setup now includes a setting to disable purchase validation before approval requests are sent. | 51173 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | An action has been added to remove the relation between the Bank Account and the Bank/Plus Giro No. | 50425 |
| General Application       | Fixed issue causing validation of purchase credit notes and purchase quotes on approval requests. | 51385 |
| General Application       | CPM Basic permission added to avoid regulatory reporting error during purchase document validation. | 50956 |
| Payment and Cash Receipts | Fixed an issue in license check that displayed incorrect error message in Payment Journal if Bank Account Verification is not activated. | 50963 |
| Payment and Cash Receipts | Resolves the problem where the payment discount date was being applied despite no specified discount amount. | 51203 |
| Statement Intelligence    | Fixed the issue that caused account statements to be potentially imported multiple times when using import job queues for Bizcuit and Rabobank. | 51425 |
| Payment and Cash Receipts | Fixed issue in payment status update caused by illegal characters in the response from the bank. The update process for payment journal lines was failing due to the presence of the text <EOR> in the PmtInfId field. | 51454 |

## Payment Management 2023 R2, Service Pack 1

*Release date: November 10, 2023*  
*Online version: 7.1.0.0*  
*Supported Business Central version: 2023 Release Wave 2 (BC23)*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Addressed an issue related to validation processes that was causing errors for customers when attempting to adjust a purchase order line. Additionally, we have introduced a new permission, Cost Type Code, in the CPM Basic permission set to enhance user control and security. This permission is now included as an addition to the CPM BASIC Permission Set. Users can now manage purchase order lines with improved permission settings. | 50357 |
| General Application       | Improved filtering by adding descriptive captions to alternative vendor information fields, distinguishing them from standard fields. | 50679 |
| Payment and Cash Receipts | Resolved an issue where customers encountered inconsistent output during notification sending, specifically with the payment notification email missing the notification content. | 50098 |
| Platform and Technology   | Implemented the DoPaymentMethodLookup() procedure as per customer request. This allows developers to verify a valid form of payment during the development process.&nbsp; | 50380 |
| Statement Intelligence    | Added a setup option to enforce checking for matching Transaction IDs between the bank account ledger entry and the reconciliation line, specifically triggered during matching, to prevent incorrect matches for entries with identical amounts and dates, particularly relevant for Direct Debit collections.&nbsp;&nbsp; | 46444 |
| Statement Intelligence    | Enhanced user experience by adding rule actions to the Additional Information dialog in the Bank Account Reconciliation page. Users can now conveniently create rules without the need to navigate away. | 47465 |
| Statement Intelligence    | Introduced a new functionality in bank account reconciliation, allowing users to set up [rules to exclude matching](@PM-372) on specific accounts (Vendor, Customer, etc.) by excluding words. This feature allows users to specify IBANs to be ignored for matching on designated accounts where consolidated Customers/Vendors share the same IBAN, preventing unintended matches and ensuring accurate reconciliation. | 50215 |
| Statement Intelligence    | Added the flexibility to import account statements using standard Data Exchange Definitions. <br />**Important**: Note that if you choose to use this option, Continia will not be responsible for any errors that may occur during the import process. There is a risk of mapping errors, so we strongly recommend that you exercise caution when using this feature. Make sure that the Data Exchange Definitions are set up correctly and carefully verify the accuracy of the imported data, as you are solely responsible for this method of import. | 50288 |

## Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Added an option to use Modulus 11 for the Payment Reference template, providing two options: Modulus 11 and Modulus 11 (KID). Useful for making KID references automatically. | 50140 |
| General Application       | Fixed permission <span style="display:inline !important;">error<span>&nbsp;</span></span>related to Bank Account Verification <span style="display:inline !important;">in Bank Account Card and Payment Journal<span>&nbsp;</span></span>if the account was verified and the user does not have Bank Acc. Verification permissions.&nbsp; | 50763 |
| General Application       | Fixed overflow error when getting CompanyGuid.               | 50792 |
| Payment and Cash Receipts | Fixed an issue where multiple lines were marked after manual summarization. | 48196 |
| Payment and Cash Receipts | Fixed an issue with approval comments not being removed when a payment journal line is reset. | 49613 |
| Payment and Cash Receipts | Addressed an issue with approval requests not being deleted when using force void payment. | 49614 |
| Statement Intelligence    | Resolved an issue causing the manual import of account statements to fail if multiple statements were imported. | 49528 |
| Statement Intelligence    | Fixed an issue causing the incorrect document to be matched on KID reference. | 50214 |
| Statement Intelligence    | Fixed issue causing Create Payments on the vendor ledger entry list to fail under specific payment journal setups.&nbsp; | 50604 |
| Statement Intelligence    | Fixed issue with incorrect status on reconciliation line if the matched entry is applied else where.&nbsp; | 50793 |

## Payment Management 2023 R2

*Release date: October 1, 2023* 
*Online version: 7.0.0.0*  
*Supported Business Central version: 2023 Release Wave 2 (BC23)*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | With the introduction of the [Bank Account Verification feature](@PM-352), you can now verify the legitimacy of bank accounts. This enhances fraud protection and security within approval workflows. | 48858 |
| General Application       | You can now [set up approval groups](@PM-254) without priority. This allows you to specify the mandatory number of approvers, and it doesn't matter who among them approves as long as the required number is reached. | 48857 |
| General Application       | To prevent unpredictable behavior and errors in the approval flow, a check has been implemented to avoid the simultaneous setup of approval flows for both Line and Batch Approval. Users will receive a warning when attempting this configuration, enhancing workflow consistency and reliability. | 48856 |
| General application       | A new feature has been added to the Bank Account Setup that allows the removal of any trailing whitespaces from the passwords. This will ensure that the system correctly recognizes the passwords and that users can access their accounts without any issues. | 43724 |
| General Application       | With the introduction of the [Continia Hub menu](@PM-355), you can easily access helpful articles, training materials, and informative videos to support your business tasks in Business Central. | 48860 |
| General Application       | To prevent validation errors on approved documents during posting, you can decide to [validate purchase documents](@PM-356) in Document Capture before sending approval requests. Please note that this functionality is not compatible with standard approval processes. | 49123 |
| General Application       | Now, when you invoke the "Update Vendor Bank Account Information" or "Update Customer Bank Account Information" actions, a notification dialog will appear, confirming that the information has been updated. | 49130 |
| General Application       | When updating vendor bank account settings or entering an invalid IBAN, a dialog box will appear. | 49311 |
| Payment and Cash Receipts | Users can now generate the "Create Vendor Payment" report from the Vendor Ledger Entries List through an external facade codeunit. | 48197 |
| Payment and Cash Receipts | The Direct Debit suggestion functionality has been expanded to include customer ledger entries with no document type. Now, it can handle entries with a blank document type. | 49598 |
| Platform and Technology   | Our file export procedures have been restructured to use standard BC File Management codeunits. This change supports customers who have integrated with File Management. | 48233 |
| Statement Intelligence    | The performance of the bank account reconciliation routine that is run upon posting a journal has been enhanced. To enable this feature, access Continia Feature Management. | 48202 |
| Statement Intelligence    | To enhance the matching of Direct Debit reversals, open bank account ledger entries are also included. The customer ledger entry is unapplied, and the bank account ledger entry is reversed and matched. | 48770 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | A new key has been implemented for the "Invoice Ledger Entry No" field in the CPM Reversal table to optimize API performance. Retrieving the Reversal Code from the Customer Ledger Entry was slow due to the absence of a key for the "Invoice Ledger Entry No." | 47815 |
| General Application       | Resolved an issue where the CPM Customer Statement No. Series was lacking ending numbers, impacting the numbering sequence. In addition, we've introduced validation to check for ending numbers within the Customer Statement No. Series, similar to other number series checks. This validation is now applied in the Bank Account Reconciliation process when the "Sales" field on the Statement Intelligence Setup Page is configured to show an error in case ending numbers are missing. | 48011 |
| General Application       | Updates were overwriting the Status Level on Danske Bank. This issue has been resolved. | 48888 |
| General Application       | Assisted setup no longer shows an error message when no balance account is set up during the initial steps of assisted setup. | 48217 |
| General Application       | Addressed the problem where the Preferred Bank Account was cleared for vendors when using the Vendor Payment Setup. | 48216 |
| Payment and Cash Receipts | You can now specify a file extension in the File Name fields on the troubleshooting page. Additionally, you can exclude the Message ID from the file name. This addresses concerns with manual exports and ensures that the file name is more user-friendly. | 47044 |
| Payment and Cash Receipts | Resolved an issue within the approval workflow that allowed payment journal lines to be added after an approval request was sent but before approval. This issue caused the journal to become locked until the approval request was canceled. | 47396 |
| Payment and Cash Receipts | We have addressed the previous limitation of email notifications being limited to vendor payments. As of now, notifications are fully supported for both employees and customers. | 49373 |
| Payment and Cash Receipts | We have addressed the issue that prevented the correct transfer of G-account information during the posting of invoices in specific setup configurations. | 49468 |
| Payment and Cash Receipts | Added a new feature that allows direct import from bank export data into the cash receipt journal without getting a file dialog. | 47486 |
| Platform and Technology   | Due to the deprecation of report layout handling in BC, an event previously utilized by Payment Management has also been deprecated.<br/>Important information for Business Central Cloud customers using reports in email notifications: To ensure a successful update to the latest version and continued access to report layout functionality, BC cloud users must take action by activating the "New Microsoft Word report rendering platform" feature. | 49474 |
| Statement Intelligence    | Fixed the issue causing matching of batch payments in Rabobank to only match one entry at a time. | 48322 |
| Statement Intelligence    | Resolved an issue that resulted in filter overflow due to incorrect formatting of the EndToEndID from specific banks. | 48421 |
| Statement Intelligence    | We've addressed an issue in Bank Account Reconciliation where filtering wasn't functioning correctly. Specifically, we fixed the functionality of the "Show Matched Bank Account Ledger Entries" and "Show all Bank Account Ledger Entries" actions, as they utilized outdated functions. | 48182 |
| Statement Intelligence    | The Cash Receipt Journal Page now has an added functionality to handle amount differences. When you use the "Insert Difference Journal Lines" action, two additional journal lines are created. One line is for the difference posted on the G/L Account specified in the Statement Intelligence setup, and the other is a balancing journal line for the Bank Account which reflects the statement amount of the related bank statement line. You can specify the G/L Account for the difference amount in the Statement Intelligence Setup Page, in the field "Default Difference Amount G/L Account." <br/><br/>The Add Applied Difference to Amount action on the Cash Receipt Journal page has been made obsolete. | 43977 |


<style>
 .content table tr td:nth-child(1),
 .content table tr td:last-child {
  width: 210px;
 }

 .content table tr td:last-child {
  width: 75px;
 }
</style>