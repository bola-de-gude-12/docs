---
title: Upgrade auf die neueste Version (On-Premises)
date: 27-03-2025
description: So führen Sie ein Upgrade auf die neueste Version von Continia Document Capture in der On-Premises-Version von Business Central durch.
id: DC-58
lang: de
---

# Upgrade auf die neueste Version (On-Premises)

Dieser Abschnitt enthält Details zum Upgrade auf die neueste Version von Continia Document Capture in der On-Premises-Version von Microsoft Dynamics 365 Business Central (einschließlich Richtlinien zur Migration von On-Premises in die Cloud). Richtlinien für die Onlineversion von Business Central finden Sie unter [Upgrade auf die neueste Version](@DC-451).

Um Document Capture für App-Versionen von Business Central zu aktualisieren, müssen Sie das speziell entwickelte Continia PowerShell-Skript verwenden, das die App und alle Abhängigkeiten automatisch aktualisiert. Weitere Informationen finden Sie unter [Upgrade von Continia Document Capture für App-Versionen von Business Central](@DC-6).

Bei FOB-Versionen von Business Central hängt Ihr Upgradepfad davon ab, welche Versionen von Document Capture und Business Central Sie derzeit haben. Nicht alle Versionen von Document Capture sind mit allen Versionen von Business Central kompatibel (und umgekehrt). Daher wird grundsätzlich empfohlen, beides auf die neueste Version zu aktualisieren.

> [!NOTE]
> Die letzte FOB-Version von Document Capture ist 2024 R2 (25.00). On-Premises-Benutzer können die App-Version von Document Capture 2025 R1 (26.00) installieren.

Beachten Sie, dass beim Upgrade Ihrer alten Version von Document Capture auf die neueste unterstützte Version ein direktes Upgrade unter Umständen nicht möglich ist und Sie eventuell auch Ihre Version von NAV/Business Central aktualisieren müssen, um die Kompatibilität sicherzustellen. Informationen zum Upgrade auf die neueste FOB-Version von Document Capture finden Sie unter [Unterstützte Upgradepfade für Continia Document Capture (FOB)](@DC-8).

Wenn Sie mehrere Continia-Lösungen in einer FOB-Version von Business Central installiert haben und eine oder mehrere dieser Lösungen aktualisieren möchten, müssen Sie beim Importieren von Objekten bestimmte Schritte ausführen. Weitere Informationen finden Sie unter [Upgrade mit mehreren installierten Continia-Lösungen (FOB)](@DC-54).

Wenn Sie Document Capture in einer alten Version von NAV/Business Central verwenden und NAV/Business Central auf eine neuere Version aktualisieren möchten, müssen Sie je nach verwendeter Version auch Document Capture aktualisieren und/oder zugehörige Aufgaben ausführen. Informationen hierzu finden Sie unter [Upgrade von NAV/Business Central mit installiertem Document Capture](@DC-7).

Wenn Ihr Unternehmen von einer On-Premises-Bereitstellung zu einer Cloud-Umgebung wechseln möchte, finden Sie hierzu die erforderlichen Schritte unter [Document Capture von Business Central On-Premises zur Cloud migrieren](@DC-106).

> [!IMPORTANT]
> Nach jedem Upgrade (sowohl für App- als auch für FOB-Versionen von Business Central) müssen Sie immer eine neue und aktualisierte Kundenlizenzdatei von Microsoft herunterladen und verwenden.

> [!TIP]
> Sie können die Document Capture-Installationspakete und Upgrade-Dateien für FOB-Versionen in der [Continia PartnerZone](https://partnerzone.continia.com/downloads/) herunterladen (nur für Partner verfügbar).

## Informationen zum Thema

[Upgrade von Continia Document Capture für App-Versionen von Business Central](@DC-6)\
[Unterstützte Upgradepfade für Continia Document Capture (FOB)](@DC-8)\
[Upgrade von NAV/Business Central mit einer Installation von Document Capture](@DC-7)\
[Document Capture von Business Central On-Premises zur Cloud migrieren](@DC-106)