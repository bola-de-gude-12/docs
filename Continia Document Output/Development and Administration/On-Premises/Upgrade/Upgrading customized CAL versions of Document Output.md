---
title: Upgrading Customized C/AL Versions of Document Output
date: 10-07-2024
description:  
id: DO-129
lang: en
---

# Upgrading Customized C/AL Versions of Document Output

The upgrade of Continia Document Output from C/AL code customizations to AL extensions is based on the standard Microsoft upgrade process, as described in [this guide](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-to-microsoft-base-app-v24). The text below functions as a sort of add-on to this guide, detailing all [additional prequisites](#prerequisites) and any [Continia-specific steps to be taken](#upgrade-process) for each task in the Microsoft guide.

To upgrade your C/AL version of Document Output to AL extensions, you must upgrade to Business Central 2024 release wave 1 (BC v24) in accordance with the Microsoft guide referenced above.

## Prerequisites

* You must first upgrade to Microsoft Dynamics 365 Business Central April 2019 (BC v14). For an overview of which BC v14 versions are compatible with BC v24, see [Dynamics 365 Business Central Upgrade Compatibility Matrix](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-v14-v15-compatibility).
* Document Output must be upgraded to the latest released version, including the latest service pack.

## Upgrade process

The numbered tasks mentioned below all refer to the tasks of the Microsoft guide [Upgrading Customized C/AL Application to Microsoft Base Application version 24](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-to-microsoft-base-app-v24). All of these tasks deal with third-party extensions, which in this case means the three Continia apps Document Output, Continia Core, and Continia Delivery Network. For each of the tasks, you must perform the actions described:

### Task 4: Create empty System, Base, and customization extensions

For this task, you'll need empty versions of the three Continia apps. You can find these using the link below:

* [Continia apps](https://continiadocsstorageprod.blob.core.windows.net/docsfiles/ContiniaApps.zip)

### Task 5: Create table migration extension

In this task, you must create two versions of an extension that consists only of the non-system table objects from your custom base application. The second version is an empty extension containing a migration.json file, as described under "Create the second version - empty" in the Microsoft guide. Append the following IDs to this migration.json file:

* 4b915d7e-c02a-435f-85ab-649086c1e002
* 0745e76d-0b72-4641-87c2-ee45db5d2c32
* f4b69b55-c90d-4937-8f53-2742898fa948

### Task 10: Publish DestinationAppsForMigrations extensions

In step 2 of this task, publish the following three extensions in the order given:

1. Continia Core
1. Continia Delivery Network
1. Continia Document Output

To do this, run the following commands, where "\<path to extension\>" is the path to the location where the empty extensions downloaded in [task 4 above](#task-4-create-empty-system-base-and-customization-extensions) have been saved:

<br>

```
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Core"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Delivery Network"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Document Output"
```

### Task 11: Synchronize tenant

In step 4 of this task, run the following commands:

<br>

```
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Core”
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Delivery Network"
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Document Output”
```

### Task 12: Install DestinationAppsForMigration and move tables

In step 3 of this task, install the Continia apps in your system, and move data from the old tables to the new tables owned by the table migration extension.

<br>

```
Install-NAVApp -ServerInstance <server instance name> -Name “Continia Core”
Install-NAVApp -ServerInstance <server instance name> -Name “Continia Delivery Network”
Install-NAVApp -ServerInstance <server instance name> -Name “Continia Document Output”
```

### Task 13: Publish final extensions

In step 5 of this task, run the following commands, where "\<path to extension\>" is the path to the location where you saved the extensions that you created in task 3 of the [Microsoft guide](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-to-microsoft-base-app-v22):

<br>

```
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Core"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Delivery Network"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Document Output"
```

### Task 14: Synchronize final extensions

In this task, run the following commands:

<br>

```
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Core”
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Delivery Network"
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Document Output”
```

### Task 17: Upgrade and install final extensions

In this task, run the following commands:

<br>

```
Start-NAVAppDataUpgrade -ServerInstance <server instance name> -Name “Continia Core”
Start-NAVAppDataUpgrade -ServerInstance <server instance name> -Name “Continia Delivery Network”
Start-NAVAppDataUpgrade -ServerInstance <server instance name> -Name “Continia Document Output”
```

## See also

[Migrating Document Output from Business Central On-Premises to Cloud](@DO-128)  