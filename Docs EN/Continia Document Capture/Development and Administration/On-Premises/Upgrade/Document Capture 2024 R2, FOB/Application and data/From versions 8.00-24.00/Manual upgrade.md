---
title: Manual upgrade from versions 8.00–24.00 to version 25.00
date: 22-04-2025
description: A guide to the direct upgrade of versions 8.00–24.00 to version 25.00.
lang: en
---

# Manual upgrade from versions 8.00–24.00 to version 25.00

With Continia Document Capture 25.00 and Continia Expense Management 25.00, Continia Software is releasing a combined guide that our partners can use to upgrade directly from Document Capture 8.00–24.00 and/or Expense Management 8.00–24.00 to Document Capture 25.00 and/or Expense Management 25.00.

This guide describes the manual upgrade of Document Capture and Expense Management. If you're looking for a more automated process, see [Automated data upgrade from versions 8.00–24.00 to version 25.00](Automated data upgrade.md). That article describes how to upgrade Document Capture or Expense Management using Microsoft's Data Upgrade tools.

> [!IMPORTANT]
> Note that Document Capture 2024 R2 (25.00) and Expense Management R2 (25.00) are only available if you're using one of the following versions of Microsoft Dynamics 365 Business Central:
>
> * Business Central 2024 release wave 2 (BC v25)
> * Business Central 2024 release wave 1 (BC v24)
> * Business Central 2023 release wave 1 (BC v23)
> * Business Central April 2019 (v14, FOB-based)
> This means that clients using older NAV/BC versions are unable to upgrade to DC25.00/EM25.00. Instead, they must upgrade to DC8.00/EM8.00, as this version will continue to be supported with service packs. 

If you're using Document Capture or Expense Management in Business Central online, the main upgrade will be performed automatically when you install DC25.00/EM25.00.

Migration from FOB-based version of NAV/BC to on-premises extension and/or online: See [Upgrading NAV/Business Central with Document Capture installed](@DC-7) and [Migrating Document Capture from Business Central on premises to cloud](@DC-106).

This upgrade guide can be used with the following versions of Document Capture and Expense Management:

**Document Capture**
* Document Capture 8.00 with any service pack
* Document Capture 9.00 with any service pack
* Document Capture 10.00 with any service pack
* Document Capture 11.00 with any service pack
* Document Capture 12.00 with any service pack
* Document Capture 24.00 with any service pack

**Expense Management**
* Expense Management 8.00 with any service pack
* Expense Management 9.00 with any service pack
* Expense Management 10.00 with any service pack
* Expense Management 11.00 with any service pack
* Expense Management 12.00 with any service pack
* Expense Management 24.00 with any service pack

If the system is running an older version, you must first upgrade to the required versions.

In this version, Continia has upgraded the Document Capture Client Components and Server Components, and you must update these components before you start working with Document Capture and Expense Management. This guide will instruct you on how to do this correctly. The Document Capture and Expense Management objects in this version are not backward-compatible with older components, and the components in this version are not backward-compatible with older objects.

If Document Capture and Expense Management aren't already installed, you shouldn't use any information in this document.

## Task 1: Check minimum version requirements

Make sure that the current system is running one of the supported versions of Document Capture or Expense Management listed in the summary section. If not, it is very important that you follow the upgrade guide from an earlier version to DC4.50 and/or EM2.60. For previous upgrade guides, see [Upgrading to Continia Document Capture 2023 R2 (12.00) for FOB versions](@DC-157).

## Task 2: Import updated BC license file

The upgrade process must be performed using a partner developer license.

After the upgrade, make sure to use a new/updated customer license file from Microsoft. 

You must restart the Business Central Server to use the new license.

## Task 3: Merge objects

If you have modified your customer's system, check if any of the modified objects conflict with Document Capture or Expense Management objects – and merge if necessary. You should merge objects in a test system, so they're ready to be imported later in the upgrade process.

## Task 4: Check pre-upgrade package

There is no Pre-Upgrade step in version 25.00.

## Task 5: Upgrade server components
You must perform all installations described below from the Setup executable, located in the root of the product folder (Setup.exe).

> [!NOTE]
> The installer updates the add-ins folder (Client and/or Server) in the standard installation path. Therefore, if your installation path differs from the standard Microsoft path, make sure to copy the new add-in folder to the folder your installation resides in.

To upgrade your server components:

<br>

| Version | Guide |
| --- | --- |
| BC14 | Only perform the following steps if you're using Business Central April 2019 (BC14): <ol><li>Stop 'Business Central Server Server'.</li><li>Uninstall 'Document Capture RTC Server Components'.&nbsp;</li><li>Install 'Document Capture RTC Server Components'.</li><li>If you haven't installed the Microsoft Business Central Server in the default location, you must move the Add-ins manually from the default location to the current location of your installation.</li><li>Start 'Microsoft Business Central Server'.</li></ol> |


## Task 6: Update BC objects and data

> [!IMPORTANT]
> Before doing object modifications or starting the data upgrade, make sure to back up the database.

Import the new DC25.00/EM25.00 objects from the product folder. Use **Replace All** in Import Worksheet. Some objects may show a warning during import, as some parts of the new Version List have changed format. Set Synchronize Schema to **Later** during object import.

>[!NOTE]
>If a modified object set was created in [Task 3: Merge objects](#task-3-merge-objects), make sure to import it – and not the objects found in the product folder.

## Task 7: Post-upgrade

> [!IMPORTANT]
> If any of your companies handle approvals in Expense Management, refer to [Task 7: Post-upgrade](@EM-263#task-7-post-upgrade) in the [equivalent Expense Management article](@EM-263).

Complete the Post-Upgrade step:

1. Import the object post-upgrade package corresponding to your BC version (BC14 - DC8.00-DC24.00 to DC25.00, EM8.00-EM24.00 to EM25.00 – Direct Upgrade Post.fob).
1. Use **Replace All** in Import Worksheet. Set Synchronize Schema to **Later** during import.
1. Compile all Document Capture and Expense Management objects (Version List filter \*DC\*|\*EM\*|\*CC\*|\*DN\*|\*BF\*|\*CA\*). Set Synchronize Schema to **Later**. Some DC/EM objects may not compile. They're deleted later in the upgrade process.
1. Compile all MenuSuites (not only DC and EM).
1. Run Tools -> 'Sync. Schema For All Tables'”' -> '**With Validation**'.
1. Restart the RTC Client.
1. Make sure that you start the upgrade in a company with either Document Capture or Expense Management activated.
1. Run the function 'Upgrade Data to Latest Version' from the Document Capture Setup card or the Expense Management Setup card in any activated company. The routine handles all companies and upgrade Document Capture data if needed, and upgrade Expense Management data if needed.
1. The Post-Update process should complete without any errors.
1. Restart the RTC Client.
1. Verify that the activation status of the upgraded companies is as expected.

## Task 8: Upgrade client components

To upgrade your client components:

<br>

| Version | Guide |
| --- | --- |
| BC14 | <ol><li>Using the **Add or remove programs** functionality in Windows, uninstall Document Capture RTC Client and Document Capture RTC Components (Scanner).</li><li>Client Add-ins are now automatically distributed to all NAV clients when needed.</li></ol> |

## Task 9: Delete unused application and upgrade objects

After completing the upgrade, please remove the upgrade objects (All object types, with Force):

Filter: 6086100..6086199

After deleting the upgrade objects, please import the upgrade placeholder objects from the fob-file containing the new DC/EM objects. Only import the objects within the id-range: 6086100..6086199.

This ensures that all objects compile, and that the upgrade isn't inadvertently started again.

## Task 10: Update the Continia Web Approval Portal

To update the Continia Web Approval Portal:

1. Compile all Document Capture and Expense Management objects (Version List filter \*DC\*|\*EM\*|\*CC\*|\*DN\*|\*BF\*|\*CA\*).
1. Run the function 'Create Web Services' from the Continia Web Portal list. It's only required to run this function in one company.
1. If you continue to use Continia Web Portal on premises, create a website in IIS or update the existing one.
1. Run the function 'Export Users' to export web users from the Continia Users page in BC.


<style>
  .content table tr td:nth-child(1) {
    width: 130px;
  }
  .content table tr td:nth-child(2) {
    width: 600px;
  }  
</style>