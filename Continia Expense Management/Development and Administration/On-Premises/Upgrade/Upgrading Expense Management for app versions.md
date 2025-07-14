---
title: Upgrading Continia Expense Management for app versions of Business Central
date: 09-07-2025
description: Learn how to how to upgrade Expense Management for app versions of Microsoft Dynamics 365 Business Central
id: EM-254
lang: en
---

# Upgrading Continia Expense Management for app versions of Business Central

> [!NOTE]
> This article describes how to upgrade Expense Management for app versions of Microsoft Dynamics 365 Business Central. For information on how to upgrade Expense Management for _FOB_ versions of Business Central, see [Supported Upgrade Paths for Continia Expense Management (FOB)](@EM-103)

All upgrade packages are free. For best practice, we recommend you upgrade regularly to benefit from all the new features that are regularly being added to the application. Ensure your Continia partner assists you whenever you carry out an upgrade.

## Upgrade Expense Management

To simplify the upgrade process, Continia developed a PowerShell script that ensures Expense Management upgrades correctly and all dependencies work as intended.

When you upgrade Expense Management using the PowerShell script, the Expense Management On Premises app is automatically upgraded along with the Continia Expense Management base app.

The script automatically scans the folder that it's running in (and all subfolders) for any existing instances of Expense Management and other Continia apps. If it detects a previous version of an app, it upgrades it and all its dependencies, then uninstalls all older versions. If no app is detected, the script automatically installs the app along with any other necessary apps.

To upgrade Expense Management using this script:

1. Go to the [Continia PartnerZone](https://partnerzone.continia.com).

1. In the menu at the top, click **Downloads**.

1. Use the filters to locate the latest version of Expense Management, and click **Download** to download the upgrade package.

1. After you've downloaded the installation package, you must unblock it so you can extract it properly: 

   1. Right-click the downloaded file, and click **Properties** to open the file properties window. 
   1. On the **General** tab, under **Security**, click **Unblock**, then **Apply**. 
   1. Close the window.

1. Extract the product package to a folder on your computer. From this folder, run the setup.exe file to open the Expense Management installer.

1. In the installer, click **Server Components**, then select your version of Business Central.

   > [!NOTE]
   > The installer updates the **Add-ins** folder (client and/or server) in the standard installation path. However, if your installation path differs from the standard Microsoft path, you must copy the new **Add-ins** folder into the folder that your installation resides in.

1. In the app folder, select the folder that matches your Business Central version (your platform), including the correct cumulative update. Continia apps are distributed as runtime packages, therefore you must select the right version. Runtime packages are only guaranteed to work if published to a platform that is the same version as the one they were created on.

1. Use one of the methods below to run the install script. If you've different versions of Business Central installed, select the relevant one in the script.

   * In the folder you selected in the previous step, right-click **Install.ps1** and select **Run with PowerShell**.
   * Run the script with PowerShell.

   > [!IMPORTANT]
   > The **Install.ps1** script doesn't support upgrading in multi-tenant environments. To upgrade Expense Management in multi-tenant environments, you must run the commands in the install script manually for your installed Continia solutions. See, [Installing or Upgrading Continia Apps in Multitenant Environments](@EM-253). 

1. Select **Expense Management** for the solution you want to install.

1. Select the server instance where the app will be upgraded.

1. This initiates the upgrade of Expense Management, which takes 1-2 minutes, depending on the size of your database. On completion, press any key to exit. When the upgrade is complete, the previous version of Expense Management is unpublished.

1. After the upgrade, you must download and use a new and updated customer license file from Microsoft.

## Related information

Refer to the following article for more information about upgrade paths:
[Supported Upgrade Paths for Continia Expense Management (FOB)](@EM-103)