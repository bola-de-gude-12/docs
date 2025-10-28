---
title: Upgrading to Continia Document Capture 2023 R1 (11.00) for FOB versions
date: 28-05-2024
description:
id: DC-122
lang: en
---

# Upgrading to Continia Document Capture 2023 R1 (11.00) for FOB versions

This article describes how to upgrade Document Capture for _FOB_ versions of Microsoft Dynamics 365 Business Central. For information on how to upgrade Document Capture for _app_ versions of Business Central, see [Upgrading Continia Document Capture for app versions of Business Central](@DC-6).

When you upgrade your old version of Document Capture (DC) to a later one, the upgrade process depends on what version you're upgrading from and what version of Microsoft Dynamics NAV/Business Central you have. It may not be possible to upgrade directly, and you might also have to update your version of NAV/Business Central to ensure compatibility. To learn how to upgrade your old version of NAV/Business Central while ensuring compatibility with Document Capture, see [Upgrading NAV/Business Central with Document Capture Installed](@DC-7).

The table below enables you to determine exactly what tasks must be carried out for your particular scenario in order for you to upgrade your old version of Document Capture to Document Capture 2023 R1 (11.00).

> [!IMPORTANT]
> Note that Document Capture 2023 R1 (11.00) is only available if you're using one of the following versions of Business Central:
> * Business Central 2023 release wave 1 (BC v22)
> * Business Central 2022 release wave 2 (BC v21)
> * Business Central 2022 release wave 1 (BC v20)
> * Business Central April 2019 (v14, FOB-based)

> [!NOTE]
> If you have multiple Continia solutions installed in a FOB version of Business Central and want to upgrade one or more of these solutions, you must take certain steps when importing objects. For more information, see [Upgrading with Multiple Continia Solutions Installed (FOB)](/Continia Document Capture/Development and Administration/On-Premises/Upgrade/Upgrading with multiple solutions installed, FOB/Upgrading with multiple solutions installed, FOB.md).

##Upgrade to Document Capture 2023 R1 (11.00)

| Scenario | Tasks |
| --- | --- |
| Full upgrade from one of the following versions: <ul><li>Versions older than Document Capture 3.50.07</li></ul> | From these versions, you must do as follows to upgrade: <ol><li>Upgrade to Document Capture 3.50.07 first. Upgrade guides can be provided by Continia upon request.</li><li>From Document Capture 3.50.07, upgrade to Document Capture 4.50 using the approach described further below in the table under "Document Capture 3.50.07".</li><li>From Document Capture 4.50, upgrade to Document Capture 8.00 using the approach described further below in the table under "Document Capture 4.50".</li><li>From Document Capture 8.00, upgrade to Document Capture 11.00 using the approach described further below in the table under "Document Capture 8.00".</li></ol> |
| Full upgrade from the following version: <ul><li>Document Capture 3.50.07</li></ul> | From this version, you must do as follows to upgrade: <ol><li>Upgrade to Document Capture 4.50 first using <a href="https://continia.zendesk.com/hc/en-us/articles/360001133259-Upgrade-Guide-from-DC3-50-to-DC4-50">this guide</a>.</li><li>From Document Capture 4.50, upgrade to Document Capture 8.00 using the approach described further below in the table under "Document Capture 4.50".</li><li>From Document Capture 8.00, upgrade to Document Capture 11.00 using the approach described further below in the table under "Document Capture 8.00".</li></ol> |
| Full upgrade from one of the following versions: <ul><li>Document Capture 4.01</li><li>Document Capture 4.02</li><li>Document Capture 4.03</li><li>Document Capture 4.04</li><li>Document Capture 4.05</li><li>Document Capture 4.06</li></ul> | From these versions, you must do as follows to upgrade: <ol><li>Upgrade to Document Capture 4.50 first using <a href="https://continia.zendesk.com/hc/en-us/articles/360001114960-Upgrade-Guide-from-DC4-0x-to-DC4-50">this guide</a>.</li><li>From Document Capture 4.50, upgrade to Document Capture 8.00 using the approach described further below in the table under "Document Capture 4.50".</li><li>From Document Capture 8.00, upgrade to Document Capture 11.00 using the approach described further below in the table under "Document Capture 8.00".</li></ol> |
| Full upgrade from the following version: <ul><li>Document Capture 4.07</li></ul> | From this version, you must do as follows to upgrade: <ol><li>Upgrade to Document Capture 4.50 first using <a href="https://continia.zendesk.com/hc/en-us/articles/360001141819-Upgrade-Guide-from-DC4-07-to-DC4-50">this guide</a>.</li><li>From Document Capture 4.50, upgrade to Document Capture 8.00 using the approach described further below in the table under "Document Capture 4.50".</li><li>From Document Capture 8.00, upgrade to Document Capture 11.00 using the approach described further below in the table under "Document Capture 8.00".</li></ol> |
| Full upgrade from the following versions: <ul><li>Document Capture 4.50</li><li>Document Capture 5.00</li><li>Document Capture 5.50</li><li>Document Capture 6.00</li><li>Document Capture 6.50</li></ul> | From these versions, you must do as follows to upgrade: <ol><li>Upgrade directly to DC8.00 using [this guide](../application-and-data/from-versions-450-650-to-800).</li><li>Upgrade templates that include the <b>Prices Incl. VAT</b> setting using <a href="https://continia.zendesk.com/hc/en-us/articles/360010610879-How-to-upgrade-templates-with-Prices-Incl-VAT-when-upgrading-to-DC6-00?_ga=2.99953438.1044206868.1630409167-1477042316.1630409167">this guide</a>.</li><li>From Document Capture 8.00, upgrade to Document Capture 11.00 using the approach described further below in the table under "Document Capture 8.00".</li></ol> |
| Full upgrade from the following versions: <ul><li>Document Capture 7.00</li></ul> | From these versions, you must do as follows to upgrade: <ol><li>Upgrade directly to DC8.00 using [this guide](../application-and-data/from-version-700/manual-upgrade).</li><li>From Document Capture 8.00, upgrade to Document Capture 11.00 using the approach described further below in the table under "Document Capture 8.00".</li></ol> |
| Full upgrade from the following versions: <ul><li>Document Capture 8.00</li><li>Document Capture 9.00</li><li>Document Capture 10.00</li></ul> | From these versions, you can upgrade directly to DC11.00 using [this guide](../application-and-data/from-versions-8001000/manual-upgrade). |

## Related information
[Supported Upgrade Paths for Continia Document Capture (FOB)](@DC-8)  
[Upgrading NAV/Business Central with Document Capture Installed](@DC-7)  
[Upgrading with Multiple Continia Solutions Installed (FOB)](/Continia Document Capture/Development and Administration/On-Premises/Upgrade/Upgrading with multiple solutions installed, FOB/Upgrading with multiple solutions installed, FOB.md)  




<style>
  .content table tr td:nth-child(1) {
    width: 230px;
  }
  .content table tr td:nth-child(2) {
    width: 500px;
  }  
</style>