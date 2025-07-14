---
title: Continia Finance permissions
description: Information about Continia Finance permissions.
date: 13-05-2025
id: CF-16
lang: en
---

# Continia Finance Permissions

To use Continia Finance, assign one or more permission sets (also called roles) to each user. These permission sets grant access to features and enable users to complete specific tasks. Continia provides several predefined permission sets, each designed for a specific purpose. You can also create custom permission sets if needed, or add users to a security group that already includes the required permission sets. For more information, see [Assign permissions to users and groups](https://learn.microsoft.com/en-us/dynamics365/business-central/ui-define-granular-permissions) (Microsoft Learn article).

> [!NOTE]
> Make sure to assign the necessary Microsoft Dynamics 365 Business Central permission sets, along with the Continia ones, to make sure that all features function correctly.

## Standard Continia permission sets

| <div style="width:150px">Permission set</div> | Description |
| --- | --- |
| CSC BASIC | It is mandatory for all Business Central users to have the CSC BASIC permission set to ensure that all standard features work as intended. This includes users who do not use Continia Products directly, as they still need certain permissions to access and run objects that may interfere with the standard Business Central code. The permission set also enables you to obtain the Continia Products activation status. It is similar to the standard Dynamics NAV/Business Central BASIC permission set. |
| CSC APP SETUP | This permission set allows you to activate Continia products, including Continia Core. It is mainly used for product installation and, in Business Central online, when making changes to subscription agreements, such as selecting and deselecting subscribed modules. |

## Continia Finance-specific permission sets

| <div style="width:150px">Permission set</div> | Description |
| --- | --- |
| CTS-CFI ALL | To ensure that all standard features work as intended, the CTS-CFI ALL permission set is mandatory for all Business Central users, including those who don't use Continia Finance directly, as they still need certain permissions to access and run objects that somehow interfere with the standard Business Central code. The permission set is similar to the standard Business Central BASIC permission set. |
| CTS-CFI CVL, READ | This permission set is mandatory for all users who want to retrieve information about customer or vendor associations or about linked customers and vendors. |
| CTS-CFI CVL, SETUP | This permission set is mandatory for all users who want to create or modify the setup of the associations module. |
| CTS-CFI CVL, USE | This permission set is mandatory for all users who want to create or modify customer or vendor associations or linked customers and vendors. |
| CTS-CFI EFR, READ | This permission set is mandatory for all users who want to use the Extended Financial Reports module without modifying data. |
| CTS-CFI EFR, SETUP | This permission set is mandatory for all users who want to create or modify the setup of the Extended Financial Reports module. |
| CTS-CFI EFR, USE | This permission set is mandatory for all users who want to use the Extended Financial Reports module and modify data, such as account groups. |
| CTS-CFI FA, READ | This permission set is mandatory for all users who want to use the Extended Fixed Assets module without modifying data. |
| CTS-CFI FA, SETUP | This permission set is mandatory for all users who want to create or modify the setup of the Extended Fixed Assets module. |
| CTS-CFI FA, USE | This permission set is mandatory for all users who want to use the Extended Fixed Assets module and modify data, such as Fixed Asset templates. |
| CTS-CFI GLOE, READ | This permission set is mandatory for all users who want to use the G/L Open Entries module without modifying data. |
| CTS-CFI GLOE, SETUP | This permission set is mandatory for all users who want to create or modify the setup of the G/L Open Entries module. |
| CTS-CFI GLOE, USE | This permission set is mandatory for all users who want to use the G/L Open Entries and modify data, such as G/L Detailed entries. |
| CTS-CFI INS, READ | This permission set is mandatory for all users who want to use the Installment module without modifying data. |
| CTS-CFI INS, SETUP | This permission set is mandatory for all users who want to create or modify the setup of the Installments module. |
| CTS-CFI INS, USE | This permission set is mandatory for all users who want to use the Installment module and modify data, such as Installment templates. |
| CTS-CFI MLPD, READ | This permission set is mandatory for all users who want to use the Multi-Level Payment Discounts module without modifying data. |
| CTS-CFI MLPD, SETUP | This permission set is mandatory for all users who want to create or modify the setup of the Multi-Level Payment Discounts module. |
| CTS-CFI MLPD, USE | This permission set is mandatory for all users who want to use the Multi-Level Payment Discounts module and modify data, such as Multi-Level Payment entries. |
| CTS-CFI TRE, READ | This permission set is mandatory for all users who want to use the Treasury module without modifying data. |
| CTS-CFI TRE, SETUP | This permission set is mandatory for all users who want to create or modify the setup of the Treasury module. |
| CTS-CFI TRE, USE | This permission set is mandatory for all users who want to use the Treasury module and modify data, such as Treasury Bank accounts, Treasury accounts and Treasury Open entries. |





<style>
  .content table tr td:nth-child(1) {
    width: 90px;
  }
  .content table tr td:nth-child(2) {
    width: 640px;
  }  
</style>
