---
title: Expense Management Upgrading to Business Central 2021 Release Wave 1 (v18)
date: 28-03-2025
description:  
lang: en
---

# Upgrading to Business Central 2021 Release Wave 1 (v18)

The following table provides an overview of what you have to do if you have Continia Expense Management (EM) installed and want to update your old version of Microsoft Dynamics NAV/Business Central (BC) to Business Central 2021 release wave 1 (v18). When you follow the guidelines given under **Tasks** below, Expense Management remains fully functional and compatible with your updated version of Business Central.

<br>

| Scenario | Tasks |
| --- | --- |
| Full upgrade from one of the following versions: <ul><li>Microsoft Dynamics NAV 2009 R2</li><li>Microsoft Dynamics NAV 2013</li><li>Microsoft Dynamics NAV 2013 R2</li><li>Microsoft Dynamics NAV 2015</li><li>Microsoft Dynamics NAV 2016</li><li>Microsoft Dynamics NAV 2017</li><li>Microsoft Dynamics NAV 2018</li><li>Business Central October 2018 (v13)</li></ul> | From these versions, you must do as follows to upgrade: <ol><li>Upgrade to BC v14 (FOB-based) using <a href="/continia-expense-management/development-and-administration/on-premises/upgrade/upgrading-nav-or-business-central-with-expense-management-installed/business-central-april-2019-v14">this guide</a>.</li><li>From BC v14 (FOB-based), upgrade to BC v18 using the approach described further below in the table under "Business Central April 2019 (v14, FOB-based)".</li></ol> |
| Full upgrade from the following version: <ul><li>Business Central April 2019 (v14, FOB-based)</li></ul> | From this version, you must do as follows to upgrade: <ol><li>Upgrade Expense Management to the latest version (unless you've already done so coming from an earlier Business Central version). Use <a href="/continia-expense-management/development-and-administration/on-premises/upgrade/supported-upgrade-paths">this page</a> to determine how to upgrade from your particular version of Expense Management.</li><li>Follow <a href="https://continia.zendesk.com/hc/da/articles/360021244220-How-to-upgrade-DC-and-EM-to-Business-Central-2021-release-wave-1-BC18-on-premises-extensions-">this guide</a> to migrate table data to extensions.</li></ol> |
| Full upgrade from one of the following versions: <ul><li>Business Central 2019 wave 2 (v15)</li><li>Business Central 2020 wave 1 (v16)</li><li>Business Central 2020 wave 2 (v17)</li></ul> | From these versions, you must do as follows to upgrade: <ol><li>Uninstall and unpublish all Continia apps.</li><li>Upgrade to BC v18 using <a href="https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-overview-v18">this Microsoft guide</a>.</li><li>Publish and install the latest versions of all Continia apps.</li></ol> |

## Related information
[Supported Upgrade Paths for Expense Management (FOB)](/Continia Expense Management/Development and Administration/On-Premises/Upgrade/Supported Upgrade Paths.md)  



<style>
  .content table tr td:nth-child(1) {
    width: 230px;
  }
  .content table tr td:nth-child(2) {
    width: 500px;
  }  
</style>