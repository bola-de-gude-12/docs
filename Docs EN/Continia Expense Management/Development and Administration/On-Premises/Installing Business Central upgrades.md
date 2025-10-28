---
title: Expense Management Installing Upgrades to Business Central On-Premises
date: 18-07-2022
description: How to install major or minor (cumulative) updates to Expense Management in Business Central on-premises
id: EM-89
lang: en
---

# Installing Upgrades to Business Central On-Premises

{{include "installing-upgrades-to-business-central-on-premises" "Expense Management"}}

| Stage | Action |
| --- | --- |
| Before upgrading Business Central | <ol><li><b>Uninstall all apps in this order</b>: <br> Document Capture OnPremise (if used) > Expense Management > Document Capture > Delivery Network > Core</li><li><b>Unpublish all apps in this order</b>: <br> Document Capture OnPremise (if used) > Expense Management > Document Capture > Delivery Network > Core</li></ol> |
| After upgrading Business Central | <ol><li><b>Publish all apps in this order</b>: <br> Core > Delivery Network > Document Capture > Expense Management > Document Capture OnPremise (if used)</li><li><b>Install all apps in this order</b>: <br> Core > Delivery Network > Document Capture > Expense Management > Document Capture OnPremise (if used)</li><div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Note</span></p><p>You must install the Expense Management runtime package that corresponds to the new version of Business Central.</p></div></ol> |

## Related information

[Upgrading to the Latest Version](@EM-87)  



<style>
  .content table tr td:nth-child(1) {
    width: 140px;
  }
  .content table tr td:nth-child(2) {
    width: 590px;
  }  
</style>