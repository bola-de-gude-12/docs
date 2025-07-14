---
title: Expense Management upgrading to the latest version
date: 09-07-2025
description:  
id: EM-87
lang: en
---

# Upgrading to the latest version
Learn how to upgrade to the latest version of Continia Expense Management in the *on-premises* version of Microsoft Dynamics 365 Business Central (including guidelines on how to migrate from on-premises to the cloud). You can find guidelines for the *online* version of Business Central [here](/Continia Expense Management/Development and Administration/Online/Updating to the latest version.md).

To upgrade Expense Management for _app_ versions of Business Central, you must use the specially developed Continia PowerShell script that automatically upgrades the app and all dependencies. For more information, see [Upgrading Continia Expense Management for app versions of Business Central](Upgrading Expense Management for app versions.md).

For _FOB_ versions of Business Central, your upgrade path depends on what versions of Expense Management and Business Central you currently have. Not all versions of Expense Management are compatible with all versions of Business Central (and vice versa), so we generally recommend that you upgrade to the latest versions of both.

Note that when you upgrade your old version of Expense Management to the latest one, it may not be possible to upgrade directly, and you may also have to upgrade your version of Microsoft Dynamics NAV/Business Central to ensure compatibility. To find out exactly what you need to do to upgrade to the latest FOB version of Expense Management, see [Supported Upgrade Paths for Continia Expense Management (FOB)](Supported Upgrade Paths.md).

Provided that you have multiple Continia solutions installed in a FOB version of Business Central and want to upgrade one or more of these solutions, you must take certain steps when importing objects. For more information, see [Upgrading with Multiple Continia Solutions Installed (FOB)](Upgrading with multiple solutions installed, FOB/Upgrading with multiple solutions installed, FOB.md).

> [!TIP]
> You can download the Expense Management installation packages and upgrade files for FOB versions on the [Continia PartnerZone](https://partnerzone.continia.com/downloads/) (only available to partners).

If you use Expense Management in an old version of NAV/Business Central and want to upgrade NAV/Business Central to a later version, you must also upgrade Expense Management and/or carry out related tasks, depending on what version you use. To learn more and find out what to do for your particular old version of NAV/Business Central, see [Upgrading NAV/Business Central with Expense Management Installed](Upgrading NAV or Business Central with Expense Management installed/Overview.md).

Last but not least, if your organization is looking to move from an on-premises deployment to a cloud environment, you can easily do so by following the steps in the article [Migrating Expense Management from Business Central On-Premises to Cloud](Migrate from on-premises to cloud.md).

> [!IMPORTANT]
> After any upgrade (for both app and FOB versions of Business Central), you must always download and use a new and updated customer license file from Microsoft.

## Related information

[Upgrading Continia Expense Management for app versions of Business Central](Upgrading Expense Management for app versions.md)  
[Supported Upgrade Paths for Continia Expense Management (FOB)](Supported Upgrade Paths.md)  
[Upgrading NAV/Business Central with Expense Management Installed](Upgrading NAV or Business Central with Expense Management installed/Overview.md)  
[Migrating Expense Management from Business Central On-Premises to Cloud](Migrate from on-premises to cloud.md)  