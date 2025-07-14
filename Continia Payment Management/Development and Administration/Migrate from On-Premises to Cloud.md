---
title: Migrating Continia Payment Management from Dynamics 365 Business Central On-Premises to Cloud
date: 24-02-2025
description: Information on how to migrate Payment Management from the Dynamics 365 Business Central On-Premises to Cloud
id: PM-192
lang: en
---

# Migrating Business Central On-Premises to Cloud

If your organization currently uses Continia Payment Management in Microsoft Dynamics NAV/Business Central on-premises but wants to move to the cloud, you can easily migrate to Business Central online using the guide below.

The migration of Payment Management to Business Central online is based on Microsoft's standard cloud migration tool. For more details, see [Migrate On-Premises Data to Business Central Online](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data) (Microsoft article).

## To prepare your on-premises environment for cloud migration

Before migrating any data to Business Central online, you must carry out the following steps in your on-premises environment:

* Upgrade to the [latest available version](@PM-376) of Business Central and Payment Management. To do this, see [Upgrading to the latest version](@PM-17) article.

## To migrate data to the cloud

Once you've prepared your on-premises environment for migration, you're ready to migrate data to Business Central online. 

To migrate data to the cloud:

1. Run the Microsoft cloud migration tool: select the {{search}} icon, enter **Cloud Migration Setup**, and then select the related link. 

2. Follow the on-screen instructions to complete the guide.

   > [!IMPORTANT]
   >
   > You can't use Payment Management when the cloud migration tool is running to avoid interrupting the migration process.

3. Once the migration process is complete, go through the Post Migration Checklist steps to ensure that all necessary actions have been carried out.

4. Disable cloud migration and define user mappings between on-premises and cloud. For more information, refer to the  "Disable Cloud Migration" and "Define User Mappings" sections in the table under [Manage the migration](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data#manage-the-migration) (Microsoft article).

5. In the Role Center, you will see a notification asking if you want to activate Continia Payment Management, which has been migrated to the Cloud. Select **Yes** to complete the guide to activate Payment Management as a cloud solution.

   All Payment Management data has now been migrated, and the app is ready for use in Business Central online.

> [!IMPORTANT]
>
> When you follow the migration process to move to Business Central online, the client credentials (client ID and password) from your on-premises environment will be copied to the online environment. This applies to both production and test environments. However, when you disable cloud migration, the type of online environment is important:
>
> * Your original client credentials are automatically deleted if you're migrating to a sandbox environment. When you activate Payment Management as a cloud solution, new client credentials are created.
> * **If you're migrating to a production environment**, your existing client credentials are reused for the online environment.

 

## To create a certificate
When migrating from On-prem to Cloud, you can reuse your User Number/Function ID, but you must request a new code from your bank. During the setup of your bank accounts in the [Bank Account Setup](@PM-3#to-set-up-company-bank-accounts), you will be prompted to enter the new code. This ensures that the old certificate is securely closed and that files are correctly imported into the new Cloud App.

## To notify Continia about the migration

When moving a Continia solution, such as Payment Management, from on-premises to the cloud, ensure a smooth transition:

1. Terminate your on-premises agreement with Continia once the cloud solution is fully operational. The migration period's duration can vary but is usually a few months.

2. After completing the migration, inform Continia by emailing accounting@continia.com. You'll receive a credit for the remaining on-premises billing period.

   > [!IMPORTANT]
   >
   > For administrative purposes, please inform us about the termination before you're invoiced for a 12-month renewal of your on-premises agreement.
