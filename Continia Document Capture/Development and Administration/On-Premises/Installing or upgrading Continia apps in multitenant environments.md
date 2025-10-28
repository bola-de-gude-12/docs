---
title: Installing or upgrading Continia apps in multitenant environments
date: 19-09-2025
description: How the PowerShell script works in singletenant environments, and how to install or upgrade Continia apps in multitenant environments.
id: DC-116
lang: en
---

# Installing or upgrading Continia apps in multitenant environments

When you need to install or upgrade one or more Continia apps, the method to use depends on your organization's overall software architecture – more specifically, whether the apps are to be used in a single-tenant or a multitenant environment:

* **Single-tenant environment** - [use the fully automated PowerShell script](#using-the-powershell-script-in-a-single-tenant-environment) developed by Continia.
* **Multitenant environment** - execute the script commands manually, [as described below](#executing-the-script-commands-manually-in-a-multitenant-environment).

## Using the PowerShell script in a single-tenant environment

Continia has developed a PowerShell script that makes it easy for you to install and upgrade Continia Document Capture and other Continia apps in a single-tenant environment. For more information, see [Installing Continia Document Capture on premises](@DC-51) and [Upgrading Continia Document Capture for app versions of Business Central](@DC-6).

When you execute the script, it automatically scans the folder that it's executed in (including all subfolders) for any existing instances of Document Capture and other Continia apps. If it detects a previous version of an app, it upgrades the app and all dependencies and then uninstalls all old versions. If no app is detected, the script automatically installs the app along with any other necessary apps.

As indicated above, the script doesn't work in multitenant environments. If your organization needs Document Capture to run on a server that serves multiple tenants, you must install and/or upgrade Document Capture by running the script commands manually in each relevant tenant instead. This process is described in detail in the following section.

## Executing the script commands manually in a multitenant environment

To install or upgrade Continia apps in a multitenant environment, you must manually run the commands from the PowerShell script in all relevant tenants. For details on how to do this, see the following installation and upgrade guides. Both guides are based on Continia Expense Management as an example, but you can also use them to install or upgrade Document Capture. In this case, simply skip all steps related to Expense Management.

> [!NOTE]
> For both guides, note that the Document Capture OnPremise app is optional. The app gives you access to features only available in on-premises installations of Business Central, and it's necessary if you want to use the document storage type **File System** or the on-premises OCR service, which also requires access to the file system.
> 
> If you decide to install Document Capture OnPremise, note that you must install the Document Capture server components (service tier libraries) before publishing and installing the app.

### To install apps

To install Expense Management, you must run the same three commands for each of the listed apps in the following order:

<br>

| Step | App name | Commands |
| --- | --- | --- |
| 1 | Continia Core | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |
| 2 | Continia Delivery Network | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |
| 3 | Document Capture | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |
| 4 | Document Capture OnPremise (optional) | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |
| 5 | Expense Management | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |

### To upgrade apps

To upgrade Expense Management, you must install the new versions of the apps using the same three commands for each of the listed apps in the order described below. 

> [!NOTE]
> This set of commands is slightly different from the one used in the installation process described above.

<br>

| Step | App name | Commands |
| --- | --- | --- |
| 1 | Continia Core | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |
| 2 | Continia Delivery Network | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |
| 3 | Document Capture | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |
| 4 | Document Capture OnPremise (if used) | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |
| 5 | Expense Management | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |

This installs the new apps and runs the upgrade processes. When you're done, you must then uninstall the old versions of the apps by running the following two commands for each of the listed apps in reverse order:

<br>

| Step | App name | Commands |
| --- | --- | --- |
| 1 | Expense Management | Run the commands in this order: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |
| 2 | Document Capture OnPremise (if used) | Run the commands in this order: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |
| 3 | Document Capture | Run the commands in this order: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |
| 4 | Continia Delivery Network | Run the commands in this order: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |
| 5 | Continia Core | Run the commands in this order: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |

## Related information

[Installing Continia Document Capture on premises](@DC-51)  
[Upgrading Continia Document Capture for app versions of Business Central](@DC-6)  







<style>
.content table tr td:nth-child(1) {
width: 80px;
}
.content table tr td:nth-child(2) {
width: 300px;
}
</style>