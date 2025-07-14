---
title: Installing Continia Document Capture on premises
date: 08-07-2025
description: How to install Document Capture on premises in Business Central.
id: DC-51
lang: en
---

# Installing Continia Document Capture on premises

This article describes how to install Document Capture in on-premises deployments of Microsoft Dynamics 365 Business Central. Note that you must be assisted by your Continia partner whenever you install the software.

The installation process involves runtime packages, as all Continia apps are distributed as such. The reason for this is that any extension in a runtime package – in this case the Document Capture app – can be installed on servers that don't have a developer license. For more information, see [Create runtime packages for Business Central on-premises](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-creating-runtime-packages) (Microsoft article).

Note that Continia releases code for all available cumulative updates (CUs) for Business Central whenever a version of Document Capture is released (applies to both major versions and service packs). Each newly released CU from Microsoft is only supported as of the next service pack released by Continia. If you need to upgrade to a currently unsupported Business Central CU – the latest one, for example – and can't wait until Continia has released a Document Capture service pack that supports this, please reach out to the Continia support team by creating a support ticket. Continia will then provide you with a fully functional package that supports the relevant Business Central CU.

## To install Document Capture
In order to simplify the installation process, Continia has developed a PowerShell script which ensures that Document Capture is installed correctly and that all dependencies work as intended.

When you execute the script, it automatically scans the folder that it's executed in (including all subfolders) for any existing instances of Document Capture and other Continia apps. If it detects a previous version of an app, it upgrades the app and all dependencies and then uninstalls all old versions. If no app is detected, the script automatically installs the app along with any other necessary apps.

> [!NOTE]
> Document Capture consists of two apps:
> * **Continia Document Capture** - the base app, which contains most of the functionality. This app is identical with the app released in Business Central online.
> * **Continia Document Capture OnPremise** - an app that gives you access to features only available in on-premises installations of Business Central. This app is necessary if you want to use the document storage type **File System** or the on-premises OCR service, which also requires access to the file system.
> When you install Document Capture using the PowerShell script as described in this guide, **the Document Capture OnPremise app is not installed by default**. To install this, follow step 12 in the guide. Also, note that you must install the Document Capture server components (service tier libraries) before publishing and installing the OnPremise app.

To install Document Capture using this script:

1. Go to the [Continia PartnerZone](https://partnerzone.continia.com).
1. In the menu at the top, click **Downloads**.
1. Use the filters to locate the latest version of Document Capture, and click **Download** to download the installation package.

   > [!IMPORTANT]
   > Once you've downloaded the installation package, you must unblock it in order to be able to extract it properly:
   > 1. Right-click the downloaded file, and select **Properties** to open the file properties window.
   > 1. On the **General** tab, under **Security**, select **Unblock** and then **Apply**. Close the window when you're done.

1. Extract the product package to a folder on the computer with the Business Central Service Tier. From this folder, run the **setup.exe** file to open the Document Capture installer.
1. In the installer, select **Server Components**, and then select your version of Business Central.
   > [!NOTE]
   > The installer will update the **Add-ins** folder (client and/or server) in the standard installation path. So if your installation path differs from the standard Microsoft path, be sure to copy the new **Add-ins** folder to the folder that your installation resides in.
1. In the app folder, select the folder that matches your Business Central version (your platform), including the correct cumulative update.
   > [!IMPORTANT]
   > As Continia apps are distributed as runtime packages, you must select the right version. Runtime packages are guaranteed to work only if published to a platform with the same version as the one on which they were created.
1. To execute the install script, do one of the following:
   * In the folder you selected in the previous step, right-click **Install.ps1** and select **Run with PowerShell**.
   * Run the script from a PowerShell shell.
   > [!IMPORTANT]
   > The **Install.ps1** script doesn't support installation in multi-tenant environments. To install Document Capture in multi-tenant environments, you must run the commands in the install script manually. For more information, see [Installing or Upgrading Continia Apps in Multitenant Environments](@DC-116). 
1. If you have different versions of Business Central installed, select the relevant one in the script.
1. When asked to select the solution you want to install, select **Document Capture**.
1. Select the server instance where the app should be installed.
1. This initiates the installation of Document Capture, which can take 1-2 minutes – depending on the size of your database. On completion, press any key to exit.
1. **Optional:** If you're going to use on-premises functionality (such as file system storage and on-premises OCR), you must install the Continia Document Capture OnPremise app. To do this:
   
   1. Repeat steps 7-11 above, but use **Install-onprem.ps1** instead of **Install.ps1**.
   1. If you're going to use on-premises OCR, follow [this guide](https://continia.zendesk.com/hc/en-us/article_attachments/13795227122450) to install the Continia Document Capture OCR service.

> [!IMPORTANT]
> If you upgrade Business Central to a different version or cumulative upgrade, you must uninstall Document Capture and then install the Document Capture runtime package that corresponds to the new version of Business Central.
>
> For more information, see [Installing upgrades to Business Central on premises](@DC-59).
