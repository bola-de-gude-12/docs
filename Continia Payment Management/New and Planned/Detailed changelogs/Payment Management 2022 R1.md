---
title: Detailed Changelog for Continia Payment Management 2022 R1
description: Changelog containing an overview of all new updates, features, and hotfixes for Continia Payment Management 2022 R1
date: 04-10-2022
id: PM-229
lang: en
---

# Detailed Changelog for Continia Payment Management 2022 R1

This article lists all new updates, features, service packs, and hotfixes for Continia Payment Management 2022 R1.  

## Payment Management 2022 R1 Service Pack 4, hotfix 2

*Released: September 29, 2022*  
*Online version: 4.4.0.2*  
*Supported Business Central version: 2022 Release Wave 1 (BC20)*

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | As it could cause the authentication to become invalid, it is no longer possible to update the Authentication to Isolated Storage multiple times. | 41695 |
| Payment and Cash Receipts | The customer balance was not calculated correctly when creating customer payment suggestions. | 41692 |
| General Application       | An error in the validation of purchase documents.            | 41693 |
| Payment and Cash Receipts | An issue that caused a potential error in the Payment Journal Setup when you suggested employee payments. | 41694 |


## Payment Management 2022 R1 Service Pack 3, hotfix 3

*Released: September 28, 2022*  
*Online version: 4.3.0.3*  
*Supported Business Central version: 2022 Release Wave 1 (BC20)*

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | The filtering of lines was not respected when validating the posting. | 41141 |
| Payment and Cash Receipts | An error stating that the Payment Journal Setup was not registered. | 41184 |
| Statement Intelligence    | Journal lines for currency differences were not created.     | 41263 |
| Payment and Cash Receipts | An error that appeared in the payment journal when opening the journal, or deleting or posting all journal lines. | 41364 |



## Payment Management 2022 R1 Service Pack 3, hotfix 2

*Released: September 8, 2022*  
*Online version: 4.3.0.2*  
*Supported Business Central version: 2022 Release Wave 1 (BC20)*

### New or changed functionality 

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | The functionality to use the email body from "Report Selection" when you send payment notifications has been added. | 41130 |



## Payment Management 2022 R1 Service Pack 3, hotfix 1

*Released: September 5, 2022*  
*Online version: 4.3.0.1*  
*Supported Business Central version: 2022 Release Wave 1 (BC20)*

### New or changed functionality 

| Functional area         | Description                                                  | ID    |
| ----------------------- | ------------------------------------------------------------ | ----- |
| General Application     | Payment Management-payment information fields have been added to the vendor template. | 39961 |
| General Application     | If the "Skip Payments" function is enabled on the vendor, the mandatory check on "Recipient Email" will not be performed. | 40679 |
| Platform and Technology | The external procedure SummarizePayments(GenJournalLine, SuppressDialog) has been added. | 40811 |
| General Application     | On the "Payment Notification Setup" page, a new option "Send Email on Posting Date" has been added. The option enables users to send email notifications based on the posting date of the payment if using a job queue. If users enable the option, email notifications will be sent for payments with a posting date equal to or greater than the work date. | 40834 |
| General Application     | On the "Email Template Mapping" page, a new option "Standard Remittance Rpt. Selection" has been added. The option enables the user to attach the report specified in the report selection for vendor remittance. If the option is enabled, the report selection is used as an attachment when sending e-mail notifications. | 40835 |

### Bug fixes

| Functional area        | Description                                                  | ID    |
| ---------------------- | ------------------------------------------------------------ | ----- |
| General Application | Added possibility to add multiple e-mail addresses for both vendor and Bcc mail fields in the Payment  Notification Setup. | 39368 |
| Statement Intelligence | An issue related to the "Payment Discount Tolerance Date" not being used when calculating entry amount in reconciliation has been fixed. | 39981 |
| Platform and Technology | The following two events has been added: OnAfterFindVendorLedgerEntries  OnAfterFindCustomerLedgerEntries OnAfterReconcile | 40052 |
| General Application | Payment Management-payment information fields have been added to the vendor template. | 40477 |
| Payment and Cash Receipts | Fixed an error with the consolidated vendor/customer balance calculation. | 40674 |
| Payment and Cash Receipts | Fixed an issue with "Total Amount LCY" not being displayed in the payment journal if the page was opened from search. | 40812 |
| Payment and Cash Receipts | Manual payment has been excluded from the creation of payment notifications. | 40862 |
| Payment and Cash Receipts | Fixed an issue with the journal balance not being calculated correctly. | 40987 |
| Payment and Cash Receipts | Changed the handling of additional transaction statuses if the group status was rejected. | 41010 |

## Payment Management 2022 R1 Service Pack 3

*Released: August 30, 2022*  
*On-premises and online version: 4.3.0.0*  
*Supported Business Central version: 2022 Release Wave 1 (BC20)*

> [!IMPORTANT]
>
> If you are using the on-premises version of Business Central, you must re-collect your license file from Microsoft and import it into your Business Central installation. 

### New or changed functionality 

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Added support for customer refunds in the payment journal and when creating customer payment suggestions. Additional payment information fields have been added to the customer card. | 12321 |
| Payment and Cash Receipts | The new feature Payment Approval Workflow has been implemented. The feature enables you to set up an approval workflow for a payment journal to require one or more approvers to approve all or specific lines in the journal before the lines can be posted. <br /><br />A new permission set, CPM365 APPRADMIN, has been added to give users permission to create and edit payment approval workflows and view all approval requests for all payment journals. | 12447 |
| Statement Intelligence    | Customer statements can now be used with Statement Intelligence. | 20811 |

### Bug fixes

| Functional area        | Description                                                  | ID    |
| ---------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Support for reminders in the cash receipt journal. |28394|
| Payment and Cash Receipts | An issue with the validation of the applied entry amount in the payment journal has been fixed. |40169|
| General Application | Fixed an error that appeared when generating a FIK payment reference on purchase documents if the payment reference template contained the Document Type Indicator field. |40313|
| Payment and Cash Receipts | An issue that caused fee lines not to be handled correctly for currency accounts has been fixed. |40705|
| Payment and Cash Receipts | An issue that caused the transaction status ACSP not to be respected if the group status was rejected. |40706|

## Payment Management 2022 R1 Service Pack 2, hotfix 9

*Released: August 26, 2022*  
*On-premises and online version: 4.2.0.9*  
*Supported Business Central version: 2022 Release Wave 1 (BC20)*

### Bug fixes

| Functional area        | Description                                                  | ID    |
| ---------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Fixed an error in the Suggest Vendor Payments functionality that caused lines to give recipients the wrong message. | 40599 |

## Payment Management 2022 R1 Service Pack 2, hotfix 8

*Released: August 24, 2022*  
*On-premises and online version: 4.2.0.8*  
*Supported Business Central version: 2022 Release Wave 1 (BC20)*


## Payment Management 2022 R1 Service Pack 2, hotfix 7

*Released: August 4, 2022*  
*On-premises and online version: 4.2.0.7*  
*Supported Business Central version: 2022 Release Wave 1 (BC20)*

### New or changed functionality

| Functional area        | Description                                                  | ID    |
| ---------------------- | ------------------------------------------------------------ | ----- |
| Statement Intelligence | Functionality to improve the matching of reversals was added. | 40092 |

## Payment Management 2022 R1 Service Pack 2, hotfix 6

*Released: August 3, 2022*  
*Online version: 4.2.0.6*  
*Supported Business Central version: 2022 Release Wave 1 (BC20)*

### New or changed functionality

| Functional area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | A new basic permission set has been added for users without access to finance. | 35052 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | A warning in Vendor Payment Suggestion has been added. You'll now get a warning if the balance account currency code doesn't match the currency of the applied entry, in which case the balance account will not be defined. | 39781 |
| General Application       | Fixed permission error caused by reversal codes while importing setup. | 39787 |
| General Application       | Fixed an error in the DK localization where a validation error appears even if the "Giro Account No." has a value. Only relevant for FIK payment methods. | 39789 |
| General Application       | Fixed a minor issue with IBAN lookup in the Assisted Bank Account Setup. | 39833 |
| Payment and Cash Receipts | Fixed a validation issue that occurred if an incorrect Payment Export Format was specified for the bank account. | 39974 |
| Statement Intelligence    | The option to define which split characters for the Bank Account Reconciliation has been added. | 40051 |
| Payment and Cash Receipts | Fixed issue that automatically enabled purchase validation for vendors with "Skip Payments" enabled on the vendor card. | 40054 |

## Payment Management 2022 R1 Service Pack 2, hotfix 5

*Released: July 14, 2022*  
*Online version: 4.2.0.5*  
*Supported Business Central version: 2022 Release Wave 1 (BC20)*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | Added the field "Notification Definition" on the Payment Journal Setup page which will be used as a first reference when generating the "Message to Recipient" field value. <br /><br />Added new fields in the Payment Notification Email setup which allow to attach a report to the email and specify a fixed name for the Best Regards email closing. | 35067 |
| Payment and Cash Receipts | The matching based on a KID reference in the import of payment receipts has been improved. For matching, Statement Intelligence now also uses the KID setup in the Sales & Receivables Setup and not only the CPM KID field on the Customer Ledger Entry. | 38294 |
| Statement Intelligence    | If a job queue is set up for a bank account, the import of files is disabled when using "Import and Match", and data will only be imported from the Bank Export Data table. | 39353 |
| Payment and Cash Receipts | Added the fields "Balance to Date" and "Balance (LCY) to Date" on the Bank Account Card. | 39367 |
| Statement Intelligence    | New action added to make it possible to import bank statements from the Bank Export Data table without selecting a file for upload. | 39428 |
| Payment and Cash Receipts | Added functionality to exclude the document types payment or refund, in addition to credit memo, when suggesting vendor payment. | 39430 |
| Payment and Cash Receipts | A field has been added to the payment journal to show the combined amount of the lines in the journal. | 39431 |
| Payment and Cash Receipts | Added the possibility to rebuild notifications for all the lines in the payment journal. | 39432 |
| General Application       | When users upgrade to 4.2.0.5, we'll go through all the customers and set the preferred mandate ID in situations where only one active mandate ID exists. We also aim to set the mandate ID on open customer ledger entries. | 39443 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Fixed an issue with an incorrect amount specified in the payment notification. | 39380 |
| Statement Intelligence    | Fixed an issue when importing more than 1000 transactions from Bizcuit. | 39423 |

## Payment Management 2022 R1 Service Pack 2, hotfix 4

*Released: July 6, 2022*  
*Online version: 4.2.0.4*  
*Supported Business Central version: 2022 Release Wave 1 (BC20)*

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Fixed an issue in payment suggestions that caused the payment date to be defined based on the Payment Discount Tolerance Date in situations where the Payment Discount Date had passed. | 39225 |

## Payment Management 2022 R1 Service Pack 2, hotfix 3

*Released: June 30, 2022*  
*Online version: 4.2.0.3*  
*Supported Business Central version: 2022 Release Wave 1 (BC20)*

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Statement Intelligence    | The creation of manual journal lines in the general journal has been improved. If Account Type and Account No. have been specified on the bank account reconciliation line, they are now added to the journal line when created manually. | 31552 |
| Payment and Cash Receipts | Fixed an issue with amount calculation when using Payment Discount Tolerance Date in Suggest Vendor Payments. | 32490 |
| Payment and Cash Receipts | The purchase notification now allows for special characters in the document number. | 38953 |
| General Application       | Fixed an error that didn't allow users to insert an IBAN manually if the IBAN lookup was not activated. | 39016 |
| Payment and Cash Receipts | Fixed an issue that caused the journal validation not to run in situations where, in the Payment Management Setup, the "Bal. Account Required" toggle is turned off, and users have chosen a payment method not enabled for Payment Management, but have not specified a balance account. | 39018 |
| General Application       | Fixed an issue that caused the communication type to be set to Direct in the assisted Bank Account Setup guide, even if Manual was previously set. | 39025 |

## Payment Management 2022 R1 Service Pack 2, hotfix 2

*Released: June 26, 2022*  
*Online version: 4.2.0.2*  
*Supported Business Central version: 2022 Release Wave 1 (BC20)*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Statement Intelligence    | The names of customers, employees, or vendors have been added to the Reconciliation Suggestions pages. | 26332 |
| Statement Intelligence    | On the Bank Card page, four fields starting with "Don't Search for ..."   have been updated to "Search for ..." to make the logic of the fields more clear. The fields are turned on by default. | 27972 |
| Payment and Cash Receipts | Support for reminders has been added in the Payment Receipt Import. | 32602 |
| General Application       | On the Bank Card page, the Account  Overview group has been removed and added as a FactBox instead. | 34839 |
| General Application       | Tooltips on the Payment Management Setup page have been improved for all supported languages. | 35035 |
| Statement Intelligence    | On the Bank Account Reconciliations page, when using the actions "Transfer Differences to General Journal" or "Create Journal Lines", the message has been updated to include the number of lines created in each of the journals. | 35160 |
| Payment and Cash Receipts | When you export payments through Bizcuit, you will now be asked if you want to open the Bizcuit approval portal, and approve the payments right away. | 38589 |
| General Application       | UX enhancements have been made to Statement Intelligence: <br /><ul><li>On the Bank Account Reconciliations page, the captions for the fields showing the number of lines created in the journals have been updated. A bold headline has been added.</li><li>On the Additional Information page, the currency fields are hidden if they are not relevant</li><li>The Additional Information field on the Bank Account  Reconciliation Line now shows if there's any additional information related to the line, and if so how many.</li></ul> | 38628 |
| Platform and Technology   | A solution has been implemented to deal with an issue where deprecated upgrades were executed. | 38632 |
| General Application       | Links to context-sensitive help pages have been added to the following pages: Bank Account Reconciliation, Statement Intelligence Setup, Payment Journal, and Payment Management Setup | 38635 |
| Country and Regional      | Notification emails are now available in Norwegian.          | 38735 |
| General Application       | Automatic IBAN lookup has been added when you enter an IBAN on either customer bank accounts or vendor bank accounts. | 38740 |
| Payment and Cash Receipts | A solution has been implemented to ensure that the Applied Amount is calculated correctly on currency payments. | 38745 |
| Statement Intelligence    | The Journal Template Name fields on the Bank Account Card page are hidden if only one journal template type exists. | 38763 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| General Application       | The posting preview action in the purchase journal threw a runtime error when validation errors exist. This has now been fixed to show an error message instead. Two new options have been added to the Payment Management Setup to enable or disable the validation and the dynamic validation in the purchase journal. | 29589 |
| Statement Intelligence    | Validation on general bank reconciliation rules and reconciliation rules has been added to ensure that the entered G/L account numbers exist. | 32292 |
| Statement Intelligence    | Fixed an issue with Customer, Employee, and Vendor Reconciliation Rules that resulted in an incorrect match when using the search principle 'Exact'. | 34886 |
| General Application       | The previously used default sender reference was 19 characters. This could result in validation errors for some banks. Therefore the default sender reference has been changed to use the first 16 digits of the Transaction ID. Note that the default sender reference is only used if no template has been specified. | 34971 |
| Payment and Cash Receipts | Fixed an issue with merging the regulatory reporting codes when payment journal lines were summarized manually. | 38453 |

## Payment Management 2022 R1 Service Pack 2

*Released: June 13, 2022*  
*On-premises and online version: 4.2.0.0*  
*Supported Business Central version: 2022 Release Wave 1 (BC20)*

### New or changed functionality

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | A new feature has been added that can automatically handle reversals from direct debit in the bank account reconciliation. It's now possible to set up rules for automatic handling of different reversal codes on individual customers, and a reversal history has been added to sales invoices and customers. From the Role Center in the Payment Management activities, an overview of new reversals can be accessed. | 31321 |
| General Application       | Captions on the Bank Holiday Setup page have been changed from Move Backward/Forward to Move Before/After. | 31537 |
| Statement Intelligence    | The requirement for specifying the Bank Account Statement Import Format on bank accounts has been removed. | 32469 |
| Payment and Cash Receipts | A new event has been added for Suggest Vendor Payments allowing additional filters for vendor ledger entries in a payment suggestion. | 32472 |
| Payment and Cash Receipts | The Payment Discount Used field has been added to the payment journal to show whether the payment discount has been used. | 32593 |
| Payment and Cash Receipts | In the Payment Management Setup, in the Payment Method lookup, the recommended setting now shows SEPA if EUR is LCY and if it's a domestic payment. | 32605 |
| Statement Intelligence    | A solution has been implemented for the issue where the customer ledger entry related to a customer payment was not closed if a payment discount was applied. | 32657 |
| General Application       | On the customer card, a new field, Skip Direct Debit, has been added to make it possible to exclude the customer from a direct debit suggestion. | 32698 |
| Payment and Cash Receipts | It is now possible to apply multiple payment journal lines to the same entry. Validation has been added to ensure that the entry amount is not exceeded. | 34339 |
| General Application       | Added the ability to handle the same document type and ID ledger entries in the payment journal. An update to support this functionality has been added to suggestions, apply entries, and field validation. | 29445 |
| Payment and Cash Receipts | Added functionality to handle G-accounts on purchase and payments (NL). | 29449 |
| Payment and Cash Receipts | Added BC20 functionality to check the customer/vendor consolidated balance. | 31328 |
| Payment and Cash Receipts | Added support for payment notifications in the payment journal for customers and employees. | 32662 |
| Payment and Cash Receipts | Added validation of payment notifications.                   | 32669 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Statement Intelligence    | Added an action in the cash receipt journal that enables the user to fully apply a customer ledger entry if there is a difference in the amount. After posting the cash receipt journal, the user can move the difference to the general journal using the existing action Transfer to General Journal. | 23510 |
| Statement Intelligence    | Fixed an issue where the Applied Difference field in the cash receipt journal didn't show the correct amount in some scenarios. | 27448 |
| Payment and Cash Receipts | An issue with amount calculation when using Payment Discount Tolerance Date in Suggest Vendor Payments has been fixed. | 32490 |
| General Application       | Permission for the table CPM Pmt.  Notification Def. has been added to the CPM365 ACC. RECON permission set. | 32571 |
| General Application       | Added validation of bank system code value.                  | 32667 |
| Payment and Cash Receipts | Added the field Bank Country Code on the employee card that will be used when creating payments. | 34640 |
| Statement Intelligence    | Fixed an error check on Bank Acc.  Stmnt. Format on the bank card. | 34884 |
| General Application       | Fixed issue with Payment Method Lookup when account type is customer. | 34972 |

  

## Payment Management 2022 R1 Service Pack 1, hotfix 3
*Released: May 19, 2022*  
*Online version: 4.1.0.3*  
*Supported Business Central version: 2022 Release Wave 1 (BC20)*

### New or changed functionality

| Functional area         | Description                                                  | ID    |
| ----------------------- | ------------------------------------------------------------ | ----- |
| Platform and Technology | A new permission set, CPM365 BEXD ADMIN, has been added to give users direct permission to Bank Export Data. Users with this permission set can open pages related to bank export data and view all the data. Users without this permission will not be able to see the bank export data pages, but they will still be able to work with all functionality. | 32831 |

### Bug fixes

| Functional area           | Description                                                  | ID    |
| ------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts | Fixed an issue that could cause credit transfer registers to be inserted. An upgrade is included to ensure the creation of the missing registers. | 34672 |
| Platform and Technology   | The Internal property has been removed from Payment Entry due to a customer request. | 34983 |

  

## Payment Management 2022 R1, Service Pack 1

*Released: April 1, 2022*  
*On-premises and online version: 4.1.0.0*  
*Supported Business Central version: 2022 Release Wave 1 (BC20)*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts                                 | Payment Notification values have been removed from the purchase documents and vendor ledger entries. | 24367 |
| Platform and Technology                                   | Added the possibility to use an alternate endpoint for Continia Online was added (for development and support purposes). | 29817 |
| Payment and Cash Receipts                                 | Added support for customer payments in the payment journal.  | 30091 |
| General Application                                       | Added use of the balance account setup in the purchase journal. | 30415 |
| General Application                                       | Minor refactoring of the bank card to give users a better overview. | 31337 |
| Statement Intelligence                                    | Added default setting for showing all the fields in Bank Account Reconciliation. | 32330 |
| General Application                                       | Teaching tips added to Payment Journal.                      | 27511 |
| General Application                                       | Teaching tips added to Bank Card.                            | 29713 |
| General Application                                       | Teaching tips added to Cash Receipt Journal.                 | 29715 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Payment and Cash Receipts                                 | Added check for notification length according to bank system payment method. | 25731 |



## Payment Management 2022 R1, hotfix 2

*Released: March 23, 2022*  
*On-premises version: 4.0.0.2*

### Bug fixes

All features and bug fixes released for [Payment Management 3.1.0.5 and 3.3.0.6](@PM-161) are also included in Payment Management 4.0.0.2. The descriptions of these features and bug fixes are not repeated here.



## Payment Management 2022 R1, hotfix 1

*Released: March 8, 2022*  
*On-premises version: 4.0.0.1*

### Bug fixes

All features and bug fixes released for [Payment Management 3.0.0.3 to 3.3.0.4](@PM-161) are also included in Payment Management 4.0.0.1. The descriptions of these features and bug fixes are not repeated here.

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| General Application                                       | Fixed an issue that caused an error when renaming Bank Accounts for customers without Statement Intelligence. | 31720 |
| Platform and Technology                                   | Fixed bad parameter in Bank API Request causing issues when using Webservice integrations. | 31747 |

## Payment Management 2022 R1

*Released: March 1, 2022*  
*On-premises version: 4.0.0.0* 

### New or changed functionality

All features and bug fixes released for [Payment Management 3.0.0.1 to 3.3.0.2](@PM-161) are also included in Payment Management 4.0. The descriptions of these features and bug fixes are not repeated here.

| <span style="white-space: nowrap;">Functional area</span> | Description | ID  |
| --- | --- | --- |
| Payment and Cash Receipts | Added basic functionality for using Direct Debit with Payment Management. Available from Feature Management. Note that to use Direct Debit, you need a new license file. | 28809 |
| Platform and Technology | Support for Sparebank1 and other banks in Norway using Tietoevry for integration. | 28486 |
| Platform and Technology | Support for Barclays bank in UK | 29072 |
| Platform and Technology | Added option to share certificates and tokens used for bank communication between companies and banks. | 22261 |
| Statement Intelligence | Added the possibility to import multiple account statements into the same bank account reconciliation. | 21154 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| Statement Intelligence | Fixed an issue with using periods in import of multiple account statements. | 30307 |