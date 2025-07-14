---
title: Continia Finance Installing Upgrades to Business Central On-Premises
date: 26-08-2024
description: How to install major or minor (cumulative) updates to Continia Finance in Business Central on-premises
id: CF-05
lang: en
---

# Installing Upgrades to Business Central On-Premises

{{include "installing-upgrades-to-business-central-on-premises" "Finance"}}

| Stage | Action |
| --- | --- |
| Before upgrading Business Central | <ol><li><b>Uninstall all apps in this order</b>: <br> Continia Finance > Core</li><li><b>Unpublish all apps in this order</b>: <br> Continia Finance > Core</li></ol> |
| After upgrading Business Central | <ol><li><b>Publish all apps in this order</b>: <br> Core > Continia Finance</li><li><b>Install all apps in this order</b>: <br> Core > Continia Finance</li><div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Note</span></p><p>You must install the Continia Finance runtime package that corresponds to the new version of Business Central.</p></div></ol> |



<style>
  .content table tr td:nth-child(1) {
    width: 140px;
  }
  .content table tr td:nth-child(2) {
    width: 590px;
  }  
</style>