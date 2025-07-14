---
title: Installing or Upgrading Continia Apps in Multitenant Environments
date: 09-07-2024
description: How the PowerShell script works in singletenant environments, and how to install or upgrade Continia apps in multitenant environments.
id: EM-253
lang: en
---

# Installing or Upgrading Continia Apps in Multitenant Environments

When you need to install or upgrade one or more Continia apps, the method to use depends on your organization's overall software architecture – more specifically, whether the apps are to be used in a singletenant or a multitenant environment:

* **Singletenant environment:** [Use the fully automated PowerShell script](#using-the-powershell-script-in-a-singletenant-environment) developed by Continia.
* **Multitenant environment:** Execute the script commands manually yourself, [as described below](#executing-the-script-commands-manually-in-a-multitenant-environment).

## Using the PowerShell script in a singletenant environment

Continia has developed a PowerShell script that makes it easy for you to install and upgrade Continia Expense Management and other Continia apps in a singletenant environment. For more information, see [Installing Continia Expense Management On-Premises](@EM-138) and [Upgrading Continia Expense Management for app versions of Business Central](@EM-254).

When you execute the script, it automatically scans the folder that it's executed in (including all subfolders) for any existing instances of Document Capture and other Continia apps. If it detects a previous version of an app, it upgrades the app and all dependencies and then uninstalls all old versions. If no app is detected, the script automatically installs the app along with any other necessary apps.

As indicated above, the script doesn't work in multitenant environments, so if your organization needs Document Capture to run on a server that serves multiple tenants, you must install and/or upgrade Document Capture yourself by running the script commands manually in each relevant tenant instead. This process is described in more detail in the following section.

## Executing the script commands manually in a multitenant environment

To install or upgrade Continia apps in a multitenant environment, you must manually run the commands from the PowerShell script in all relevant tenants. For details on how to do this, see the following installation and upgrade guides. Both guides are based on Continia Expense Management as an example, but you can also easily use them to install or upgrade Document Capture – if so, simply skip all steps related to Expense Management.

### To install apps

In order to install Expense Management, you must run the same three commands for each of the listed apps in the following order:

<br>

| Step | App name | Commands |
| --- | --- | --- |
| 1 | Continia Core | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |
| 2 | Continia Delivery Network | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |
| 3 | Document Capture | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |
| 4 | Document Capture OnPremise (optional) | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |
| 5 | Expense Management | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |

### To upgrade apps

In order to upgrade Expense Management, you must install the new versions of the apps using the same three commands for each of the listed apps in the order described below. 

> [!TIP]
> Note that this set of commands is slightly different from the one used in the installation process described above.

<br>

| Step | App name | Commands |
| --- | --- | --- |
| 1 | Continia Core | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |
| 2 | Continia Delivery Network | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |
| 3 | Document Capture | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |
| 4 | Document Capture OnPremise (if used) | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |
| 5 | Expense Management | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |

This will install the new apps and run the upgrade processes. When you're done, you must then uninstall the old versions of the apps by running the following two commands for each of the listed apps in reverse order:

<br>

| Step | App name | Commands |
| --- | --- | --- |
| 1 | Expense Management | Run the commands in this order: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |
| 2 | Document Capture OnPremise (if used) | Run the commands in this order: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |
| 3 | Document Capture | Run the commands in this order: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |
| 4 | Continia Delivery Network | Run the commands in this order: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |
| 5 | Continia Core | Run the commands in this order: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |

## See also

[Installing Continia Expense Management On-Premises](@EM-138)  
[Upgrading Continia Expense Management for app versions of Business Central](@EM-254)  







<style>
.content table tr td:nth-child(1) {
width: 80px;
}
.content table tr td:nth-child(2) {
width: 300px;
}
</style>