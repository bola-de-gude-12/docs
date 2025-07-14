---
title: Installing Continia Document Output On-Premises
description: How to install Document Output on-premises in Business Central
date: 20-08-2021
id: DO-141
lang: en
---

# Installing Continia Document Output On-Premises

This article describes how to install Document Output in on-premises deployments of Microsoft Dynamics 365 Business Central. Note that you must be assisted by your Continia partner whenever you install the software.

## To install Document Output
In order to simplify the installation process, Continia has developed a PowerShell script which ensures that Document Output is installed correctly and that all dependencies work as intended.

To install Document Output using this script, follow these steps:

1. Go to the [Continia PartnerZone](https://partnerzone.continia.com).
1. In the menu at the top, select **Downloads**.
1. Use the filters to locate the latest version of Document Output, and select **Download** to download the installation package.
1. Extract the product package to a folder on the computer with the Business Central Service Tier.
1. Go to Software\Service Tier\\\[Business Central version], and copy the **Continia Doc. Output** folder to the **Add-ins** folder on the relevant server(s).
   > [!NOTE]
   > The **Add-ins** folder is typically located at C:\Program Files\Microsoft Dynamics 365 Business Central\\\[three-digit version number]\Service\Add-ins.
1. Make sure that no DLL files are blocked: For each DLL file in the **Continia Doc. Output** folder that you just copied, right-click the DLL file and select **Properties**. If a security message appears at the bottom of the **General** tab of the **Properties** page, select **Unblock** and then **OK**.
1. In the app folder, select the folder that matches your Business Central version (your platform), including the correct cumulative update.
   > [!NOTE]
   > As Continia apps are distributed as runtime packages, you must select the right version. Runtime packages are guaranteed to work only if published to a platform with the same version as the one on which they were created.
1. To execute the install script, do as follows:
   1. Run Windows PowerShell as an administrator.
   1. In the PowerShell prompt, change the directory to the folder you selected in step 7, and then execute **Install.ps1**.
1. If you have different versions of Business Central installed, select the relevant one in the script.
1. When asked to select the solution you want to install, select **Document Output**.
1. Select the server instance where the app should be installed.
1. This will initiate the installation of Document Output, which can take 1-2 minutes, depending on the size of your database. On completion, press any key to exit.

Following the installation, make sure that your setup is up to date by running the assisted setup guide: In the **Search** box, enter **Setup Wizard** and choose the related link. Then follow the on-screen instructions to complete the guide.

> [!IMPORTANT]
> If you upgrade Business Central to a different version or cumulative upgrade, you must uninstall Document Output and then install the Document Output runtime package that corresponds to the new version of Business Central.