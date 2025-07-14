---
title: Payment Management permissions
description: Information about payment management permissions.
date: 03-05-2022
id: PM-16
lang: en
---

# Payment Management Permissions

For users to work with Continia Payment Management, they must be assigned one or more permission sets (also known as "roles") that provide them with the permissions they need. There are several different predefined permission sets, each of which includes a number of permissions that grant access to certain features and enable users to carry out various tasks.

Users can also be granted the relevant permissions by becoming a member of a user group that has the relevant permissions. For more information, see [Assigning permissions to users and user groups](#assigning-permissions-to-users-and-user-groups).

> [!NOTE]
>
> In addition to the Continia permission sets mentioned in this article, you must also be assigned the standard Microsoft Dynamics 365 Business Central permission sets in order for all permitted operations to work as intended.



## Standard Continia permission sets

| Permission set | Description |
| --- | --- |
| CSC BASIC | This permission set grants users access to all Continia Core features, and enables them to obtain the Payment Management activation status. All users of Payment Management must be assigned the CSC BASIC permission set to ensure that all standard features work as intended. |
| CSC APP SETUP | This permission set allows users to activate Continia products, including Continia Core. It's mainly used for product installation and – in Business Central online – when making changes to subscription agreements, such as selecting and deselecting subscribed modules. The permission set is mostly required in online deployments of Business Central. Users who set up on-premises environments typically use the CPM-365 ADMIN permission set. |

## Payment Management specific permission sets

| Permission set      | Description                                                  |
| ------------------- | ------------------------------------------------------------ |
| CPM365 BASIC        | Basic permission set for users not working in finance.       |
| CPM365 ADMIN        | This permission set is intended for the Payment Management administrator, and it's required for setting up Payment Management. In addition, this permission set also includes the permissions included in *CPM365 ACC. RECON.* , *CPM365 ACC. PAY*, and *CMP PSP Import*. |
| CPM365 ACC. PAY     | Users with this permission set can import and post payments. |
| CPM365 ACC. RECON.  | The Payment Management Account Reconciliation permission set allows users to use the Statement Intelligence module to, for example, import bank account statements, perform account reconciliation, and manage general ledger accounting. |
| CPM365 BEXD ADMIN   | Users with this permission set can access the Bank Export Data table. |
| CPM365 APPRADMIN    | Users with this permission set can create, edit, and delete payment approval workflows for all payment journals. In addition, they can also view and delegate all open approval requests. |
| CPM PSP IMPORT      | Users with this permission set can create PSP agreements and import PSP files. |
| CPM BANK ACC. VERIF | Users with this permission set can [enable bank account verification](@PM-352). |

## Assigning permissions to users and user groups

To assign Payment Management permissions to users and user groups is a standard Business Central process. For more information, see Microsoft's article [Assign Permissions to Users and User Groups](https://docs.microsoft.com/en-us/dynamics365/business-central/ui-define-granular-permissions).

##  Creating custom permission sets

To manually create your own permission sets is a standard Business Central process. For more information, see Microsoft's article [Assign Permissions to Users and User Groups](https://docs.microsoft.com/en-us/dynamics365/business-central/ui-define-granular-permissions).

<style>
  .content table tr td:nth-child(1) {
    width: 90px;
  }
  .content table tr td:nth-child(2) {
    width: 640px;
  }  
</style>