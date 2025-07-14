---
title: Upgrading to the latest version (on premises)
date: 27-03-2025
description: How to upgrade to the latest version of Continia Document Capture in the on-premises version of Business Central.
id: DC-58
lang: en
---

# Upgrading to the latest version (on premises)

This section provides details on how to upgrade to the latest version of Continia Document Capture in the on-premises version of Microsoft Dynamics 365 Business Central (including guidelines on how to migrate from on-premises to the cloud). For guidelines for the online version of Business Central, see [Upgrading to the latest version](@DC-451).

To upgrade Document Capture for app versions of Business Central, you must use the specially developed Continia PowerShell script that automatically upgrades the app and all dependencies. For more information, see [Upgrading Continia Document Capture for app versions of Business Central](@DC-6).

For FOB versions of Business Central, your upgrade path depends on what versions of Document Capture and Business Central you currently have. Not all versions of Document Capture are compatible with all versions of Business Central (and vice versa), so it's generally recommended that you upgrade to the latest versions of both.

>[!NOTE]
>The last FOB version of Document Capture is 2024 R2 (25.00). On-premises users can install the app version of Document Capture 2025 R1 (26.00).

Note that when you upgrade your old version of Document Capture to the latest supported one, it may not be possible to upgrade directly – and you may also have to upgrade your version of NAV/Business Central to ensure compatibility. To find out how to upgrade to the latest FOB version of Document Capture, see [Supported upgrade paths for Continia Document Capture (FOB)](@DC-8).

If you have multiple Continia solutions installed in a FOB version of Business Central and want to upgrade one or more of these solutions, you must take certain steps when importing objects. For more information, see [Upgrading with multiple Continia solutions installed (FOB)](@DC-54).

If you use Document Capture in an old version of NAV/Business Central and want to upgrade NAV/Business Central to a later version, you must also upgrade Document Capture and/or carry out related tasks – depending on what version you use. To learn more, see [Upgrading NAV/Business Central with Document Capture installed](@DC-7).

Lastly, if your organization is looking to move from an on-premises deployment to a cloud environment, you can do so by following the steps in [Migrating Document Capture from Business Central on premises to cloud](@DC-106).

> [!IMPORTANT]
> After any upgrade (for both app and FOB versions of Business Central), you must always download and use a new and updated customer license file from Microsoft.

> [!TIP]
> You can download the Document Capture installation packages and upgrade files for FOB versions on the [Continia PartnerZone](https://partnerzone.continia.com/downloads/) (only available to partners).

## Related information
[Upgrading Continia Document Capture for app versions of Business Central](@DC-6)  
[Supported upgrade paths for Continia Document Capture (FOB)](@DC-8)  
[Upgrading NAV/Business Central with Document Capture installed](@DC-7)  
[Migrating Document Capture from Business Central on premises to cloud](@DC-106)  