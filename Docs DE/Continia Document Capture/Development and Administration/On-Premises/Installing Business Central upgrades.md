---
title: Upgrades für Business Central On-Premises installieren
date: 17-11-2022
description: So installieren Sie größere oder kleinere (kumulative) Updates für Document Capture in Business Central On-Premises
id: DC-59
lang: de
---

# Upgrades für Business Central On-Premises installieren

{{include "installing-upgrades-to-business-central-on-premises" "Document Capture"}}

| Stufe                                 | Schritte                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Vor dem Upgrade von Business Central  | <ol><li><b>Deinstallieren Sie alle Apps in dieser Reihenfolge</b>: <br> Document Capture OnPremise (falls verwendet) > Document Capture > Delivery Network > Core</li><li><b>Heben Sie die Veröffentlichung aller Apps in dieser Reihenfolge auf</b>: <br> Document Capture OnPremise (falls verwendet) > Document Capture > Delivery Network > Core</li></ol>                                                                                                                                                                                                                                                                                                                                                                                                             |
| Nach dem Upgrade von Business Central | <ol><li><b>Veröffentlichen Sie alle Apps in dieser Reihenfolge</b>: <br> Core > Delivery Network > Document Capture > Document Capture OnPremise (falls verwendet)</li><li><b>Installieren Sie alle Apps in dieser Reihenfolge</b>: <br> Core > Delivery Network > Document Capture > Document Capture OnPremise (falls verwendet)</li><div class="alarm alarm-important"><p class="alert-title"><i class="icon icon-info"></i><span>Wichtig</span></p><p>Sie müssen das Document Capture Runtime Package installieren, das der neuen Version von Business Central entspricht. Die Funktionsfähigkeit von Runtime Packages wird nur dann garantiert, wenn sie auf einer Plattform mit derselben Version veröffentlicht werden, auf der sie erstellt wurden.</p></div></ol> |

## Informationen zum Thema

[Upgrade auf die neueste Version](@DC-58)

<style>
  .content table tr td:nth-child(1) {
    width: 140px;
  }
  .content table tr td:nth-child(2) {
    width: 590px;
  }  
</style>