---
title: Installing Payment Management On-Premises
description: How to install a Payment Management on-premises in Business Central
date: 16-03-2022
id: PM-64
lang: en
---

# Installing Payment Management On-Premises

This article describes how to install Payment Management in on-premises deployments of Microsoft Dynamics 365 Business Central. Note that you must be assisted by your Continia partner whenever you install the software.

> [!IMPORTANT]
> If you upgrade Business Central to a different version or cumulative upgrade, you must uninstall Payment Management and then install the Payment Management runtime package that corresponds to the new version of Business Central.

Payment Management consists of multiple functional areas, however, not all customers might request the same functionality. To facilitate this, Payment Management contains granules that each represent a small area of functionality. Refer to the [License and granules](@PM-18) article to learn more about configuring your Business Central license file with Payment Management granules.

##To install Payment Management

In order to simplify the installation process, Continia has developed a PowerShell script which ensures that Payment Management is installed correctly and that all dependencies work as intended. 

To install Payment Management using this script, follow these steps:

1. Go to the [Continia PartnerZone](https://partnerzone.continia.com).

1. In the menu at the top, select **Downloads**.

1. Use the filters to locate the latest version of Payment Management, and select **Download** to download the installation package.

1. Extract the product package to a folder on your computer.

1. In the app folder, select the folder that matches your Business Central version (your platform), including the correct cumulative update.
   > [!NOTE]
   > As Continia apps are distributed as runtime packages, you must select the right version. Runtime packages are guaranteed to work only if published to a platform with the same version as the one on which they were created.
   
1. To execute the install script, do one of the following:
   1. Run Windows PowerShell as an administrator.
   1. In the PowerShell prompt, change the directory to the folder you selected in step 5, and then execute **Install.ps1**.
   
1. If you have different versions of Business Central installed, select the relevant one in the script.

1. When asked to select the solution you want to install, select **Payment Management**.

1. Select the server instance where the app should be installed.

1. This will initiate the installation of payment Management, which can take 1-2 minutes, depending on the size of your database. On completion, press any key to exit.  

When the app is installed, a notification appears asking you to [activate the Payment Management solution](@PM-56). Follow the link in the notification to begin the activation and set up of the solution. 


## Related information
[Continia PartnerZone](https://partnerzone.continia.com/)  
[Managing your solutions](@PM-56)  
[Finding a reseller](@PM-63)  
[Upgrade the solution](@PM-17) 

