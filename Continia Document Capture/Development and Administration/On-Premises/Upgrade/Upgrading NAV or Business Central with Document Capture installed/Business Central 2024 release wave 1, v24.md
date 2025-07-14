---
title: Upgrading to Business Central 2024 Release Wave 1 (v24)
date: 08-04-2024
description:  
id: DC-203
lang: en
---

# Upgrading to Business Central 2024 Release Wave 1 (v24)

The following table provides an overview of what you have to do if you have Continia Document Capture (DC) installed and want to update your old version of Microsoft Dynamics NAV/Business Central (BC) to Business Central 2024 release wave 1 (v24). When you follow the guidelines given under **Tasks** below, Document Capture remains fully functional and compatible with your updated version of Business Central.

<br>

| Scenario | Tasks |
| --- | --- |
| Full upgrade from one of the following versions: <ul><li>Microsoft Navision NAV 3.70</li><li>Microsoft Dynamics NAV 4.0</li><li>Microsoft Dynamics NAV 4.0 SP1</li><li>Microsoft Dynamics NAV 4.0 SP2</li><li>Microsoft Dynamics NAV 4.0 SP3</li><li>Microsoft Dynamics NAV 5.0</li><li>Microsoft Dynamics NAV 5.0 SP1</li><li>Microsoft Dynamics NAV 2009</li><li>Microsoft Dynamics NAV 2009 SP1</li><li>Microsoft Dynamics NAV 2009 R2</li><li>Microsoft Dynamics NAV 2013</li><li>Microsoft Dynamics NAV 2013 R2</li><li>Microsoft Dynamics NAV 2015</li><li>Microsoft Dynamics NAV 2016</li><li>Microsoft Dynamics NAV 2017</li><li>Microsoft Dynamics NAV 2018</li><li>Business Central October 2018 (v13)</li></ul> | From these versions, you must do as follows to upgrade: <ol><li>Upgrade to BC v14 (FOB-based) using [this guide](@DC-102).</li><li>From BC v14 (FOB-based), upgrade to BC v24 using the approach described further below in the table under "Business Central April 2019 (v14, FOB-based)".</li></ol> |
| Full upgrade from the following version: <ul><li>Business Central April 2019 (v14, FOB-based)</li></ul> | From this version, you must do as follows to upgrade: <ol><li>Upgrade DC to the latest version (unless you've already done so coming from an earlier BC version). Use [this page](@DC-8) to determine how to upgrade from your particular version of DC.</li><li>Follow [this guide](@DC-113) to migrate table data to extensions. </li></ol> |
| Full upgrade from one of the following versions: <ul><li>Business Central 2019 wave 2 (v15)</li><li>Business Central 2020 wave 1 (v16)</li><li>Business Central 2020 wave 2 (v17)</li><li>Business Central 2021 wave 1 (v18)</li><li>Business Central 2021 wave 2 (v19)</li><li>Business Central 2022 wave 1 (v20)</li><li>Business Central 2022 wave 2 (v21)</li><li>Business Central 2023 wave 1 (v22)</li><li>Business Central 2023 wave 2 (v23)</li></ul> | From these versions, you must do as follows to upgrade: <ol><li>Uninstall and unpublish all Continia apps.</li><li>Upgrade to BC v24 using [this Microsoft guide](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-overview-v24). </li><li>Publish and install the latest versions of all Continia apps, using [this guide](@DC-51).</li></ol> |

## Related information
[Supported Upgrade Paths for Continia Document Capture (FOB)](@DC-8)  



<style>
  .content table tr td:nth-child(1) {
    width: 230px;
  }
  .content table tr td:nth-child(2) {
    width: 500px;
  }  
</style>