---
title: Detailed Changelog for Continia Payment Management 2020 R2
description: Changelog containing an overview of all new updates, features and hotfixes for each version of Continia Payment Management 2020 R2
date: 23-02-2024
id: PM-52
lang: en
---

# Detailed Changelog for Continia Payment Management 2020 R2

This article lists all new updates, features, service packs, and hotfixes for Continia Payment Management 2020 R2.

{{include "pm-not-supported-warning"}}

## Payment Management 2020 R2 Service Pack 1

*Released: January 27, 2021*  
*Online version: 1.9.0.1*  
*On-premises version: 1.9.0.2* 

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description| ID|
| ---| --- | --- |
| General Application| Checks has been added to ensure the currency code is not assigned to journal lines or bank statement lines if the currency code on the Bank Account equals the LCY code of the company. | 21287 |
| General Application| Support for multiple bank systems added to the assisted bank account setup. If multiple bank systems are available for a bank, the user must select which bank system to use for the bank account. | 11645 |
| General Application| It is now possible to see what version of a given bank system setup is active in the system. The data is available on the Bank system card. | 18488 |
| Payment and Cash Receipts | Fixed bug in Update Posting Date from status.| 21622 |
| Payment and Cash Receipts | Fixed issue with the filter on status being disregarded when posting. | 21932 |
| Payment and Cash Receipts | Improvements to Payment Export to ensure "Exported To Payment File" is set properly. | 21998 |
| Payment and Cash Receipts | OCR reference type added to Sales and receivables setup for use with reports. | 22450 |
| Payment and Cash Receipts | Added option to specify if closed entries should be searched when matching Customer Ledger Entries in the Payment Receipt Journal. | 22499 |
| Payment and Cash Receipts | Added a setting to exclude credit memo when summarizing payments when using the suggest vendor payments action. A default for the setting can be set on the payment journal setup page. A new field on the vendor makes it possible to enable the excluding of credit memos when summarizing payments. The new setting includes the following options: Vendor Specific No All "Vendor specific" excludes credit memos based on the setting on the vendor. "No" does not exclude credit memos. "All" exclude all credit memos. | 20780 |
| Payment and Cash Receipts | When creating vendor payment suggestions it is now possible to exclude vendors with a negative balance. | 20783 |
| Payment and Cash Receipts | Improvements for the payment notification email. This involves that the vendor name is added to the subject line. Also, if there is no email or web address in the company information, the labels in the footer will not be shown | 19055 |
| Statement  Intelligence   | Better support for Vendor payments in Statement intelligence. It is now possible to set up Reconciliation Rules for vendors just as it always has been for customers. This will help recognize reconciliation lines that belong to vendor payments. Possibility to support reconciliation of payments created via SEPA Direct Debit or created outside of Business Central. This new feature makes it easier to create the payment journal lines based on the reconciliation lines and transfer them to the payment journal ready for posting, after which they will be automatically reconciled. | 20990 |
| Statement Intelligence| The Customer Reconciliation Rules has been deprecated and Account Reconciliation Rules is introduced to support  reconciliation suggestions for vendors. | 21134 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description| ID|
| --- | --- | --- |
| General Application| Standard sender reference definition template is now set.| 21709 |
| General Application| An issue has been fixed concerning a missing step in the vendor setup  tool leading to not being possible to choose payment methods or  change them. Also, a filter has been added to the vendor no. column in the  assisted setup tool. | 22226 |
| Payment and Cash Receipts | Fixed issue with validation of Cost Type Code.| 22154 |
| Payment and Cash Receipts | Fixed issue with Balance Account/Payment Method validation on Purchase Documents. | 22162 |
| Payment and Cash Receipts | Fixed issue concerning a blank test  email for email notifications. | 22210 |
| Payment and Cash Receipts | An option to disable customer search when importing payment receipts has been added. Default is now disabled. | 22253 |
| Payment and Cash Receipts | Fixed issue concerning blank amounts in payment receipt import. | 22274 |
| Payment and Cash Receipts | Fixed issue with currency adjustment for Bank Accounts in foreign currencies. | 22731 |

## Payment Management 2020 R2 - RTM

*Released: December 3, 2020*  
*Online version: 1.8.0.3*  
*On-premises version: 1.8.0.3* 

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description| ID|
| --- | --- | --- |
| General Application| The fields on Bank Export Data List Page has been rearranged to give a better overview of the most used fields. | 18741 |
| General Application| The Exchange Rate Setup page is made searchable from the client. | 19491 |
| General Application| Indentation of entries implemented on the Bank Export Data List Page to give the user a better overview of the relation  between header and line entries. Implemented a freeze column on the page making the most important fields visible when using the scroll bar. | 20238 |
| General Application| Actions added on the Bank Export Data page that enables a simple view with fewer fields visible and an advanced view with all the fields. | 20239 |
| General Application| The field "Text Encoding" is added to the Bank Card to enable setting a specific text encoding when creating the payment file. | 20570 |
| General Application| Alternate Address 2 field added to Vendor.| 20727 |
| Statement Intelligence | Differences in the symbols of transaction-IDs can now be handled. | 20966 |
| Statement Intelligence | The field "Customer Name" has been added to the Customer Ledger Entries Page used in the Bank Account Reconciliation. The field is visible if the setting  "Copy Customer Name to Entries" is enabled in the Sales & Receivables Setup. | 21015 |
| Statement Intelligence | A setting "Include Statement No. in journal description" has been added to the Payment Management Setup Page. The setting can be enabled if the Statement No. from the Bank Account Reconciliation must be included in the description of the journal lines created by Statement Intelligence. | 21016 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description| ID|
| --- | --- | --- |
| Payment and Cash Receipts | Fixed issue with permission error in cash receipt journal.| 21017 |
| Payment and Cash Receipts | A fix has been made so Applied Entry No. is not 0 in Credit Transfers. | 21105 |
| Payment and Cash Receipts | Fixed issue with table lock being set to late, potentially enabling double export. | 21125 |
| Payment and Cash Receipts | Created message to recipient if no entry is applied, and notifications are rebuild. | 21160 |
| Payment and Cash Receipts | The Payment discount date is now correctly moved and and added to lines made through 'Make Suggestions'. | 21201 |
| Payment and Cash Receipts | Fixed Dimension error when suggesting vendor payments.| 21885 |
| Payment and Cash Receipts | Fix run modal error caused by number series management when importing Payment receipts. | 21913 |
| Payment and Cash Receipts | When assigning the account no. on the cash receipt journal line with a customer no. an additional check is made to ensure the customer exists and is not blocked. When looking for customer ledger entries to apply the search is skipped if the document number found in a payment identification or notification is blank or zero. | 21952 |
| Payment and Cash Receipts | Fixed an issue with currency code and Amount LCY  when importing customer payments in FCY in the cash receipt journal. | 20314 |
| Statement Intelligence| Fixed a bug where a general journal line is posted where both the account and the balance account is of type Bank Account. The reconciliation reconciles the wrong Bank Account Reconciliation Line with the wrong Bank Account Ledger Entry. | 20602 |

