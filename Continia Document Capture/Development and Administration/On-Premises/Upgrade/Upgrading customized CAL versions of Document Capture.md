---
title: Upgrading customized C/AL versions of Document Capture
date: 02-04-2025
id: DC-113
lang: en
description: >-
  How to upgrade Continia Document Capture and Continia Expense Management from
  C/AL code customizations to AL extensions.
---

# Upgrading customized C/AL versions of Document Capture

The upgrade of Continia Document Capture and Continia Expense Management from C/AL code customizations to AL extensions is based on the standard Microsoft upgrade process, as described in [Upgrading customized C/AL application to Microsoft Base Application version 25](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-to-microsoft-base-app-v25) (Microsoft article). The text below functions as a sort of add-on to this guide, detailing all [additional prerequisites](<Upgrading customized CAL versions of Document Capture.md#prerequisites>) and any [Continia-specific steps to be taken](<Upgrading customized CAL versions of Document Capture.md#upgrade-process>) for each task in the Microsoft guide.

> \[!NOTE] Starting in 2025 release wave 1 (v26), the direct upgrade from Business Central 2019 (v14) to the latest release isn't supported. The supported upgrade path is through 2024 release wave 2 (v25), then to v26. For more information, see [Deprecated features in the platform - clients, server, and database](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-platform#changes-in-2025-release-wave-1-version-260) (Microsoft article).

Note that you must upgrade both Document Capture and Expense Management at the same time. To upgrade your C/AL versions of these apps to AL extensions, you must upgrade to Business Central 2024 release wave 2 (BC v25) in accordance with the Microsoft guide referenced above.

## Prerequisites

* You must first upgrade to Microsoft Dynamics 365 Business Central April 2019 (BC v14). For an overview of which BC v14 versions are compatible with BC v25, see [Dynamics 365 Business Central upgrade compatibility matrix](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-v14-v15-compatibility) (Microsoft article).
* Document Capture must be upgraded to the latest released version, including the latest service pack.

## Upgrade process

> \[!IMPORTANT] To ensure a consistent migration to BC v25, Expense Management must be installed even if it isn't used in the database. When the migration is complete, you can uninstall Expense Management again if needed.

The numbered tasks mentioned below all refer to the tasks of the Microsoft guide [Upgrading customized C/AL application to Microsoft base application version 25](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-to-microsoft-base-app-v25) (Microsoft article). All of these tasks deal with third-party extensions, which in this case means the five Continia apps Document Capture, Expense Management, Continia Core, Continia Delivery Network, and Continia Business Foundation. For each of the tasks, you must perform the actions described:

### Task 4: Create empty System, Base, Business Foundation, and customization extensions

For this task, you'll need empty versions of the five Continia apps. You can find these using the link below:

* [Continia apps](https://continiadocsstorageprod.blob.core.windows.net/docsfiles/ContiniaApps.zip)

### Task 5: Create table migration extension

In this task, you must create two versions of an extension that consists only of the non-system table objects from your custom base application. The second version is an empty extension containing a migration.json file, as described under "Create the second version - empty" in the Microsoft guide. Append the following IDs to this migration.json file:

* 4b915d7e-c02a-435f-85ab-649086c1e002
* bbb72c8a-3abf-478f-9239-a34dbc252d07
* 0745e76d-0b72-4641-87c2-ee45db5d2c32
* 6da8dd2f-e698-461f-9147-8e404244dd85
* 8d4eab29-8c7f-4b6c-be9a-b7fdfb9da196

### Task 10: Publish DestinationAppsForMigrations extensions

In step 2 of this task, publish the following five extensions in the order given:

1. Continia Core
2. Continia Business Foundation
3. Continia Delivery Network
4. Continia Document Capture
5. Continia Expense Management

To do this, run the following commands, where "\<path to extension>" is the path to the location where the empty extensions downloaded in [task 4 above](<Upgrading customized CAL versions of Document Capture.md#task-4-create-empty-system-base-and-customization-extensions>) have been saved:

\


```
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Core"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Business Foundation"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Delivery Network"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Document Capture"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Expense Management"
```

### Task 11: Synchronize tenant

In step 4 of this task, run the following commands:

\


```
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Core”
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Business Foundation”
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Delivery Network"
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Document Capture”
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Expense Management”
```

### Task 12: Install DestinationAppsForMigration and move tables

In step 3 of this task, install the Continia apps in your system, and move data from the old tables to the new tables owned by the table migration extension.

\


```
Install-NAVApp -ServerInstance <server instance name> -Name “Continia Core”
Install-NAVApp -ServerInstance <server instance name> -Name “Continia Business Foundation”
Install-NAVApp -ServerInstance <server instance name> -Name “Continia Delivery Network”
Install-NAVApp -ServerInstance <server instance name> -Name “Continia Document Capture”
Install-NAVApp -ServerInstance <server instance name> -Name “Continia Expense Management”
```

### Task 13: Publish final extensions

In step 5 of this task, run the following commands, where "\<path to extension>" is the path to the location where you saved the extensions that you created in task 3 of the [Microsoft guide](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-to-microsoft-base-app-v25):

\


```
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Core"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Business Foundation"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Delivery Network"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Document Capture"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Expense Management"
```

### Task 14: Synchronize final extensions

In this task, run the following commands:

\


```
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Core”
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Business Foundation”
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Delivery Network"
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Document Capture”
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Expense Management”
```

### Task 17: Upgrade and install final extensions

In this task, run the following commands:

\


```
Start-NAVAppDataUpgrade -ServerInstance <server instance name> -Name “Continia Core”
Start-NAVAppDataUpgrade -ServerInstance <server instance name> -Name “Continia Business Foundation”
Start-NAVAppDataUpgrade -ServerInstance <server instance name> -Name “Continia Delivery Network”
Start-NAVAppDataUpgrade -ServerInstance <server instance name> -Name “Continia Document Capture”
Start-NAVAppDataUpgrade -ServerInstance <server instance name> -Name “Continia Expense Management”
```

## Related information

[Migrating Document Capture from Business Central on premises to cloud](../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Upgrade/@DC-106/)
