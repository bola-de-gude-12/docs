---
title: Upgrading to Continia Document Capture 2021 R1 (7.00) for FOB versions
date: 25-03-2022
description:
id: DC-9
lang: en
---

# Upgrading to Continia Document Capture 2021 R1 (7.00) for FOB versions

This article describes how to upgrade Document Capture for _FOB_ versions of Microsoft Dynamics 365 Business Central. For information on how to upgrade Document Capture for _app_ versions of Business Central, see [Upgrading Continia Document Capture for app versions of Business Central](@DC-6).

When you upgrade your old version of Document Capture (DC) to a later one, the upgrade process depends on what version you're upgrading from and what version of Microsoft Dynamics NAV/Business Central you have. It may not be possible to upgrade directly, and you might also have to update your version of NAV/Business Central to ensure compatibility. To learn how to upgrade your old version of NAV/Business Central while ensuring compatibility with Document Capture, see [Upgrading NAV/Business Central with Document Capture Installed](@DC-7).

The table below enables you to determine exactly what tasks must be carried out for your particular scenario in order for you to upgrade your old version of Document Capture to Document Capture 2021 R1 (7.00).

> [!NOTE]
> If you have multiple Continia solutions installed in a FOB version of Business Central and want to upgrade one or more of these solutions, you must take certain steps when importing objects. For more information, see [Upgrading with Multiple Continia Solutions Installed (FOB)](@DC-54).

## Upgrade to Document Capture 2021 R1 (7.00)

| Scenario | Tasks |
| --- | --- |
| Full upgrade from one of the following versions: <ul><li>Versions older than Document Capture 3.50.07</li></ul> | From these versions, you must do as follows to upgrade: <ol><li>Upgrade to Document Capture 3.50.07 first. Upgrade guides can be provided by Continia upon request.</li><li>From Document Capture 3.50.07, upgrade to Document Capture 4.50 using the approach described further below in the table under "Document Capture 3.50.07".</li><li>From Document Capture 4.50, upgrade to Document Capture 7.00 using the approach described further below in the table under "Document Capture 4.50".</li></ol> |
| Full upgrade from the following version: <ul><li>Document Capture 3.50.07</li></ul> | From this version, you must do as follows to upgrade: <ol><li>Upgrade to Document Capture 4.50 first using <a href="https://continia.zendesk.com/hc/en-us/articles/360001133259-Upgrade-Guide-from-DC3-50-to-DC4-50">this guide</a>.</li><li>From Document Capture 4.50, upgrade to Document Capture 7.00 using the approach described further below in the table under "Document Capture 4.50".</li></ol> |
| Full upgrade from one of the following versions: <ul><li>Document Capture 4.01</li><li>Document Capture 4.02</li><li>Document Capture 4.03</li><li>Document Capture 4.04</li><li>Document Capture 4.05</li><li>Document Capture 4.06</li></ul> | From these versions, you must do as follows to upgrade: <ol><li>Upgrade to Document Capture 4.50 first using <a href="https://continia.zendesk.com/hc/en-us/articles/360001114960-Upgrade-Guide-from-DC4-0x-to-DC4-50">this guide</a>.</li><li>From Document Capture 4.50, upgrade to Document Capture 7.00 using the approach described further below in the table under "Document Capture 4.50".</li></ol> |
| Full upgrade from the following version: <ul><li>Document Capture 4.07</li></ul> | From this version, you must do as follows to upgrade: <ol><li>Upgrade to Document Capture 4.50 first using <a href="https://continia.zendesk.com/hc/en-us/articles/360001141819-Upgrade-Guide-from-DC4-07-to-DC4-50">this guide</a>.</li><li>From Document Capture 4.50, upgrade to Document Capture 7.00 using the approach described further below in the table under "Document Capture 4.50".</li></ol> |
| Full upgrade from the following version: <ul><li>Document Capture 4.50</li></ul> | From this version, you must upgrade in steps (DC4.50 > DC5.00 > DC5.50 > DC6.00 > DC6.50 > DC7.00) as follows: <ol><li>Upgrade from DC4.50 to DC5.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360001141939-Upgrade-Guide-from-DC4-50-and-or-EM2-60-to-DC5-00-and-or-EM3-00">this guide</a>.</li><li>Upgrade from DC5.00 to DC5.50 using <a href="https://continia.zendesk.com/hc/en-us/articles/360010348160-Upgrade-Guide-from-DC5-00-and-or-EM3-00-to-DC5-50-and-or-EM3-50">this guide</a>.</li><li>Upgrade from DC5.50 to DC6.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360010666220-Upgrade-Guide-from-DC5-50-and-or-EM3-50-to-DC6-00-and-or-EM4-00">this guide</a>.</li><li>Upgrade templates that include the <b>Prices Incl. VAT</b> setting using <a href="https://continia.zendesk.com/hc/en-us/articles/360010610879-How-to-upgrade-templates-with-Prices-Incl-VAT-when-upgrading-to-DC6-00">this guide</a>.</li><li>Upgrade from DC6.00 to DC6.50 using <a href="https://continia.zendesk.com/hc/en-us/articles/360019268860-Upgrade-Guide-from-DC6-00-and-or-EM4-00-to-DC6-50-and-or-EM6-50">this guide</a>.</li><li>Upgrade from DC6.50 to DC7.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360021304720-Upgrade-Guide-from-DC6-50-and-or-EM6-50-to-DC7-00-and-or-EM7-00">this guide</a>.</li></ol>  |
| Full upgrade from the following version: <ul><li>Document Capture 5.00</li></ul> | From this version, you must upgrade in steps (DC5.00 > DC5.50 > DC6.00 > DC6.50 > DC7.00) as follows: <ol><li>Upgrade from DC5.00 to DC5.50 using <a href="https://continia.zendesk.com/hc/en-us/articles/360010348160-Upgrade-Guide-from-DC5-00-and-or-EM3-00-to-DC5-50-and-or-EM3-50">this guide</a>.</li><li>Upgrade from DC5.50 to DC6.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360010666220-Upgrade-Guide-from-DC5-50-and-or-EM3-50-to-DC6-00-and-or-EM4-00">this guide</a>.</li><li>Upgrade templates that include the <b>Prices Incl. VAT</b> setting using <a href="https://continia.zendesk.com/hc/en-us/articles/360010610879-How-to-upgrade-templates-with-Prices-Incl-VAT-when-upgrading-to-DC6-00">this guide</a>.</li><li>Upgrade from DC6.00 to DC6.50 using <a href="https://continia.zendesk.com/hc/en-us/articles/360019268860-Upgrade-Guide-from-DC6-00-and-or-EM4-00-to-DC6-50-and-or-EM6-50">this guide</a>.</li><li>Upgrade from DC6.50 to DC7.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360021304720-Upgrade-Guide-from-DC6-50-and-or-EM6-50-to-DC7-00-and-or-EM7-00">this guide</a>.</li></ol> |
| Full upgrade from the following version: <ul><li>Document Capture 5.50</li></ul> | From this version, you must upgrade in steps (DC5.50 > DC6.00 > DC6.50 > DC7.00) as follows: <ol><li>Upgrade from DC5.50 to DC6.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360010666220-Upgrade-Guide-from-DC5-50-and-or-EM3-50-to-DC6-00-and-or-EM4-00">this guide</a>.</li><li>Upgrade templates that include the <b>Prices Incl. VAT</b> setting using <a href="https://continia.zendesk.com/hc/en-us/articles/360010610879-How-to-upgrade-templates-with-Prices-Incl-VAT-when-upgrading-to-DC6-00">this guide</a>.</li><li>Upgrade from DC6.00 to DC6.50 using <a href="https://continia.zendesk.com/hc/en-us/articles/360019268860-Upgrade-Guide-from-DC6-00-and-or-EM4-00-to-DC6-50-and-or-EM6-50">this guide</a>.</li><li>Upgrade from DC6.50 to DC7.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360021304720-Upgrade-Guide-from-DC6-50-and-or-EM6-50-to-DC7-00-and-or-EM7-00">this guide</a>.</li></ol> |
| Full upgrade from the following version: <ul><li>Document Capture 6.00</li></ul> | From this version, you must upgrade in steps (DC6.00 > DC6.50 > DC7.00) as follows: <ol><li>Upgrade from DC6.00 to DC6.50 using <a href="https://continia.zendesk.com/hc/en-us/articles/360019268860-Upgrade-Guide-from-DC6-00-and-or-EM4-00-to-DC6-50-and-or-EM6-50">this guide</a>.</li><li>Upgrade from DC6.50 to DC7.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360021304720-Upgrade-Guide-from-DC6-50-and-or-EM6-50-to-DC7-00-and-or-EM7-00">this guide</a>.</li></ol> |
| Full upgrade from the following version: <ul><li>Document Capture 6.50</li></ul> | From this version, you can upgrade directly to DC7.00 as follows: <ul><li>Upgrade from DC6.50 to DC7.00 using <a href="https://continia.zendesk.com/hc/en-us/articles/360021304720-Upgrade-Guide-from-DC6-50-and-or-EM6-50-to-DC7-00-and-or-EM7-00">this guide</a>.</li></ul> |

> [!NOTE]
> It's now possible to upgrade from Document Capture 4.50 or later directly to [Document Capture 8.00](@DC-10). This renders the stepped upgrades described above completely unnecessary and makes it much easier for you to bring your software up to date. However, note that this is only possible as of Document Capture 8.00 – you can't upgrade directly from older versions to Document Capture 7.00.

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