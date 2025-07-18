---
title: Automated Data Upgrade from Versions 8.00–12.00 to Version 24.00
date: 20-03-2024
lang: en
---

# Automated Data Upgrade from Versions 8.00–12.00 to Version 24.00

With Document Capture version 24.00 and Expense Management version 24.00, Continia Software is releasing a combined upgrade guide that our partners can use to upgrade Document Capture 8.00–12.00, Expense Management 8.00–12.00 or a system with both Document Capture 8.00–12.00 and Expense Management 8.00–12.00 installed.

> \[!IMPORTANT] Note that Document Capture 2024 R1 (24.00) and Expense Management 2024 R1 (24.00) are only available if you're using one of the following versions of Business Central:
>
> * Business Central 2024 release wave 1 (BC v24)
> * Business Central 2023 release wave 2 (BC v23)
> * Business Central 2023 release wave 1 (BC v22)
> * Business Central April 2019 (v14, FOB-based) This means that clients using older NAV/BC versions will not be able to upgrade to DC24.00/EM24.00. Instead, they must upgrade to DC8.00, as this version will continue to be supported with service packs.

This upgrade guide describes the upgrade of Document Capture and Expense Management using the more automated Data Upgrade on BC14.

If you are looking for the manual Pre and Post Upgrade process, please refer to \[Manual Upgrade from Versions 8.00–12.00 to Version 24.00]\(Manual upgrade.md).

If you are using Document Capture or Expense Management in Microsoft Business Central Cloud, the main upgrade will be performed automatically when you install Document Capture 24.00 and/or Expense Management 24.00.

Migration from FOB-based version of NAV/BC to On-Premises Extension and/or Cloud: See [Upgrading NAV/Business Central with Expense Management Installed](../../../../../../../Continia%20Expense%20Management/Development%20and%20Administration/On-Premises/Upgrade/Expense%20Management%202024%20R1%20\(FOB\)/Application%20and%20data/From%20versions%208.00-12.00/@EM-107/) and [Migrating Expense Management from Business Central On-Premises to Cloud](../../../../../../../Continia%20Expense%20Management/Development%20and%20Administration/On-Premises/Upgrade/Expense%20Management%202024%20R1%20\(FOB\)/Application%20and%20data/From%20versions%208.00-12.00/@EM-112/).

This upgrade guide can be used with the following versions of Document Capture and Expense Management:

**Document Capture**

* Document Capture 8.00 with any service pack
* Document Capture 9.00 with any service pack
* Document Capture 10.00 with any service pack
* Document Capture 11.00 with any service pack
* Document Capture 12.00 with any service pack

**Expense Management**

* Expense Management 8.00 with any service pack
* Expense Management 9.00 with any service pack
* Expense Management 10.00 with any service pack
* Expense Management 11.00 with any service pack
* Expense Management 12.00 with any service pack

If the system is running an older version, you must first upgrade to the required versions (8.00).

In this version, we have upgraded the Document Capture Client Components and Server Components, and you must update these components before you start working with Document Capture and Expense Management. This guide will instruct you how to do this correctly. The Document Capture and Expense Management objects in this version are not backwards-compatible with older components, and the components in this version are not backwards-compatible with older objects.

If Document Capture and Expense Management are not already installed, you should not use any information in this document.

## Task 1: Check minimum version requirements

Please be sure that the current system is running one of the supported versions of Document Capture or Expense Management listed in the summary section. If not, it is very important you follow the upgrade guide from an earlier version to DC8.00–12.00 and/or EM8.00–12.00. Previous upgrade guides can be found in [Supported Upgrade Paths for Continia Document Capture (FOB)](../../../../../../../Continia%20Expense%20Management/Development%20and%20Administration/On-Premises/Upgrade/Expense%20Management%202024%20R1%20\(FOB\)/Application%20and%20data/From%20versions%208.00-12.00/@DC-8/) and [Supported Upgrade Paths for Continia Expense Management (FOB)](../../../../../../../Continia%20Expense%20Management/Development%20and%20Administration/On-Premises/Upgrade/Expense%20Management%202024%20R1%20\(FOB\)/Application%20and%20data/From%20versions%208.00-12.00/@EM-103/).

## Task 2: Import updated BC license file

The upgrade process must be performed using a partner developer license.

After the upgrade please ensure to use a new/updated customer license file from Microsoft.

You must restart the Business Central Server to use the new license.

## Task 3: Merge objects

If you have modified your customer's system, then check if any of the modified objects conflict with Document Capture or Expense Management objects and merge if necessary. You should merge objects in a test system, so they are ready to be imported later in the upgrade process.

## Task 4: Upgrade server components

You must perform all installations described below from the Setup executable, located in the root of the product folder (Setup.exe).

> \[!NOTE] The installer will update the add-ins folder (Client and/or Server) in the standard installation path. Therefore, if your installation path differs from the standard Microsoft path, make sure to copy the new add-in folder to the folder your installation resides in.

To upgrade your server components, follow the guide below:

\


| Version | Guide                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BC14    | <p>Only perform the following steps if you are using Business Central April 2019 (BC14):</p><ol><li>Stop “Business Central Server Server”.</li><li>Uninstall “Document Capture RTC Server Components”. </li><li>Install “Document Capture RTC Server Components”.</li><li>If you haven’t installed the Microsoft Business Central Server in the default location, you must move the Add-ins manually from the default location to the current location of your installation.</li><li>Start “Microsoft Business Central Server”.</li></ol> |

## Task 5: Update BC objects and data

> \[!IMPORTANT] Before doing object modifications or starting the data upgrade, make sure to back up the database.

Import the new DC24.00 / EM24.00 objects from the product folder. Please note, some objects may show a warning during import as some parts of the new Version List has changed format. Use “**Replace All**” in Import Worksheet. Set Synchronize Schema to “**Later**” during object import.

## Task 6: Data upgrade

Follow below to complete the Post-Upgrade step:

1. Import the object package named “BC14 - DC8.00-DC11.00 to DC24.00, EM8.00-EM11.00 to EM24.00 – Direct Upgrade Post”. Use “Replace All” in Import Worksheet. Set Synchronize Schema to “**Later**” during import.
2. Compile all Document Capture and Expense Management objects (Version List filter \*DC\*|\*EM\*|\*CC\*|\*DN\*|\*BF\*). Set Synchronize Schema to “**Later**”.
3. Compile all MenuSuites (not only DC and EM).
4. Run Tools -> “Sync. Schema For All Tables” -> “**With Validation**”.
5. Run Tools -> “Data Upgrade” -> “Start…” to open the **Start Data Upgrade** page.
6. Under **Execution Mode**, select **Serial**, and then clear the checkbox under **Continue on Error**. Select **OK** to close the page.

The Data Upgrade process should complete without any errors.

> \[!NOTE] The Purch. Contracts Administrator field is being obsoleted in the Continia User Setup. Therefore, after the upgrade, Purchase Contracts Administrator users must be assigned the CDC-PC-ADMIN permission set.

### Data upgrade troubleshooting

1. In case the Data Upgrade fails, you will have to run the Get-NAVDataUpgrade \[ServerInstance] -ErrorOnly powershell command to find out what the actual error is or use the debugger with “Debug Next”.
2. If the Error message looks like “Function 'UpdatePerDatabase' in the upgrade codeunit '6086106' has failed because of the following error: 'A call to System.Net.WebClient.DownloadData failed with this message: The remote server returned an error: (404) Not Found.'.” this means that there is a problem downloading the Control Add-in resources. This problem can occur when our services are down, or it could be a server Firewall problem.
3. You can choose to try again by Running Tools -> “Data Upgrade” -> “Resume…”.
4. If the same error is thrown, you can Design Codeunit 6086106 and comment the following line of code: CODEUNIT.RUN(CODEUNIT::"CDC Capture RTC Library");
5. Then Run Tools -> “Data Upgrade” -> “Resume…”.
6. This will skip the downloading of the Control Add-in when upgrading therefore you must download them manually after the Data Upgrade from Document Capture Setup page: On the **Actions** tab, select **Import Continia Web Client Add-Ins** and **Import Client Add-Ins** to import all relevant add-ins.

## Task 7: Upgrade client components

To upgrade your client components, follow the guide below:

\


| Version | Guide                                                                                                                                                                                                             |
| ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BC14    | <ol><li>Uninstall “Document Capture RTC Client”.</li><li>Uninstall ”Document Capture RTC Components (Scanner)”.</li><li>Client Add-ins are now automatically distributed to all BC clients when needed.</li></ol> |

## Task 8: Delete unused application and upgrade objects

After completing the upgrade, please remove the upgrade objects (All object types, with Force):

Filter: 6086100..6086199

After deleteing the upgrade objects, please import the upgrade placeholder objects from the fob-file containing the new DC/EM objects. Only import the objects within the id-range: 6086100..6086199

This will ensure that all objects compile and that the upgrade is not inadvertible started again.

## Task 9: Update the Continia Web Approval Portal

To update the Continia Web Approval Portal, follow these steps:

1. Compile all Document Capture and Expense Management objects (Version List filter \*DC\*|\*EM\*|\*CC\*|\*DN\*|\*BF\*).
2. Run the function “Create Web Services” from the Continia Web Portal list. It is only required to run this function in one company.
3. If you continue to use Continia Web Portal on-premises, then create a new website in IIS or update the existing one.
4. Run the function “Export Users” to export web users from the Continia Users page in BC.
