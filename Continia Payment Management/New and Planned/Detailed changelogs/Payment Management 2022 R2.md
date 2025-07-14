---
title: Detailed Changelog for Continia Payment Management 2022 R2
description: Changelog containing an overview of all new updates, features, and hotfixes for Continia Payment Management 2022 R2
date: 04-10-2022
id: PM-265
lang: en
---

# Detailed Changelog for Continia Payment Management 2022 R2

This article lists all new updates, features, service packs, and hotfixes for Continia Payment Management 2022 R2.  

## Payment Management 2022 R2, Service Pack 3, Hotfix 1

*Released: March 17, 2023*  
*Online version: 5.3.1.0*   
*Supported Business Central version: 2022 Release Wave 2 (BC21)*

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | The Balance Account Setup for a new vendor always adds the balance account based on currency code. | 44752 |
| Payment and Cash Receipts | Fixes issue with missing permissions for Employee and Customer Ledger Entries when summarizing payments manually. | 45783 |
| Payment and Cash Receipts | Payment suggestion issue with multiple entries with the same document type and document no. | 45841 |
| Platform and Technology   | Standard report generation using a commit when running report for payment notifications. | 45854 |
| Statement Intelligence    | Unable to display Show more fields on the Statement Intelligence Setup when you create a new bank account reconciliation. | 45773 |
| Statement Intelligence    | Bank returning texts when no EndToEndID is available (e.g. NOTPROVIDED) | 45715 |
| Statement Intelligence    | Wrong splitting of words in the Bank Account Reconciliation matching routine. | 45873 |



## Payment Management 2022 R2, Service Pack 3

*Released: March 2, 2023*  
*Online version: 5.3.0.0*   
*Supported Business Central version: 2022 Release Wave 2 (BC21)*



### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Country and Regional      | Bankgirot OCR reference support for Swedish localization.    | 42412 |
| Payment and Cash Receipts | You can now enable auto-import functionality in Cash Receipt Journal actions. | 43091 |
| Payment and Cash Receipts | Display the External Reference No. during manual application of customer ledger entries. | 43438 |
| Payment and Cash Receipts | Line inspection and Document Information actions added. You can use the Line inspection action in the purchase journal and the document Information action in the purchase order and purchase invoice pages to view bank account details such as bank system, payment method (mapping) code, and country code. | 44354 |
| Payment and Cash Receipts | Possibility to import rules to a new PSP agreement.          | 44783 |
| Payment and Cash Receipts | Enhancement of handling dimensions so that values from the applied sales invoice are also set on fees related to a payment. | 43436 |
| Payment and Cash Receipts | Added setting to merge the lines with same fees and same posting date. | 43437 |
| Payment and Cash Receipts | Added statistics page to the Cash Receipt Journal that shows the total amount per account type, account no., and currency code. | 44372 |
| Statement Intelligence    | Finance Charge memo customer ledger entries are added to bank account reconciliation matching. | 34842 |
| Statement Intelligence    | Added possibility not to apply ledger entries to journal lines if you apply to oldest application method. | 42492 |
| General Application       | When setting up a bank account through the bank account assisted setup, you can is now copy the authentication from another company if this  company has a valid authentication. | 43970 |
| General Application       | When sharing authentication with another company, you can now copy the bank information to the bank in the other company. | 43971 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Added action to download email notification and report attachment if exists. | 42266 |
| General Application       | Unable to delete bank branch number.                         | 44654 |
| General Application       | Upgrade issue due to split character check in No. Series.    | 45461 |
| General Application       | Wrong datetime format Rabobank.                              | 45453 |
| Payment and Cash Receipts | Journal lines with payment method Manual are not updated and not posted when suggesting vendor payments. | 45268 |
| Payment and Cash Receipts | Files unnecessarily split at manual export for some banks.   | 45380 |
| Statement Intelligence    | The import of additional information adds empty lines.       | 45039 |
| Statement Intelligence    | The creation of journals during install or activation of Statement Intelligence has been improved. | 44834 |
| Statement Intelligence    | Error when reconciling the Bank Account with a Bank Account Reconciliation Rule that has Bal. Account as Bank Account with different currency. | 45240 |



## Payment Management 2022 R2, Service Pack 2, Hotfix 4

*Released: February 10, 2023*  
*Online version: 5.2.4.0*   
*Supported Business Central version: 2022 Release Wave 2 (BC21)*



### New or changed functionality

| Functional area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Added notification for failing Payment Management job queues. | 44381 |
| General Application | Changed the visibility of the Payment Discount fields in Applied Entries FactBox. To display the fields, go to the General Ledger Setup, and in the "Show Amounts" field, select "All Amounts." | 44908 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Payment Discount posted on both Discount Tolerance G/L account and Payment Discount G/L account. | 44872 |
| General Application       | Potential infinite loop in purchase validation when the BG/PG payment method is used. | 44952 |
| General Application       | Balance Account setup not respected on purchase documents.   | 44955 |
| Payment and Cash Receipts | Payment validation functionality triggered in standard payment journals. | 44822 |
| Payment and Cash Receipts | Applies-to ID not set on Customer and Employee ledger entries when summarizing payments manually. | 44949 |
| Platform and Technology   | Payment Management job queues running in deactivated companies. | 44825 |
| Statement Intelligence    | If + sign in number series causes issues.                    | 44912 |



## Payment Management 2022 R2, Service Pack 2, Hotfix 3

*Released: February 2, 2023*  
*Online version: 5.2.3.0*   
*Supported Business Central version: 2022 Release Wave 2 (BC21)*



### New or changed functionality

| Functional area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | Job Queue code units now have a minimum time between runs check. If the execution time is less than the minimum, an error shows the user that there is an issue with the time settings. | 43796 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Payment Method Code causing standard validation error in DK localization. | 44676 |
| Payment and Cash Receipts | Cost Type Code not formatted on Payment Export.              | 44677 |
| Platform and Technology   | Empty account statement fields cause an error in Continia Online, and the file does not get status processed. | 44678 |
| Payment and Cash Receipts | Missing Bank Giro tag in in-house payment file.              | 44691 |



## Payment Management 2022 R2, Service Pack 2, Hotfix 2

*Released: January 31, 2023*  
*Online version: 5.2.2.0*   
*Supported Business Central version: 2022 Release Wave 2 (BC21)*



### New or changed functionality

| Functional area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | If automatic update is enabled, the message for new Bank System Setup availability is disabled. | 44623 |

### Bug fixes

| Functional area         | Description                                                  | ID    |
| ----------------------- | ------------------------------------------------------------ | ----- |
| General Application     | Vendor No. validation error. Modulus 11 is now fixed to work correctly with number lengths up to 25 numbers. | 44072 |
| General Application     | Removed validation of Import formats on the Bank card to avoid errors when importing text formats on XML-based bank systems. | 43816 |
| Platform and Technology | Refresh token called when using manual communication for Rabobank. | 44622 |



## Payment Management 2022 R2, Service Pack 2, Hotfix 1

*Released: January 25, 2023*  
*Online version: 5.2.1.0*   
*Supported Business Central version: 2022 Release Wave 2 (BC21)*



### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | The Creditor No. and Bank Giro No. was taken from the vendor ledger entry. Fixed to assign Creditor No. and Giro No. during suggest vendor payments according to the payment journal setup. | 43713 |
| Statement Intelligence    | Import of bank account statements if multiple statements are enabled on the bank account, and there are new bank account reconciliations with a blank date. | 44235 |
| Statement Intelligence    | Bank Account Reconciliation page closes if the statement date is empty. | 44262 |



## Payment Management 2022 R2, Service Pack 2

*Released: January 18, 2023*  
*Online version: 5.2.0.0*   
*Supported Business Central version: 2022 Release Wave 2 (BC21)*



### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | To prevent run-away job queues, the Job Queue codeunits now have a minimum time between runs checks. | 43796 |
| Payment and Cash Receipts | Added support for importing files from Payment Service Providers (e.g., Amazon, Bol, PayPal, Klarna) into the Cash Receipt journal. | 35031 |
| Platform and Technology   | Preview feature - Direct communication for Rabobank.         | 31197 |
| Platform and Technology   | Added event to apply Dimensions when Gen Journal Lines are created from Recon rule. | 44067 |
| Statement Intelligence    | The pages used for manual application in Statement Intelligence now contain the standard search functionality and the *Show Posted Document* and *Find Entries* actions. | 42273 |
| Statement Intelligence    | New functionality to suggest the possible ending number for the number series when it is missing. | 43089 |



### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Ability to copy the default reference and add a space between fields. | 43634 |
| Statement Intelligence    | Importing bank account statements if multiple statements are enabled on the bank account, and there are new bank account reconciliations with a blank date. | 44235 |
| Statement Intelligence    | Vendor currency overwrites the currency code from the Bank Account on the General Journal Line. | 43161 |
| Statement Intelligence    | Changes to the standard filter set on the Bank Account Ledger Entries subpage on the Bank Account Reconciliation Page. The filter now filters on posting date but also respects any tolerance days (after) setup on the bank. | 43359 |
| Statement Intelligence    | Bank Account Reconciliation Page closes if statement date is blank. | 44262 |
| Payment and Cash Receipts | Missing indirect permissions for Cust. Ledger Entry and Employee Ledger Entry in Gen. Jnl. Apply Events codeunit. | 43729 |
| Payment and Cash Receipts | Balance account currency setup ignored.                      | 43985 |
| Payment and Cash Receipts | Not all lines validated for purchase validation.             | 44111 |
| Payment and Cash Receipts | Creditor No. and Giro No. are now assigned during suggested vendor payments according to the payment journal setup. | 43713 |



## Payment Management 2022 R2, Service Pack 1, Hotfix 3

*Released: January 9, 2023*  
*Online version: 5.1.3.0*   
*Supported Business Central version: 2022 Release Wave 2 (BC21)*  


### Bug fixes


| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts                                 | Payment Discount Date not considered when calculating the Discount amount. | 43962 |





## Payment Management 2022 R2, Service Pack 1, Hotfix 2

*Released: December 30, 2022*  
*Online version: 5.1.2.0*   
*Supported Business Central version: 2022 Release Wave 2 (BC21)*  


### Bug fixes


| <span style="white-space: nowrap;">Functional area</span> | Description                                       | ID    |
| --------------------------------------------------------- | ------------------------------------------------- | ----- |
| Statement Intelligence                                    | Balance error when importing multiple statements. | 43824 |



## Payment Management 2022 R2, Service Pack 1, Hotfix 1

*Released: December 20, 2022*  
*Online version: 5.1.1.0*  
*Supported Business Central version: 2022 Release Wave 2 (BC21)*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts                                 | Validation rule added to enable US Nacha counter.            | 43397 |
| Payment and Cash Receipts                                 | Transfer creditor number for bank and plus giro payment methods | 43633 |
| Platform and Technology                                   | General support for Business Central FI.                     | 43566 |
| Platform and Technology                                   | General support for Business Central DE.                     | 43567 |



### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| General Application                                       | Editing, creating, and copying Payment Reference Template with spaces between the fields. | 42625 |
| General Application                                       | Error on updating bank account on the vendor. If Bank Branch No.  lookup was used with inserted Bank Account No., and lookup is used for the same Bank Branch No. again it would rewrite Bank Account No. to the saved one before. Now it rewrites the Bank Account No. only when IBAN lookup is used. | 42906 |
| General Application                                       | Initial setup after activation not ran.                      | 43466 |
| Payment and Cash Receipts                                 | Added functionality to exclude payment notification from bank file based on validation rule. | 43035 |
| Payment and Cash Receipts                                 | When suggesting a customer, if a vendor exists with the same number, the vendor information was validated. Fixed to use Customer information. | 43193 |
| Payment and Cash Receipts                                 | Payment Discount Tolerance not calculated correctly.         | 43463 |
| Payment and Cash Receipts                                 | Cost Type Code on vendor card ignored.                       | 43468 |
| Platform and Technology                                   | Statement import queue fails.                                | 43469 |
| Platform and Technology                                   | Unable to add Incoming document factbox.                     | 43672 |
| Statement Intelligence                                    | Unable to import all available statements if new statement is disabled. | 43501 |



## Payment Management 2022 R2 Service Pack 1

*Released: December 2, 2022*  
*Online version: 5.1.0.0*   
*Supported Business Central version: 2022 Release Wave 2 (BC21)*

### New or changed functionality

All features and bug fixes released for [Payment Management 4.4.0.1 to 4.4.0.2](@PM-229) are also included in Payment Management 5.0. The descriptions of these features and bug fixes are not repeated here.

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID               |
| --------------------------------------------------------- | ------------------------------------------------------------ | ---------------- |
| General Application                                       | Detailed information on Payment Journal and Collection Entry lines. | 35063            |
| General Application                                       | Specification of the validation error in an error message that displays after posting invalid purchase documents. | 40295<br />42132 |
| General Application                                       | Page search terms updated with Continia Payment Management and page name in English. | 40804            |
| General Application                                       | Approval actions Approve, Reject, and Delegate work for multiple lines. | 41613            |
| General Application                                       | Actions in Payment Journal, Cash Receipt Journal, and Bank Account Reconciliation moved to align with new Business Central layout. | 41616            |
| General Application                                       | When using the Payment Approval workflow, and some lines are waiting for approval, only the approved lines will be exported, and no error is thrown. | 42069            |
| General Application                                       | Setting in the bank card that enables a bank status update for automatic payment journal lines. | 42435            |
| Payment and Cash Receipts                                 | Payment Management now supports US Nacha payment export.     | 42427            |
| Statement Intelligence                                    | Setup option added that specifies if Ending No. field on sales or purchase documents must be ignored if the field is empty. | 34841            |
| Statement Intelligence                                    | The General Reconciliation Rules and Bank Account Reconciliation Rules now support searching the notifications. | 34877            |
| Statement Intelligence                                    | Tolerance setup for reconciliation suggestions to widen the search for entries. | 40118            |
| Statement Intelligence                                    | Message added that summarizes all number series that have missing starting and ending numbers. | 34845            |
| Statement Intelligence                                    | Import multiple statements when using current week/month. The recurring message asking the user if the starting balance should be updated is removed. Reconciliation lines that exceed the aggregation period are no longer added to the wrong reconciliation. | 42428            |
| Statement Intelligence                                    | Setting in the bank account that allows to import files to the reconciliation and reconcile automatically. | 42434            |
| Statement Intelligence                                    | Job queue to import bank account statements automatically is now created separately for each bank account no. | 42432            |
| Statement Intelligence                                    | When switched on, the setting *Copy Notification to Description* on the Bank Card page, copies the first line of the notification to the description field of the Bank Account Reconciliation line. | 40066            |



### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID               |
| --------------------------------------------------------- | ------------------------------------------------------------ | ---------------- |
| General Application                                       | Customer statement report without payment reference type set on Sales and Receivables setup throws error. | 41520            |
| General Application                                       | Retention policy to cause errors for delegate users.         | 43166            |
| Platform and Technology                                   | Field validation for Modulus 11 compliance does not work for strings longer than ten characters. | 42413            |
| Statement Intelligence                                    | Cannot transfer vendor ledger entry with the positive amount to correct journal in Statement Intelligence when creating refunds for customer and vendors. Issue only applies to bank account reconciliation lines when a customer or vendor is identified, no reconciliation suggestions were found, and the setting *Handle journal lines* is set to *Create journal lines on Import* in the Statement Intelligence Setup. | 30923            |
| Statement Intelligence                                    | Reconciliation suggestion entries created for entries with a posting date after the date of the bank account reconciliation line throws an error. | 43056            |
| Statement Intelligence                                    | Statement Intelligence causes an error when trying to access the *Data Imported from Bank for Line* on the Bank Account Reconciliation Line if users have the CPM Recon permission set. | 41519<br />41517 |
| Statement Intelligence                                    | Statement Intelligence causes an error when trying to access the *Additional Information* on the Bank Account Reconciliation Line if users have the CPM Recon permission set. | 41516            |
| Statement Intelligence                                    | The statement date on the Bank Account Reconciliation is not updated when importing multiple bank account statements into the same Bank Account Reconciliation. | 42429            |
| Payment and Cash Receipts                                 | Incorrect payment discount at vendor invoices and credit notes. Updated payment validation now includes discounts when checking the amount. Credit notes with overdue amount suggestions throw a validation. After posting date changes, the amount is recalculated to include discount and tolerance calculations. | 42061            |
| Payment and Cash Receipts                                 | Manual payments potentially exported to payment file.        | 43081            |



## Payment Management 2022 R2, Hotfix 5

*Released: November 16, 2022*  
*Online version: 5.0.5.0*  
*Supported Business Central version: 2022 Release Wave 2 (BC21)*

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Statement Intelligence    | Missing dialog that specifies transaction start date at initial statement import in Bizcuit. | 42918 |
| Platform and Technology   | Job queue causing error during activation by delegated user. | 42917 |
| Payment and Cash Receipts | Standard approval action not displayed in Payment Journal.   | 42919 |



## Payment Management 2022 R2, Hotfix 4

*Released: November 9, 2022*  
*Online version: 5.0.4.0*  
*Supported Business Central version: 2022 Release Wave 2 (BC21)*

### Bug fixes

| Functional area        | Description                                                  | ID    |
| ---------------------- | ------------------------------------------------------------ | ----- |
| Statement Intelligence | Bank Account Reconciliation notifications not deleted during posting. | 42916 |



## Payment Management 2022 R2, Hotfix 3

*Released: November 8, 2022*  
*Online version: 5.0.3.0*  
*Supported Business Central version: 2022 Release Wave 2 (BC21)*

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Statement Intelligence    | Applied amount incorrect error when posting Bank Account Reconciliation (BC21 only). | 42553 |
| Payment and Cash Receipts | Fields not transferred from the journal to the Employee Ledger Entry. | 42560 |
| General Application       | Assisted setup for bank accounts not run after an installation using the connected apps functionality. | 42569 |
| General Application       | Missing basic permissions for table "Payment Jnl. Export Error Text." | 42588 |
| Payment and Cash Receipts | Reappearing Payment Journal Setup notification.              | 42589 |
| General Application       | Payment Method view setting ignored when using the Payment Method Code field. | 42522 |
| General Application       | Error message display if no payment reference type is set on the Sales and Receivables setup and the Customer Statement report is run. | 41520 |
| General Application       | Error message display when posting employee payments from the payment journal. | 42556 |



## Payment Management 2022 R2, Hotfix 2

*Released: October 28, 2022*  
*Online version: 5.0.2.0*  
*Supported Business Central version: 2022 Release Wave 2 (BC21)*

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Support added for multiple accounts with the same IBAN/Account number but for different currencies. | 39837 |
| Payment and Cash Receipts | Limited regulatory reporting description in payment file causing error due to length limit for some banks. | 41954 |
| General Application       | Field caption length causing an error when adding it to the Payment Notification template. | 42089 |
| General Application       | Added external document number, account name, and payment method when suggesting customer payments. | 42175 |
| General Application       | Recipient reference miscalculated.                           | 42222 |
| Statement Intelligence    | Added permission/license check before inserting minimum length search exceptions. | 42224 |
| General Application       | Added import of URLs if the table is empty.                  | 42264 |
| General Application       | Added validation to synchronize payment method on customers when setting value. | 42265 |
| General Application       | Added check to avoid error on upgrade if payment method on the customer has been deleted. | 42267 |
| General Application       | Payment method is not editable in Vendor Payment Setup.      | 42417 |

## Payment Management 2022 R2, Hotfix 1

*Released: October 18, 2022*  
*Online version: 5.0.1.0*  
*Supported Business Central version: 2022 Release Wave 2 (BC21)*

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Platform and Technology   | Upgrade error if the company has been used and Payment Management is no longer activated. | 41970 |
| General Application       | Synchronization of Customer Payment Method Code on upgrade.  | 42038 |
| Payment and Cash Receipts | KID reference not transferred to the Payment Journal Lines when a payment suggestion is made. | 42044 |
| Payment and Cash Receipts | Payment Receipt import errors if the description is longer than 20 characters. | 42055 |

## Payment Management 2022 R2

*Released: October 1, 2022*  
*Online version: 5.0.0.0*   
*Supported Business Central version: 2022 Release Wave 2 (BC21)*

### New or changed functionality

All features and bug fixes released for [Payment Management 4.4.0.1 to 4.4.0.2](@PM-229) are also included in Payment Management 5.0. The descriptions of these features and bug fixes are not repeated here.

| <span style="white-space: nowrap;">Functional area</span> | Description | ID  |
| --- | --- | --- |
| General Application                                       | Payment Management now supports the new Microsoft Connected Apps onboarding experience in Business Central. | 40854 |
| General Application                                       | The assisted Payment Management Setup guide has been removed and replaced by default settings. | 40855 |
| General Application                                       | The assisted Payment Method Setup guide has been removed and replaced by default settings. | 41213 |
| General Application                                       | The assisted Bank Account Setup guide is now the first setup to complete. The Bank Account Setup guide now runs automatically after you activate the Payment Management app. | 41214 |
| General Application                                       | Telemetry logging for the assisted Bank Account Setup guide has been added to improve the user experience. | 41216 |
| General Application                                       | In the payment journal and Bank Account Reconciliations setup, links to videos have been added to the teaching tips. | 41252 |
| General Application                                       | In the payment journal, the approve, reject and delegate actions now work with multiple lines. | 41613 |
| Statement Intelligence                                    | Actions in the Bank Account Reconciliations page for Business Central have been repositioned. | 41717 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| Statement Intelligence | The error that caused the wrong vendor and wrong vendor number on bank account reconciliation lines. | 41739 |

<style>
  .content table tr td:nth-child(1) {
    width: 200px;
  }
</style>