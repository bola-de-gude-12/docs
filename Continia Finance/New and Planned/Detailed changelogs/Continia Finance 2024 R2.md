---
title: Detailed Changelog for Continia Finance 2024 R2
description: Changelog containing an overview of all new updates, features, and hotfixes for Continia Finance 2024 R2.
date: 27-05-2025
id: CF-46
lang: en
---

# Detailed Changelog for Continia Finance 2024 R2

This article lists all new updates, features, service packs, and hot fixes for Continia Finance 2024 R2.

> [!TIP]
> As a Continia partner, you can be notified of new Continia Finance versions and service packs whenever we release them. To sign up for this service, go to [Receive a notification upon new Continia Finance releases](https://continia.zendesk.com/hc/en-us/articles/21777523738386-Receive-a-notification-upon-new-Continia-Finance-releases) in the Continia PartnerZone (only available to partners).

## Continia Finance 2024 R2, Service Pack 1, hotfix 1
*Release date, online: April 8, 2025*  
*App version: 25.1.1*

### Bug Fixes

| Functional Area | Description | ID |
| --- | --- | --- |
| General Application | The **Open G/L Accounts** page's **Apply Partial Payment** function previously did not operate correctly. This issue has been resolved. Now, when you use the **Apply Partial Payment** function, the system accurately calculates and sets the balancing amount in the **Amount to Apply** column, ensuring correct partial payment application. | 64917 |
| General Application | The issue where installment plan lines could not be deleted in the **General Journals**, **Sales Journals**, and **Purchase Journals** pages has been resolved. This problem occurred when the **Enable Data Check** option was activated in the **General Ledger Setup**. | 65490 |
| General Application | In the on-premises version, new functionality in the Installments module incorrectly triggered a license check. This issue caused customers who did not have the Installments module to encounter a license error. This has now been resolved, ensuring that the license check is not performed for customers without the Installments module. | 65671 |

## Continia Finance 2024 R2, Service Pack 1
*Release date, online: March 8, 2025*  
*App version: 25.1.0*

### New or Changed Functionality

| Functional Area | Description | ID |
| --- | --- | --- |
| General Application | The Factoring module known from OPplus is now available in Continia Finance. | 52604 |
| General Application | The functionality for handling full installments has been integrated into **General Journals**, **Sales Journals**, and **Purchase Journals**. This enhancement allows users to efficiently manage installment payments directly within these journal entries. Users can now specify installment terms and schedules, ensuring accurate tracking and processing of installment-based transactions. This update streamlines the financial management process by providing a comprehensive solution for handling installment payments across various journal types. | 53663 |
| General Application | The Dutch translations have been reviewed, and many missing translations have been added. | 63668 |

### Bug Fixes

| Functional Area | Description | ID |
| --- | --- | --- |
| General Application | Whenever an attempt was made to retrieve the **Master Account No.** of an association within the Finance/Banking Connector app, an error occurred. This issue has now been resolved, ensuring that the **Master Account No.** can be successfully obtained without errors. | 60353 |

## Continia Finance 2024 R2, hotfix 8
*Release date, online: February 25, 2025*  
*App version: 25.0.8*

### New or Changed Functionality

| Functional Area | Description | ID |
| --- | --- | --- |
| General Application | The Dutch translations have been reviewed, and many missing translations have been added. | 63668 |

### Bug Fixes

| Functional Area | Description | ID |
| --- | --- | --- |
| General Application | When creating a new row definition, if you select **Insert** > **Insert Account Groups** and choose your account groups, the **Totaling Type** column was incorrectly populated with *Posting Accounts* instead of the expected *G/L Account Group*. This issue has now been resolved, ensuring that the **Totaling Type** column correctly reflects the selected account groups. | 63501 |

## Continia Finance 2024 R2, hotfix 7
*Release date, online: February 11, 2025*  
*App version: 25.0.7*

### New or changed functionality

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| General Application | Made an app available that uses US terms, for exampe 'sales tax' instead of 'VAT'. |      |

## Continia Finance 2024 R2, hotfix 6
*Release date, online: February 6, 2025*  
*App version: 25.0.6*

### Bug fixes

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| General Application | Usage of standard Business Central function "Find Entries" with activated Continia Finance module "Open G/L Entries" and having installed certain Australia localization apps could rise the error: "The record in table Document Entry already exists. Identification fields and values: Entry No .= ...". Fixed in version 25.0.6. | 62571     |

## Continia Finance 2024 R2, hotfix 5
*Release date, online: January 23, 2025*  
*App version: 25.0.5*

### Bug fixes

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| General Application | <ul><li>Fixed issues with customer/vendor balance confirmations batch emailing using "Send all Balance Confirmations" from customer/vendor list: errors about missing references, emails with empty reports, wrong balance confirmation setup usage</li><li>General batch/single email sending usability improvements: added statuses and messages that corresponds to actual outcome - i.e. it is no more gives messages that email is send then user decided cancel emailing or there is nothing to send.</li><li>Function "Send all Balance Confirmations" uses customer/vendor list page view and send emails only for customers/vendors that are filtered.</li><li>During the product activation following setup is created automatically: email profiles, report selection, default balance confirmation code. It enables to start using balance confirmation emailing with minimal effort.</li></ul> | 62527     |

## Continia Finance 2024 R2, hotfix 4
*Release date, online: November 29, 2024*  
*App version: 25.0.4*

### New or changed functionality

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| General Application | A new field in the customer table "Settle with linked Vendor" is made available on the customer card.  It can be left empty, set to "Yes" or to "No". This field can be used as a filter criteria e.g. when creating a payment proposal in Continia Banking when the option "Settle with Vendor Entries" is selected. | 61438     |
| General Application | In the G/L Setup, the VAT Setup and the User Setup new date formula fields are added to simpify the Posting Allowed From and Posting Allowed To functionality of Standard BC. With these fields it is possible to setup this formulas once and therefor it is not needed to renew the "Allow From" and "Allow To" fields each month. | 61440     |
| General Application | A new field has been added which specifies the fields to be checked, if the Check VAT Key field is enabled. If no specification is select the following fields are checked: Gen. Posting Type Gen. Business Group Gen. Product Group VAT Business Group VAT Product Group IF VAT Posting Groups is selected the following fields are checked: VAT Business Group VAT Product Group IF General Posting Groups is selected the following fields are checked: Gen. Business Group Gen. Product Group If a specific field is selected only this field is checked. | 61441    |
| General Application | The VAT Key Code field has been integrated to the VAT Statement lines. So the VAT Key Code can be used to review the VAT Statements easier. | 61442     |

## Continia Finance 2024 R2, hotfix 3
*Release date, online: November 25, 2024*  
*App version: 25.0.3*

### New or changed functionality

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| General Application | If the field "Adjust for Payment Disc." is activated in the General Ledger Setup the system will  recalculate tax amounts when you post payments that trigger payment discounts. For that functionality a new field has been created in the Essentials Setup: "Use Invoice Dimensions for Pmt. Discount". It specifies whether the dimensions of the payment discount entries should be according to the dimensions of the paid invoices. | 58702     |
| General Application | The possibility of using G/L Account groups in Financial Reports has been extended with four more account groups. The Fields are G/L Account Group 5, G/L Account Group 6, G/L Account Group 7 and G/L Account Group 8. The G/L Accounts Group 3 - 8 in the G/L Account list or the Chart of Accounts are only visible, if a caption for these groups is provided in the Extended Financial Reports Setup. | 58851     |
| General Application | The demo Data for US had been updated. | 61058    |
| General Application | 4 more fields to edit G/L Account Groups have been added into G/L Accounts. The groups can be evaulated in Financial Reports. The fields are only visible in the G/L Account List if a caption is provided for the new G/L Account Groups. | 61130    |
| General Application | The Demo data for US and UK have been refreshed. | 61479     |
| General Application | If applying customer or vender ledger entries and the extended application mode is activated, the payment might be splitted into payments of several customers or customers and vendors. The lines, which are created by the system might have a positive or negative amount. Both signs are allowed for these general journal lines, created by the system. | 61668     |

### Bug fixes

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| General Application | When Continia Finance is installed in a Sandbox or a live environment the assisted setup of the Essentials module failed if no manual setup has been done before. | 61472     |

## Continia Finance 2024 R2, hotfix 2
*Release date, online: October 29, 2024*  
*App version: 25.0.2*

### New or changed functionality

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| General Application | A link to Continia Hub was integrated to all Setup Pages. When using Continia Hub a content specific link is available. | 50259     |
| General Application | The Demo Portal now is available with Demo Data for Australia and New Zealand with the specific Demo Data. | 58544     |
| General Application | If installing Continia Finance in the Demo Portal the company Continia Finance Demo was not created automatically. | 60249    |

### Bug fixes

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| General Application | The Factbox for Vendor Ledger Entries has been aligned to Customer Ledger Entries Factbox if Multiple Pmt. Discount Entries exist. | 60708     |

## Continia Finance 2024 R2, hotfix 1
*Release date, online: October 7, 2024*  
*App version: 25.0.1*

### Bug fixes

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| General Application | Getting the Master Account No. of an Association failed in the Finance / Banking Connector app. | 60353     |

## Continia Finance 2024 R2

*Release date, online: October 4, 2024*  
*App version: 25.0.0*

### New or changed functionality

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| General Application | Continia Finance has been released for BC v23, BC v24, and BC v25 – including [localizations for AT, AU, CH, DE, DK, GB, and NZ](@CF-128). For more information, see [Business Functionality](@CF-01). | N/A     |

### Bug fixes

| **Functional Area** | **Description**                                              | **ID** |
| ------------------- | ------------------------------------------------------------ | ------ |
| General Application | Incorrect posting of installment when using multiple posting groups was corrected. Now the posting group for installement entries uses the original ledger entry. | 55267     |

<style>
 .content table tr td:nth-child(1),
 .content table tr td:last-child {
  width: 210px;
 }

 .content table tr td:last-child {
  width: 75px;
 }
</style>