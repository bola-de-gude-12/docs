---
title: Installing Continia Finance On-Premises
date: 27-08-2024
description: How to install Continia Finance on-premises in Business Central
id: CF-22
lang: en
---

# Installing Continia Finance On-Premises

This article describes how to install Continia Finance in on-premises deployments of Microsoft Dynamics 365 Business Central. Note that you must be assisted by your Continia partner whenever you install the software.

The installation process involves runtime packages, as all Continia apps are distributed as such. The reason for this is that any extension in a runtime package – in this case the Continia Finance app – can be installed on servers that don't have a developer license. For more information, see [this Microsoft article](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-creating-runtime-packages).

Note that Continia releases code for all available cumulative updates (CUs) for Business Central whenever a version of Continia Finance is released (applies to both major versions and service packs). Each newly released CU from Microsoft is only supported as of the next service pack released by Continia. If you need to upgrade to a currently unsupported Business Central CU – the latest one, for example – and can't wait until Continia has released a Continia Finance service pack that supports this, please reach out to the Continia support team by creating a support ticket. Continia will then provide you with a fully functional package that supports the relevant Business Central CU.

## To install Continia Finance
In order to simplify the installation process, Continia has developed a PowerShell script which ensures that Continia Finance is installed correctly and that all dependencies work as intended.

When you execute the script, it automatically scans the folder that it's executed in (including all subfolders) for any existing instances of Continia Finance and other Continia apps. If it detects a previous version of an app, it upgrades the app and all dependencies and then uninstalls all old versions. If no app is detected, the script automatically installs the app along with any other necessary apps.

To install Continia Finance using this script, follow these steps:

1. Go to the [Continia PartnerZone](https://partnerzone.continia.com).
1. In the menu at the top, select **Downloads**.
1. Use the filters to locate the latest version of Continia Finance, and select **Download** to download the installation package.

   > [!IMPORTANT]
   > Once you've downloaded the installation package, you must unblock it in order to be able to extract it properly:
   > 1. Right-click the downloaded file, and select **Properties** to open the file properties window.
   > 1. On the **General** tab, under **Security**, select **Unblock** and then **Apply**. Close the window when you're done.

1. Extract the product package to a folder on the computer with the Business Central Service Tier. From this folder, run the setup.exe file to open the Continia Finance installer.
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
   > The **Install.ps1** script doesn't support installation in multi-tenant environments. To install Continia Finance in multi-tenant environments, you must run the commands in the install script manually. For more information, see [Installing or Upgrading Continia Apps in Multitenant Environments](@CF-23). 
1. If you have different versions of Business Central installed, select the relevant one in the script.
1. When asked to select the solution you want to install, select **Continia Finance**.
1. Select the server instance where the app should be installed.
1. This will initiate the installation of Continia Finance, which can take 1-2 minutes, depending on the size of your database. On completion, press any key to exit.

> [!IMPORTANT]
> If you upgrade Business Central to a different version or cumulative upgrade, you must uninstall Continia Finance and then install the Continia Finance runtime package that corresponds to the new version of Business Central.
>
> For more information, see [Installing Upgrades to Business Central On-Premises](@CF-05).

## See also

[Installing Upgrades to Business Central On-Premises](@CF-05)  