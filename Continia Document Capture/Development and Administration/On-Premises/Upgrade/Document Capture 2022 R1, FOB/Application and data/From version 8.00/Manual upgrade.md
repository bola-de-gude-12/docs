---
title: Manual Upgrade from Version 8.00 to Version 9.00
date: 17-01-2025
id: DC-42
lang: en
---

# Manual Upgrade from Version 8.00 to Version 9.00

In Document Capture version 9.00 and Expense Management version 9.00, Continia Software is releasing a combined upgrade guide that our partners can use to upgrade Document Capture 8.00, Expense Management 8.00 or a system with both Document Capture 8.00 and Expense Management 8.00 installed.

This upgrade guide describes the manual upgrade of Document Capture and Expense Management on the version of Business Central 14, currently used with Document Capture and Expense Management.

Note that Document Capture 9.00 and Expense Management 9.00 are available only for Business Central April 2019 (v14, FOB-based) and newer. Older NAV / BC versions will have to be upgraded to Business Central April 2019 before upgrading to Document Capture version 9.00 and Expense Management version 9.00. For more details, see [this table](../../../../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Upgrade/Document%20Capture%202022%20R1,%20FOB/Application%20and%20data/From%20version%208.00/@DC-43/).

If you are upgrading from a NAV client older than BC14, you cannot upgrade to Document Capture and Expense Management unless you have also upgraded the client to Business Central 14.

If you are using Document Capture or Expense Management in Microsoft Business Central Cloud, the main upgrade will be performed automatically when you install Document Capture 9.00 or Expense Management 9.00 (after uninstallation of Document Capture 8.00 or Expense Management 9.00).

Migration from FOB-based version of NAV/BC to On-Premises Extension and/or Cloud: See [this article on the Continia PartnerZone](https://continia.zendesk.com/hc/da/articles/360015942380-Overview-Migrating-from-BC14-FOB-based-to-BC15-or-newer-versions-On-Premises-and-or-Cloud-)

This upgrade guide can be used with the following versions of Document Capture and Expense Management:

**Document Capture**

* Document Capture 8.00 with any service pack.

**Expense Management**

* Expense Management 8.00 with any service pack.

If the system is running an older version, you must first upgrade to the required versions.

In this version, we have upgraded the Document Capture Client Components and Server Components, and you must update these components before you start working with Document Capture and Expense Management. This guide will instruct you how to do this correctly. The Document Capture and Expense Management objects in this version are not backwards-compatible with older components, and the components in this version are not backwards-compatible with older objects.

If Document Capture and Expense Management are not already installed, you should not use any information in this document. Please see the Quick Guide for installing Document Capture or Expense Management.

## Task 1: Check version requirements

Please be sure that the current system is running one of the supported versions of Document Capture or Expense Management listed in the summary section. If not, it is very important you follow the upgrade guide from an earlier version to DC8.00 and or EM8.00. Previous upgrade guides can be found in [Supported Upgrade Paths for Continia Document Capture (FOB)](../../../../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Upgrade/Document%20Capture%202022%20R1,%20FOB/Application%20and%20data/From%20version%208.00/@DC-8/) and [Supported Upgrade Paths for Continia Expense Management (FOB)](../../../../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Upgrade/Document%20Capture%202022%20R1,%20FOB/Application%20and%20data/From%20version%208.00/@EM-103/).

## Task 2: Import updated NAV license file

The upgrade process must be performed using a partner developer license.

After the upgrade please ensure to use a new/updated customer license file from Microsoft and import it into NAV.

You must restart the Business Central Server to use the new license.

## Task 3: Merge objects

If you have modified your customer's system, then check if any of the modified objects conflict with Document Capture or Expense Management objects and merge if necessary. You should merge objects in a test system, so they are ready to be imported later in the upgrade process.

## Task 4: Check pre-upgrade package

There is no Pre-Upgrade step in version 9.00.

## Task 5: Upgrade server components

To upgrade your server components, follow the steps below:

\


1. Stop "Microsoft Dynamics NAV Server".
2. Uninstall ”Document Capture RTC Server” and ”Document Capture RTC Components (Scanner)”.
3. Install “Document Capture RTC Server”.
4. Install “Document Capture RTC Component (Scanner)” if needed.
5. Start "Microsoft Dynamics NAV Server"

> \[!NOTE] The installer will update the add-ins folder (Client and/or Server) in the standard installation path. Therefore, if your installation path differs from the standard Microsoft path, make sure to copy the new add-in folder to the folder your installation resides in.

\


## Task 6: Upgrade client components on the upgrade client

The Role Tailored Client that performs the upgrade must also have the client components installed. This is necessary since the objects will not compile otherwise. Please follow the following steps for the MS Dynamics NAV Role Tailored Client:

1. Stop "Microsoft Dynamics NAV Client".
2. Uninstall ”Document Capture RTC Client” and ”Document Capture RTC Components (Scanner)”.
3. Install “Document Capture RTC Client”.
4. Install “Document Capture RTC Component (Scanner)” if needed.
5. Start "Microsoft Dynamics NAV Client"

> \[!NOTE] The installer will update the add-ins folder (Client and/or Server) in the standard installation path. Therefore, if your installation path differs from the standard Microsoft path, make sure to copy the new add-in folder to the folder your installation resides in.

## Task 7: Update NAV objects and data

> \[!IMPORTANT] Before doing object modifications or starting the data upgrade, make sure to back up the database.

Import the new DC9.00 / EM9.00 objects from the product folder. Use “Replace All” in Import Worksheet. Please note, some objects may show a warning during import as some parts of the new Version List has changed format. Set Synchronize Schema to “Later” during object import.

## Task 8: Post-upgrade

Follow the steps below to complete the post-upgrade step:

1. Import the object package named “(Your NAV version) - Document Capture 9.00, Expense Management 9.00 - PostUpgrade.fob”. Use “Replace All” in the Import Worksheet.
2. Compile all Document Capture and Expense Management objects (Version List filter \*DC\*|\*EM\*|\*CC\*|\*DN\*). Set Synchronize Schema to “Later”. Some DC/EM objects will not compile – they will be deleted later in the upgrade process.
3. Compile all MenuSuites (not only DC and EM).
4. Run Tools -> “Sync. Schema For All Tables” -> “With Validation”.
5. Restart the RTC Client.
6. Run the function “Upgrade Data to Latest Version” from the Document Capture Setup card or the Expense Management Setup card in any company. The routine will handle all companies and upgrade Document Capture data if needed, and upgrade Expense Management data if needed.
7. The Post-Update process should complete without any errors.

## Task 9: Upgrade client components

Client Add-ins are now automatically distributed to all NAV clients when needed.

## Task 10: Delete upgrade objects

After completing the upgrade please remove the upgrade objects (All object types, with Force):

Filter: 6086100..6086199

> \[!NOTE] On versions before NAV 2015, upgrade tables must be emptied manually prior to deletion.

## Task 11: Update the Continia Web Approval Portal

To update the Continia Web Portal, follow these steps:

1. If you continue to use Continia Web Portal On-Premise, then create a new Web Site in IIS or update the existing one.
2. Run the function “Export Users” to export web users from the Continia Users screen in NAV.
