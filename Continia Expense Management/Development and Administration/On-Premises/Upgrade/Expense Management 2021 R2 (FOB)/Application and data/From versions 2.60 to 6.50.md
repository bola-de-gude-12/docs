---
title: Expense Management Upgrading from Versions 2.60–6.50 to Version 8.00
date: 31-03-2025
id: EM-29
lang: en
---

# Upgrading from Versions 2.60–6.50 to Version 8.00

With Document Capture 8.00 and Expense Management 8.00, Continia Software is releasing an upgrade guide that our partners can use to upgrade directly from Document Capture 4.50-6.50 and/or Expense Management 2.60-6.50 to Document Capture 8.00 and or Expense Management 8.00.

When upgrading from Document Capture 7.00 and/or Expense Management 7.00 to version 8.00, use the regular upgrade procedure described in [Manual Upgrade from Version 7.00 to Version 8.00](../../../../../../Continia%20Expense%20Management/Development%20and%20Administration/On-Premises/Upgrade/Expense%20Management%202021%20R2%20\(FOB\)/Application%20and%20data/@EM-30/) or [Automated Data Upgrade from Version 7.00 to Version 8.00](../../../../../../Continia%20Expense%20Management/Development%20and%20Administration/On-Premises/Upgrade/Expense%20Management%202021%20R2%20\(FOB\)/Application%20and%20data/@EM-31/).

This upgrade guide describes the manual upgrade of Document Capture and Expense Management on the version of NAV (NAV 3.70 to BC14) currently used with Document Capture and Expense Management.

If you are using Document Capture or Expense Management in Microsoft Business Central online, the main upgrade will be performed automatically when you install DC8.00/EM8.00 (after uninstallation of DC7.00/EM7.00).

Migration from FOB-based version of NAV/BC to an on-premises extension and/or online: See [Upgrading NAV/Business Central with Expense Management Installed](../../../../../../Continia%20Expense%20Management/Development%20and%20Administration/On-Premises/Upgrade/Expense%20Management%202021%20R2%20\(FOB\)/Application%20and%20data/@EM-107/) and [Migrating Expense Management from Business Central On-Premises to Cloud](../../../../../../Continia%20Expense%20Management/Development%20and%20Administration/On-Premises/Upgrade/Expense%20Management%202021%20R2%20\(FOB\)/Application%20and%20data/@EM-112/).

This upgrade guide can be used with the following versions of Document Capture and Expense Management:

**Document Capture**

* Document Capture 4.50 with any service pack
* Document Capture 5.00 with any service pack
* Document Capture 5.50 with any service pack
* Document Capture 6.00 with any service pack
* Document Capture 6.50 with any service pack

**Expense Management**

* Expense Management 2.60 with any service pack
* Expense Management 3.00 with any service pack
* Expense Management 3.50 with any service pack
* Expense Management 4.00 with any service pack
* Expense Management 6.50 with any service pack

If the system is running an older version, you must first upgrade to the required versions.

In this version, we have upgraded the Document Capture Client Components and Server Components, and you must update these components before you start working with Document Capture and Expense Management. This guide will instruct you on how to do this correctly. The Document Capture and Expense Management objects in this version are not backward-compatible with older components, and the components in this version are not backward-compatible with older objects.

If Document Capture and Expense Management are not already installed, you should not use any information in this document. Instead, see the Quick Guide for installing Document Capture or Expense Management.

## Task 1: Check minimum version requirements

Ensure the current system is running one of the supported versions of Document Capture or Expense Management listed in the summary section. If not, it is very important that you follow the upgrade guide from an earlier version to DC4.50 and or EM2.60. Previous upgrade guides can be found here:

For Document Capture: https://continia.zendesk.com/hc/en-us/sections/201853305-Upgrade-Guides

For Expense Management: https://continia.zendesk.com/hc/da/sections/360000175700-Upgrade-Guides

## Task 2: Import updated NAV license file

The upgrade process must be performed using a developer license.

After the upgrade, ensure to use a new/updated customer license file from Microsoft and import it into NAV.

If you are using the Dynamics NAV Server, you must restart the Dynamics NAV Server to use the new license.

## Task 3: Merge objects

If you have modified your customer's system, then check if any of the modified objects conflict with Document Capture or Expense Management objects and merge if necessary. You should merge objects in a test system so they are ready to be imported later in the upgrade process.

## Task 4: Verify product activation status before upgrading

> \[!NOTE] This task is not relevant when upgrading from DC6.00.x or DC6.50.x or when upgrading from EM4.00.x or EM6.50.x.

Before starting the upgrade, make sure that the product activation status is correct in all companies that are being upgraded.

If the upgrade code detects a company without a valid activation state, it will stop with the following error message:

* "One or more companies have a wrong activation state. Run page 6086102 "CDC Company Registration Upg." to update the companies activation state, and then rerun the pre-migration to continue the upgrade process."

Running this page/form (depending on the NAV version) will allow you to activate or deactivate DC and EM separately in each company. The upgrade can not continue unless all product/company combinations are either Activated or Deactivated.

## Task 5: Check pre-upgrade package

The pre-upgrade package depends on both the DC/EM version you are upgrading from and the NAV/BC version.

Make sure to use the correct upgrade package

Examples of pre-upgrade filename and interpretation:

* “NAV 2016 to BC14 - DC4.50 to DC8.00, EM2.60 to EM8.00 – Direct Upgrade **Pre**”.fob
  * The NAV version is between NAV 2016 and BC14 (Business Central April 2019 )
  * The DC/EM version before the upgrade is DC4.50 and EM2.60
  * This is the pre-upgrade .fob

After importing the correct pre-upgrade package (replace all), go to either “Document Capture Setup” or “Expense Management Setup” and press “Upgrade Upgrade Data to Latest Version”. This will perform the pre-upgrade.

**Make sure that you start the upgrade in a company with either Document Capture or Expense Management activated.**

## Task 6: Install all tools and components

You must perform all installations described below from the Setup executable, located in the root of the product folder (Setup.exe).

> \[!NOTE] The installer will update the add-ins folder (Client and/or Server) in the standard installation path. Therefore, if your installation path differs from the standard Microsoft path, make sure to copy the new add-in folder to the folder your installation resides in.

## Task 7: Upgrade server components

To upgrade your server components, follow one of the guides below, depending on your version of NAV/Business Central:

\


| Version                    | Guide                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NAV Server 2009 -> 2009 R2 | <p>Only perform the following steps if you are using Dynamics NAV 2009 -> 2009 R2:</p><ol><li>Stop “Microsoft Dynamics NAV Server”. Set it to start up manually.</li><li>Stop “Microsoft Dynamics NAV Business Web Services” if started. Set it to start up manually.</li><li>Restart the Windows server.</li><li>Uninstall “Document Capture RTC Server Components”. </li><li>Install “Document Capture RTC Server Components”.</li><li>If you haven’t installed the Microsoft Dynamics NAV Server in the default location, you must move the Add-ins manually from the default location to the current location of your installation.</li><li>Start “Microsoft Dynamics NAV Server”. Set it to start up automatically.</li><li>Start “Microsoft Dynamics NAV Business Web Services”, if needed. Set it to start up automatically.</li></ol> |
| NAV Server 2013 -> BC14    | <p>Only perform the following steps if you are using Dynamics NAV 2013 -> Microsoft Dynamics 365 Business Central April 2019 (BC14):</p><ol><li>Stop “Microsoft Dynamics NAV Server”.</li><li>Uninstall “Document Capture RTC Server Components”. </li><li>Install “Document Capture RTC Server Components”.</li><li>If you haven’t installed the Microsoft Dynamics NAV Server in the default location, you must move the Add-ins manually from the default location to the current location of your installation.</li><li>Start “Microsoft Dynamics NAV Server”.</li></ol>                                                                                                                                                                                                                                                                  |
| NAV Classic Upgrade PC     | <p>Only perform the following steps if you are using Dynamics NAV Classic:</p><ol><li>On the computer where you perform the upgrade, you must uninstall “Document Capture Classic Client Components” and “Document Capture Classic Components (Scanner)”</li><li>Install “Document Capture Classic Client Components”.</li><li>Install “Document Capture Classic Components (Scanner)” if needed.</li></ol>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| NAV RTC Upgrade PC         | <p>Only perform the following steps if you are using Dynamics NAV RTC:</p><ol><li>On the computer where you perform the upgrade, you must uninstall ”Document Capture RTC Client” and ”Document Capture RTC Components (Scanner)”.</li><li>Install “Document Capture RTC Client”.</li><li>Install “Document Capture RTC Component (Scanner)” if needed.</li><li>If you haven’t installed the Microsoft Dynamics NAV RTC Client in the default location, you must move the Add-ins manually from the default location to the current location of your installation.</li></ol>                                                                                                                                                                                                                                                                  |

## Task 8: Update NAV objects and data

> \[!IMPORTANT] Before doing object modifications or starting the data upgrade, make sure to back up the database.

Import the new DC8.00/EM8.00 objects from the product folder. Use “Replace All” in Import Worksheet. Some objects may show a warning during import as some parts of the new Version List have changed format. For NAV 2015 and later, set Synchronize Schema to “Later” during object import.

> \[!WARNING] For all versions from NAV 2013 to Business Central October 2018 (BC v13), the following applies: When importing the DC8.00/EM8.00 object package, skip the four pages mentioned below. The pages were unintentionally included in the release packages – they will be removed in service pack 1.
>
> * Page 5 **Currencies**
> * Page 10 **Countries/Regions**
> * Page 209 **Units of Measure**
> * Page 472 **VAT Posting Setup**

## Task 9: Post-upgrade

Follow the below to complete the Post-Upgrade step:

1. Import the object post-upgrade package corresponding to your NAV/BC version and the DC/EM version that you are upgrading from (e.g: “NAV 2016 to BC14 - DC4.50 to DC8.00, EM2.60 to EM8.00 – Direct Upgrade Post.fob”).
2. Use “Replace All” in Import Worksheet. When using NAV 2015 or a newer version, set Synchronize Schema to “Later” during import.
3. Compile all Document Capture and Expense Management objects (Version List filter \*DC\*|\*EM\*|\*CC\*|\*DN\*). When using NAV 2015 or a newer version, set Synchronize Schema to “Later”. Some DC/EM objects will not compile. They will be deleted later in the upgrade process.
4. Compile all MenuSuites (not only DC and EM).
5. When using NAV 2015 or a newer version, run Tools -> “Sync. Schema For All Tables” -> “With Validation”.
6. Restart the RTC Client.
7. Make sure that you start the upgrade in a company with either Document Capture or Expense Management activated.
8. Run the function “Upgrade Data to Latest Version” from the Document Capture Setup card or the Expense Management Setup Card in any activated company. The routine will handle all companies and upgrade Document Capture data if needed, and upgrade Expense Management data if needed.
9. The Post-Update process should complete without any errors.
10. Restart the RTC Client.
11. Verify that the activation status of the upgraded companies is as expected.

## Task 10: Upgrade client components

To upgrade your client components, follow one of the guides below, depending on your version of NAV/Business Central:

\


| Version                      | Guide                                                                                                                                                                                                                                                                                                                                                               |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NAV Classic Clients          | <p>Only perform the following steps if you are using Dynamics NAV Classic:</p><ol><li>Uninstall “Document Capture Classic Client Components”.</li><li>Uninstall “Document Capture Classic Components (Scanner)”.</li><li>Install “Document Capture Classic Client Components”.</li><li>Install “Document Capture Classic Components (Scanner)” if needed.</li></ol> |
| NAV RTC Clients 2009 -> 2016 | <p>Only perform the following steps if you are using Dynamics NAV 2009 -> 2016:</p><ol><li>Uninstall “Document Capture RTC Client Components”.</li><li>Install “Document Capture RTC Client Components”</li></ol>                                                                                                                                                   |
| NAV RTC Clients 2017 -> BC14 | <ol><li>Uninstall “Document Capture RTC Client”.</li><li>Uninstall ”Document Capture RTC Components (Scanner)”.</li><li>Client Add-ins are now automatically distributed to all NAV clients when needed.</li></ol>                                                                                                                                                  |

## Task 11: Delete unused application and upgrade objects

After completing the upgrade, remove the upgrade objects (All object types, with Force):

Filter: 6086100..6086199

> \[!NOTE] On versions before NAV 2015, upgrade tables and obsolete tables must be emptied manually before deletion.

Some objects that were part of the Document Capture/Expense Management version that you upgraded from are not needed anymore. Therefore, whenever you upgrade from one of the versions below, delete the objects specified:

* Tables:\
  6085620|6085701

The objects below are deleted in code, it is therefore not necessary to delete them manually.

* Forms:\
  6085606|6085716|6085751|6086348|6086403|6086418|6192771|6192773|6192776
* Pages:\
  6085606|6086037|6086054|6086348|6192771|6192777|6192778|6192773|6192776
* Codeunits:\
  6085620|6085622|6085747|6085800|6086335|6085929|6192774|6192776|6192778

### Specifically for 2009 R2 RTC

Support for the NAV 2009 R2 RoleTaylored Client has been discontinued in DC8.00 and EM8.00. Only the classic client is supported.

All Document Capture and Expense Managementpages, except web service pages, should be deleted. Pages used as web services by the Continia Web Approval Portal all end with “(WS)” in the object name.

DC contains modifications to the following 4 standard pages. These modifications should be removed manually after the upgrade:

* Page 26 Vendor Card
* Page 138 Posted Purchase Invoice
* Page 140 Posted Purchase Credit Memo
* Page 344 Navigate

## Task 12: Update the Continia Web Approval Portal

To update the Continia Web Approval Portal, follow these steps:

1. If you use NAV objects below NAV 2009 R2, you must import the updated Web Approval Portal objects from the product folder. For NAV 2009 R2 and later versions, these objects will be included in the base package.
2. Compile all Document Capture and Expense Management objects (Version List filter \*DC\*|\*EM\*|\*CC\*|\*DN\*).
3. Run the function “Create Web Services” from the Continia Web Portal list. It is only required to run this function in one company.
4. If you continue to use Continia Web Portal on-premises, then create a new website in IIS or update the existing one.
5. Run the function “Export Users” to export web users from the Continia Users screen in NAV.

## See also

[Manual Upgrade from Version 7.00 to Version 8.00](../../../../../../Continia%20Expense%20Management/Development%20and%20Administration/On-Premises/Upgrade/Expense%20Management%202021%20R2%20\(FOB\)/Application%20and%20data/@EM-30/)\
[Automated Data Upgrade from Version 7.00 to Version 8.00](../../../../../../Continia%20Expense%20Management/Development%20and%20Administration/On-Premises/Upgrade/Expense%20Management%202021%20R2%20\(FOB\)/Application%20and%20data/@EM-31/)
