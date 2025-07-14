---
title: Upgrading to Continia Document Output 2023 R2 (9.00) for FOB versions
date: 28-09-2023
description:
id: DO-138
lang: en
---

# Upgrading to Continia Document Output 2023 R2 (9.00) for FOB versions

This article describes how to upgrade Document Output for _FOB_ versions of Microsoft Dynamics 365 Business Central. For information on how to upgrade Document Output for _app_ versions of Business Central, see [Upgrading Continia Document Output for app versions of Business Central](Upgrading Document Output for app versions.md).

When you upgrade your old version of Document Output to a later one, the upgrade process depends on what version you're upgrading from and what version of Microsoft Dynamics NAV/Business Central you have. It may not be possible to upgrade directly, and you might also have to update your version of NAV/Business Central to ensure compatibility. To learn how to upgrade your old FOB version of NAV/Business Central to an app version while ensuring compatibility with Document Output, see [Migrating Document Output from FOB to App for Business Central On-Premises](Migrating Document Output from FOB to app.md).

The table below enables you to determine exactly what tasks must be carried out for your particular scenario in order for you to upgrade your old version of Document Output to Document Output 2023 R2 (9.00).

## Upgrade to Document Output 2023 R2 (9.00)

| Scenario | Tasks |
| --- | --- |
| Full upgrade from one of the following versions: <ul><li>Document Output 1.xx (any version between 1.35 and 1.48)</li></ul> | From these versions, you must do as follows to upgrade: <ol><li>In the <a href="https://partnerzone.continia.com/dashboard/">Continia PartnerZone</a>, go to <b>Downloads</b> and download the relevant product package.</li><li>Using the setup guide from the product package, install Document Output as usual. This will upgrade your software.</li></ol> <div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Note</span></p><p>The table "6175271 E-Mail Template" isn't used in later versions. The first time you open **E-Mail Templates** in a later version, all the old templates in table 6175271 will be converted to the two new tables "6175283 E-Mail Template Header" and "6175284 E-Mail Template Line". For this reason, it's important that you **don't delete table 6175271**. <br><br> Likewise, the page "6175279 E-Mail Language Templates” isn't used in later versions. When you've upgraded to a later version, this page can't compile and **may therefore be deleted**.</p></div> |
| Full upgrade from one of the following versions: <ul><li>Document Output 2.xx (any version between 2.00 and 2.35.04)</li><li>Document Output 3.xx (any version between 3.00 and 3.27)</li><li>Document Output 4.xx (any version between 4.01 and 4.04)</li><li>Document Output 5.xx (any version between 5.01 and 5.03)</li><li>Document Output 6.xx (any version between 6.01 and 6.02)</li><li>Document Output 7.xx (any version between 7.01 and 7.04)</li><li>Document Output 8.xx (any version between 8.00 and 8.02)</li></ul> | From these versions, you must do as follows to upgrade: <ol><li>In the <a href="https://partnerzone.continia.com/dashboard/">Continia PartnerZone</a>, go to <b>Downloads</b> and download the relevant product package.</li><li>Using the setup guide from the product package, install Document Output as usual. This will upgrade your software.</li></ol> |

> [!NOTE]
> Following any upgrade, you must download a new developer and customer license from Microsoft in order to obtain permissions for all new object numbers.

##See also
[Supported Upgrade Paths for Continia Document Output (FOB)](Supported Upgrade Paths.md)  
[Migrating Document Output from FOB to App for Business Central On-Premises](Migrating Document Output from FOB to app.md)  




<style>
  .content table tr td:nth-child(1) {
    width: 230px;
  }
  .content table tr td:nth-child(2) {
    width: 500px;
  }  
</style>