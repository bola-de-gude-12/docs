---
title: Installing Upgrades to Business Central On-Premises in Payment Management
description: How to manage your Continia solutions when you upgrade Business Central On-Premises in Payment Management.
date: 30-09-2022
id: PM-236
lang: en
---

# Installing Upgrades to Business Central On-Premises

{{include "installing-upgrades-to-business-central-on-premises" "Payment Management"}}


| Stage                             | Steps                                                        |
| --------------------------------- | ------------------------------------------------------------ |
| Before upgrading Business Central | <ol><li>**Uninstall all apps in this order**:<br />    Continia Payment Management (DK, SE, NO, NL, or IE) > Continia Payment Management > Continia Core</li><li>**Unpublish all apps in this order**: <br />    Continia Payment Management (DK, SE, NO, NL, or IE) > Continia Payment Management > Continia Core</li></ol> |
| After upgrading Business Central  | <ol><li>**Republish all apps in this order**:<br/> Continia Core > Continia Payment Management > Continia Payment Management (DK, SE, NO, NL, or IE)</li><li>**Reinstall all apps in this order**:<br/>Continia Core > Continia Payment Management > Continia Payment Management (DK, SE, NO, NL, or IE)</li><div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Note</span></p><p>You must install the Payment Management runtime package that corresponds to the new version of Business Central.</p></div></ol> |

## Related information
[Upgrading Payment Management On-Premises](@PM-17) 

<style>
  .content table tr td:nth-child(1) {
    width: 140px;
  }
  .content table tr td:nth-child(2) {
    width: 590px;
  }  
</style>
