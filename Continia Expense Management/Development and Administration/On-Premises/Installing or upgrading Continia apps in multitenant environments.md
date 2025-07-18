---
title: Installing or Upgrading Continia Apps in Multitenant Environments
date: 09-07-2024
id: EM-253
lang: en
description: >-
  How the PowerShell script works in singletenant environments, and how to
  install or upgrade Continia apps in multitenant environments.
---

# Installing or Upgrading Continia Apps in Multitenant Environments

When you need to install or upgrade one or more Continia apps, the method to use depends on your organization's overall software architecture – more specifically, whether the apps are to be used in a singletenant or a multitenant environment:

* **Singletenant environment:** [Use the fully automated PowerShell script](<Installing or upgrading Continia apps in multitenant environments.md#using-the-powershell-script-in-a-singletenant-environment>) developed by Continia.
* **Multitenant environment:** Execute the script commands manually yourself, [as described below](<Installing or upgrading Continia apps in multitenant environments.md#executing-the-script-commands-manually-in-a-multitenant-environment>).

## Using the PowerShell script in a singletenant environment

Continia has developed a PowerShell script that makes it easy for you to install and upgrade Continia Expense Management and other Continia apps in a singletenant environment. For more information, see [Installing Continia Expense Management On-Premises](../../../Continia%20Expense%20Management/Development%20and%20Administration/On-Premises/@EM-138/) and [Upgrading Continia Expense Management for app versions of Business Central](../../../Continia%20Expense%20Management/Development%20and%20Administration/On-Premises/@EM-254/).

When you execute the script, it automatically scans the folder that it's executed in (including all subfolders) for any existing instances of Document Capture and other Continia apps. If it detects a previous version of an app, it upgrades the app and all dependencies and then uninstalls all old versions. If no app is detected, the script automatically installs the app along with any other necessary apps.

As indicated above, the script doesn't work in multitenant environments, so if your organization needs Document Capture to run on a server that serves multiple tenants, you must install and/or upgrade Document Capture yourself by running the script commands manually in each relevant tenant instead. This process is described in more detail in the following section.

## Executing the script commands manually in a multitenant environment

To install or upgrade Continia apps in a multitenant environment, you must manually run the commands from the PowerShell script in all relevant tenants. For details on how to do this, see the following installation and upgrade guides. Both guides are based on Continia Expense Management as an example, but you can also easily use them to install or upgrade Document Capture – if so, simply skip all steps related to Expense Management.

### To install apps

In order to install Expense Management, you must run the same three commands for each of the listed apps in the following order:

\


| Step | App name                              | Commands                                                                                                                                            |
| ---- | ------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | Continia Core                         | <p>Run the commands in this order:<br>1. <strong>Publish-NavApp</strong> > 2. <strong>Sync-NavApp</strong> > 3. <strong>Install-NavApp</strong></p> |
| 2    | Continia Delivery Network             | <p>Run the commands in this order:<br>1. <strong>Publish-NavApp</strong> > 2. <strong>Sync-NavApp</strong> > 3. <strong>Install-NavApp</strong></p> |
| 3    | Document Capture                      | <p>Run the commands in this order:<br>1. <strong>Publish-NavApp</strong> > 2. <strong>Sync-NavApp</strong> > 3. <strong>Install-NavApp</strong></p> |
| 4    | Document Capture OnPremise (optional) | <p>Run the commands in this order:<br>1. <strong>Publish-NavApp</strong> > 2. <strong>Sync-NavApp</strong> > 3. <strong>Install-NavApp</strong></p> |
| 5    | Expense Management                    | <p>Run the commands in this order:<br>1. <strong>Publish-NavApp</strong> > 2. <strong>Sync-NavApp</strong> > 3. <strong>Install-NavApp</strong></p> |

### To upgrade apps

In order to upgrade Expense Management, you must install the new versions of the apps using the same three commands for each of the listed apps in the order described below.

> \[!TIP] Note that this set of commands is slightly different from the one used in the installation process described above.

\


| Step | App name                             | Commands                                                                                                                                                     |
| ---- | ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1    | Continia Core                        | <p>Run the commands in this order:<br>1. <strong>Publish-NavApp</strong> > 2. <strong>Sync-NavApp</strong> > 3. <strong>Start-NAVAppDataUpgrade</strong></p> |
| 2    | Continia Delivery Network            | <p>Run the commands in this order:<br>1. <strong>Publish-NavApp</strong> > 2. <strong>Sync-NavApp</strong> > 3. <strong>Start-NAVAppDataUpgrade</strong></p> |
| 3    | Document Capture                     | <p>Run the commands in this order:<br>1. <strong>Publish-NavApp</strong> > 2. <strong>Sync-NavApp</strong> > 3. <strong>Start-NAVAppDataUpgrade</strong></p> |
| 4    | Document Capture OnPremise (if used) | <p>Run the commands in this order:<br>1. <strong>Publish-NavApp</strong> > 2. <strong>Sync-NavApp</strong> > 3. <strong>Start-NAVAppDataUpgrade</strong></p> |
| 5    | Expense Management                   | <p>Run the commands in this order:<br>1. <strong>Publish-NavApp</strong> > 2. <strong>Sync-NavApp</strong> > 3. <strong>Start-NAVAppDataUpgrade</strong></p> |

This will install the new apps and run the upgrade processes. When you're done, you must then uninstall the old versions of the apps by running the following two commands for each of the listed apps in reverse order:

\


| Step | App name                             | Commands                                                                                                              |
| ---- | ------------------------------------ | --------------------------------------------------------------------------------------------------------------------- |
| 1    | Expense Management                   | <p>Run the commands in this order:<br>1. <strong>UnInstall-NavApp</strong> > 2. <strong>UnPublish-NavApp</strong></p> |
| 2    | Document Capture OnPremise (if used) | <p>Run the commands in this order:<br>1. <strong>UnInstall-NavApp</strong> > 2. <strong>UnPublish-NavApp</strong></p> |
| 3    | Document Capture                     | <p>Run the commands in this order:<br>1. <strong>UnInstall-NavApp</strong> > 2. <strong>UnPublish-NavApp</strong></p> |
| 4    | Continia Delivery Network            | <p>Run the commands in this order:<br>1. <strong>UnInstall-NavApp</strong> > 2. <strong>UnPublish-NavApp</strong></p> |
| 5    | Continia Core                        | <p>Run the commands in this order:<br>1. <strong>UnInstall-NavApp</strong> > 2. <strong>UnPublish-NavApp</strong></p> |

## See also

[Installing Continia Expense Management On-Premises](../../../Continia%20Expense%20Management/Development%20and%20Administration/On-Premises/@EM-138/)\
[Upgrading Continia Expense Management for app versions of Business Central](../../../Continia%20Expense%20Management/Development%20and%20Administration/On-Premises/@EM-254/)
