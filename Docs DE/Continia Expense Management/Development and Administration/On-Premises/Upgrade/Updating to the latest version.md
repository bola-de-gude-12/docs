---
title: Expense Management Upgrade auf die neueste Version
date: 09-07-2025
description:
id: EM-87
lang: de
---

# Auf die neueste Version aktualisieren

Informationen zum Upgrade auf die neueste Version von Continia Expense Management in der _On-Premises_-Version von Microsoft Dynamics 365 Business Central (einschließlich Richtlinien zur Migration von On-Premises in die Cloud). Eine Anleitung für die _Online_-Version von Business Central finden Sie [hier](/Continia Expense Management/Development and Administration/Online/Updating to the latest version.md).

Um Expense Management für _App_-Versionen von Business Central zu aktualisieren, müssen Sie das speziell entwickelte Continia PowerShell-Skript verwenden, das die App und alle Abhängigkeiten automatisch aktualisiert. Weitere Informationen finden Sie unter [Upgrade von Expense Management Capture für App-Versionen von Business Central](Upgrading Expense Management for app versions.md).

Bei _FOB_-Versionen von Business Central hängt Ihr Upgradepfad davon ab, welche Versionen von Expense Management und Business Central Sie derzeit haben. Nicht alle Versionen von Expense Management sind mit allen Versionen von Business Central kompatibel (und umgekehrt). Daher empfehlen wir Ihnen grundsätzlich, beides auf die neueste Version zu aktualisieren.

Beachten Sie, dass beim Upgrade Ihrer alten Version von Expense Management auf die neueste Version ein direktes Upgrade unter Umständen nicht möglich ist und Sie eventuell auch Ihre Version von Microsoft Dynamics NAV/Business Central aktualisieren müssen, um die Kompatibilität sicherzustellen. Genaue Informationen zum Aktualisieren auf die neueste FOB-Version von Expense Management finden Sie unter [Unterstützte Upgradepfade für Continia Expense Management (FOB)](Supported Upgrade Paths.md).

Wenn Sie mehrere Continia-Lösungen in einer FOB-Version von Business Central installiert haben und eine oder mehrere dieser Lösungen aktualisieren möchten, müssen Sie beim Importieren von Objekten bestimmte Schritte ausführen. Weitere Informationen finden Sie unter [Upgrade mit mehreren installierten Continia-Lösungen (FOB)](/Continia Document Capture/Development and Administration/On-Premises/Upgrade/Upgrading with multiple solutions installed, FOB/Upgrading with multiple solutions installed, FOB.md).

> [!TIP]
> Sie können die Expense Management-Installationspakete und Upgrade-Dateien für FOB-Versionen in der [Continia PartnerZone](https://partnerzone.continia.com/downloads/) herunterladen (nur für Partner verfügbar).

Wenn Sie Expense Management in einer alten Version von NAV/Business Central verwenden und NAV/Business Central auf eine neuere Version aktualisieren möchten, müssen Sie je nach verwendeter Version auch Expense Management aktualisieren und/oder zugehörige Aufgaben ausführen. Weitere Informationen sowie Hinweise zur Vorgehensweise bei Ihrer jeweiligen alten Version von NAV/Business Central finden Sie unter [Upgrade von NAV/Business Central mit einer Installation von Expense Management](Upgrading NAV or Business Central with Expense Management installed/Overview.md).

Wenn Ihr Unternehmen von einer On-Premises-Bereitstellung zu einer Cloud-Umgebung wechseln möchte, finden Sie hierzu die erforderlichen Schritte im Artikel [Expense Management von Business Central On-Premises zur Cloud migrieren](Migrate from on-premises to cloud.md).

> [!IMPORTANT]
> Nach jedem Upgrade (sowohl für App- als auch für FOB-Versionen von Business Central) müssen Sie immer eine neue und aktualisierte Kundenlizenzdatei von Microsoft herunterladen und verwenden.

## Informationen zum Thema

[Upgrade von Continia Expense Management für App-Versionen von Business Central](Upgrading Expense Management for app versions.md)  
[Unterstützte Upgradepfade für Continia Expense Management (FOB)](Supported Upgrade Paths.md)  
[Upgrade von NAV/Business Central mit einer Installation von Expense Management](Upgrading NAV or Business Central with Expense Management installed/Overview.md)  
[Expense Management von Business Central On-Premises zur Cloud migrieren](Migrate from on-premises to cloud.md)