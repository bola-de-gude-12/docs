---
title: Continia Finance Installing or Upgrading Continia Apps in Multitenant Environments
date: 27-08-2024
description: How the PowerShell script works in singletenant environments, and how to install or upgrade Continia apps in multitenant environments for Continia Finance.
id: CF-23
lang: en
---

# Installing or Upgrading Continia Apps in Multitenant Environments

When you need to install or upgrade one or more Continia apps, the method to use depends on your organization's overall software architecture – more specifically, whether the apps are to be used in a singletenant or a multitenant environment:

* **Singletenant environment:** [Use the fully automated PowerShell script](#using-the-powershell-script-in-a-singletenant-environment) developed by Continia.
* **Multitenant environment:** Execute the script commands manually yourself, [as described below](#executing-the-script-commands-manually-in-a-multitenant-environment).

## Using the PowerShell script in a singletenant environment

Continia has developed a PowerShell script that makes it easy for you to install and upgrade Continia Finance and other Continia apps in a singletenant environment. For more information, see [Installing Continia Finance On-Premises](@CF-22).

When you execute the script, it automatically scans the folder that it's executed in (including all subfolders) for any existing instances of Continia Finance and other Continia apps. If it detects a previous version of an app, it upgrades the app and all dependencies and then uninstalls all old versions. If no app is detected, the script automatically installs the app along with any other necessary apps.

As indicated above, the script doesn't work in multitenant environments, so if your organization needs Continia Finance to run on a server that serves multiple tenants, you must install and/or upgrade Continia Finance yourself by running the script commands manually in each relevant tenant instead. This process is described in more detail in the following section.

## Executing the script commands manually in a multitenant environment

To install or upgrade Continia apps in a multitenant environment, you must manually run the commands from the PowerShell script in all relevant tenants. For details on how to do this, see the following installation and upgrade guides. Both guides are based on Continia Finance as an example.

### To install apps

In order to install Continia Finance, you must run the same three commands for each of the listed apps in the following order:

<br>

| Step | App name | Commands |
| --- | --- | --- |
| 1 | Continia Core | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |
| 5 | Continia Finance | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |

### To upgrade apps

In order to upgrade Continia Finance, you must install the new versions of the apps using the same three commands for each of the listed apps in the order described below. 

> [!TIP]
> Note that this set of commands is slightly different from the one used in the installation process described above.

<br>

| Step | App name | Commands |
| --- | --- | --- |
| 1 | Continia Core | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |
| 5 | Continia Finance | Run the commands in this order: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |

This will install the new apps and run the upgrade processes. When you're done, you must then uninstall the old versions of the apps by running the following two commands for each of the listed apps in reverse order:

<br>

| Step | App name | Commands |
| --- | --- | --- |
| 1 | Continia Finance | Run the commands in this order: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |
| 5 | Continia Core | Run the commands in this order: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |

## See also

[Installing Continia Finance On-Premises](@CF-22)  







<style>
.content table tr td:nth-child(1) {
width: 80px;
}
.content table tr td:nth-child(2) {
width: 300px;
}
</style>