---
title: Manual Upgrade from Versions 8.00–10.00 to Version 11.00
date: 17-01-2025
lang: en
description: A guide to the direct upgrade of versions 8.00–10.00 to version 11.00
---

# Manual Upgrade from Versions 8.00–10.00 to Version 11.00

With Continia Document Capture 11.00 and Continia Expense Management 11.00, Continia Software is releasing a combined upgrade guide that our partners can use to upgrade directly from Document Capture 8.00-10.00 and/or Expense Management 8.00-10.00 to Document Capture 11.00 and/or Expense Management 11.00.

This upgrade guide describes the manual upgrade of Document Capture and Expense Management. If you are looking for a more automated process, please refer to \[Automated Data Upgrade from Versions 8.00-10.00 to Version 11.00]\(Automated data upgrade.md). That document describes how to upgrade Document Capture or Expense Management using the new Data Upgrade tools from Microsoft.

> \[!IMPORTANT] Note that Document Capture 2023 R1 (11.00) is only available if you're using one of the following versions of Business Central:
>
> * Business Central 2023 release wave 1 (BC v22)
> * Business Central 2022 release wave 2 (BC v21)
> * Business Central 2022 release wave 1 (BC v20)
> * Business Central April 2019 (v14, FOB-based) This means that clients using older NAV/BC versions will not be able to upgrade to DC11.00. Instead, they must upgrade to DC8.00, as this version will continue to be supported with service packs.

If you are using Document Capture or Expense Management in Microsoft Business Central online, the main upgrade will be performed automatically when you install DC11.00/EM11.00.

Migration from FOB-based version of NAV/BC to on-premises extension and/or online: See [Upgrading NAV/Business Central with Document Capture Installed](../../../../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Upgrade/Document%20Capture%202023%20R1,%20FOB/Application%20and%20data/From%20versions%208.00%E2%80%9310.00/@DC-7/) and [Migrating Document Capture from Business Central On-Premises to Cloud](../../../../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Upgrade/Document%20Capture%202023%20R1,%20FOB/Application%20and%20data/From%20versions%208.00%E2%80%9310.00/@DC-106/).

This upgrade guide can be used with the following versions of Document Capture and Expense Management:

**Document Capture**

* Document Capture 8.00 with any service pack
* Document Capture 9.00 with any service pack
* Document Capture 10.00 with any service pack

**Expense Management**

* Expense Management 8.00 with any service pack
* Expense Management 9.00 with any service pack
* Expense Management 10.00 with any service pack

If the system is running an older version, you must first upgrade to the required versions.

In this version, we have upgraded the Document Capture Client Components and Server Components, and you must update these components before you start working with Document Capture and Expense Management. This guide will instruct you on how to do this correctly. The Document Capture and Expense Management objects in this version are not backward-compatible with older components, and the components in this version are not backward-compatible with older objects.

If Document Capture and Expense Management are not already installed, you should not use any information in this document.

## Task 1: Check minimum version requirements

Please be sure that the current system is running one of the supported versions of Document Capture or Expense Management listed in the summary section. If not, it is very important that you follow the upgrade guide from an earlier version to DC4.50 and or EM2.60. Previous upgrade guides can be found [here](../../../../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Upgrade/document-capture-2023-r1-fob/).

## Task 2: Import updated BC license file

The upgrade process must be performed using a partner developer license.

After the upgrade please ensure to use a new/updated customer license file from Microsoft.

You must restart the Business Central Server to use the new license.

## Task 3: Merge objects

If you have modified your customer's system, then check if any of the modified objects conflict with Document Capture or Expense Management objects and merge if necessary. You should merge objects in a test system so they are ready to be imported later in the upgrade process.

## Task 4: Check pre-upgrade package

There is no Pre-Upgrade step in version 11.00.

## Task 5: Upgrade server components

You must perform all installations described below from the Setup executable, located in the root of the product folder (Setup.exe).

> \[!NOTE] The installer will update the add-ins folder (Client and/or Server) in the standard installation path. Therefore, if your installation path differs from the standard Microsoft path, make sure to copy the new add-in folder to the folder your installation resides in.

To upgrade your server components, follow the guide below:

\


| Version | Guide                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BC14    | <p>Only perform the following steps if you are using Business Central April 2019 (BC14):</p><ol><li>Stop “Business Central Server Server”.</li><li>Uninstall “Document Capture RTC Server Components”. </li><li>Install “Document Capture RTC Server Components”.</li><li>If you haven’t installed the Microsoft Business Central Server in the default location, you must move the Add-ins manually from the default location to the current location of your installation.</li><li>Start “Microsoft Business Central Server”.</li></ol> |

## Task 6: Update BC objects and data

> \[!IMPORTANT] Before doing object modifications or starting the data upgrade, make sure to back up the database.

Import the new DC11.00/EM11.00 objects from the product folder. Use “**Replace All**” in Import Worksheet. Please note, some objects may show a warning during import as some parts of the new Version List have changed format. Set Synchronize Schema to “**Later**” during object import.

## Task 7: Post-upgrade

**Make sure that you start the upgrade in a company with either Document Capture or Expense Management activated.**

Follow the steps below to complete the Post-Upgrade step:

1. Import the object post-upgrade package corresponding to your BC version (“BC14 - DC8.00-DC10.00 to DC11.00, EM8.00-EM10.00 to EM11.00 – Direct Upgrade Post.fob”).
2. Use “**Replace All**” in Import Worksheet. Set Synchronize Schema to “**Later**” during import.
3. Compile all Document Capture and Expense Management objects (Version List filter \*DC\*|\*EM\*|\*CC\*|\*DN\*). Set Synchronize Schema to “**Later**”. Some DC/EM objects may not compile. They will be deleted later in the upgrade process.
4. Compile all MenuSuites (not only DC and EM).
5. Run Tools -> “Sync. Schema For All Tables” -> “**With Validation**”.
6. Restart the RTC Client.
7. Make sure that you start the upgrade in a company with either Document Capture or Expense Management activated.
8. Run the function “Upgrade Data to Latest Version” from the Document Capture Setup card or the Expense Management Setup card in any activated company. The routine will handle all companies and upgrade Document Capture data if needed, and upgrade Expense Management data if needed.
9. The Post-Update process should complete without any errors.
10. Restart the RTC Client.
11. Verify that the activation status of the upgraded companies is as expected.

## Task 8: Upgrade client components

To upgrade your client components, follow the guide below:

\


| Version | Guide                                                                                                                                                                                                              |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| BC14    | <ol><li>Uninstall “Document Capture RTC Client”.</li><li>Uninstall ”Document Capture RTC Components (Scanner)”.</li><li>Client Add-ins are now automatically distributed to all NAV clients when needed.</li></ol> |

## Task 9: Delete unused application and upgrade objects

After completing the upgrade, please remove the upgrade objects (All object types, with Force):

Filter: 6086100..6086199

After deleteing the upgrade objects, please import the upgrade placeholder objects from the fob-file containing the new DC/EM objects. Only import the objects within the id-range: 6086100..6086199

This will ensure that all objects compile and that the upgrade is not inadvertible started again.

The objects below are deleted in code, it is therefore not necessary to delete them manually.

* Pages:\
  6086203|6086205|6086206|6086207|6085605
* Codeunits:\
  6086213

## Task 10: Update the Continia Web Approval Portal

To update the Continia Web Approval Portal, follow these steps:

1. Compile all Document Capture and Expense Management objects (Version List filter \*DC\*|\*EM\*|\*CC\*|\*DN\*).
2. Run the function “Create Web Services” from the Continia Web Portal list. It is only required to run this function in one company.
3. If you continue to use Continia Web Portal on-premises, then create a new website in IIS or update the existing one.
4. Run the function “Export Users” to export web users from the Continia Users screen in NAV.
