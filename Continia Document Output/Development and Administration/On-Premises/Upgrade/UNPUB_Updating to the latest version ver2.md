---
title: Document Output Upgrading to the Latest Version
date: 10-07-2024
description:  
lang: en
---

# Upgrading to the Latest Version
This section provides details on how to upgrade to the latest version of Continia Document Output in the *on-premises* version of Microsoft Dynamics 365 Business Central (including guidelines on how to migrate from on-premises to the cloud). You can find guidelines for the *online* version of Business Central [here](/Continia Document Output/Development and Administration/Online/Updating to the latest version.md).

To upgrade Document Output for _app_ versions of Business Central, you must use the specially developed Continia PowerShell script that automatically upgrades the app and all dependencies. For more information, see [Upgrading Continia Document Output for app versions of Business Central](Upgrading Document Output for app versions.md).

For *FOB* versions of Business Central, your upgrade path depends on what versions of Document Output and Business Central you currently have. Not all versions of Document Output are compatible with all versions of Business Central (and vice versa), so we generally recommend that you upgrade to the latest versions of both.

Note that when you upgrade your old version of Document Output to the latest one, it may not be possible to upgrade directly, and you may also have to upgrade your version of Microsoft Dynamics NAV/Business Central to ensure compatibility. To find out exactly what you need to do to upgrade to the latest FOB version of Document Output, see [Supported Upgrade Paths for Continia Document Output (FOB)](Supported Upgrade Paths.md).

Provided that you have multiple Continia solutions installed in a FOB version of Business Central and want to upgrade one or more of these solutions, you must take certain steps when importing objects. For more information, see [Upgrading with Multiple Continia Solutions Installed (FOB)](Upgrading with multiple solutions installed, FOB/Upgrading with multiple solutions installed, FOB.md).

If you use Document Output in an old version of NAV/Business Central and want to upgrade NAV/Business Central to a later version, you must also upgrade Document Output and/or carry out related tasks, depending on what version you use. To learn more and find out what to do for your particular old version of NAV/Business Central, see [Upgrading NAV/Business Central with Document Output Installed] (Upgrading NAV or Business Central with Document Output installed/Overview.md).

Last but not least, if your organization is looking to move from an on-premises deployment to a cloud environment, you can easily do so by following the steps in the article [Migrating Document Output from Business Central On-Premises to Cloud](Migrate from on-premises to cloud.md).

> [!IMPORTANT]
> After any upgrade (for both app and FOB versions of Business Central), you must always download and use a new and updated customer license file from Microsoft.

> [!TIP]
> You can download the Document Capture installation packages and upgrade files for FOB versions on the [Continia PartnerZone](https://partnerzone.continia.com/downloads/) (only available to partners).

## See also
[Upgrading Continia Document Output for app versions of Business Central](Upgrading Document Output for app versions.md)  
[Supported Upgrade Paths for Continia Document Output (FOB)](Supported Upgrade Paths.md)  
[Migrating Document Output from FOB to App for Business Central On-Premises](Migrating Document Output from FOB to app.md)  
[Migrating Document Output from Business Central On-Premises to Cloud](Migrate from on-premises to cloud.md)  