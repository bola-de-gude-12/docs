# em-manual-upgrade-from-version-7.00-to-version-8.00

With Document Capture version 8.00 and Expense Management version 8.00, Continia Software is releasing an upgrade guide that our partners can use to upgrade Document Capture 7.00, Expense Management 7.00 or a system with both Document Capture 7.00 and Expense Management 7.00 installed.

This upgrade guide describes the manual upgrade of Document Capture and Expense Management on the version of NAV (NAV 3.70 to BC14) currently used with Document Capture and Expense Management.

If you are looking for a more automated process, please refer to [Automated Data Upgrade from Version 7.00 to Version 8.00](@EM-31/). That document describes how to upgrade Document Capture or Expense Management using the new Data Upgrade tools from Microsoft.

If you are using Document Capture or Expense Management in Microsoft Business Central Online, the main upgrade will be performed automatically when you install Document Capture 8.00 (after uninstallation of Document Capture 7.00).

Migration from FOB-based version of NAV/BC to an on-premises extension and/or online: See [Upgrading NAV/Business Central with Expense Management Installed](@EM-107/) and [Migrating Expense Management from Business Central On-Premises to Cloud](@EM-112/).

This upgrade guide can be used with the following versions of Document Capture and Expense Management:

**Document Capture**

* Document Capture 7.00 with any service pack.

**Expense Management**

* Expense Management 7.00 with any service pack.

If the system is running an older version, you must first upgrade to the required versions.

In this version, we have upgraded the Document Capture Client Components and Server Components, and you must update these components before you start working with Document Capture and Expense Management. This guide will instruct you how to do this correctly. The Document Capture and Expense Management objects in this version are not backwards-compatible with older components, and the components in this version are not backwards-compatible with older objects.

If Document Capture and Expense Management are not already installed, you should not use any information in this document. Please see the Quick Guide for installing Document Capture or Expense Management.

### Task 1: Check minimum version requirements

Please be sure that the current system is running one of the supported versions of Document Capture or Expense Management listed in the summary section. If not, it is very important you follow the upgrade guide from an earlier version to DC7.00 and or EM7.00. Previous upgrade guides can be found here:

For Document Capture: https://continia.zendesk.com/hc/en-us/sections/201853305-Upgrade-Guides

For Expense Management: https://continia.zendesk.com/hc/da/sections/360000175700-Upgrade-Guides

### Task 2: Import updated NAV license file

The upgrade process must be performed using a developer license.

After the upgrade please ensure to use a new/updated customer license file from Microsoft and import it into NAV.

If you are using the Dynamics NAV Server, you must restart the Dynamics NAV Server to use the new license.

### Task 3: Merge objects

If you have modified your customer's system, then check if any of the modified objects conflict with Document Capture or Expense Management objects and merge if necessary. You should merge objects in a test system, so they are ready to be imported later in the upgrade process.

### Task 4: Check pre-upgrade package

There is no Pre-Upgrade step in version 8.00.

### Task 5: Install all tools and components

You must perform all installations described below from the Document Capture Setup executable, located in the root of the product folder (Setup.exe).

> \[!NOTE] The installer will update the add-ins folder (Client and/or Server) in the standard installation path. Therefore, if your installation path differs from the standard Microsoft path, make sure to copy the new add-in folder to the folder your installation resides in.

### Task 6: Upgrade server components

To upgrade your server components, follow one of the guides below, depending on your version of NAV/Business Central:

\


| Version                    | Guide                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NAV Server 2009 -> 2009 R2 | <p>Only perform the following steps if you are using Dynamics NAV 2009 -> 2009 R2:</p><ol><li>Stop “Microsoft Dynamics NAV Server”. Set it to start up manually.</li><li>Stop “Microsoft Dynamics NAV Business Web Services” if started. Set it to start up manually.</li><li>Restart the Windows server.</li><li>Uninstall “Document Capture RTC Server Components”. </li><li>Install “Document Capture RTC Server Components”.</li><li>If you haven’t installed the Microsoft Dynamics NAV Server in the default location, you must move the Add-ins manually from the default location to the current location of your installation.</li><li>Start “Microsoft Dynamics NAV Server”. Set it to start up automatically.</li><li>Start “Microsoft Dynamics NAV Business Web Services”, if needed. Set it to start up automatically.</li></ol> |
| NAV Server 2013 -> BC14    | <p>Only perform the following steps if you are using Dynamics NAV 2013 -> Microsoft Dynamics 365 Business Central Spring 2019 Update (BC14):</p><ol><li>Stop “Microsoft Dynamics NAV Server”.</li><li>Uninstall “Document Capture RTC Server Components”. </li><li>Install “Document Capture RTC Server Components”.</li><li>If you haven’t installed the Microsoft Dynamics NAV Server in the default location, you must move the Add-ins manually from the default location to the current location of your installation.</li><li>Start “Microsoft Dynamics NAV Server”.</li></ol>                                                                                                                                                                                                                                                          |
| NAV Classic Upgrade PC     | <p>Only perform the following steps if you are using Dynamics NAV Classic:</p><ol><li>On the computer where you perform the upgrade, you must uninstall “Document Capture Classic Client Components” and “Document Capture Classic Components (Scanner)”</li><li>Install “Document Capture Classic Client Components”.</li><li>Install “Document Capture Classic Components (Scanner)” if needed.</li></ol>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| NAV RTC Upgrade PC         | <p>Only perform the following steps if you are using Dynamics NAV RTC:</p><ol><li>On the computer where you perform the upgrade, you must uninstall ”Document Capture RTC Client” and ”Document Capture RTC Components (Scanner)”.</li><li>Install “Document Capture RTC Client”.</li><li>Install “Document Capture RTC Component (Scanner)” if needed.</li><li>If you haven’t installed the Microsoft Dynamics NAV RTC Client in the default location, you must move the Add-ins manually from the default location to the current location of your installation.</li></ol>                                                                                                                                                                                                                                                                  |

### Task 7: Update NAV objects and data

> \[!IMPORTANT] Before doing object modifications or starting the data upgrade, make sure to back up the database.

Import the new DC8.00 / EM8.00 objects from the product folder. Use “Replace All” in Import Worksheet. Please note, some objects may show a warning during import as some parts of the new Version List has changed format. For NAV 2015 and later, set Synchronize Schema to “Later” during object import.

> \[!WARNING] For all versions from NAV 2013 to Business Central October 2018 (BC v13), the following applies: When importing the DC8.00/EM8.00 object package, please skip the 4 pages mentioned below. The pages were unintentionally included in the release packages – they will be removed in service pack 1.
>
> * Page 5 **Currencies**
> * Page 10 **Countries/Regions**
> * Page 209 **Units of Measure**
> * Page 472 **VAT Posting Setup**

### Task 8: Post-upgrade

Follow below to complete the Post-Upgrade step:

1. Import the object package named “(Your NAV version) - Document Capture 8.00, Expense Management 8.00 - PostUpgrade.fob”. Use “Replace All” in the Import Worksheet. When using NAV 2015 or a newer version, set Synchronize Schema to “Later” during import.
2. Compile all Document Capture and Expense Management objects (Version List filter \*DC\*|\*EM\*|\*CC\*|\*DN\*). When using NAV 2015 or a newer version, set Synchronize Schema to “Later”. Some DC/EM objects will not compile – they will be deleted later in the upgrade process.
3. Compile all MenuSuites (not only DC and EM).
4. When using NAV 2015 or a newer version, run Tools -> “Sync. Schema For All Tables” -> “With Validation”.
5. Restart the RTC Client.
6. Run the function “Upgrade Data to Latest Version” from the Document Capture Setup card or the Expense Management Setup Card in any company. The routine will handle all companies and upgrade Document Capture data if needed, and upgrade Expense Management data if needed.
7. The Post-Update process should complete without any errors.

### Task 9: Upgrade client components

To upgrade your client components, follow one of the guides below, depending on your version of NAV/Business Central:

\


| Version                      | Guide                                                                                                                                                                                                                                                                                                                                                               |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NAV Classic Clients          | <p>Only perform the following steps if you are using Dynamics NAV Classic:</p><ol><li>Uninstall “Document Capture Classic Client Components”.</li><li>Uninstall “Document Capture Classic Components (Scanner)”.</li><li>Install “Document Capture Classic Client Components”.</li><li>Install “Document Capture Classic Components (Scanner)” if needed.</li></ol> |
| NAV RTC Clients 2009 -> 2016 | <p>Only perform the following steps if you are using Dynamics NAV 2009 -> 2016:</p><ol><li>Uninstall “Document Capture RTC Client Components”.</li><li>Install “Document Capture RTC Client Components”</li></ol>                                                                                                                                                   |
| NAV RTC Clients 2017 -> BC14 | <ol><li>Uninstall “Document Capture RTC Client”.</li><li>Uninstall ”Document Capture RTC Components (Scanner)”.</li><li>Client Add-ins are now automatically distributed to all NAV clients when needed.</li></ol>                                                                                                                                                  |

### Task 10: Delete upgrade objects

After completing the upgrade please remove the upgrade objects (All object types, with Force):

Filter: 6086100..6086199

> \[!NOTE] On versions before NAV 2015, upgrade tables must be emptied manually prior to deletion.

### Task 11: Update the Continia Web Approval Portal

To update the Continia Web Portal, follow these steps:

1. If you are using NAV objects below NAV 2009 R2, you will need to import the updated Web Portal objects from the product folder. For NAV 2009 R2 and later versions, these objects will be included in the base package.
2. Compile all Document Capture and Expense Management objects (Version List filter \*DC\*|\*EM\*|\*CC\*|\*DN\*).
3. Run the function “Create Web Services” from the Continia Web Portal list. It is only required to run this function in one company.
4. If you continue to use Continia Web Portal On-Premise, then create a new Web Site in IIS or update the existing one.
5. Run the function “Export Users” to export web users from the Continia Users screen in NAV.

### Related information

[Automated Data Upgrade from Version 7.00 to Version 8.00](@EM-31/)
