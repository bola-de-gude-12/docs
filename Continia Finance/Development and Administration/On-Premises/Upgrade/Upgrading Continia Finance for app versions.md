---
title: Upgrading Continia Finance for app versions of Business Central
date: 27-08-2024
description:
id: CF-25
lang: en
---

# Upgrading Continia Finance for App Versions of Business Central

This article describes how to upgrade Continia Finance for _app_ versions of Microsoft Dynamics 365 Business Central.

All upgrade packages are completely free of charge, and we recommend that you upgrade regularly to benefit from all the new features that are continually added to the application. Note that you must be assisted by your Continia partner whenever you carry out an upgrade.

## To upgrade Continia Finance

In order to simplify the upgrade process, Continia has developed a PowerShell script which ensures that Continia Finance is upgraded correctly and that all dependencies work as intended.

When you execute the script, it automatically scans the folder that it's executed in (including all subfolders) for any existing instances of Continia Finance and other Continia apps. If it detects a previous version of an app, it upgrades the app and all dependencies and then uninstalls all old versions. If no app is detected, the script automatically installs the app along with any other necessary apps.

> [!NOTE]
> When you upgrade Continia Finance using the PowerShell script as described in this guide, the Continia Finance OnPremise app is automatically upgraded along with the Continia Finance base app.

To upgrade Continia Finance using this script, follow these steps:

1. Go to the [Continia PartnerZone](https://partnerzone.continia.com).
1. In the menu at the top, select **Downloads**.
1. Use the filters to locate the latest version of Continia Finance, and select **Download** to download the upgrade package.

   > [!IMPORTANT]
   > Once you've downloaded the installation package, you must unblock it in order to be able to extract it properly:
   > 1. Right-click the downloaded file, and select **Properties** to open the file properties window.
   > 1. On the **General** tab, under **Security**, select **Unblock** and then **Apply**. Close the window when you're done.


1. Extract the product package to a folder on your computer. From this folder, run the setup.exe file to open the Continia Finance installer.
1. In the installer, select **Server Components**, and then select your version of Business Central.
   > [!NOTE]
   > The installer will update the **Add-ins** folder (client and/or server) in the standard installation path. So if your installation path differs from the standard Microsoft path, be sure to copy the new **Add-ins** folder to the folder that your installation resides in.
1. In the app folder, select the folder that matches your Business Central version (your platform), including the correct cumulative update.
   > [!IMPORTANT]
   > As Continia apps are distributed as runtime packages, you must select the right version. Runtime packages are guaranteed to work only if published to a platform with the same version as the one on which they were created.
1. To execute the install script, do one of the following:
   * In the folder you selected in the previous step, right-click on **Install.ps1** and select **Run with PowerShell**.
   * Run the script from a PowerShell shell.
   > [!IMPORTANT]
   > The **Install.ps1** script doesn't support upgrading in multi-tenant environments. To upgrade Continia Finance in multi-tenant environments, you must run the commands in the install script manually for your installed Continia solutions. For more information, see [Installing or Upgrading Continia Apps in Multitenant Environments](@CF-23). 
1. If you have different versions of Business Central installed, select the relevant one in the script.
1. When asked to select the solution you want to install, select **Continia Finance**.
1. Select the server instance where the app should be upgraded.
1. This will initiate the upgrade of Continia Finance, which can take 1-2 minutes, depending on the size of your database. On completion, press any key to exit.

When the upgrade is complete, the previous version of Continia Finance is unpublished.

> [!IMPORTANT]
> After the upgrade, you must download and use a new and updated customer license file from Microsoft.