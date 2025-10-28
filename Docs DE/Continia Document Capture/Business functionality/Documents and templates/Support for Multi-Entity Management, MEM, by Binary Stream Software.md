---
title: Unterstützung für Multi-Entity-Management (MEM) von Binary Stream Software
date: 03-05-2024
description:
id: DC-218
lang: de
---

# Unterstützung für Multi-Entity-Management (MEM) von Binary Stream Software

> [!IMPORTANT]
> Dieser Artikel gilt nur für Microsoft Dynamics 365 Business Central 2024 Release Wave 1 (BC v24) und höher.

Continia Document Capture unterstützt [Multi-Entity Management](https://binarystream.com/products/D365BC-MEM/) (MEM) von Binary Stream Software. MEM ist eine beliebte Erweiterung, mit der Sie mehrere juristische Entitäten in Business Central zu einem einzigen Mandanten konsolidieren können. Die Entitäten sind als Dimensionen in diesem einzelnen Mandanten vorhanden und diese Entitätsdimensionen müssen zuerst validiert werden, wenn Transaktionen in Business Central eingegeben werden.

Um Ihren Arbeitsablauf zu optimieren, können Sie alle in eingehenden Belegen erfassten Dimensionswerte von Document Capture automatisch als Entitätsdimensionen an MEM übertragen lassen. Dies ist sowohl für Einkaufs- als auch für Verkaufsbelege möglich und wird durchgeführt, wenn Sie die Belege wie unten beschrieben in Ihrem Belegjournal registrieren.

> [!NOTE]
> Diese Funktionalität ersetzt die App „DC+MEM Dimension Helper“, die zuvor für die Integration von Document Capture und MEM erforderlich war. Um die nahtlose Integration zwischen beiden aufrechtzuerhalten und die Leistung der neuen Funktion in Document Capture 2024 R1 zu optimieren, müssen Sie möglicherweise diese Helper-App und alle anderen benutzerdefinierten MEM-Erweiterungen deinstallieren.

## Allgemeine Funktionalität

Die Integration zwischen Document Capture und MEM bietet Folgendes: Wenn Sie im Belegjournal einen Einkaufs- oder Verkaufsbeleg registrieren, für den eine Entitätsdimension (auf der Seite **MEM Multi-Entity Management Setup** unter **Entitätsdimension**) definiert wurde, wird der Wert des Vorlagenfelds, das der definierten Entitätsdimension entspricht, automatisch in MEM übertragen. Betrachten Sie folgendes Beispiel:

1. **Entitätsdimension** wurde auf der Seite **MEM Multi-Entity Management Setup** als **Code der globalen Dimension 1** definiert.
2. **Code der globalen Dimension 1** wurde im Inforegister **Dimensionen** der **Finanzbuchhaltung Einrichtung** als **Abteilung** konfiguriert.
3. Das Feld **Abteilung** wurde der entsprechenden Vorlage hinzugefügt (im Abschnitt **Belegkopf** des Belegjournals) und der Wert **ADM** wurde für dieses Feld erfasst.

Der Wert **ADM** wird dann automatisch als Entitätsdimension in MEM übertragen, wenn Sie einen Beleg mit dieser Vorlage im Belegjournal registrieren. Dies bedeutet, dass Sie die Entitätsdimension nicht manuell in einem MEM-Dialog angeben müssen, was zu einem reibungsloseren Arbeitsablauf und einer einfacheren Belegregistrierung führt.

## Verhalten bei fehlenden Entitätsdimensionswerten

Die obige Funktionalität gilt für die Kategorien **EINKAUF** und **VERKAUF** und die Funktionalität ist für beide Kategorien identisch, solange Dimensionswerte erfasst werden. Wenn jedoch keine solchen Werte erkannt werden, gibt es hinsichtlich des Verhaltens von Document Capture bestimmte Unterschiede zwischen den Kategorien:

Sollte bei einem Beleg der Kategorie **EINKAUF** ein Entitätsdimensionswert fehlen, wird bei der Erfassung des Belegs ein Dialogfenster eingeblendet, in dem Sie die Entitätsdimension manuell festlegen können. Aufgrund bestimmter Einschränkungen in der MEM-Erweiterung wird dieses Dialogfeld jedoch nicht angezeigt, wenn Entitätsdimensionswerte für Belege in der Kategorie **VERKAUF** fehlen. Stattdessen zeigt Document Capture den folgenden nicht konfigurierbaren Fehlerkommentar im Abschnitt **Bemerkungen** des Belegjournals an, um zu verhindern, dass Sie einen Verkaufsbeleg ohne Entitätsdimension registrieren, was zu einer Fehlfunktion von MEM führen würde:

- _Multi Entity Company is missing._