---
title: Migrating Document Output from Business Central On-Premises to Cloud
date: 23-09-2024
description:
id: DO-128
lang: en
---

# Migrating Document Output from Business Central On-Premises to Cloud

If your organization currently uses Continia Document Output in Microsoft Dynamics NAV/Business Central on-premises but would like to move to the cloud, you can easily migrate to Business Central online using the guide below.

The migration of Document Output to Business Central online is based on Microsoft's standard cloud migration tool. For more details, see [Migrating On-Premises Data to Business Central Online](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data).

## To migrate from on-premises to cloud

1. Upgrade to the latest on-premises version of Business Central using [this Microsoft guide](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrading-to-business-central).
1. Upgrade Document Output to the version that matches the one currently available in [Microsoft AppSource](https://appsource.microsoft.com/).
1. In Document Output, do the following for all companies in the database: 
   1. Open **Document Output Setup**.
   1. If **Log Storage Type** is set to **File System**, it must be changed to **Database**. This will move all files from the file share into the database.

   > [!IMPORTANT]
   > Emails must be available on the file share when they're moved into the database.

1. Run the Microsoft cloud migration tool. For more information, see [this Microsoft article](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migration-setup). When running the tool, follow the instructions in the **Cloud Migration Setup** guide in Business Central. 

   > [!IMPORTANT]
   > To avoid importing data from production, Document Output isn't activated when the cloud migration tool is running.

1. Disable cloud migration, and define user mappings between on-premises and cloud. For more information, see "Disable Cloud Migration" and "Define User Mappings" in [this Microsoft article](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migration-finish).
1. In the Business Central Role Center, the following notification is now displayed: "Continia Document Output has been migrated from On-premises to Cloud. Would you like to activate it?" Select **Yes** to open the activation guide.
1. Complete the guide to activate Document Output as a cloud solution.

## See also
[Migrating On-Premises Data to Business Central Online](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data).  