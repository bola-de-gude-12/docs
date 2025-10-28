---
title: Belege und Vorlagen in Document Capture
date: 25-09-2025
description: Ein Überblick über die Dokumentation zur Funktionsweise von Belegen und Vorlagen.
id: DC-120
lang: de
---

# Belege und Vorlagen

Sobald Ihre Belege in Continia Document Capture importiert wurden, können Sie damit arbeiten. Alle Belege sind in Belegkategorien eingeteilt und die meisten von ihnen verwenden Belegvorlagen. Diese beiden Konzepte und wie sie mit Ihren Belegen verwendet werden, sind von grundlegender Bedeutung. Deshalb werden sie in den folgenden Abschnitten zusammen mit einigen anderen wichtigen Konzepten erläutert.

## Belegkategorien

Alle Belege gehören einer bestimmten Belegkategorie an, in denen alle Belege eines bestimmten Typs zusammengefasst sind. Beispielsweise gehören alle Einkaufsrechnungen und Gutschriften zur Belegkategorie **EINKAUF**, während alle Verkaufsaufträge zur Kategorie **VERKAUF** gehören. Jede Belegkategorie enthält eine Reihe von Regeln und Konfigurationen, die definieren, wie Belege innerhalb dieser Kategorie verarbeitet werden. Dies ist für Sie möglicherweise nicht so relevant, wenn Sie beispielsweise überwiegend Einkaufsbelege verarbeiten. Denken Sie aber daran, dass es verschiedene Arten von Belegen und unterschiedliche Belegkategorien gibt, falls Sie diese später benötigen.

## Vorlagen

Eine Vorlage ist eine Sammlung von Regeln und Konfigurationseinstellungen, die festlegen, wie Belege erfasst und verarbeitet werden sollen. Alle Vorlagen sind einer Belegkategorie zugeordnet, und jede Vorlage ist mit einem bestimmten Kreditor verknüpft. Vorlagen können auch mit anderen Entitäten als Kreditoren verknüpft werden, aber dieser Artikel konzentriert sich zur Veranschaulichung ausschließlich auf Kreditoren. In der Vorlage legen Sie fest, welche Informationen und welche Felder erfasst werden sollen, wenn Sie einen Beleg von einem bestimmten Kreditor erhalten. Da jeder Kreditor über eine eigene Vorlage verfügt, können Sie Vorlagen verwenden, um für jeden Kreditor unterschiedliche Informationen zu erfassen oder unterschiedliche Regeln und Konfigurationen anzuwenden.

Vorlagen verfügen normalerweise über ein oder mehrere Vorlagenfeld(er). Dabei handelt es sich um die Felder, die Sie in einem Beleg erfassen möchten. Beispielsweise enthalten Vorlagen für den Einkauf meist Vorlagenfelder wie **Rechnungsnr.**, **Buchungsdatum**, **Fälligkeitsdatum**, **Währung** und **Betrag**. Für jedes Vorlagenfeld können Sie unterschiedliche Regeln und Prüfungen einrichten, die immer dann angewendet werden, wenn Informationen für dieses bestimmte Feld erfasst werden. Beispielsweise möchten Sie möglicherweise eine Regel einrichten, um sicherzustellen, dass alle Rechnungen eine Bestellnummer enthalten oder dass Sie nur Rechnungen in einer bestimmten Währung von einem bestimmten Kreditor erhalten.

Document Capture umfasst vorkonfigurierte Vorlagen, sodass Sie nicht alles von Grund auf einrichten müssen. Sie müssen nur dann Änderungen an einer Vorlage oder einem der Vorlagenfelder vornehmen, wenn Sie ändern möchten, wie Informationen in Belegen bestimmter Kreditoren erfasst werden oder wenn Sie zusätzliche Informationen in Belegen erfassen möchten.

## Belege

Belege sind die eigentlichen Entitäten, die in Document Capture verarbeitet und gespeichert werden, wie z. B. Wenn Sie einen Beleg importieren, identifiziert Document Capture die Herkunft dieses Belegs (z. B. den Kreditor, der diesen gesendet hat) und verknüpft ihn mit der jeweiligen Vorlage, die dieser Herkunft zugeordnet ist. Sobald eine Herkunft identifiziert bzw. manuell zugewiesen wurde und die zugehörige Vorlage angewendet wurde, werden alle relevanten Informationen im Beleg automatisch erfasst, und der Beleg wird gemäß den Regeln und der Konfiguration der angewendeten Vorlage verarbeitet.

| Thema                                                                                                                                                                 | Siehe                                                                                |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| Überblick über die Methoden zum Importieren von Belegen in Document Capture                                                                                           | [Belege importieren](@DC-82)                                                         |
| Mehr Informationen zum OCR-Prozess                                                                                                                                    | [OCR-Verarbeitung von Belegen](@DC-145)                                              |
| Überblick über das Belegjournal, Belegen neue Kreditoren zuweisen und Anzeigen bestimmter Belegarten mit einem Filter                                                 | [Mit Papier- und PDF-Belegen arbeiten](@DC-71)                                       |
| Identifizieren oder Ändern von Kopffeldsuchtexten, Erfassen von Kopffeldwerten und Hinzufügen und Entfernen von Vorlagenfeldern                                       | [Kopffelder in einem Beleg erfassen](@DC-110)                                        |
| Identifizieren oder Ändern von Zeilenfeldsuchtexten und Erfassen von Zeilenfeldwerten (Zeilenerkennung)                                            | [Zeilenfelder in einem Beleg erfassen (Zeilenerkennung)](@DC-147) |
| Erfahren Sie mehr über die verbesserte Zeilenerkennung, einschließlich erweiterter KI-Funktionen, und nutzen Sie diese                                                | [Verbesserte Zeilenerkennung](@DC-191)                                               |
| Übersetzen erfasster Werte aus dem Feld **Einkäufer/Verkäufer** in Einkäufercodes für eine korrekte Registrierung                                                     | [Einkäufercodeübersetzung](@DC-128)                                                  |
| Registrieren von Belegen, um sie als echte Geschäftsentitäten in Microsoft Dynamics 365 Business Central verfügbar zu machen                                          | [Belege registrieren](@DC-67)                                                        |
| Artikelzu-/Abschläge den Zeilen eingehender Belege anhand vordefinierter Methoden automatisch zuweisen                                                                | [Artikelzu-/Abschläge automatisch zuweisen](@DC-137)                                 |
| Erneutes Öffnen von Belegen, beispielsweise zum erneuten Abgleich, zur Fehlerkorrektur oder bei irrtümlicher Ablehnung                                                | [Belege erneut öffnen](@DC-442)                                                      |
| Ablehnen von Belegen, um sie in der Datenbank zu behalten (anstatt sie vollständig zu löschen)                                                     | [Dokumente ablehnen](@DC-478)                                                        |
| Aufteilen von Dateien in mehrere separate Belege (entweder manuell oder automatisch) oder manuelles Zusammenführen mehrerer Dateien zu einem Beleg | [Belege aufteilen und zusammenführen](@DC-80)                                        |
| Verschieben von Belegen zu anderen Mandanten (manuell oder automatisch)                                                                            | [Belege zu anderen Mandanten verschieben](@DC-74)                                    |
| Näheres zur Identifizierung von Vorlagen                                                                                                                              | [Belegherkunft und -vorlage identifizieren](@DC-109)                                 |
| Erstellen und Einrichten neuer Vorlagenfelder                                                                                                                         | [Neue Vorlagenfelder einrichten](@DC-19)                                             |
| Hinzufügen von Suchtexten, die von Document Capture vorgeschlagenen wurde, in PDF-Mastervorlagen                                                                      | [Suchtexte zu PDF-Mastervorlagen hinzufügen](@DC-117)                                |
| Möglichkeiten zum Zugreifen auf das Belegarchiv                                                                                                                       | [Auf das Belegarchiv zugreifen](@DC-390)                                             |
| Konfigurieren von Bemerkungen und Näheres zu Kommentartypen                                                                                                           | [Bemerkungsarten und deren Wichtigkeit konfigurieren](@DC-72)                        |
