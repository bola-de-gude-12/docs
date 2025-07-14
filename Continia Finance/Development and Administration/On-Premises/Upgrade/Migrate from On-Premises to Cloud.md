---
title: Migrating Continia Finance from Business Central On-Premises to Cloud
date: 29-08-2024
description:  
id: CF-26
lang: en
---

# Migrating Continia Finance from Business Central On-Premises to Cloud

If your organization uses Continia Finance in Microsoft Dynamics Business Central on-premises but would like to move to the cloud, you can migrate to Business Central online using the guide below.

The migration of Continia Finance to Business Central online is based on Microsoft's standard cloud migration tool. For more details, see [Migrate On-Premises Data to Business Central Online](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data) (Microsoft article).

## To migrate data to the cloud

To migrate your data to Business Central online, carry out the following steps in your online environment:

1. Run the Microsoft cloud migration tool: Choose the {{search}} icon, enter **Cloud Migration Setup**, and then choose the related link to open the **Cloud Migration Setup** guide. For more information, see [Run the assisted setup guide](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data#run-the-assisted-setup-guide) (Microsoft article).

1. Follow the on-screen instructions to complete the guide.

   >[!IMPORTANT]
   >Note that you can't use your demo credentials in a production environment. To perform a test migration, please use a sandbox environment instead.
   >
   >To avoid interrupting the migration process, don't use Continia Finance while the cloud migration tool is running.

1. Disable cloud migration, and define user mappings between on-premises and cloud. For more information, see "Disable Cloud Migration" and "Define User Mappings" in the table under [Manage the migration](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data#manage-the-migration) (Microsoft article).

1. In the Role Center, the following notification is now displayed: "Continia Finance has been migrated from On-premises to Cloud. Would you like to activate it?". Select **Yes** to open the activation guide.

1. Complete the guide to activate Continia Finance as a cloud solution. As you complete the guide, be sure to check that your client credentials are correct.

All Continia Finance data has now been migrated, and the app is ready for use in Business Central online.

> [!IMPORTANT]
> When you migrate to Business Central online as described above, client credentials (client ID and password) are copied from your on-premises environment to the online one – no matter what type of environment you're migrating from (production or test) and to (production or sandbox).
> 
> However, when you disable cloud migration (step 4 above), the type of online environment is important:
> * **If you're migrating to a sandbox environment**, your original client credentials are automatically deleted. When you then activate Continia Finance as a cloud solution (steps 5-6 above), new client credentials are created.
> * **If you're migrating to a production environment**, your existing client credentials are reused for the online environment.

## Notifying Continia about the migration

When you migrate a Continia solution like Continia Finance from an on-premises environment to the cloud, it's important that you take the necessary steps described below to ensure that the invoicing process remains smooth and trouble-free:

As a partner or customer, it’s your responsibility to terminate your on-premises agreement with Continia once you've migrated the entire solution and it's fully operational in the cloud. Most customers migrate their solutions gradually during a period of transition that can last up to several months, but the process varies from organization to organization. In any case, once the migration process is complete, you must inform Continia about the termination by sending an email to accounting@continia.com. You'll then be credited for the remainder of your on-premises billing period.

> [!IMPORTANT]
> For administrative purposes, please let us know about the termination before you're invoiced for a 12-month renewal of your on-premises agreement.

