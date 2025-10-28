---
title: Expense Management Upgrades für Business Central On-Premises installieren
date: 18-07-2022
description: So installieren Sie größere oder kleinere (kumulative) Updates für Expense Management in Business Central On-Premises
id: EM-89
lang: de
---

# Upgrades für Business Central On-Premises installieren

{{include "installing-upgrades-to-business-central-on-premises" "Expense Management"}}

| Stufe                                 | Aktion                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| ------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Vor dem Upgrade von Business Central  | <ol><li><b>Deinstallieren Sie alle Apps in dieser Reihenfolge</b>: <br> Document Capture OnPremise (falls verwendet) > Expense Management > Delivery Network > Core</li><li><b>Heben Sie die Veröffentlichung aller Apps in dieser Reihenfolge auf</b>: <br> Document Capture OnPremise (falls verwendet) > Expense Management > Document Capture > Delivery Network > Core</li></ol>                                                                                                                                                                                                                                                  |
| Nach dem Upgrade von Business Central | <ol><li><b>Veröffentlichen Sie alle Apps in dieser Reihenfolge</b>: <br> Core > Delivery Network > Document Capture > Expense Management > Document Capture OnPremise (falls verwendet)</li><li><b>Installieren Sie alle Apps in dieser Reihenfolge</b>: <br> Core > Delivery Network > Document Capture > Expense Management > Document Capture OnPremise (falls verwendet)</li><div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Note</span></p><p>Sie müssen das Expense Management Runtime Package installieren, das der neuen Version von Business Central entspricht.</p></div></ol> |

## Informationen zum Thema

[Upgrade auf die neueste Version](@EM-87)

<style>
  .content table tr td:nth-child(1) {
    width: 140px;
  }
  .content table tr td:nth-child(2) {
    width: 590px;
  }  
</style>
