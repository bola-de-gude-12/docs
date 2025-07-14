---
title: Detailed Changelog for Continia Finance 2025 R1
description: Changelog containing an overview of all new updates, features, and hotfixes for Continia Finance 2025 R1.
date: 27-05-2025
id: CF-142
lang: en
---

# Detailed Changelog for Continia Finance 2025 R1

This article lists all new updates, features, service packs, and hotfixes for Continia Finance 2025 R1.

> [!TIP]
> As a Continia partner, you can be notified of new Continia Finance versions and service packs whenever we release them. To sign up for this service, go to [Receive a notification upon new Continia Finance releases](https://continia.zendesk.com/hc/en-us/articles/21777523738386-Receive-a-notification-upon-new-Continia-Finance-releases) in the Continia PartnerZone (only available to partners).

## Continia Finance 2025 R1, Service Pack 1

*Release date, online: May 19, 2025*  
*App version: 26.1.0*

### Bug Fixes

| Functional Area | Description | ID |
| --- | --- | --- |
| General Application | An issue has been resolved on the customer/vendor application page where additional and misleading lines appeared when multiple lines shared the same document number. This issue has been addressed to ensure accurate line display. <br><br> Additionally, a problem was fixed where extra empty lines appeared when the application selection was initiated without selecting any lines to apply. This ensures that only relevant lines are displayed during the application process. | 64411 |
| General Application | When account groups were used in financial reports, the account schedule calculation did not adhere to the **Show Opposite Sign** setting in the row definition. This issue has been resolved, ensuring that the account schedule calculation now correctly reflects the **Show Opposite Sign** configuration when account groups are utilized. | 64799 |
| General Application | On the **Open G/L Accounts** page, it wasn't possible to manually edit or enter amounts in the **Amount to Apply** column. The visibility and editability of this column has now been fixed. | 64915 |
| General Application | Additional data is now accessible in the FactBox, providing users with enhanced financial insights. To activate this feature, navigate to **Extended Financial Reports Setup** > **Ledger Entry Views** and enable the **Show Extended Data Factbox** option. This enhancement allows users to view more comprehensive data directly within the FactBox, improving the analysis and decision-making process. | 64916 |
| General Application | Whenever the **Customer Open Entries** report was printed, every second page appeared blank. This issue has now been resolved, ensuring that all pages of the report display the correct information without any blank pages. | 64947 |

## Continia Finance 2025 R1, hotfix 2

*Release date, online: April 22, 2025*  
*App version: 26.0.2*

### Bug Fixes

| Functional Area | Description | ID |
| --- | --- | --- |
| General Application | The **Open G/L Accounts** page's **Apply Partial Payment** function previously did not operate correctly. This issue has been resolved. Now, when you use the **Apply Partial Payment** function, the system accurately calculates and sets the balancing amount in the **Amount to Apply** column, ensuring correct partial payment application. | 64917 |
| General Application | The issue where installment plan lines could not be deleted in the **General Journals**, **Sales Journals**, and **Purchase Journals** pages has been resolved. This problem occurred when the **Enable Data Check** option was activated in the **General Ledger Setup**. | 65490 |
| General Application | In the on-premises version, new functionality in the Installments module incorrectly triggered a license check. This issue caused customers who did not have the Installments module to encounter a license error. This has now been resolved, ensuring that the license check is not performed for customers without the Installments module. | 65671 |

## Continia Finance 2025 R1, hotfix 1

*Release date, online: April 8, 2025*  
*App version: 26.0.1*

Internal release.

## Continia Finance 2025 R1

*Release date, online: March 25, 2024*  
*App version: 26.0.0*

### New or Changed Functionality

| Functional Area | Description | ID |
| --- | --- | --- |
| General Application | The Factoring module known from OPplus is now available in Continia Finance. | 52604 |
| General Application | The functionality for handling full installments has been integrated into **General Journals**, **Sales Journals**, and **Purchase Journals**. This enhancement allows users to efficiently manage installment payments directly within these journal entries. Users can now specify installment terms and schedules, ensuring accurate tracking and processing of installment-based transactions. This update streamlines the financial management process by providing a comprehensive solution for handling installment payments across various journal types. | 53663 |
| General Application | The Dutch translations have been reviewed, and many missing translations have been added. | 63668 |
| General Application | Continia Finance is now supported in English in Norway, Sweden, Finland, and Belgium | 64376 |
| General Application | Continia Finance is now supported in the United States and Canada. |  |


<style>
 .content table tr td:nth-child(1),
 .content table tr td:last-child {
  width: 210px;
 }

 .content table tr td:last-child {
  width: 75px;
 }
</style>