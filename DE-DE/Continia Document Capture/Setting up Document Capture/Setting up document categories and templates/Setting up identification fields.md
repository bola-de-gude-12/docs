---
title: Identifikationsfelder einrichten
date: 19-08-2022
description: null
id: DC-81
lang: de
---

# Identifikationsfelder einrichten

Zur Veranschaulichung konzentriert sich die folgende Erklärung der Identifikationsfelder auf Kreditoren. Beachten Sie jedoch, dass Identifikationsfelder immer gemäß der Herkunftstabelle konfiguriert werden, die in der entsprechenden Belegkategorie eingerichtet ist.

Identifikationsfelder werden verwendet, um die Herkunft eines importierten Belegs zu identifizieren, in diesem Fall den Kreditor. In der Tabelle Kreditor können Sie ein Feld oder mehrere Felder auswählen, die Document Capture verwendet, um den Kreditor zu identifizieren (z. B. Name, Adresse, Telefonnummer oder Umsatzsteuer-Identifikationsnummer). Um zu ermitteln, welchem Kreditor ein bestimmter Beleg zugeordnet werden soll, durchsucht Document Capture alle Kreditoren in der Tabelle Kreditor nach den Werten der ausgewählten Identifikationsfelder (Name, Adresse usw.) innerhalb des Belegs. Der Beleg wird dann dem Kreditor zugewiesen, dessen Feldwerte am besten mit den im Beleg identifizierten Werten übereinstimmen.

Beim Identifizieren des Kreditors eines Belegs ist es möglich, dass mehrere Kreditoren vollständig oder teilweise mit dem Kreditor im Beleg übereinstimmen. Um den richtigen Kreditor zu bestimmen, weist Document Capture jedem Kreditor eine Zuverlässigkeitsbewertung (Confidence Score) zu, die darüber entscheidet, welcher Kreditor dem Beleg zugeordnet wird.

> [!NOTE]
> Die Verwendung von Identifikationsfeldern ist einer von drei Schritten bei der Identifizierung der Belegherkunft. Weitere Informationen finden Sie unter [Belegherkunft und -vorlage identifizieren](/Continia Document Capture/Business functionality/Documents and templates/Finding the document source and template.md).

## So konfigurieren Sie Identifikationsfelder für Einkaufsbelege

Sie können Identifikationsfelder für alle Belegkategorien konfigurieren. Gehen Sie dazu folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Belegkategorien** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die entsprechende Belegkategorie. Um beispielsweise die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF,** da dadurch das Belegjournal geöffnet wird) und wählen Sie dann **Bearbeiten** in der Aktionsleiste.
3. Wählen Sie auf der Seite **Belegkategorie** in der Aktionsleiste **Identifikationsfelder** aus.
4. Die Seite **Identifikationsfelder** wird geöffnet und zeigt die aktuelle Auswahl an Identifikationsfeldern an. Um ein neues Feld hinzuzufügen, wählen Sie in der Aktionsleiste **Neu** aus und wählen Sie dann unter **Feldnr.** die drei Punkte in der neu hinzugefügten Zeile aus.
5. Dadurch wird die Seite **Felder-Lookup** geöffnet, auf der alle Felder in der Tabelle Kreditor angezeigt werden. Fügen Sie das gewünschte Feld hinzu, indem Sie die entsprechende Nummer in der Spalte **Nr.** auswählen.
6. Die Seite **Felder-Lookup** wird geschlossen und Sie kehren zur Seite **Identifikationsfelder** zurück, wo das ausgewählte Identifikationsfeld jetzt hinzugefügt wurde.
7. Auf der Seite **Identifikationsfelder** können Sie auch vorhandene Identifikationsfelder löschen, indem Sie das/die entsprechende(n) Feld(er) auswählen und dann in der Aktionsleiste **Löschen** wählen. Mit Strg+Klicken können Sie mehrere Einträge auswählen.
8. Auf der Seite **Identifikationsfelder** können Sie auch alle vorhandenen Identifikationsfelder bearbeiten: Wählen Sie das Feld **Feldnr.** für das Identifikationsfeld aus, das Sie bearbeiten möchten, und wählen Sie dann die drei Punkte aus, um die Seite **Felder-Lookup** Seite zu öffnen. Hier können Sie das gewünschte Feld hinzufügen, indem Sie die entsprechende Nummer in der Spalte **Nr.** auswählen.
9. Für jedes der ausgewählten Identifikationsfelder können Sie die zugewiesene Einstufung bearbeiten, indem Sie eine Zahl in die Spalte **Einstufung** eingeben. Je höher die Zahl, desto mehr Gewicht hat das Feld, wenn Document Capture versucht, die Herkunft eines importierten Belegs zu identifizieren. Weitere Informationen finden Sie unter [Zuverlässigkeitsbewertungen berechnen](/continia-document-capture/setting-up-document-capture/setting-up-document-categories-and-templates/setting-up-identification-fields#calculating-confidence-scores).

> [!NOTE]
> Beim Erstellen eines neuen oder Bearbeiten eines vorhandenen Identifikationsfelds können Sie keine Identifikationsfelder auswählen, die bereits in der aktuellen Auswahl enthalten sind, d. h. in der Liste, die auf der Seite **Identifikationsfelder** angezeigt wird.

## Zuverlässigkeitsbewertungen berechnen
Für jeden Kreditor berechnet Document Capture eine Zuverlässigkeitsbewertung. Dabei wird nach jedem als Identifikationsfeld konfigurierten Feld gesucht und die Anzahl der Zeichen des erkannten Feldwertes mit der konfigurierten Einstufung multipliziert. Im Folgenden finden Sie ein Beispiel:

| Feld              | Wert               | Einstufung | Zuverlässigkeitsbewertung      |
| ----------------- | ------------------ | ---------- | ------------------- |
| **Name**          | Microsoft          | 1          | 9 (1 × 9 Zeichen)   |
| **Adresse**       | One Microsoft Road | 1          | 18 (1 × 18 Zeichen) |
| **Bankkonto Nr.** | 1212-1928381887231 | 2          | 36 (2 × 18 Zeichen) |
| _Gesamtbewertung_     |                    |            | 63                  |

Der Grund dafür, dass einigen Feldern möglicherweise höhere Einstufungen zugewiesen werden, liegt darin, dass einige Werte mit größerer Wahrscheinlichkeit eindeutig sind als andere. Beispielsweise kann die Adresse eines Unternehmens mit der eines anderen Unternehmens identisch sein; die Bankkontonummer eines Unternehmens ist jedoch eindeutig, da sie immer nur zu einem Unternehmen gehört.

Document Capture findet nicht immer alle Identifikationsfelder für Kreditoren in importierten Belegen. Es ist möglich, dass in manchen Belegen mehrere Kreditoren identifiziert werden, die alle dem richtigen Kreditor zugeordnet werden könnten. Im folgenden Beispiel könnte ein Beleg mit zwei Kreditoren übereinstimmen:

Kreditor 1:

| Feld              | Wert im Beleg      | Wert für Kreditor 1 | Einstufung | Zuverlässigkeitsbewertung |
| ----------------- | ------------------ | ------------------- | ---------- | -------------- |
| **Name**          | Microsoft          | Microsoft           | 1          | 9              |
| **Adresse**       | One Microsoft Road | One Microsoft Road  | 1          | 18             |
| **Bankkonto Nr.** | 1212-1928381887231 | 1212-1928381887231  | 2          | 36             |
| _Gesamtbewertung_     |                    |                     |            | 63             |

Kreditor 2:

| Feld              | Wert im Beleg      | Wert für Kreditor 2 | Einstufung | Zuverlässigkeitsbewertung |
| ----------------- | ------------------ | ------------------- | ---------- | -------------- |
| **Name**          | Microsoft          | Microsoft           | 1          | 9              |
| **Adresse**       | One Microsoft Road | One Microsoft Road  | 1          | 18             |
| **Bankkonto Nr.** | 1212-1928381887231 | 0000-0000000000000  | 2          | 0              |
| _Gesamtbewertung_     |                    |                     |            | 27             |

In diesem Beispiel hat Kreditor 1 die höchste Zuverlässigkeitsbewertung und wird daher dem Beleg zugeordnet.

> [!NOTE]
> Um unzuverlässige Ergebnisse zu vermeiden, muss eine Mindestzuverlässigkeitsbewertung erreicht werden, damit ein Kreditor einem Beleg zugewiesen werden kann. Wenn beispielsweise die einzige Übereinstimmung zwischen einem Beleg und einem Kreditor die Stadt des Kreditors ist, wurde möglicherweise nicht der richtige Kreditor identifiziert, da andere Kreditoren ebenfalls in derselben Stadt ansässig sein können.

## Informationen zum Thema

[Belegherkunft und -vorlage identifizieren](@DC-109)
