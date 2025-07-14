---
title: Detailed Changelog for Continia Payment Management 2021 R2
description: Changelog containing an overview of all new updates, features and hotfixes for Continia Payment Management 2021 R2
date: 30-03-2022
id: PM-161
lang: en
---

# Detailed Changelog for Continia Payment Management 2021 R2

This article lists all new updates, features, service packs, and hotfixes for Continia Payment Management 2021 R2.

## Payment Management 2021 R2 Service Pack 3, hotfix 6

*Released: March 23, 2022*  
*Online and on-premises version: 3.3.0.6*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts                                 | Added a message to notify users if no lines are available for import in the cash receipt journal. | 25952 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Statement Intelligence                                    | Fixed an issue in IBAN matching in Statement Intelligence.   | 32021 |
| General Application                                       | Added missing fields in the foreign notification designation import. | 32023 |



## Payment Management 2021 R2 Service Pack 3, hotfix 5

*Released: March 16, 2022*  
*Online and on-premises version: 3.3.0.5*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Statement Intelligence                                    | Added functionality to match customers and vendors from IBAN on the bank account. | 31945 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts                                 | Fix to Bizcuit status import to ensure the status for all payments are updated. | 31904 |
| Payment and Cash Receipts                                 | Fixed issue when creating Payment Notifications for entries with identical document type and document number. | 31906 |
| Payment and Cash Receipts                                 | Fixed potential issue causing an insert error while sending email notifications. | 31908 |
| Statement Intelligence                                    | Fixed potential issue with incorrect account type when creating journal lines from Statement Intelligence. | 31921 |

## Payment Management 2021 R2 Service Pack 3, hotfix 4

*Released: March 7, 2022*  
*Online and on-premises version: 3.3.0.4*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts                                 | Fixed issue with Credit Transfer Registers potentially not being split correctly, causing issues with matching in Statement Intelligence. | 31821 |

## Payment Management 2021 R2 Service Pack 3, hotfix 3

*Released: March 4, 2022*  
*Online and on-premises version: 3.3.0.3*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| General Application                                       | Support for new Business Central email connectors. Due to a Microsoft validation, the old SMTP setup is no longer supported.   <br />Note: Only applicable for Business Central Cloud and OnPremises BC19 and later. | 24221 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Statement Intelligence                                    | Fixed issue with matching Bank Account Reconciliation lines from Payment Batch ID. | 31721 |

## Payment Management 2021 R2 Service Pack 3, hotfix 2

*Released: February 28, 2022*  
*Online and on-premises version: 3.3.0.2*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Statement Intelligence                                    | Fixed an issue that caused an incorrect match of debit reconciliation lines. | 31600 |

## Payment Management 2021 R2 Service Pack 3, hotfix 1

*Released: February 22, 2022*  
*Online and on-premises version: 3.3.0.1*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Platform and Technology                                   | Fixed potential issue with users getting prompted for Authorization Update when not required. | 31475 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| General Application                                       | Minor improvement to the bank update due to changes in the way bank systems are managed. | 31398 |
| Payment and Cash Receipts                                 | Fixed issue with Batch Id from Bizcuit. This is used for bank account reconciliation. | 31402 |
| Country and Regional                                      | Fixed issue with applying entries for the Bank Giro Journal (NL only). | 31532 |

## Payment Management 2021 R2 Service Pack 3

*Released: February 17, 2022*  
*Online and on-premises version: 3.3.0.0*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| Payment and Cash Receipts                                 | Added report for suggesting employee payments with the ability to use employee payment method and balance account. | 27895 |
| Payment and Cash Receipts              | Added basic functionality for using Direct Debit with Payment Management. Available from  Feature Management. | 28809 |

## Payment Management 2021 R2 Service Pack 2, hotfix 3

*Released: February 02, 2022*  
*Online and on-premises version: 3.2.0.3*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| Payment and Cash Receipts                                 | Added the Skip Payments toggle on the Vendor card that will exclude all payments to the vendor when creating a Payment Suggestion. | 30414 |
| General Application                                       | Moved Unique References for DNB and SpareBank1 to Authentication. | 30539 |
| Statement Intelligence                                    | Added an action on the Bank Account to set up a job queue for automatic import of account statements. | 30541 |
| Development                                               | Added an event to override the "Direct" check for the Automatic Imports code units. | 30590 |
| General Application                                       | Added validation of the Organization ID for DNB bank.        | 30950 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| Payment and Cash Reciepts                                 | Fixed a potential currency issue in the Cash Receipt Journal. | 30828 |

## Payment Management 2021 R2 Service Pack 2, hotfix 2

*Released: January 03, 2022*  
*Online and on-premises version: 3.2.0.2*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Fixed issue with Payment Reference not being calculated correctly in the Purchase Journal. | 30305 |
| General Application | Added possibility to use balancing lines in Purchase Journal. | 30400 |
| Payment and Cash Receipts | Fixed potential issue with Payment Journal Setup initiation. | 30306 |
| Payment and Cash Receipts | Fixed issue with potential false positives if Customer No. used in Payment Reference Mask. | 30377 |
| Payment and Cash Receipts | Fixed issue resulting in Payment Notification error when summarizing payments manually. | 30341 |
| Statement Intelligence | Fixed issue when searching for External Payment References found in notifications. | 30359 |
| Statement Intelligence | Added permission checks to avoid error when Statement Intelligence is not added to  License. | 30361 |


## Payment Management 2021 R2 Service Pack 2, hotfix 1

*Released: December 22, 2021*  
*Online and on-premises version: 3.2.0.1*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| Platform and Technology | Support for Sparebank1 and other banks in Norway using TietoEvry for integration. | 28486 |
| Platform and Technology | Support for Barclays bank in UK. | 29072 |
| Platform and Technology | Added the event OnAfterImportPaymentReceipt() from customer request. | 29696 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Fixed issue with Recipient reference validation error in purchase journal. | 30260 |
| Platform and Technology | Fixed error handling issue in HTTP communication, causing misguiding error message. | 30081 |
| Payment and Cash Receipts | Fixed issue with KID being overwritten in Payment suggestion. | 30218 |
| Statement Intelligence | Fixed potential issue with starting balance when using multiple account statement import. | 29852 |

## Payment Management 2021 R2 Service Pack 2

*Released: November 29, 2021*  
*Online and on-premises version: 3.2.0.0*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| Payment and Cash Receipts | Improved check for notification length when summarizing payments manually. | 29083 |
| Payment and Cash Receipts | Added option to use Invoice Posting Date for Payment Notifications. | 28994 |
| Platform and Technology | Added option to share Certificates and tokens used for bank communication between companies and banks. | 22261 |
| Platform and Technology | Added codeunits for automatic creation of Payment Suggestion and Payment Export. | 28464 |
| Platform and Technology | Added codeunits for automatic import of Account Statements and Cash receipt files. | 28467 |
| Statement Intelligence | Added possibility to import multiple account statements into the same bank account reconciliation. | 21154 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Added access to Bank File Check List from Troubleshooting page in order to resolve Danske Bank Error code 29. | 28422 |
| Payment and Cash Receipts | Fixed issue with Recipient Reference being capitalized. | 26356 |
| Payment and Cash Receipts | Fixed an issue with handling multiple currencies in the Cash Receipt Journal. | 28182 |
| Statement Intelligence | Fixed issue with Vendor Ledger Entries not being identified by External Document No. | 29748 |



## Payment Management 2021 R2 Service Pack 1, hotfix 1

*Released: October 25, 2021*  
*Online and on-premises version: 3.1.0.1*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Fixed issue where Regulatory Reporting might not be validated correct on purchase documents. | 27087 |
| General Application | Added code to ensure that the Balance Account Setup related to a Bank Account is deleted if the Bank Account is deleted. | 27845 |
| General Application | Added an additional filter when selecting the Cash Receipt Journal template to  create the Payment Management journals in. This is added to avoid conflicts with Collection Management. | 28788 |
| Payment and Cash Receipts | Fixed  an error that caused the an update setup dialog to appear every time payments where exported from the Payment Journal. | 28337 |
| Payment and Cash Receipts | Added code to ensure that the Payment Journal Setup is renamed if the Payment Journal Batch is renamed. | 28344 |
| Payment and Cash Receipts | Fixed  an error when using the Summarize Lines action in the Payment Journal. The summarized lines did not contain all the applications of Vendor Ledger  Entries in some cases. | 28790 |
| Statement Intelligence | Cash  Receipt Journal lines created from Statement Intelligence are created with the wrong currency code if the bank account has local currency and the customer has a currency code different from the local currency code. This is now fixed so the currency code is cleared if the bank account has currency  code that equals LCY. | 27943 |
| Statement Intelligence | Fixed  an error in the code that caused Statement Intelligence to require Ending No.  on all number series used on General Journals. | 28365 |
| Statement Intelligence | Additional validation added in Statement Intelligence to ensure the Customer Nos.  assigned to the Bank Account Reconciliation Lines are valid. | 28493 |
| Statement Intelligence | Indirect permissions for Bank Account Ledger Entry table added in Statement  Intelligence. | 28762 |
| Statement Intelligence | An incorrect Reconciliation Suggestion was found based on External Document No. on multiple lines even though it had not reference related to the entry. | 28803 |
| Statement Intelligence | Added possibility to use Payment Reference Search rules to match a Bank Account  Ledger Entry based on the content of the External Payment Reference field. | 28860 |
| Statement Intelligence | Added additional check to valid Customer/Vendor Nos in the reconciliation. | 28870 |


## Payment Management 2021 R2 Service Pack 1

*Released: October 1, 2021*  
*Online and on-premises version: 3.1.0.0*

### New or changed functionality
| <span style="white-space: nowrap;">Functional area</span> | Description | ID  |
| --- | --- | --- |
| General Application | Minor UX related changes made to the Currency Exchange Rate Setup page. | 17238 |
| General Application | Regulatory Reporting Codes are added to the Vendor and can be accessed from the Vendor Card page. The Regulatory Reporting Codes is copied to a purchase document when the Pay-To Vendor No. is assigned. | 27161 |
| General Application | Indentation on records of type Line is removed on the Bank Export Data page to improve the overall performance of  the page. | 27989 |
| General  Application | File conversion logging. | 28135 |
| General Application | An additional step has been added to the assisted setup for vendor payment information to enable the user to setup balancing accounts based on currencies. | 27192 |
| Payment and Cash Receipts | Added a new setting "Use Payment Information from Vendor" when suggesting vendor payments in the Payment Journal. The new setting is also added to the Payment Journal Setup to enable the user to set a default value. The setting makes it possible to decide if payment information from the vendor should be used when suggesting vendor payments. The setting includes three options: Yes - takes the information from the vendor Use for Missing Fields - takes the information from the Vendor Ledger Entry but if values are missing it uses the vendor information No - takes the information from the Vendor Ledger Entry Use Payment Summarize Setup - uses the settings from the summarizing payments available on the Payment Journal Setup page or the request page on Suggest Vendor Payments. | 25976 |
| Payment and Cash Receipts | Changed the check on the IBAN field on the Bank Account. The message with a warning about the same IBAN on more than one Bank Account does not appear when the IBAN field is cleared. | 27245 |
| Payment and  Cash Receipts | It is now possible to create a custom name for manually exported payment files. The feature can be found on the troubleshooting page which can be opened from the Payment setup page. | 12425 |
| Payment and  Cash Receipts | Enhanced and optimized the initialization of the validation engine in the Payment Journal. Additional checks has been added to only initialize the validation engine when needed. | 26838 |
| Payment and Cash Receipts | Added new setting to the Payment Journal Setup and on the request page of Suggest Vendor Payments. The setting  enables the possibility of having Vendor Ledger Entries like Credit Memos and other non-payable entries created as journal lines in the payment journal. | 26072 |
| Payment and Cash Receipts | When suggesting vendor payments the Cost Type code from the Vendor is used if not available on the Vendor Ledger  Entry is empty. Only applicable for payment methods where Cost Type Codes are relevant. | 27159 |
| Payment and Cash Receipts | It is now possible to allow automatically renumbering of journal lines on the payment journal setup page. | 16704 |
| Statement Intelligence | Notification lines from the bank account reconciliation lines are now shown on the posted bank account statement. | 19740 |
| Statement Intelligence | A new manual setup page for Statement Intelligence has been introduced. here you can setup default values and journals for Statement Intelligence. The Statement Intelligence fields on the Payment Management Setup page has been moved to the new page. | 27127 |
| Statement Intelligence | When setting up default journals for Statement Intelligence through the general assisted setup, journals for vendor and employee reconciliation is created. | 27128 |


### Bug fixes
| <span style="white-space: nowrap;">Functional area</span> | Description | ID  |
| --- | --- | --- |
| Payment and  Cash Receipts | Fixed an error when importing payment receipts that caused multiple applications not to be set. Only the first found Customer Ledger Entry was applied. | 26857 |
| Payment and  Cash Receipts | Fixed an error when importing payment in the Cash Receipt. When enabling the setting Create Balancing Account Lines Per Day the Document Type was blank on the created balancing journal lines. This resulted in an error when posting the journal. The issue is only relevant for files that are of filetype .text. | 27339 |
| Payment and Cash Receipts | Added indirect permission Vendor Ledger Entries in codeunit used by Suggest Vendor Payments. | 27851 |
| Payment and  Cash Receipts | An issue has ben resolved related to the import of status files if using a bank with direct communication where direct import is disabled and direct export id enabled. When updating status in the Payment Journal we looked at the wrong  field (Direct Import) and we should have been looking at the Direct Export field because this field is related to exporting payment files AND importing status files. The issue would show itself when importing status and a dialog is shown to import a file. | 27860 |
| Statement Intelligence | Fixed an issue with the action "Data imported from bank for reconciliation" on the Bank Account Reconciliation Page. The action did not show the correct header and related lines. | 26859 |


## Payment Management 2021 R2, hotfix 1

*Released: September 15, 2021*  
*On-premises version: 3.0.0.1* 

### Bug fixes
| <span style="white-space: nowrap;">Functional area</span> | Description | ID  |
| --- | --- | --- |
| General Application | Fixed issue with fields being cleared after running Bank Account Setup. | 27682 |
| Payment and Cash Receipts | Fixed issue causing error when opening payment journals in companies that have not been activated. | 27708 |
| Statement Intelligence | Fixed issue with overflow for KID filter in bank account reconciliation. | 27683 |
| Statement Intelligence | When changing statement no. the notifications on the bank account reconciliation lines are no longer disappearing. | 27067 |

## Payment Management 2021 R2

*Released: September 1, 2021*  
*On-premises version: 3.0.0.0* 

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID  |
| --- | --- | --- |
| General Application | The Payment Reference Templates page is available when searching. | 27202 |
| Payment and Cash Receipts | Summarize payments manually. The action "Analyze" has been added to the payment journal to be able to check if a set of selected journal lines can be summarized. The feature can be enabled through the Continia Feature Management page. The action "Summarize Payments" has been added to the payment journal to enable the user to manually summarize payments in the Payment Journal. Furthermore fields have been added to the Payment Journal Setup related to  the setup of manually summarizing payments. The feature can be enabled through the Continia Feature Management page. | 25400 |
| Payment and Cash Receipts | New action to Search file archive for key words from the payment journal. | 26898 |
| Statement Intelligence | Support for reconciliation of Employees in Statement Intelligence. Field has been added to the Bank Account  to be able to appoint a payment journal where journal lines related to reconciliation of employees will be created. On the Bank Account Reconciliation Page fields has been added to access the Payment Journal related to employee reconciliation and show the number of journal lines created. Due to a limitation in Business Central only Bank Accounts where the "Currency Code" is blank is supported when reconciliation employees. If the Bank Account does not have a blank currency code then the reconciliation is not executed and related page elements are hidden. Added support for creating Employee Reconciliation Rules in the Bank Account Reconciliation. The action "Customer/Vendor Reconciliation Rules" has been split into two separate actions; "Customer Reconciliation Rules" and "Vendor Reconciliation Rules". The feature can be enabled through the Continia Feature Management page. Support for manual application of Employee Ledger Entries from the Bank Account Reconciliation page. Entries can be selected and journal lines will be created in the Payment Journal specified on the Bank Account Card page. The feature can be enabled through the Continia Feature Management page. | 24949 |


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Fixed issue with missing ending no, in PM number series. | 27168 |
| General Application | Fixed minor issue in Bank Account  Setup causing error due to missing Bank System code. | 27059 |
| General Application | Fixes error in Vendor Information Setup if BTI payment method territory mapping does not exist. | 27137 |
| Payment and Cash Receipts | Fixed issue with potentially getting wrong group status. | 27176 |
| Payment and Cash Receipts | Fixed missing Application for credit memos in some cases when summarizing payments. | 27401 |
| Statement Intelligence | Fixed issue with blank notification lines. | 27063 |
| Statement Intelligence | When changing statement no. the notifications on the bank account reconciliation lines are no longer disappearing. | 27067 |

