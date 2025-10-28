---
title: Upgrade auf Business Central 2025 Release Wave 1 (v26)
date: 07-04-2025
description: So führen Sie ein Upgrade auf Business Central 2025 Release Wave 1 (v26) durch.
id: DC-457
lang: de
---

# Upgrade auf Business Central 2025 Release Wave 1 (v26)

Die folgende Tabelle bietet einen Überblick darüber, welche Schritte erforderlich sind, wenn Sie Continia Document Capture (DC) installiert haben und Ihre alte Version von Microsoft Dynamics NAV/Business Central (BC) auf Business Central 2025 Release Wave 1 (v26) aktualisieren möchten. Wenn Sie die unter **Aufgaben** unten angegebenen Richtlinien befolgen, bleibt Document Capture voll funktionsfähig und mit Ihrer aktualisierten Version von Business Central kompatibel.

> [!NOTE]
> Ab Release Wave 1 (v26) 2025 wird das direkte Upgrade von Business Central 2019 (v14) auf die neueste Version nicht mehr unterstützt. Der unterstützte Upgradepfad erfolgt über Release Wave 2 (v25) 2024 und dann auf v26. Weitere Informationen finden Sie unter [Deprecated features in the platform - clients, server, and database](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-platform#changes-in-2025-release-wave-1-version-260) (Microsoft-Artikel).

<br>

| Szenario                                                     | Aufgaben                                                     |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Vollständiges Upgrade von einer der folgenden Versionen: <li>Microsoft Dynamics NAV 2015</li><li>Microsoft Dynamics NAV 2016</li><li>Microsoft Dynamics NAV 2017</li><li>Microsoft Dynamics NAV 2018</li><li>Business Central Oktober 2018 (v13)</li></ul> | <ol><li>Führen Sie ein Upgrade auf BC v14 (FOB-basiert) mit [dieser Anleitung](@DC-102) durch.</li><li>Führen Sie von BC v14 (FOB-basiert) ein Upgrade auf BC v24 durch, indem Sie der Anleitung folgen, die weiter unten in der Tabelle „Business Central April 2019 (v14, FOB-basiert)“ beschrieben ist.</li></ol> |
| Vollständiges Upgrade von der folgenden Version: <ul><li>Business Central April 2019 (v14, FOB-basiert)</li></ul> | <ol><li>Führen Sie ein Upgrade auf BC v25 mit [dieser Anleitung](@DC-235) durch.</li><li>Führen Sie ein Upgrade auf BC v26 mit [dieser Anleitung](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-overview-v26) durch.</li><li>Aktualisieren Sie DC auf die neueste Version (sofern Sie dies nicht bereits mit einer früheren BC-Version vorgenommen haben). Auf [dieser Seite](@DC-8) finden Sie Informationen dazu, wie Sie ein Upgrade von Ihrer jeweiligen Version von DC durchführen.</li><li>Folgen Sie [dieser Anleitung](@DC-113), um Tabellendaten zu Erweiterungen zu migrieren. </li></ol> |
| Vollständiges Upgrade von einer der folgenden Versionen: <ul><li>Business Central 2019 Wave 2 (v15)</li><li>Business Central 2020 Wave 1 (v16)</li><li>Business Central 2020 Wave 2 (v17)</li><li>Business Central 2021 Wave 1 (v18)</li><li>Business Central 2021 Wave 2 (v19)</li><li>Business Central 2022 Wave 1 (v20)</li><li>Business Central 2022 Wave 2 (v21)</li><li>Business Central 2023 Wave 1 (v22)</li><li>Business Central 2023 Wave 2 (v23)</li></ul><li>Business Central 2024 Wave 1 (v24)</li></ul> | <ol><li>Deinstallieren Sie alle Continia-Apps und heben Sie deren Veröffentlichung auf.</li><li>Führen Sie mithilfe der [Microsoft-Anleitung](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-overview-v26) ein Upgrade auf BC v26 durch.</li><li>Veröffentlichen und installieren Sie die neuesten Versionen aller Continia-Apps mithilfe der Anleitung [Continia Document Capture On-Premises installieren](@DC-51).</li></ol> |

## Informationen zum Thema

[Unterstützte Upgradepfade für Continia Document Capture (FOB)](@DC-8)

<style>
  .content table tr td:nth-child(1) {
    width: 230px;
  }
  .content table tr td:nth-child(2) {
    width: 500px;
  }  
</style>