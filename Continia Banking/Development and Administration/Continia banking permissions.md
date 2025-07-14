---
title: Continia Banking permissions
description: Information about Continia Banking permissions.
date: 23-06-2025
id: CB-59
lang: en
---

# Continia Banking permissions

{{include "permissions" "Banking"}}



## Standard Continia permission sets

| Permission set | Description |
| --- | --- |
| CTS-CB BASIC | This permission set grants users access to all Continia Core features, and enables them to obtain the Continia Banking activation status. All users of Continia Banking must be assigned the CTS-CB BASIC permission set to ensure that all standard features work as intended. |
| CSC APP SETUP | This permission set allows users to activate Continia products, including Continia Core. It's mainly used for product installation and – in Business Central online – when making changes to subscription agreements, such as selecting and deselecting subscribed modules. The permission set is mostly required in online deployments of Business Central. Users who set up on-premises environments typically use the CCB-365 ADMIN permission set. |

## Continia Banking-specific permission sets

| Permission set | Description                                                  |
| -------------- | ------------------------------------------------------------ |
| CTS-AW ADMIN   | Grants full control over payment approval workflows, allowing users to create, edit, and delete workflows for all payment journals. Users can also view and delegate all open approval requests. |
| CTS-CB ADMIN   | Required for Continia Banking administrators, enabling the setup and configuration of Continia Banking. |
| CTS-CBCP ADMIN | Provides permissions to create Transaction Ports and import CSV files for data processing. |
| CTS-CBCP BASIC | Allows users to manage and work with imported CSV files.     |
| CTS-CBPP ADMIN | Grants administrative privileges for PSP (Payment Service Provider) import processes, including setup and configuration. |
| CTS-CBPP BASIC | Provides basic access to PSP import functionality, allowing users to process PSP imports with limited permissions. |
| CTS-CBPP USER  | Enables users to work with PSP import data, but without administrative privileges. |
| CTS-PE ADMIN   | Grants full control over Banking Export processes, including setup and management. |
| CTS-PE BASIC   | Provides read-only access to Banking Export data.            |
| CTS-PE USER    | Enables users to access and manage banking export data with standard user privileges. |
| CTS-PI ADMIN   | Grants administrative control over banking import processes, including configuration and management. |
| CTS-PI BASIC   | Provides read-only access to Banking Import data.            |
| CTS-PI USER    | Enables users to work with banking import data with standard user permissions. |

<style>
  .content table tr td:nth-child(1) {
    width: 150px;
  }
  .content table tr td:nth-child(2) {
    width: 650px;
  }  
</style>