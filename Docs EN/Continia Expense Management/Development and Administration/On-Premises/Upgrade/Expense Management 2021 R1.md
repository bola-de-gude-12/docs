---
title: Upgrading to Continia Expense Management 2021 R1 (7.00) for FOB versions
date: 09-07-2025
description:  
lang: en
---

# Upgrading to Continia Expense Management 2021 R1 (7.00) for FOB versions

This article describes how to upgrade Expense Management for _FOB_ versions of Microsoft Dynamics 365 Business Central. For information on how to upgrade Expense Management for _app_ versions of Business Central, see [Upgrading Continia Expense Management for app versions of Business Central](Upgrading Expense Management for app versions.md).

When you upgrade your old version of Expense Management (EM) to a later one, the upgrade process depends on what version you're upgrading from and what version of Microsoft Dynamics NAV/Business Central you have. It may not be possible to upgrade directly, and you might also have to update your version of NAV/Business Central to ensure compatibility. To learn how to upgrade your old version of NAV/Business Central while ensuring compatibility with Expense Management, see [Upgrading NAV/Business Central with Expense Management Installed](Upgrading NAV or Business Central with Expense Management installed/Overview.md).

The table below enables you to determine exactly what tasks must be carried out for your particular scenario in order for you to upgrade your old version of Expense Management to Expense Management 2021 R1 (7.00).

##Upgrade to Expense Management 2021 R1 (7.00)

| Scenario | Tasks |
| --- | --- |
| Full upgrade from one of the following versions: <ul><li>Expense Management 1.03</li><li>Expense Management 2.00</li><li>Expense Management 2.50</li> | From these versions, you must do as follows to upgrade: <ol><li>Do one of the following, depending on whether or not you use Expense Management on its own: <ul><li>When using both Expense Management and Continia Document Capture, upgrade to Expense Management 2.60 first using <a href="https://continia.zendesk.com/hc/en-us/articles/360021971820-Upgrade-Guide-from-DC4-05-4-06-and-EM-1-03-2-00-to-DC-4-50-and-EM-2-60">this guide</a>.</li><li>When using only Expense Management, upgrade to Expense Management 2.60 first using <a href="https://continia.zendesk.com/hc/en-us/articles/360022000219-Upgrade-Guide-from-EM-1-03-and-2-00-to-2-60-latest-service-pack-">this guide</a>.</li></ul><li>From Expense Management 2.60, upgrade to Expense Management 7.00 using the approach described further below in the table under "Expense Management 2.60".</li></ol> |
| Full upgrade from the following version: <ul><li>Expense Management 2.60</li></ul> | From this version, you must upgrade in steps (EM2.60 > EM3.00 > EM3.50 > EM4.00 > EM6.50 > EM7.00) as follows: <ol><li>Upgrade from EM2.60 to EM3.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360001141939-Upgrade-Guide-from-EM4-50-and-or-EM2-60-to-EM5-00-and-or-EM3-00">this guide</a>.</li><li>Upgrade from EM3.00 to EM3.50 using <a href="https://continia.zendesk.com/hc/en-us/articles/360010348160-Upgrade-Guide-from-DC5-00-and-or-EM3-00-to-DC5-50-and-or-EM3-50">this guide</a>.</li><li>Upgrade from EM3.50 to EM4.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360010666220-Upgrade-Guide-from-DC5-50-and-or-EM3-50-to-DC6-00-and-or-EM4-00">this guide</a>.</li><li>Upgrade from EM4.00 to EM6.50 using <a href="https://continia.zendesk.com/hc/en-us/articles/360019268860-Upgrade-Guide-from-DC6-00-and-or-EM4-00-to-DC6-50-and-or-EM6-50">this guide</a>.</li><li>Upgrade from EM6.50 to EM7.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360021304720-Upgrade-Guide-from-DC6-50-and-or-EM6-50-to-DC7-00-and-or-EM7-00">this guide</a>.</li></ol>  |
| Full upgrade from the following version: <ul><li>Expense Management 3.00</li></ul> | From this version, you must upgrade in steps (EM3.00 > EM3.50 > EM4.00 > EM6.50 > EM7.00) as follows: <ol><li>Upgrade from EM3.00 to EM3.50 using <a href="https://continia.zendesk.com/hc/en-us/articles/360010348160-Upgrade-Guide-from-DC5-00-and-or-EM3-00-to-DC5-50-and-or-EM3-50">this guide</a>.</li><li>Upgrade from EM3.50 to EM4.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360010666220-Upgrade-Guide-from-DC5-50-and-or-EM3-50-to-DC6-00-and-or-EM4-00">this guide</a>.</li><li>Upgrade from EM4.00 to EM6.50 using <a href="https://continia.zendesk.com/hc/en-us/articles/360019268860-Upgrade-Guide-from-DC6-00-and-or-EM4-00-to-DC6-50-and-or-EM6-50">this guide</a>.</li><li>Upgrade from EM6.50 to EM7.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360021304720-Upgrade-Guide-from-DC6-50-and-or-EM6-50-to-DC7-00-and-or-EM7-00">this guide</a>.</li></ol> |
| Full upgrade from the following version: <ul><li>Expense Management 3.50</li></ul> | From this version, you must upgrade in steps (EM3.50 > EM4.00 > EM6.50 > EM7.00) as follows: <ol><li>Upgrade from EM3.50 to EM4.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360010666220-Upgrade-Guide-from-DC5-50-and-or-EM3-50-to-DC6-00-and-or-EM4-00">this guide</a>.</li><li>Upgrade from EM4.00 to EM6.50 using <a href="https://continia.zendesk.com/hc/en-us/articles/360019268860-Upgrade-Guide-from-DC6-00-and-or-EM4-00-to-DC6-50-and-or-EM6-50">this guide</a>.</li><li>Upgrade from EM6.50 to EM7.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360021304720-Upgrade-Guide-from-DC6-50-and-or-EM6-50-to-DC7-00-and-or-EM7-00">this guide</a>.</li></ol> |
| Full upgrade from the following version: <ul><li>Expense Management 4.00</li></ul> | From this version, you must upgrade in steps (EM4.00 > EM6.50 > EM7.00) as follows: <ol><li>Upgrade from EM4.00 to EM6.50 using <a href="https://continia.zendesk.com/hc/en-us/articles/360019268860-Upgrade-Guide-from-DC6-00-and-or-EM4-00-to-DC6-50-and-or-EM6-50">this guide</a>.</li><li>Upgrade from EM6.50 to EM7.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360021304720-Upgrade-Guide-from-DC6-50-and-or-EM6-50-to-DC7-00-and-or-EM7-00">this guide</a>.</li></ol> |
| Full upgrade from the following version: <ul><li>Expense Management 6.50</li></ul> | From this version, you can upgrade directly to EM7.00 as follows: <ul><li>Upgrade from EM6.50 to EM7.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360021304720-Upgrade-Guide-from-EM6-50-and-or-EM6-50-to-EM7-00-and-or-EM7-00">this guide</a>.</li></ul> |

> [!NOTE]
> It's now possible to upgrade from Expense Management 2.60 or later directly to [Expense Management 8.00](@EM-28). This renders the stepped upgrades described above completely unnecessary and makes it much easier for you to bring your software up to date. However, note that this is only possible as of Expense Management 8.00 – you can't upgrade directly from older versions to Expense Management 7.00.

## Related information
[Supported Upgrade Paths for Continia Expense Management (FOB)](Supported Upgrade Paths.md)  
[Upgrading NAV/Business Central with Expense Management Installed](Upgrading NAV or Business Central with Expense Management installed/Overview.md)  




<style>
  .content table tr td:nth-child(1) {
    width: 230px;
  }
  .content table tr td:nth-child(2) {
    width: 500px;
  }  
</style>