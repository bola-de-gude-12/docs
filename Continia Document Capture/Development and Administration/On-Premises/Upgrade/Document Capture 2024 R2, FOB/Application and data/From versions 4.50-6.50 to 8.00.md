---
title: Upgrading from Versions 4.50–6.50 to Version 8.00
date: 17-01-2025
lang: en
description: A guide on how to upgrade directly from versions 4.50–6.50 to version 8.00
---

# Upgrading from Versions 4.50–6.50 to Version 8.00

With Continia Document Capture 8.00 and Continia Expense Management 8.00, Continia Software released a combined upgrade guide that our partners can use to upgrade directly from Document Capture 4.50–6.50 and/or Expense Management 2.60–6.50 to Document Capture 8.00 and/or Expense Management 8.00.

> \[!NOTE] When you upgrade from Document Capture 7.00 and/or Expense Management 7.00 to version 8.00, follow the regular upgrade procedure described in [Manual Upgrade from Version 7.00 to Version 8.00](../../../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Upgrade/Document%20Capture%202024%20R2,%20FOB/from-version-700/manual-upgrade/) or [Automated Data Upgrade from Version 7.00 to Version 8.00](../../../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Upgrade/Document%20Capture%202024%20R2,%20FOB/from-version-700/automated-data-upgrade/).

This upgrade guide describes the manual upgrade of Document Capture (DC) and Expense Management (EM) in the version of Microsoft Dynamics NAV/Business Central (BC) currently used with Document Capture and Expense Management (NAV 3.70 to BC v14).

If you're using Document Capture or Expense Management in Microsoft Dynamics 365 Business Central online, the main upgrade will be performed automatically when you install Document Capture 8.00/Expense Management 8.00 (after uninstallating Document Capture 7.00/Expense Management 7.00).

As regards migration from a FOB-based version of NAV/Business Central to an on-premises extension and/or online, see [Upgrading NAV/Business Central with Document Capture Installed](../../../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Upgrade/Document%20Capture%202024%20R2,%20FOB/Application%20and%20data/@DC-7/) and [Migrating Document Capture from Business Central On-Premises to Cloud](../../../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Upgrade/Document%20Capture%202024%20R2,%20FOB/Application%20and%20data/@DC-106/).

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

If your system is running an older version, you must first upgrade to the required versions.

In this version, we have upgraded the Document Capture client components and server components, which you must update before you start working with Document Capture and Expense Management. This guide will help you to do this correctly. The Document Capture and Expense Management objects in this version aren't backward-compatible with older components, just as the components included in this version aren't backward-compatible with older objects.

If Document Capture and Expense Management haven't already been installed in your system, you shouldn't use any information in this document.

## Task 1: Check minimum version requirements

Make sure that your current system is running one of the supported versions of Document Capture or Expense Management listed in the summary section. If not, it's very important that you follow the relevant upgrade guide from an earlier version to Document Capture 4.50 and/or Expense Management 2.60. Previous upgrade guides can be found here:

For Document Capture: https://continia.zendesk.com/hc/en-us/sections/201853305-Upgrade-Guides (only available to partners)

For Expense Management: https://continia.zendesk.com/hc/da/sections/360000175700-Upgrade-Guides (only available to partners)

## Task 2: Import updated NAV license file

The upgrade process must be performed using a partner developer license.

After the upgrade, make sure that you use a new or updated customer license file from Microsoft and import it into NAV.

If you're using the Microsoft Dynamics NAV Server, you must restart it to use the new license.

## Task 3: Merge objects

If you've modified your customer's system, check if any of the modified objects conflict with Document Capture or Expense Management objects, and then merge if necessary. You should merge objects in a test system, so they're ready to be imported later in the upgrade process.

## Task 4: Import pre-upgrade package

The pre-upgrade package depends on both your NAV/Business Central version and the version of Document Capture/Expense Management that you're upgrading from.

> \[!IMPORTANT] Make sure that you use the correct upgrade package.

Example of a pre-upgrade filename and how to interpret it:

* “NAV 2016 to BC14 - DC4.50 to DC8.00, EM2.60 to EM8.00 – Direct Upgrade **Pre**”.fob
  * The NAV version is between NAV 2016 and BC v14 (Business Central April 2019)
  * The DC/EM version before the upgrade is DC v4.50 and EM v2.60
  * This is the pre-upgrade .fob

## Task 5: Run pre-upgrade step

After importing the correct pre-upgrade package (replace all), go to either **Document Capture Setup** or **Expense Management Setup**, and then select **Upgrade Data to Latest Version**. This will perform the pre-upgrade.

**Make sure that you start the upgrade in a company with either Document Capture or Expense Management activated.**

> \[!NOTE] _The following isn't relevant when you upgrade from DC v6.00.x or DC v6.50.x, or from EM v4.00.x or EM v6.50.x:_
>
> Before starting the upgrade, make sure that the product activation status is correct in all companies that are being upgraded. If the upgrade code detects a company without a valid activation state, it will stop with the following error message:
>
> * _One or more companies have a wrong activation state. Run page 6086102 CDC Company Registration Upg. to update the companies activation state, and then rerun the pre-migration to continue the upgrade process._
>
> Running this page/form (depending on the NAV version) will allow you to activate or deactivate DC and EM separately for each company. The upgrade can't continue unless all product/company combinations are either activated or deactivated.

## Task 6: Install all tools and components

You must perform all installations described below using the **Setup** executable, located in the root of the product folder (Setup.exe).

> \[!NOTE] The installer will update the add-ins folder (Client and/or Server) in the standard installation path. Therefore, if your installation path differs from the standard Microsoft path, make sure to copy the new add-in folder to the folder that your installation resides in.

## Task 7: Upgrade server components

To upgrade your server components, follow one of the guides below, depending on your version of NAV/Business Central:

\


| Version                   | Guide                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NAV Server 2009 – 2009 R2 | <p>Only perform the following steps if you're using Dynamics NAV 2009 – 2009 R2:</p><ol><li>Stop “Microsoft Dynamics NAV Server”. Set it to start up manually.</li><li>Stop “Microsoft Dynamics NAV Business Web Services”, if it has been started. Set it to start up manually.</li><li>Restart the Windows server.</li><li>Uninstall “Document Capture RTC Server Components”. </li><li>Install “Document Capture RTC Server Components”.</li><li>If you haven’t installed the Microsoft Dynamics NAV Server in the default location, you must move the Add-ins manually from the default location to the current location of your installation.</li><li>Start “Microsoft Dynamics NAV Server”. Set it to start up automatically.</li><li>Start “Microsoft Dynamics NAV Business Web Services”, if needed. Set it to start up automatically.</li></ol> |
| NAV Server 2013 – BC14    | <p>Only perform the following steps if you're using Dynamics NAV 2013 – Business Central April 2019 (BC14):</p><ol><li>Stop “Microsoft Dynamics NAV Server”.</li><li>Uninstall “Document Capture RTC Server Components”. </li><li>Install “Document Capture RTC Server Components”.</li><li>If you haven’t installed the Microsoft Dynamics NAV Server in the default location, you must move the Add-ins manually from the default location to the current location of your installation.</li><li>Start “Microsoft Dynamics NAV Server”.</li></ol>                                                                                                                                                                                                                                                                                                      |
| NAV Classic Upgrade PC    | <p>Only perform the following steps if you're using Dynamics NAV Classic:</p><ol><li>On the computer where you perform the upgrade, you must uninstall “Document Capture Classic Client Components” and “Document Capture Classic Components (Scanner)”</li><li>Install “Document Capture Classic Client Components”.</li><li>Install “Document Capture Classic Components (Scanner)”, if needed.</li></ol>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| NAV RTC Upgrade PC        | <p>Only perform the following steps if you're using Dynamics NAV RTC:</p><ol><li>On the computer where you perform the upgrade, you must uninstall ”Document Capture RTC Client” and ”Document Capture RTC Components (Scanner)”.</li><li>Install “Document Capture RTC Client”.</li><li>Install “Document Capture RTC Component (Scanner)”, if needed.</li><li>If you haven’t installed the Microsoft Dynamics NAV RTC Client in the default location, you must move the Add-ins manually from the default location to the current location of your installation.</li></ol>                                                                                                                                                                                                                                                                             |

## Task 8: Update NAV objects and data

> \[!IMPORTANT] Before carrying out object modifications or starting the data upgrade, be sure to back up the database.

Import the new DC v8.00/EM v8.00 objects from the product folder. Use “Replace All” in Import Worksheet. Note that some objects may show a warning during import, as some parts of the new Version List have a changed format. For NAV 2015 and later, set Synchronize Schema to “Later” during object import.

> \[!WARNING] For all versions from NAV 2013 to Business Central October 2018 (BC v13), the following applies: When importing the DC v8.00/EM v8.00 object package, skip the four pages mentioned below. The pages were unintentionally included in the release packages but will be removed in service pack 1.
>
> * Page 5 **Currencies**
> * Page 10 **Countries/Regions**
> * Page 209 **Units of Measure**
> * Page 472 **VAT Posting Setup**

## Task 9: Post-upgrade

Follow the guide below to complete the post-upgrade step:

1. Import the object post-upgrade package corresponding to your NAV/BC version and the DC/EM version that you're upgrading from (such as “NAV 2016 to BC14 – DC4.50 to DC8.00, EM2.60 to EM8.00 – Direct Upgrade Post.fob”).
2. Use “Replace All” in Import Worksheet. When using NAV 2015 or a newer version, set Synchronize Schema to “Later” during import.
3. Compile all Document Capture and Expense Management objects (Version List filter \*DC\*|\*EM\*|\*CC\*|\*DN\*). When using NAV 2015 or a newer version, set Synchronize Schema to “Later”. Some DC/EM objects will not compile. They'll be deleted later in the upgrade process.
4. Compile all MenuSuites (not only DC and EM).
5. When using NAV 2015 or a newer version, run **Tools** > **Sync. Schema For All Tables** > **With Validation**.
6. Restart the RTC Client.
7. Make sure that you start the upgrade in a company with either Document Capture or Expense Management activated.
8. Run the function **Upgrade Data to Latest Version** from the **Document Capture Setup** card or the **Expense Management Setup** Card in any activated company. This will:
   * Handle all companies and upgrade Document Capture data, if needed.
   * Upgrade Expense Management data, if needed.
9. The post-update process should complete without any errors.
10. Restart the RTC Client.
11. Verify that the activation status of the upgraded companies is as expected.

## Task 10: Upgrade client components

To upgrade your client components, follow one of the guides below, depending on your version of NAV/Business Central:

\


| Version                     | Guide                                                                                                                                                                                                                                                                                                                                                               |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NAV Classic Clients         | <p>Only perform the following steps if you're using Dynamics NAV Classic:</p><ol><li>Uninstall “Document Capture Classic Client Components”.</li><li>Uninstall “Document Capture Classic Components (Scanner)”.</li><li>Install “Document Capture Classic Client Components”.</li><li>Install “Document Capture Classic Components (Scanner)”, if needed.</li></ol> |
| NAV RTC Clients 2009 – 2016 | <p>Only perform the following steps if you're using Dynamics NAV 2009 – 2016:</p><ol><li>Uninstall “Document Capture RTC Client Components”.</li><li>Install “Document Capture RTC Client Components”</li></ol>                                                                                                                                                     |
| NAV RTC Clients 2017 – BC14 | <ol><li>Uninstall “Document Capture RTC Client”.</li><li>Uninstall ”Document Capture RTC Components (Scanner)”.</li><li>Client Add-ins are now automatically distributed to all NAV clients when needed.</li></ol>                                                                                                                                                  |

## Task 11: Delete unused application and upgrade objects

After completing the upgrade, please remove the upgrade objects (All object types, with Force):

Filter: 6086100..6086199

> \[!NOTE] On versions before NAV 2015, upgrade tables and obsolete tables must be emptied manually before deletion.

Some objects that were part of the DC/EM version that you upgraded from are not needed anymore. Therefore, whenever you upgrade from one of the versions below, please delete the objects specified:

* Tables:\
  6085620|6085701

The objects below are deleted in code, so it's unnecessary to delete them manually:

* Forms:\
  6085606|6085716|6085751|6086348|6086403|6086418|6192771|6192773|6192776
* Pages:\
  6085606|6086037|6086054|6086348|6192771|6192777|6192778|6192773|6192776
* Codeunits:\
  6085620|6085622|6085747|6085800|6086335|6085929|6192774|6192776|6192778

### Specifically for 2009 R2 RTC

Support for the NAV 2009 R2 RoleTailored Client has been discontinued as of DC v8.00 and EM v8.00. Only the Classic Client is supported.

All DC and EM pages, except web service pages, should be deleted. Pages used as web services by the Continia Web Approval Portal all end with “(WS)” in the object name.

DC contains modifications to the four standard pages mentioned below. These modifications should be removed manually after the upgrade.

* Page 26 **Vendor Card**
* Page 138 **Posted Purchase Invoice**
* Page 140 **Posted Purchase Credit Memo**
* Page 344 **Navigate**

## Task 12: Update the Continia Web Approval Portal

To update the Continia Web Approval Portal, follow these steps:

1. If you use NAV objects below NAV 2009 R2, you must import the updated Web Approval Portal objects from the product folder. For NAV 2009 R2 and later versions, these objects will be included in the base package.
2. Compile all Document Capture and Expense Management objects (Version List filter \*DC\*|\*EM\*|\*CC\*|\*DN\*).
3. Run the function **Create Web Services** from the Continia Web Portal list. It's only required to run this function in one company.
4. If you continue to use Continia Web Portal on-premises, create a new website in IIS or update the existing one.
5. From the **Continia Users** screen in NAV, run the function **Export Users** to export web users.

## Task 13: Update vendor templates configured with “Prices incl. VAT”

The following is only necessary if you upgrade from versions DC v4.50, DC v5.00, or DC v5.50 and the system contains vendor templates with “Prices incl. VAT”.

With the release of DC v6.00, the registration of purchase documents with “Prices incl. VAT” was changed. For you to fully benefit from the new functionality, some modifications to existing vendor templates are needed. The updated functionality and the necessary changes are described in [this article](https://continia.zendesk.com/hc/da/articles/360010610879-How-to-upgrade-templates-with-Prices-Incl-VAT-when-upgrading-to-DC6-00) (only available to partners).

The article mentions the “Template Upgrade Tool”. You can find this in the DC v8.00 product .fob by importing the following objects:

Table: 6086110 and 6086111\
Page: 6086100 and 6086101

## Related information

[Manual Upgrade from Version 7.00 to Version 8.00](../../../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Upgrade/Document%20Capture%202024%20R2,%20FOB/from-version-700/manual-upgrade/)\
[Automated Data Upgrade from Version 7.00 to Version 8.00](../../../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Upgrade/Document%20Capture%202024%20R2,%20FOB/from-version-700/automated-data-upgrade/)
