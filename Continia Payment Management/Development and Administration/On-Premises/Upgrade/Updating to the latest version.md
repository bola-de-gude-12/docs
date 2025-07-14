---
title: Upgrading Payment Management for app Versions of Business Central
date: 24-02-2025
description: Upgrading Payment Management for app Versions of Business Central
id: PM-17
lang: en
---

# Upgrading Payment Management for app Versions of Business Central

This article describes how to upgrade Payment Management for app versions of Microsoft Dynamics 365 Business Central. 

All upgrade packages are completely free of charge, and we recommend that you upgrade regularly to benefit from all the new features that are continually added to the application. Note that your Continia partner must assist you whenever you carry out an upgrade.

> [!TIP]
>
> Need information on the **on-premises** versions? Refer to the [Supported On-Premises Versions of Business Central](@PM-376) article.

## To upgrade Payment Management

Continia has developed a PowerShell script in order to simplify the upgrade process, which ensures that Payment Management is upgraded correctly and that all dependencies work as intended.

When you execute the script, it automatically scans the folder that it's executed in (including all subfolders) for any existing instances of Payment Management and other Continia apps. If it detects a previous version of an app, it upgrades the app and all dependencies and then uninstalls all old versions. If no app is detected, the script automatically installs the app along with any other necessary apps.

To upgrade Payment Management using this script, follow these steps:

1. Go to the [Continia PartnerZone](https://partnerzone.continia.com).
1. In the menu at the top, select **Downloads**.
1. Use the filters to locate the latest version of Payment Management, and select **Download** to download the upgrade package. 
1. Once you've downloaded the installation package, you must unblock it in order to be able to extract it properly. Right-click the downloaded file, and select **Properties** to open the file properties window.
1. On the **General** tab, under **Security**, select **Unblock** and then **Apply**. Close the window when you're done.
1. To execute the install script, do one of the following:

    * In the folder you selected in the previous step, right-click on **Install.ps1** and select **Run with PowerShell**.

    * Run the script from a PowerShell shell.

      > [!IMPORTANT]
      >
      > The Install.ps1 script doesn't support upgrading in multi-tenant environments. To upgrade Payment Management in multi-tenant environments, you must run the commands in the install script manually for your installed Continia solutions.
      >
1. If you have different versions of Business Central installed, select the relevant one in the script. When asked to select the solution you want to install, select Payment Management. Select the server instance where the app should be upgraded.
1. This will initiate the upgrade of Payment Management, which can take 1-2 minutes, depending on the size of your database. On completion, press any key to exit.

    When the upgrade is complete, the previous version of Payment Management is unpublished.

    > [!IMPORTANT]
    >
    > After the upgrade, you must download and use a new and updated customer license file from Microsoft.
