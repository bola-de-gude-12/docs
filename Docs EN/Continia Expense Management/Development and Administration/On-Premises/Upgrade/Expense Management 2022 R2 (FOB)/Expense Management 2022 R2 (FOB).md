---
title: Upgrading to Continia Expense Management 2022 R2 (10.00) for FOB versions
date: 01-10-2022
description:  
id: EM-99
lang: en
---

# Upgrading to Continia Expense Management 2022 R2 (10.00) for FOB versions

This article describes how to upgrade Expense Management for _FOB_ versions of Microsoft Dynamics 365 Business Central. For information on how to upgrade Expense Management for _app_ versions of Business Central, see [Upgrading Continia Expense Management for app versions of Business Central](/Continia Expense Management/Development and Administration/On-Premises/Upgrade/Upgrading Expense Management for app versions.md).

When you upgrade your old version of Expense Management (EM) to a later one, the upgrade process depends on what version you're upgrading from and what version of Microsoft Dynamics NAV/Business Central you have. It may not be possible to upgrade directly, and you might also have to update your version of NAV/Business Central to ensure compatibility. To learn how to upgrade your old version of NAV/Business Central while ensuring compatibility with Expense Management, see [Upgrading NAV/Business Central with Expense Management Installed](/Continia Expense Management/Development and Administration/On-Premises/Upgrade/Upgrading NAV or Business Central with Expense Management installed/Overview.md).

The table below enables you to determine exactly what tasks must be carried out for your particular scenario in order for you to upgrade your old version of Expense Management to Expense Management 2022 R2 (10.00).

## Upgrade to Expense Management 2022 R2 (10.00)

Please note that Expense Management 2022 R2 (10.00) is available from Business Central April 2019 (v14, FOB-based) and newer. This means that any client installations running versions prior to that version will not be able to upgrade to 10.00. Instead they should be upgraded to version 8.00 as this version will continue to be supported with service packs beyond the normal product life cycle (2 years).

| Scenario | Tasks |
| --- | --- |
| Full upgrade from one of the following versions: <ul><li>Expense Management 1.03</li><li>Expense Management 2.00</li><li>Expense Management 2.50</li> | From these versions, you must do as follows to upgrade: <ol><li>Do one of the following, depending on whether or not you use Expense Management on its own: <ul><li>When using both Expense Management and Continia Document Capture, upgrade to Expense Management 2.60 first using <a href="https://continia.zendesk.com/hc/en-us/articles/360021971820-Upgrade-Guide-from-DC4-05-4-06-and-EM-1-03-2-00-to-DC-4-50-and-EM-2-60">this guide</a>.</li><li>When using only Expense Management, upgrade to Expense Management 2.60 first using <a href="https://continia.zendesk.com/hc/en-us/articles/360022000219-Upgrade-Guide-from-EM-1-03-and-2-00-to-2-60-latest-service-pack-">this guide</a>.</li></ul><li>From Expense Management 2.60, upgrade to Expense Management 7.00 using the approach described further below in the table under "Expense Management 2.60".</li></ol> |
| Full upgrade from the following versions: <ul><li>Expense Management 2.60</li><li>Expense Management 3.00</li><li>Expense Management 3.50</li><li>Expense Management 4.00</li><li>Expense Management 6.50</li></ul> | From these versions, you must do as follows to upgrade: <ol><li>Upgrade directly to EM8.00 using [this guide](@EM-29).</li><li>From Expense Management 8.00, upgrade to Expense Management 10.00 using the approach described further below in the table under "Expense Management 8.00".</li></ol> |
| Full upgrade from the following version: <ul><li>Expense Management 7.00</li></ul> | From this version, you must do as follows to upgrade: <ol><li>Upgrade directly to EM8.00 using [this guide](@EM-30).</li><li>From Expense Management 8.00, upgrade to Expense Management 10.00 using the approach described further below in the table under "Expense Management 8.00".</li></ol>. |
| Full upgrade from the following versions: <ul><li>Expense Management 8.00</li><li>Expense Management 9.00</li></ul> | From these versions, you can upgrade directly to EM10.00 using [this guide](@EM-101). |

## Related information
[Supported Upgrade Paths for Continia Expense Management (FOB)](/Continia Expense Management/Development and Administration/On-Premises/Upgrade/Supported Upgrade Paths.md)  
[Upgrading NAV/Business Central with Expense Management Installed](/Continia Expense Management/Development and Administration/On-Premises/Upgrade/Upgrading NAV or Business Central with Expense Management installed/Overview.md)  




<style>
  .content table tr td:nth-child(1) {
    width: 230px;
  }
  .content table tr td:nth-child(2) {
    width: 500px;
  }  
</style>