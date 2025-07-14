---
title: Migrating Expense Management from Business Central On-Premises to Cloud
date: 09-07-2025
description:  
id: EM-112
lang: en
---

# Migrating Expense Management from Business Central On-Premises to Cloud

If your organization currently uses Continia Expense Management in Microsoft Dynamics NAV/Business Central on-premises, but wants to move to the cloud, use this guide to migrate to Business Central online.

Migrating Expense Management to Business Central online is based on Microsoft's standard cloud migration tool. For more details, see Microsoft's documentation [Migrate On-Premises Data to Business Central Online](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data).

## Document storage type considerations when migrating to the cloud

*Before* migrating, you must set your **Document Storage Type**. We recommend that you set it to Database, based on the following considerations:

* The **File System**/**File Service** storage type isn't available in Business Central online, so you have to select a different storage type (i.e. **Database** or **Azure Blob Storage** before migrating. 
* If you have a lot of documents, the **Database** storage type saves all documents in the database for migration and ensures no files are missed. Bear in mind that documents take up database storage space and can make the transfer of data to Business Central online more time-consuming. Unless you purchase additional space, which can be costly, you have limited space available (80 GB plus additional storage capacity, depending on your number of Business Central licenses). For more information, see [this Microsoft article](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-capacity#storage).
* If you have a lot of data to transfer but no documents, it's much faster for you to transfer your database to Business Central online, as there are no documents stored in it. If you prefer to use **Azure Blob Storage**, you can change to this *after* the migration.

For more information on storage types and how to set them up, see [Setting up Document Storage](@EM-144).

## Pre requisites

Before migrating any data to Business Central online, you must carry out the following steps in your on-premises environment to prepare it for cloud migration.

1. Upgrade to Business Central April 2019 (BC v14) or later, unless you've already done so at an earlier point. To do this, see [Upgrading NAV/Business Central with Expense Management Installed](@EM-107).
1. Upgrade to Expense Management 2021 R2 (8.00) or later, unless you've already done so.
1. As mentioned in the previous section, you must set **Document Storage Type** to **Database** at the time of migration – otherwise, no files will be migrated. If necessary, you can change the storage type later, (for example **Azure Blob Storage**). However, **File System** storage type isn't available in Business Central online.

> [!NOTE]
> Previously, you had to upgrade to the latest available versions of both Business Central and Expense Management to migrate to the cloud. This is no longer necessary if you use version 24.1.0 or later of Expense Management in your Business Central online environment (target).

## Migrating data to the cloud

After you've prepared your on-premises environment for migration, you're ready to migrate your data to Business Central online. To do this, carry out the following steps in your new online environment:

1. Run the Microsoft cloud migration tool: select the {{search}} icon, enter **Cloud Migration Setup**, then choose the related link to open the **Cloud Migration Setup** guide. For more information, see [Run the assisted setup guide](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data#run-the-assisted-setup-guide) (Microsoft article).
1. Follow the on-screen instructions to complete the guide.

   >[!IMPORTANT]
   >You cannot use Expense Management when the cloud migration tool is running as it will interrupt the migration process.

1. After the migration process is complete, go through the steps of the **Post Migration Checklist** to ensure you've carried out all necessary actions.

   > [!IMPORTANT]
   > 
   > Before you disable cloud migration, consider the type of online environment you've migrated to:
   > * **If you've migrated to a sandbox environment**, your original client credentials are automatically deleted. When you then activate Expense Management as a cloud solution (steps 5-6), new client credentials are created.
   > * **If you've migrated to a production environment**, your existing client credentials are reused for the online environment.
1. Disable cloud migration, and define user mappings between on-premises and cloud. For more information, see "Disable Cloud Migration" and "Define User Mappings" in the table under [Manage the migration](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data#manage-the-migration) (Microsoft article).
1. In the **Role Center**, you'll see the following notification: "Continia Expense Management has been migrated from On-premises to Cloud. Would you like to activate it?" Select **Yes** to open the activation guide.
1. Complete the guide to activate Expense Management as a cloud solution.

   > [!NOTE]
   > If the Continia Web Approval Portal was enabled in the old on-premises environment, you must set it up again. For more information, see [Setting up Web Approval](@EM-82).

You've now migrated all Expense Management data, and the app is ready for use in Business Central online. When you migrate to Business Central online as described above, client credentials (client ID and password) are copied from your on-premises environment to the online one, regardless of the type of environment you're migrating from (production or test) and to (production or sandbox).

## Notifying Continia about the migration

To ensure your invoicing process remains smooth and trouble-free when migrating a Continia solution such as Expense Management from an on-premises environment to the cloud, we recommend you review the following points:

* As a partner or customer, it’s your responsibility to terminate your on-premises agreement with Continia after you've migrated the entire solution and it's fully operational in the cloud. 
* Most customers migrate their solutions gradually during a period of transition that can last up to several months, but the process varies from organization to organization. 
* When the migration process is complete, you must inform Continia about the termination by sending an email to accounting@continia.com, where you'll then be credited for the remainder of your on-premises billing period.

> [!IMPORTANT]
> For administrative purposes, let us know about the termination before you're invoiced for a 12-month renewal of your on-premises agreement.

## Related information
[How to migrate Document Capture and Expense Management to Business Central 2021 release wave 1 (BC18) in BC cloud](https://continia.zendesk.com/hc/en-us/articles/360014053519-How-to-migrate-Document-Capture-and-Expense-Management-to-Microsoft-Dynamics-365-Business-Central-2020-release-wave-2-BC17-in-Microsoft-Business-Central-cloud?_ga=2.13216625.79067120.1621259529-972812024.1595933616)  