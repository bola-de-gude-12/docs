---
title: Upgrading to Business Central 2025 Release Wave 2 (v27)
date: 30-09-2025
description: How to upgrade to Business Central 2025 Release Wave 1 (v26).
id: DC-491
lang: en
---

# Upgrading to Business Central 2025 Release Wave 2 (v27)

The following table provides an overview of what you have to do if you have Continia Document Capture (DC) installed and want to update your old version of Microsoft Dynamics NAV/Business Central (BC) to Business Central 2025 release wave 2 (v27). When you follow the guidelines given under **Tasks** below, Document Capture remains fully functional and compatible with your updated version of Business Central.

>[!NOTE]
>Starting in 2025 release wave 1 (v26), the direct upgrade from Business Central 2019 (v14) to the latest release isn't supported. The supported upgrade path is through 2024 release wave 2 (v25), then to the latest release. For more information, see [Deprecated features in the platform - clients, server, and database](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-platform#changes-in-2025-release-wave-1-version-260) (Microsoft article).

<br>

| Scenario | Tasks |
| --- | --- |
| Full upgrade from one of the following versions: <li>Microsoft Dynamics NAV 2015</li><li>Microsoft Dynamics NAV 2016</li><li>Microsoft Dynamics NAV 2017</li><li>Microsoft Dynamics NAV 2018</li><li>Business Central October 2018 (v13)</li></ul> | <ol><li>Upgrade to BC v14 (FOB-based) using [this guide](@DC-102).</li><li>From BC v14 (FOB-based), upgrade to BC v24 using the approach described below in the table under 'Business Central April 2019 (v14, FOB-based)'.</li></ol> |
| Full upgrade from the following version: <ul><li>Business Central April 2019 (v14, FOB-based)</li></ul> | <ol><li>Upgrade to BC v25 using [this guide](@DC-235).</li><li>Upgrade to BC v26 using [this guide](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-overview-v26).</li><li>Upgrade DC to the latest version (unless you've already done so coming from an earlier BC version). Use [this page](@DC-8) to determine how to upgrade from your particular version of DC.</li><li>Follow [this guide](@DC-113) to migrate table data to extensions. </li></ol> |
| Full upgrade from one of the following versions: <ul><li>Business Central 2019 wave 2 (v15)</li><li>Business Central 2020 wave 1 (v16)</li><li>Business Central 2020 wave 2 (v17)</li><li>Business Central 2021 wave 1 (v18)</li><li>Business Central 2021 wave 2 (v19)</li><li>Business Central 2022 wave 1 (v20)</li><li>Business Central 2022 wave 2 (v21)</li><li>Business Central 2023 wave 1 (v22)</li><li>Business Central 2023 wave 2 (v23)</li></ul><li>Business Central 2024 wave 1 (v24)</li></ul> | <ol><li>Uninstall and unpublish all Continia apps.</li><li>Upgrade to BC v27 using the [Microsoft guide](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-overview-v27).</li><li>Publish and install the latest versions of all Continia apps using the [Installing Continia Document Capture on premises](@DC-51) guide.</li></ol> |

## Related information
[Supported upgrade paths for Continia Document Capture (FOB)](@DC-8)  



<style>
  .content table tr td:nth-child(1) {
    width: 230px;
  }
  .content table tr td:nth-child(2) {
    width: 500px;
  }  
</style>