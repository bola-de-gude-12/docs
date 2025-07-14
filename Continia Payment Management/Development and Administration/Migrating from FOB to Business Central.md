---
title: Migrating Payment Management from FOB to App
description: How to use the Continia Payment Management migration tool to migrate Payment Management data from the FOB version to the app versions of Business Central.
date: 04-12-2021
id: PM-53
lang: en
---

# Migrating from FOB to App

Continia offers a free migration tool to safely transfer Payment Management data from FOB to app versions of Microsoft Dynamics 365 Business Central (version 15 and later).

> [!NOTE]
>
> To ensure that the installation runs as expected, you should install the app in a sandbox environment before you install it on the host machine.

## Prerequisites

We recommend you familiarize yourself with upgrading to Business Central before migrating data from one system to another. You can find more information on how to upgrade to Microsoft Dynamics 365 Business Central and upgrade considerations on [Microsoft Docs](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrading-to-business-central-online) and [upgrade concerns](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrading-to-business-central-online).

Complete the following actions before using the Payment Management migration tool:

- **Version requirements** - Payment Management version 2.15 or higher, NAV 3.60 or higher.
- **Post open payment entries** - ensure everything is posted in the cash receipt journal, payment journal, and bank account reconciliation. 
- **Export data from Microsoft Dynamics NAV**. - move all standard data before moving the Payment Management data. Microsoft Dynamics 365 has developed the [Cloud Migration Tool](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migration-tool) for this purpose, which we recommended using for the data export. The Continia migration tool can *only* be used when transferring Payment Management data.
- **Upgrade to Microsoft Dynamics 365 Business Central** - set up a Business Central sandbox environment. The upgrade process depends on your current Microsoft Dynamics NAV version. Microsoft Dynamics 365 has made an [overview](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrading-to-business-central-on-premises) of [on-premise](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrading-to-business-central-on-premises) and [online](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-considerations#upgrading-from--to--online) that guides you through the upgrade process.
- **Install and activate Payment Management** - install Payment Management in the sandbox environment before moving the Payment Management data. The assisted Payment Management setup guides must be completed.

  > [!NOTE]
  >
  > When activating Payment Management on-premises, you will be requested to fill in the customer's client credentials. If you haven't received the requested client credentials, please contact Continia by emailing accounting@continia.com containing the customer's Voice ID and your (Microsoft Partner's) email address, or call +45 8230 5000.
  >
- **Download the Continia Payment Management migration tool** - before migrating the Payment Management data, the tool must be downloaded from [Continia PartnerZone](https://partnerzone.continia.com/). On the PartnerZone webpage, navigate to the Download Center, filter by **Payment Management**, and use the tag **Misc** to find the migration tool. After downloading the migration tool, you can start the migration process.

## To export Payment Management data from NAV

1. Open Microsoft Dynamics NAV Development and select **Tools** > **Object Designer**.
1. In the **Object Designer**, select **File** > **Import**.
1. In the migration package downloaded from PartnerZone, select the FOB file from the folder matching the current NAV/BC version:
   * NAV 2009 - W6.00.10
   * NAV 2013 and higher - W7.00.00
   * BC14/BC2019 and higher - W14.00.00
1. Run page **51666**.
1. On the **Perform Data Migration PM** page, enter the following information:
   - **Scope** - select **Setup**. Do *not* select **ALL** or **History**.
   - **Company** - select the given legal entity. If you do not select a legal entity, all legal entities will be included in the file.
   - **Choose the folder for export** - select the path to place the file.
   - **From date/To date** - select the start and end date.
   - **Split setup file lines** - to manage large files, specify the maximum number of records per file by entering a number. The data will be automatically split into multiple files accordingly.
   - **Total setup file lines** - specify the number of records to be exported by entering a number. This ensures the export is limited to the specified number of records.
1. On the action bar, select **Create migration data**.
1. On the action bar, select **Export Migration data**.

## To import the migration file to Business Central

1. Open your Business Central sandbox environment and install Payment Management. For more information about installing the online version of Payment Management, see the article [Installing the Payment Management app](@PM-9).
1. Upload the migration app:
   - **Cloud**: Before migration, note that it might be necessary to renumber the objects in the migration app before installing it in Business Central. This is necessary if another 3rd party product already uses the object numbers. The ID of the objects must be renumbered so that they are within the range of 50000..99999. We recommend that you do this in Microsoft Visual Studio. Once the app is generated, it loads in Business Central.
   - **On-premises**: Find the app located in Continia's Migration Package
1. When the installation is complete, use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Management Migration Main page**, then select the related link.
1. Specify which data you want to import into Business Central on the migration page. You can import data several times to make the import more manageable. 
1. In the action bar, select **Import Migration File**. Data selected for import will now be imported into Business Central.
1. Review and verify the imported data.
1. Once the data has been reviewed and verified, navigate to the action bar and select **Approve Import Suggestion**.

Payment Management data will now be imported into the Payment Management solution in Business Central. We recommend verifying all data and settings before migrating to your production environment. 

When the migration is complete, you can run the standard setup wizards listed in the [Overview of tasks to set up Payment Management](@PM-1).   

> [!IMPORTANT]
>
> When you migrate from Payment Management FOB to the Payment Management app version, you can reuse your User Number/Function ID, but you need to order a new code from your bank. Then, when you set up your bank accounts in the assisted [Bank Account Setup](https://docs.continia.com/en-us/continia-payment-management/setting-up-payment-management/setting-up-bank-information/setting-up-bank-accounts#to-set-up-company-bank-accounts), you will be asked for the new code.   
> 

