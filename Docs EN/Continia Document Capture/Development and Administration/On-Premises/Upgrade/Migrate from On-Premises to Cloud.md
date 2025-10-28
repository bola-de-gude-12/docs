---
title: Migrating Document Capture from Business Central on premises to cloud
date: 15-09-2025
description: How to migrate Document Capture from Business Central on premises to cloud.
id: DC-106
lang: en
---

# Migrating Document Capture from Business Central on premises to cloud

If your organization uses Continia Document Capture in Microsoft Dynamics NAV/Business Central on premises but would like to move to the cloud, you can migrate to Business Central online using the guide below.

The migration of Document Capture to Business Central online is based on Microsoft's standard cloud migration tool. For more details, see [Migrate on-premises data to Business Central Online](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data) (Microsoft article).

>[!NOTE]
>Starting in 2025 release wave 1 (v26), the direct upgrade from Business Central 2019 (v14) to the latest release isn't supported. The supported upgrade path is through 2024 release wave 2 (v25), then to the latest version. For more information, see [Deprecated features in the platform - clients, server, and database](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-platform#changes-in-2025-release-wave-1-version-260) (Microsoft article).

## Considerations when migrating to the cloud

The following are some of the most important considerations to make – and things to note – before migrating:

- The **File System**/**File Service** storage type isn't available in Business Central online, so you have to select a different storage type (i.e.: **Database** or **Azure Blob Storage**) before migrating.
- If you choose **Database**, all documents are saved in the database, thereby taking up database storage space and making the transfer of data to Business Central online more time-consuming. In case you have a lot of data to transfer, you may want to consider selecting **Azure Blob Storage** instead, as you have limited space available (80 GB plus additional storage capacity, based on your number of Business Central licenses) – unless you purchase additional space, which can be costly. For more information, see the **Storage** section in the [Managing capacity](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-capacity#storage) article (Microsoft article).
- If you select **Azure Blob Storage**, it's recommended that you change to this storage type before initiating the migration. This makes it much faster for you to transfer your database to Business Central online, as there are no documents stored in the database. For more information, see [Setting up Azure Blob Storage](https://docs.continia.com/en-us/continia-document-capture/development-and-administration/setting-up-azure-blob-storage).
- Once you've migrated to Business Central online, you can no longer use on-premises OCR.

>[!NOTE]
>It’s no longer required to run the pre-migration wizard to convert from TIFF to PNG files, as these are now generated on-the-fly when accessing documents.

For more information on storage types and how to set them up, see [Setting up document storage](@DC-3).

## To prepare your on-premises environment for cloud migration

Before migrating any data to Business Central online, you must carry out the following steps in your on-premises environment:

1. Upgrade to Business Central April 2024 release wave 2 (BC v25) or later, unless you did so at an earlier point. To do this, see [Upgrading NAV/Business Central with Document Capture installed](Upgrading NAV or Business Central with Document Capture installed/Overview.md).

1. Upgrade to Document Capture 2024 R2 (25.00) or later, unless you've already done so.

>[!NOTE]
>There's a direct upgrade path from Document Capture 4.50 or later to Document Capture 2021 R2 (8.00), but upgrading from a version earlier than Document Capture 4.50 requires multiple manual steps.

## To migrate data to the cloud

Once you've prepared your on-premises environment for migration [as described above](#to-prepare-your-on-premises-environment-for-cloud-migration), [install and configure Document Capture](@DC-214) in Business Central online. When you're done with this process, you can migrate your data to Business Central online. To do this, carry out the following steps in your new online environment:

1. Run the Microsoft cloud migration tool: Search ({{search}}) for and select **Cloud Migration Setup** to open the **Cloud Migration Setup** guide. For more information, see [Run the assisted setup guide](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data#run-the-assisted-setup-guide) (Microsoft article).
1. Follow the on-screen instructions to complete the guide.

   >[!IMPORTANT]
   >Note that you can't use your demo credentials in a production environment. To perform a test migration, use a sandbox environment instead.
   >To avoid interrupting the migration process, don't use Document Capture while the cloud migration tool is running.

1. Once the migration process is complete, go through the steps of the **Post Migration Checklist** to make sure that all necessary actions have been carried out.
1. Disable cloud migration, and define user mappings between on premises and cloud. For more information, see 'Disable Cloud Migration' and 'Define User Mappings' in the table under [Manage the migration](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data#manage-the-migration) (Microsoft article).
1. In the Role Center, the following notification is now displayed: "Continia Document Capture has been migrated from on premises to cloud. Would you like to activate it?". Click **Yes** to open the activation guide.
1. Complete the guide to activate Document Capture as a cloud solution. As you complete the guide, be sure to check that your client credentials are correct.

   >[!NOTE]
   >If the Continia Web Approval Portal was enabled in the old on-premises environment, you must set it up again. For more information, see [Setting up Web Approval](@DC-76).

All Document Capture data has now been migrated, and the app is ready for use in Business Central online.

>[!IMPORTANT]
>When you migrate to Business Central online as described above, client credentials (client ID and password) are copied from your on-premises environment to the online one – no matter what type of environment you're migrating from (production or test) and to (production or sandbox).
>
>However, when you disable cloud migration (step 4 above), the type of online environment is important:
>
>- **If you're migrating to a sandbox environment**, your original client credentials are automatically deleted. When you then activate Document Capture as a cloud solution (steps 5-6 above), new client credentials are created.
>- **If you're migrating to a production environment**, your existing client credentials are reused for the online environment.

## Notifying Continia about the migration

When you migrate a Continia solution like Document Capture from an on-premises environment to the cloud, it's important that you take the necessary steps described below to ensure that the invoicing process remains smooth and trouble-free.

As a partner or customer, it’s your responsibility to terminate your on-premises agreement with Continia once you've migrated the entire solution and it's fully operational in the cloud. Most customers migrate their solutions gradually during a period of transition that can last up to several months, but the process varies from organization to organization. In any case, once the migration process is complete, you must inform Continia about the termination by sending an email to accounting@continia.com. You'll then be credited for the remainder of your on-premises billing period.

>[!IMPORTANT]
>For administrative purposes, make sure to inform Continia about the termination before you're invoiced for a 12-month renewal of your on-premises agreement.

## Related information

[How to migrate DC and EM to Business Central 2021 release wave 1 (BC18) in BC cloud](https://continia.zendesk.com/hc/en-us/articles/360014053519-How-to-migrate-Document-Capture-and-Expense-Management-to-Microsoft-Dynamics-365-Business-Central-2020-release-wave-2-BC17-in-Microsoft-Business-Central-cloud?_ga=2.13216625.79067120.1621259529-972812024.1595933616)  
[Setting up document storage](@DC-3)
