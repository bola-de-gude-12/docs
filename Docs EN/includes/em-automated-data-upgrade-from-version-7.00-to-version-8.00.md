With Document Capture version 8.00 and Expense Management version 8.00, Continia Software is releasing a combined upgrade guide that our partners can use to upgrade Document Capture 7.00, Expense Management 7.00 or a system with both Document Capture 7.00 and Expense Management 7.00 installed.

> [!IMPORTANT]
> This upgrade guide can only be used with the versions of Dynamics NAV that supports the new Data Upgrade Tools from Microsoft. (Microsoft Dynamics NAV 2016 and above).

This upgrade guide describes the upgrade of Document Capture and Expense Management using the more automated Data Upgrade on the version of NAV (NAV 2016 to BC14) currently used with Document Capture and Expense Management.

If the Dynamics NAV version does not support Data Upgrade or you are looking for the manual Pre and Post Upgrade process, please refer to [Manual Upgrade from Version 7.00 to Version 8.00](@EM-30).

If you are using Document Capture or Expense Management in Microsoft Business Central Cloud, the main upgrade will be performed automatically when you install Document Capture 8.00.

Migration from FOB-based version of NAV/BC to On-Premises Extension and/or Cloud: See [this article on the Continia PartnerZone](https://continia.zendesk.com/hc/da/articles/360015942380-Overview-Migrating-from-BC14-FOB-based-to-BC15-or-newer-versions-On-Premises-and-or-Cloud-).

This upgrade guide can be used with the following versions of Document Capture and Expense Management:

**Document Capture**
* Document Capture 7.00 with any service pack

**Expense Management** 
* Expense Management 7.00 with any service pack

If the system is running an older version, you must first upgrade to the required versions.

In this version, we have upgraded the Document Capture Client Components and Server Components, and you must update these components before you start working with Document Capture and Expense Management. This guide will instruct you how to do this correctly. The Document Capture and Expense Management objects in this version are not backwards-compatible with older components, and the components in this version are not backwards-compatible with older objects.

If Document Capture and Expense Management are not already installed, you should not use any information in this document. Please see the Quick Guide for installing Document Capture or Expense Management.

## Task 1: Check minimum version requirements

Please be sure that the current system is running one of the supported versions of Document Capture or Expense Management listed in the summary section. If not, it is very important you follow the upgrade guide from an earlier version to DC7.00 and or EM7.00. Previous upgrade guides can be found here:

For Document Capture: https://continia.zendesk.com/hc/en-us/sections/201853305-Upgrade-Guides 

For Expense Management: https://continia.zendesk.com/hc/da/sections/360000175700-Upgrade-Guides

## Task 2: Import updated NAV license file

The upgrade process must be performed using a developer license.

After the upgrade please ensure to use a new/updated customer license file from Microsoft and import it into NAV. 

If you are using the Dynamics NAV Server, you must restart the Dynamics NAV Server to use the new license.

## Task 3: Merge objects

If you have modified your customer's system, then check if any of the modified objects conflict with Document Capture or Expense Management objects and merge if necessary. You should merge objects in a test system, so they are ready to be imported later in the upgrade process.

## Task 4: Install all tools and components

You must perform all installations described below from the Document Capture Setup executable, located in the root of the product folder (Setup.exe).

> [!NOTE]
> The installer will update the add-ins folder (Client and/or Server) in the standard installation path. Therefore, if your installation path differs from the standard Microsoft path, make sure to copy the new add-in folder to the folder your installation resides in.

## Task 5: Upgrade server components

To upgrade your server components, follow one of the guides below, depending on your version of NAV/Business Central:

<br>

| Version | Guide |
| --- | --- |
| NAV Server 2016 -> BC14 | Only perform the following steps if you are using Dynamics NAV 2016 -> Microsoft Dynamics 365 Business Central Spring 2019 Update (BC14): <ol><li>Stop &ldquo;Microsoft Dynamics NAV Server&rdquo;.</li><li>Uninstall &ldquo;Document Capture RTC Server Components&rdquo;.</li><li>Install &ldquo;Document Capture RTC Server Components&rdquo;.</li><li>If you haven&rsquo;t installed the Microsoft Dynamics NAV Server in the default location, you must move the Add-ins manually from the default location to the current location of your installation.</li><li>Start &ldquo;Microsoft Dynamics NAV Server&rdquo;.</li></ol> |
| NAV RTC Upgrade PC | Only perform the following steps if you are using Dynamics NAV RTC: <ol><li>On the computer where you perform the upgrade, you must uninstall &rdquo;Document Capture RTC Client&rdquo; and &rdquo;Document Capture RTC Components (Scanner)&rdquo;.</li><li>Install &ldquo;Document Capture RTC Client&rdquo;.</li><li>Install &ldquo;Document Capture RTC Component (Scanner)&rdquo; if needed.</li><li>If you haven&rsquo;t installed the Microsoft Dynamics NAV RTC Client in the default location, you must move the Add-ins manually from the default location to the current location of your installation.</li></ol> |

## Task 6: Update NAV objects and data

> [!IMPORTANT]
> Before doing object modifications or starting the data upgrade, make sure to back up the database.

Import the new DC8.00 / EM8.00 objects from the product folder. Please note, some objects may show a warning during import as some parts of the new Version List has changed format. Use “Replace All” in Import Worksheet. Set Synchronize Schema to “Later” during object import.

> [!WARNING]
> For all versions from NAV 2013 to Business Central October 2018 (BC v13), the following applies: When importing the DC8.00/EM8.00 object package, please skip the 4 pages mentioned below. The pages were unintentionally included in the release packages – they will be removed in service pack 1.
>
>* Page 5 **Currencies**
>* Page 10 **Countries/Regions**
>* Page 209 **Units of Measure**
>* Page 472 **VAT Posting Setup**

## Task 7: Data upgrade

Follow below to complete the Post-Upgrade step:

1. Import the object package named “(Your NAV version) - Document Capture 8.00, Expense Management 8.00 - DataUpgrade.fob”. Use “Replace All” in Import Worksheet. Set Synchronize Schema to “Later” during import.
2. Compile all Document Capture and Expense Management objects (Version List filter \*DC\*|\*EM\*|\*CC\*|\*DN\*). Set Synchronize Schema to “**Later**”.
3. Compile all MenuSuites (not only DC and EM).
4. Run Tools -> “Sync. Schema For All Tables” -> “**With Validation**”.
5. Run Tools -> “Data Upgrade” -> “Start…” to open the **Start Data Upgrade** page.
6. Under **Execution Mode**, select **Serial**, and then clear the checkbox under **Continue on Error**. Select **OK** to close the page.

The Data Upgrade process should complete without any errors.

### Data upgrade troubleshooting

1. In case the Data Upgrade fails, you will have to run the Get-NAVDataUpgrade [ServerInstance] -ErrorOnly powershell command to find out what the actual error is or use the debugger with “Debug Next”.
1. If the Error message looks like “Function 'UpdatePerDatabase' in the upgrade codeunit '6086102' has failed because of the following error: 'A call to System.Net.WebClient.DownloadData failed with this message: The remote server returned an error: (404) Not Found.'.” this means that there is a problem downloading the Control Add-in resources. This problem can occur when our services are down, or it could be a server Firewall problem.
1. You can choose to try again by Running Tools -> “Data Upgrade” -> “Resume…”.
1. If the same error is thrown, you can Design Codeunit 6086102 and comment the following line of code:  CODEUNIT.RUN(CODEUNIT::"CDC Capture RTC Library");
1. Then Run Tools -> “Data Upgrade” -> “Resume…”.
1. This will skip the downloading of the Control Add-in when upgrading therefore you must download them manually after the Data Upgrade from Document Capture Setup page: On the **Actions** tab, select **Import Continia Web Client Add-Ins** and **Import Client Add-Ins** to import all relevant add-ins.

## Task 8: Upgrade client components

To upgrade your client components, follow one of the guides below, depending on your version of NAV/Business Central:

<br>

| Version | Guide |
| --- | --- |
| NAV RTC Clients 2016 | Only perform the following steps if you are using Dynamics NAV 2016: <ol><li>Uninstall &ldquo;Document Capture RTC Client Components&rdquo;.</li><li>Install &ldquo;Document Capture RTC Client Components&rdquo;.</li></ol> |
| NAV RTC Clients 2017 -> BC14 | <ol><li>Uninstall &ldquo;Document Capture RTC Client&rdquo;.</li><li>Uninstall &rdquo;Document Capture RTC Components (Scanner)&rdquo;.</li><li>Client Add-ins are now automatically distributed to all NAV clients when needed.</li></ol> |

## Task 9: Delete upgrade objects

After completing the upgrade please remove the upgrade objects (All object types, with Force):

Filter: 6086100..6086199

> [!NOTE]
> On versions before NAV 2015, upgrade tables must be emptied manually prior to deletion.

## Task 10: Update the Continia Web Approval Portal

To update the Continia Web Portal, follow these steps:

1. If you are using NAV objects below NAV 2009 R2, you will need to import the updated Web Portal objects from the product folder. For NAV 2009 R2 and later versions, these objects will be included in the base package.
2. Compile all Document Capture and Expense Management objects (Version List filter \*DC\*|\*EM\*|\*CC\*|\*DN\*).
3. Run the function “Create Web Services” from the Continia Web Portal list. It is only required to run this function in one company.
4. If you continue to use Continia Web Portal On-Premise, then create a new Web Site in IIS or update the existing one.
5. Run the function “Export Users” to export web users from the Continia Users screen in NAV.

## Related information
[Manual Upgrade from Version 7.00 to Version 8.00](@EM-30)  





<style>
  .content table tr td:nth-child(1) {
    width: 130px;
  }
  .content table tr td:nth-child(2) {
    width: 600px;
  }  
</style>