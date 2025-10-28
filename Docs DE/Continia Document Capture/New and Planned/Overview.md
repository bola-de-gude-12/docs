---
title: Veröffentlichungsplan für Document Capture
date: 17-10-2025
description: Die Document Capture-Roadmap bietet einen Überblick über kommende Funktionen.
id: DC-56
lang: de
---

# Veröffentlichungsplan für Document Capture

{{include "new-and-planned-overview" "Document Capture"}}

| Funktion                                                     |  Öffentliche Vorschau   |                   Allgemeine Verfügbarkeit                   |
| ------------------------------------------------------------ | :---------------------: | :----------------------------------------------------------: |
| [eDocuments first](@DC-467)                                  | {{checkmark}} Sep. 2025 |                   {{checkmark}} Sep. 2025                    |
| [Unterstützung für das SimplerInvoicing-Format in den Niederlanden](Documents and Templates/Support for the SimplerInvoicing format in the Netherlands.md) | {{checkmark}} Sep. 2025 | {{checkmark}} Sep. 2025<a href="#footnote-7"><sup>7</sup></a> |
| [Option zum Einbetten von PDF-Dateien](@DC-465)              | {{checkmark}} Sep. 2025 |                   {{checkmark}} Okt. 2025                    |
| [Lookup in Vorlagenfeldübersetzungen](@DC-468)               | {{checkmark}} Sep. 2025 |                   {{checkmark}} Okt. 2025                    |
| [Verarbeitung von Dokumenten mit Rundungsproblemen](@DC-469) | {{checkmark}} Sep. 2025 |                   {{checkmark}} Okt. 2025                    |
| [Erfassen von Informationen zur Artikelverfolgung](@DC-470)  | {{checkmark}} Sep. 2025 |                   {{checkmark}} Okt. 2025                    |
| [Unterstützung für die Nachhaltigkeitsfunktion von Business Central](@DC-322) | {{checkmark}} Sep. 2025 |                   {{checkmark}} Okt. 2025                    |
| [eDokumente-Validierung](@DC-466)                            |            -            |       Nov. 2025<a href="#footnote-9"><sup>9</sup></a>        |
| [Unterstützung für das FA(3)-Format in Polen](@DC-417)       |            -            |      Nov. 2025<a href="#footnote-10"><sup>10</sup></a>       |
| [Unterstützung für OData V4 für das Continia Web Approval Portal](Web Approval Portal/Support for OData V4 for the Continia Web Approval Portal.md) |            -            |          N/A<a href="#footnote-1"><sup>1</sup></a>           |
| [Benachrichtigung über offene Genehmigungsposten in allen Mandanten mit nur einer E-Mail](Document Approval/One email for all companies to notify about open approval entries.md) |            -            |          N/A<a href="#footnote-1"><sup>1</sup></a>           |
| [Continia eDocuments – Unterstützung für OIOUBL 3.0](Documents and Templates/Continia eDocuments support for OIOUBL 3.0.md) |            -            |          N/A<a href="#footnote-2"><sup>2</sup></a>           |
| [Überprüfung von PDF-Signaturen](Documents and Templates/Checking PDF signatures.md) |            -            |          N/A<a href="#footnote-3"><sup>3</sup></a>           |
| [Optimierter Export von Benutzern - Teil 2](Web Approval Portal/Optimized export of users - part 2.md) |            -            |          N/A<a href="#footnote-4"><sup>4</sup></a>           |
| [Identifizierung von Kontonummern mithilfe künstlicher Intelligenz](Documents and Templates/Identification of account numbers using artificial intelligence.md) |            -            |          N/A<a href="#footnote-5"><sup>5</sup></a>           |
| [Unterstützung für Verkaufslieferungen](Documents and Templates/Support for sales shipments.md) |            -            |          N/A<a href="#footnote-8"><sup>8</sup></a>           |
| [Unterstützung für das EHF-Format für eBestellungen in Norwegen](Documents and Templates/Support for the EHF format for eOrders in Norway.md) |            -            |          N/A<a href="#footnote-8"><sup>8</sup></a>           |
| [Eine neue Seite, auf der Benutzer mehr Informationen über eDocuments und Formate finden](Documents and Templates/Educational page to improve user knowledge of eDocuments and formats.md) |            -            |          N/A<a href="#footnote-8"><sup>8</sup></a>           |
| [Leichteres eDocuments-Onboarding](Documents and Templates/Simpler eDocuments onboarding.md) |            -            |          N/A<a href="#footnote-8"><sup>8</sup></a>           |
| [Verarbeiten von XML-Dateien, die über E-Mail empfangen werden, mit dem eDocuments-Framework](@DC-401) |            -            |          N/A<a href="#footnote-8"><sup>8</sup></a>           |

<small style>

<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1">Das Veröffentlichungsdatum für diese Funktion steht noch nicht fest.</li>
    <li id="footnote-2">Die Veröffentlichung dieser Funktion hängt von der offiziellen Veröffentlichung von OIOUBL 3.0 ab, an der die dänische Wirtschaftsbehörde (Erhvervsstyrelsen) derzeit arbeitet.</li>
    <li id="footnote-3">Da es bei Continia bislang keine rechtlichen oder geschäftlichen Anforderungen hinsichtlich der Überprüfung von Signaturen auf eingehenden PDF-Dateien gibt, wurde diese Funktion auf eine spätere Version von Document Capture verschoben.</li>
    <li id="footnote-4">Der erste Teil dieser Funktion hat die meisten Probleme mit Bezug auf die Benutzeraktualisierung behoben. Daher ist es nicht mehr erforderlich, den zweiten Teil der Optimierung zu implementieren.</li>
    <li id="footnote-5">Nach Prüfung der Möglichkeiten ist Continia zu dem Schluss gekommen, dass der Einsatz künstlicher Intelligenz zur Ermittlung von Kontonummern die Bearbeitungszeit vorerst nicht verkürzen würde.</li>
    <li id="footnote-6">Diese Funktion wurde im Mai 2025 gemäß den Anforderungen der australischen und neuseeländischen Regierung veröffentlicht.</li>
    <li id="footnote-7">Diese Funktion wird entweder als Teil eines Hotfixes oder eines Service Packs veröffentlicht.</li>
    <li id="footnote-8">Aufgrund von Änderungen im Fokus und der Gesetzgebung hat Continia beschlossen, die Veröffentlichung dieser Funktion zu verschieben.</li>
    <li id="footnote-9">Diese Funktion wird im November 2025 als Teil eines Service Packs veröffentlicht.</li>
    <li id="footnote-10">Da die offizielle Version der KSeF-API erst Ende September verfügbar sein wird, kann diese Funktion nicht im Oktober veröffentlicht werden – sie wird jedoch mit dem nächsten Service Pack veröffentlicht.</li>
  </ol>
</div>

</small>

## Detailliertes Changelog

Für jede Änderung an Document Capture wird das detaillierte Changelog von Continia mit einer Beschreibung der Änderungen aktualisiert. Die vollständigen Änderungsprotokolle finden Sie unter [Detaillierte Changelogs für Document Capture](@DC-449).