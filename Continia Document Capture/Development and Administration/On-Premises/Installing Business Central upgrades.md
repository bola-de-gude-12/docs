---
title: Installing Upgrades to Business Central On-Premises
date: 17-11-2022
description: How to install major or minor (cumulative) updates to Document Capture in Business Central on-premises
id: DC-59
lang: en
---

# Installing Upgrades to Business Central On-Premises

{{include "installing-upgrades-to-business-central-on-premises" "Document Capture"}}


| Stage | Steps |
| --- | --- |
| Before upgrading Business Central | <ol><li><b>Uninstall all apps in this order</b>: <br> Document Capture OnPremise (if used) > Document Capture > Delivery Network > Core</li><li><b>Unpublish all apps in this order</b>: <br> Document Capture OnPremise (if used) > Document Capture > Delivery Network > Core</li></ol> |
| After upgrading Business Central | <ol><li><b>Publish all apps in this order</b>: <br> Core > Delivery Network > Document Capture > Document Capture OnPremise (if used)</li><li><b>Install all apps in this order</b>: <br> Core > Delivery Network > Document Capture > Document Capture OnPremise (if used)</li><div class="alarm alarm-important"><p class="alert-title"><i class="icon icon-info"></i><span>Important</span></p><p>You must install the Document Capture runtime package that corresponds to the new version of Business Central. Runtime packages are guaranteed to work only if published to a platform with the same version as the one on which they were created.</p></div></ol> |

## Related information

[Upgrading to the Latest Version](@DC-58)  




<style>
  .content table tr td:nth-child(1) {
    width: 140px;
  }
  .content table tr td:nth-child(2) {
    width: 590px;
  }  
</style>