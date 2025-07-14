---
title: Detailed Changelog for Continia Payment Management 2021 R1
description: Changelog containing an overview of all new updates, features and hotfixes for Continia Payment Management 2021 R1
date: 24-09-2021
id: PM-51
lang: en
---

# Detailed Changelog for Continia Payment Management 2021 R1

This article lists all new updates, features, service packs and hotfixes for Continia Payment Management 2021 R1.

## Payment Management 2021 R1 Service Pack 3, hotfix 6

*Released: September 27, 2021*  
*Online version: 2.3.0.6*

### Bug fixes
| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Fixed issue where Regulatory Reporting Codes caused insert error on Purchase Documents. | 27195 |
| Payment and Cash Receipts | Added indirect permission Vendor Ledger Entries in codeunit used by Suggest Vendor Payments. | 27851 |
| Platform and Technology | Fixed issue where files potentially would not get inserted into the file archive when importing large amounts of files. | 28166 |
| Platform and Technology | Added log for File conversion | 28168 |

## Payment Management 2021 R1 Service Pack 3, hotfix 4

*Released: September 15, 2021*  
*Online version: 2.3.0.4*

### Bug fixes
| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Fixed issue with fields being cleared after running Bank Account Setup. | 27682 |
| Payment and Cash Receipts | Fixed issue causing error when opening payment journals in companies that have not been activated. | 27708 |
| Statement Intelligence | When changing statement no. the notifications on the bank account reconciliation lines are no longer disappearing. | 27067 |
| Statement Intelligence | Fixed issue with overflow for KID filter in bank account reconciliation. | 27683 |

## Payment Management 2021 R1 Service Pack 3, hotfix 3

*Released: September 1, 2021*  
*Online version: 2.3.0.3*

### Bug fixes
| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Fixed minor issue in Bank Account  Setup causing error due to missing Bank System code. | 27059 |
| General Application | Fixes error in Vendor Information Setup if BTI  payment method territory mapping does not exist. | 27137 |
| Payment and Cash Receipts | Fixed issue with potentially getting wrong group status. | 27176 |
| Payment and Cash Receipts | Fixed missing Application for credit memos in some cases when summarizing payments. | 27401 |
| Statement Intelligence | Fixed issue with blank notification lines. | 27063 |
| Statement Intelligence | When changing statement no. the notifications on the bank account reconciliation lines are no longer disappearing. | 27067 |




## Payment Management 2021 R1 Service Pack 3, hotfix 2

*Released: August 16, 2021*  
*Online and on-premises version: 2.3.0.2*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Fixed issue with missing permission sets. | 26888 |
| Platform and Technology | Minor fix to Import Access Token, resulting in Remaining Time Valid not being entered. | 26896 |



## Payment Management 2021 R1 Service Pack 3

*Released: August 6, 2021*  
*Online version: 2.3.0.0*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| Country and Regional | It is now possible to make direct payments and direct import of files through Bizcuit in the Netherlands. | 25412 |
| General  Application | When choosing which file to import  from list, it is now possible to change the selection if pressing no to the confirm. | 23642 |
| General Application | Confirmation dialogs for fields Use Exchange Rate Adjustment and Allow update posting date removed on the Payment Management Setup page. | 26757 |
| Payment and  Cash Receipts | Support for batch payments in DNB. | 20791 |
| Payment and Cash Receipts | Fixed an error when using the "Preview Posting" action in the payment journal causing e-mail notifications to be sent. | 26737 |
| Statement  Intelligence | Payment Reference rules on the bank  now also looks for a match on External Document No. on Customer ledger entries and Vendor ledger entries. | 24933 |
| Statement Intelligence | When using "Manual Selection" method to import account statements, only statements relevant for the selected bank is shown. | 25531 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Fixed an error in the Purchase Journal that caused the validation errors to be deleted in some scenarios. | 26536 |
| General Application | Fixed a bug when trying to disable Statement Intelligence on the  Payment Management Setup page. | 26759 |
| General Application | Fixed a permission error when trying to merge lines manually in the Bank Account Reconciliation. | 26801 |
| General Application | Code for deleting Regulatory Reporting Codes changed so it only executes if the journal is of type Purchase or Payment. | 26850 |



## Payment Management 2021 R1 Service Pack 2, hotfix 2

*Released: July 5, 2021*  
*Online and on-premises version: 2.2.0.2*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID    |
| --- | --- | --- |
| Payment  and Cash Receipts | Added support for Regulatory reporting on Purchase documents-/Journals and Payment Journal. | 25542 |
| Payment and Cash Receipts | Changed  Filter fields to reflect CPM Payment Method Code. | 26112 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Fixed issue with certificate tags not being removed form Status files from BankData. | 25954 |
| General Application | Fixed issue with Unique Company Code not being set correct. | 26484 |
| General Application | Fixed permission error when posting std. journals without PM permissions. | 26103 |
| General Application | Upgrade codeunit for 1.9.0.0 refactored for performance improvement. | 26139 |
| General Application | Added previously removed procedure causing BC upgrade error. | 26466 |
| Payment and Cash Receipts | Added additional check on existing Credit Transfer Entries to ensure that the  TransactionID does not already exist. | 26465 |
| Platform and Technology | Fixed error in certificate update. | 26482 |
| Statement Intelligence | "Don't search for Vendor" added | 26436 |
| Statement Intelligence | Fixed issue with leftover Difference lines in Statement Intelligence, causing posting of Diff. Gen. Jnl. Lines to fail. | 26059 |



## Payment Management 2021 R1 Service Pack 2, hotfix 1

*Released: June 14, 2021*  
*Online and on-premises version: 2.2.0.1*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| Country  and Regional| Standard BC validation on Bank Account No. and Vendor Bank Account No. has been disabled. so leading zeros won't be added. <br />*Note - this is a country and  regional update that applies to: DK* | 25638 |
| General Application| Fixed Don't show again on Payment Journal notification.| 25868 |
| General Application| Fix  setExportFormat on bank table| 25837 |
| General Application| Finance que filter and activity tiles.| 25929 |
| General Application| User Id is no longer set when importing certificate from bank card. | 25835 |
| Payment and Cash Receipts | Fixed issue with Vendor Ledger entries potentially being locked causing Payment  Export to fail. | 25852 |
| Platform and Technology | Fixed permission error for Archived File.| 26010 |
| Statement  Intelligence| When using Customer/Vendor Reconciliation Rules to identify account statement lines and creating journal lines, Account No. will now be set on the Journal line. | 25557|
| Statement Intelligence| filter error in statement for () characters| 25644 |

## Payment Management 2021 R1 Service Pack 2

*Released: May 25, 2021*  
*Online and on-premises version: 2.2.0.0*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General  Application | Added new File Archive for files imported and exported from Payment Management 365. Improvements have been made to references between archive and Bank Export Data as well as improvements to ensure all files are imported correctly. | 21970 |
| General Application | On the Vendor Card page the fields Gen. Bus. Posting  Group, VAT Bus. Posting Group and Vendor Posting Group is promoted. When the Invoicing FastTab is collapsed the fields is shown in the header of the FastTab. | 12177 |
| General  Application | Enhancements to functionality  related to Bank Giro Account No. and Plus Giro Account No. It is now possible to set a relation between the company Bank Giro Account No. or Plus  Giro Account No. and a bank account. This can be done using two new actions  on the Company Information page. On the Bank Account Card page a field is  visible in the general group if a bank account is set as a Bank  Giro Account or Plus Giro Account. The field Bank/Plus Giro No. is added to the payment journal line. The field is assigned a value when using the suggest vendor payments action. The value is taken from the company information if the bank account on the journal line is set as a Bank Giro or Plus Giro Bank Account. <br />*Note - this is a country and regional update that applies to: SE.* | 24832 |
| General Application | Added notification for notifying user if a setup update is required after updating the product. The user can initialize updating the setups from the notification. Validation will only be updated if necessary. | 25451 |
| Payment and  Cash Receipts | Functionality added to the Cash Receipt Journal to be able to setup Customer Application Rules. The functionality can be enabled in feature management. | 20434 |
| Platform and Technology    | Support for direct communication for DNB bank in Norway. | 24151 |
| Statement Intelligence | Added action to mark multiple lines for Manual handling. | 25222 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General  Application | Fixed an issue with visibility of page controls on Payment Management 365 journals in DK,NO and SE  localizations. <br />*Note - this is a country and regional update that applies to: DK, NO, SE.* | 24796 |
| General Application | Fixed issue where new Payment Reference templates could not be  created from Vendor and Purchase Documents. | 25103 |
| General Application | Fixed issue with Bank Export Data  text used for notifications in imported files, not being shared across companies. | 25443 |
| Payment and Cash Receipts | The field Bank/Plus Giro No. has been added to the  Purchase Journal and the related payment validation in the journal. <br />*Note - this is a country and regional update that applies to: SE.* | 24798 |
| Payment and  Cash Receipts | Vendor Bank/Plus giro field added  to Payment Journal. <br />*Note - this is a country and regional update that applies to: SE.* | 24833 |
| Statement Intelligence | When selecting bank account statements manually, empty statements are  now gone. | 24083 |
| Statement  Intelligence | Error has been corrected to handle currency code | 24666 |

## Payment Management 2021 R1 Service Pack 1, hotfix 1

*Released: April 21, 2021*  
*Online and on-premises version: 2.1.0.1*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| Payment and Cash Receipts | Added support for Nordea Camt.054.001.02C files. | 24849 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Fixed issue regarding modifying permissions for entries due to changes in standard  permissions in BC18 on-premises. | 24976 |
| General Application | Added fix for Cost Type Code not being set to InitValue by Microsoft when validating payments. | 24979 |
| General Application | Fixed issue in the Payment Management on-premises version, so that it is now to be shown in Solution Management for Business Central on-premises. | 24993 |

## Payment Management 2021 R1 Service Pack 1

*Released: April 06, 2021*  
*Online and on-premises version: 2.1.0.0*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application| Support of KID in the Purchase Journal Validation. | 23371 |
| General  Application | Added filter so Sender reference can not be added to vendors, purchase documents or payment methods. | 24396 |
| General  Application | Removed need for VAT no. when communicating with Continia Online. | 24605 |
| General Application | With Payment Management 2021 R1 (2.1.0.0), we have released Payment Management for Microsoft Dynamics 365 Business Central 2021 release wave 1 (BC18). |       |
| Payment and Cash Receipts | Support of KID reference when importing payments in the Cash Receipt Journal. | 23911 |
| Statement Intelligence | Support for KID in the Bank Account Reconciliation. | 23924 |
| Statement Intelligence | Added new action to view all Bank Export Data for the file imported to a Bank Account Reconciliation. | 24262 |

###Country and regional

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| Country and regional | SE localization added to Payment Management | 11336 |
| Country and regional | NO localization added to Payment Management | 11337 |
| Country and regional | NL localization added to Payment Management | 20671 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General  Application | Fixed issue with deleting vendor if Creditor No. had been entered. | 24171 |
| General  Application | Fixed issue with "Direct" flowfield on Bank Account card. | 24261 |
| General  Application | Fixed issue with Payment Method Assisted setup if no SEPA payment method exist. | 24355 |
| General  Application | Fixed issue with installing Migration App for OnPrem 16.4. | 24587 |
| General  Application | Fixed issue with validations not being deleted in Setup Import. Added reinitialization of validation on setup import. | 24591 |
| General  Application | Fixed issue with Cost Type Code not being set on purchase documents. | 24457 |
| General  Application | Fixed issue with "drilldown" no longer working in wizards in BC18. | 24626 |
| General  Application | Fixed issue with Bank Export Data being reimported with "Allow file reimport" set to false, causing Bank Export Data Text blocking import. | 24663 |
| General  Application | Fixed issue when searching for the payment method assisted setup. | 24766 |
| Payment  and Cash Receipts | Fixed issue with BCC mail not being used in Email Notification. | 24197 |
| Payment  and Cash Receipts | Fixed issue with sending Email notifications. | 24259 |
| Payment  and Cash Receipts | Fixed issue with fixed text be added twice to payment notifications. | 24375 |
| Payment  and Cash Receipts | Fixed issue with Group Message description for Payment Status | 24583 |
| Payment  and Cash Receipts | Fixed issue with Purchase Journal lines being posted to Bank Account. | 24700 |
| Statement  Intelligence | Fixed issue with possibly matching reversed Bank Account Ledger Entries. | 24064 |
| Statement  Intelligence | Added check for illegal filter characters when reconciling account statements. | 24161 |

## Payment Management 2021 R1, hotfix 2

*Released: March 25, 2021*  
*Online version: 1.10.0.2*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Fixed issue with validations not being deleted in Setup Import. Added reinitialization of validation on setup import. | 24591 |
| General Application | Fixed issue with Bank Export Data being reimported with "Allow file reimport" set to false, causing Bank Export Data Text blocking import. | 24663 |
| Payment and Cash Receipts | Fixed issue with Purchase Journal lines being posted to Bank Account. | 24700 |

## Payment Management 2021 R1, hotfix 1

*Released: March 19, 2021*  
*Online version: 1.10.0.1*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Added filter so Sender reference can not be added to vendors, purchase documents or payment methods. | 24396 |
| Statement Intelligence | Added check for illegal filter characters when reconciling account statements. | 24161 |
| Statement Intelligence | Added new action to view all Bank Export Data for the file imported to a Bank Account Reconciliation. | 24262 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Fixed issue with deleting vendor if Creditor No. had been entered. | 24171 |
| General Application | Fixed issue with "Direct" flowfield on Bank Account card. | 24261 |
| General Application | Fixed issue with Payment Method Assisted setup if no SEPA payment method exist. | 24355 |
| General Application | Fixed issue with Cost Type Code not being set on purchase documents. | 24457 |
| Payment and Cash Receipts | Fixed issue with BCC mail not being used in Email Notification. | 24197 |
| Payment and Cash Receipts | Fixed issue with sending Email notifications. | 24259 |
| Payment and Cash Receipts | Fixed issue with fixed text be added twice to payment notifications. | 24375 |
| Payment and Cash Receipts | Fixed issue with Group Message description for Payment Status | 24583 |
| Statement Intelligence | Fixed issue with possibly matching reversed Bank Account Ledger Entries. | 24064 |

## Payment Management 2021 R1

*Released: March 1, 2021*  
*Online version: 1.10.0.0*  
*On-premises version: 2.0.0.0* 

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID  |
| --- | --- | --- |
| General Application | The purchase journal now supports payment validation. The functionality can be enabled from the Continia Feature Management page. | 11984 |
| General Application | Various visual improvements throughout the product. Simplified  view of Payment Management Setup. New Manual Setups added. Welcome page and Wizard overview removed and replaced with standard Assisted Setup  page. New troubleshoot page added. Vendor information setup redesigned. | 22914 |
| General Application | Documentation on Continia Docs of the OCR Reference interface is updated with more information about  how to use it. | 21362 |
| General Application | An option to deactivate the generation of a Payment Reference has been added to the Payment Management 365 Setup. | 22502 |
| General Application | Improvement to notification email validation. | 22195 |
| General Application | Enhanced the user experience in the Payment Journal when the Payment Notification Setup is not setup. The user is now presented with an option to open the page directly. | 23982 |
| Payment and  Cash Receipts | Added possibility to edit some fields in the Payment Journal after the payment has been exported. | 22814 |
| Payment and Cash Receipts  | Added handling of Bank Holidays when suggesting vendor payments. | 23069 |
| Payment and  Cash Receipts | Added Publisher in Payment Export to allow checking for Approval Entries. | 23893 |
| Payment and Cash Receipts  | Added possibility to edit some fields in the payment journal after payments have been exported. | 22664 |
| Payment and  Cash Receipts | Added handling KID to Payment Type Validation in order to support KID payments. | 23446 |
| Platform and Technology | Added performance improvements to validation, including an option to disable dynamic validation on purchase documents and in the payment journal. | 22799 |
| Platform and  Technology   | Performance improvements on keys. | 23612 |
| Statement Intelligence | Added new option for importing account statements by statement date or selecting from a list of available statements. | 22667 |
| Statement  Intelligence | Added new shortcuts to Gen. Journal and Cash receipt journal. | 21029 |
| Statement Intelligence | When using the action "Transfer Diff. To General Journal" on the Bank Account Reconciliation page the created lines now includes the statement no. if enabled on the Payment Management Setup. | 21823 |
| Statement  Intelligence | Action to delete and mark Bank Account Reconciliation Lines as imported is added to the Bank Account Reconciliation page. | 22364 |
| Statement Intelligence | Improved the creation of lines in the Cash Receipt Journal and Payment Journal. | 22945 |
| Statement Intelligence | Added camt.053 extended to import. | 23795 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | More simple error message in bank account setup. | 23005 |
| General Application | Added validation to remove spaces from IBAN to avoid errors. | 23394 |
| General  Application| Fixed issue with Bank Statement Import Format not being set on Bank Account in the assisted setup. | 23395 |
| General Application| Fixed issue with payment journal setup not being initialized on bank account setup. | 23397 |
| General  Application| Fixed issue with bank holidays not being imported for en-US region. | 23422 |
| General Application| Fixed issue with missing Cost Type Code Validation on Purchase Documents. | 23686 |
| General  Application| Fixes possible issue when importing Currency exchange rates from foreign service. | 23733 |
| General Application| Fixed issue where Handle Bank Holidays could not be reset.| 23976 |
| Payment and  Cash Receipts | Fixed bug when summarizing  payments that contain more than 1 dimension. | 23300 |
| Payment and Cash Receipts| Fixed an issue potentially causing vendor ledger entries not being set as exported. | 23752 |
| Payment and  Cash Receipts | Fixed minor issue with payment journal lines not being added due to balance account issue. | 23818 |
| Statement Intelligence| Fixed an issue when using the action "Ledger Entry" on the Reconciliation Suggestion page. The Customer Ledger Entry page was opened with an empty filter if the reconciliation suggestion belonged to a Vendor Ledger Entry. | 22988 |