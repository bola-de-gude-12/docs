---
title: Installing Continia Expense Management On-Premises
description: How to install Expense Management on-premises in Business Central
date: 18-08-2021
id: EM-138
lang: en
---

# Installing Continia Expense Management On-Premises

This article describes how to install Expense Management in on-premises deployments of Microsoft Dynamics 365 Business Central. Note that you must be assisted by your Continia partner whenever you install the software.

##To install Expense Management
In order to simplify the installation process, Continia has developed a PowerShell script which ensures that Expense Management is installed correctly and that all dependencies work as intended.

To install Expense Management using this script, follow these steps:

1. Go to the [Continia PartnerZone](https://partnerzone.continia.com).
1. In the menu at the top, select **Downloads**.
1. Use the filters to locate the latest version of Expense Management, and select **Download** to download the installation package.
1. Extract the product package to a folder on the computer with the Business Central Service Tier. From this folder, run the setup.exe file to open the Expense Management installer.
1. In the installer, select **Server Components**, and then select your version of Business Central.
   > [!NOTE]
   > The installer will update the **Add-ins** folder (client and/or server) in the standard installation path. So if your installation path differs from the standard Microsoft path, be sure to copy the new **Add-ins** folder to the folder that your installation resides in.
1. In the app folder, select the folder that matches your Business Central version (your platform), including the correct cumulative update.
   > [!NOTE]
   > As Continia apps are distributed as runtime packages, you must select the right version. Runtime packages are guaranteed to work only if published to a platform with the same version as the one on which they were created.
1. To execute the install script, do as follows:
   1. Run Windows PowerShell as an administrator.
   1. In the PowerShell prompt, change the directory to the folder you selected in step 6, and then execute **Install.ps1**.
1. If you have different versions of Business Central installed, select the relevant one in the script.
1. When asked to select the solution you want to install, select **Expense Management**.
1. Select the server instance where the app should be installed.
1. This will initiate the installation of Expense Management, which can take 1-2 minutes, depending on the size of your database. On completion, press any key to exit.

> [!IMPORTANT]
> If you upgrade Business Central to a different version or cumulative upgrade, you must uninstall Expense Management and then install the Expense Management runtime package that corresponds to the new version of Business Central.