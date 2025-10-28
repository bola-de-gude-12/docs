---
title: Die Belegart und andere grundlegende Details identifizieren
date: 08-06-2023
description: Eine Beschreibung, wie Document Capture versucht, bestimmte grundlegende Informationen für jeden eingehenden Beleg zu identifizieren, einschließlich Währung, Belegart, Fälligkeitsdatum, Verkäufer/Einkäufer, Sachkonto und andere Kontotypen.
id: DC-146
lang: de
---

# Die Belegart und andere grundlegende Details identifizieren

Sobald ein importierter [Beleg mit OCR verarbeitet wurde](@DC-145) und eine [Belegherkunft (z. B. ein Kreditor) zugewiesen wurde](@DC-109) (entweder automatisch oder manuell), versucht Continia Document Capture automatisch, die Belegart und weitere grundlegende Informationen im Beleg zu identifizieren. Dabei hängen die Details, die identifiziert werden sollen, von der jeweiligen Belegkategorie ab. Für die Kategorie Einkauf versucht Document Capture folgende Informationen zu identifizieren:

- Währung
- Belegart
- Fälligkeitsdatum
- Verkäufer/Einkäufer
- Sachkonto und ggf. weitere Kontoarten

Wenn Document Capture diese Informationen nicht identifizieren kann, müssen Sie sie selbst manuell eingeben.

Dieser Artikel bezieht sich zur Veranschaulichung auf Rechnungen, die in die Kategorie Einkauf importiert werden. Die meisten Informationen und alle zugrunde liegenden Prinzipien gelten jedoch auch für andere Kategorien und Belegarten.

## Die Belegart identifizieren

Um die Belegart zu identifizieren, überprüft Document Capture die erste Seite des importierten Belegs auf Suchtexte, die auf einen bestimmten Belegtyp hinweisen könnten (z. B. die Begriffe _Rechnung_ oder _Gutschrift_). Wenn mehrere relevante Suchtexte identifiziert werden, wird der Text mit der höchsten Position auf der Seite ausgewählt. Wenn beispielsweise das Wort _Rechnung_ vertikal über allen anderen identifizierten Suchtexten steht, wird der Beleg als Rechnung identifiziert.

> [!NOTE]
> Diese Methode unterscheidet sich von der Standardmethode zur Identifizierung: Bei anderen Vorlagenfeldern bestimmt die Suchtextlänge (d. h. die Anzahl der Zeichen in jedem identifizierten Suchtext) die Erkennungsreihenfolge.

Selbst wenn _Gutschrift_ direkt unter dem Wort _Rechnung_ steht, wird der Beleg standardmäßig als Rechnung betrachtet. Es ist jedoch möglich, dieses Standardverhalten zu ändern. Sie können Document Capture so einrichten, dass Gutschriften bei der Erkennung Vorrang vor Rechnungen haben. Gehen Sie dazu folgendermaßen vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Um die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**), und wählen Sie dann **Bearbeiten** in der Aktionsleiste.
3. Wählen Sie im Inforegister **Vorlagen** in der Liste der Vorlagen die Vorlage aus, die Sie bearbeiten möchten, und wählen Sie dann **Bearbeiten** aus, um die Vorlagenkarte zu öffnen.
4. Aktivieren Sie im Inforegister **Einkaufsbelege** die Option **Priorisiere Gutschrift als Belegart**.

Wenn diese Einstellung aktiviert ist, identifiziert Document Capture jeden importierten Beleg, der diese Vorlage verwendet und den Text _Gutschrift_ (oder ähnliches) enthält, als Gutschrift, auch wenn das Wort _Rechnung_ in diesem Beleg weiter oben über _Gutschrift_ steht.

## Weitere Informationen im Beleg identifizieren

**Um die Währung zu identifizieren**, sucht Document Capture zunächst nach einem Währungscode in der importierten Rechnung. Wenn im Beleg kein solcher Code vorhanden ist, wird geprüft, ob ein Code auf der Kreditorenkarte vorhanden ist. Falls auch hier kein Währungscode gefunden wird, verwendet Document Capture die lokale Währung, sofern diese in der **Finanzbuchhaltung Einrichtung** angegeben wurde.

**Um das Fälligkeitsdatum zu identifizieren**, sucht Document Capture zunächst in der importierten Rechnung danach. Wenn dies fehlschlägt, wird ein Fälligkeitsdatum basierend auf den Zahlungsbedingungen des Kreditors in Kombination mit dem Buchungsdatum erstellt, das normalerweise im Beleg enthalten ist.

**Um den Verkäufer/Einkäufer zu identifizieren**, prüft Document Capture das Feld **Einkäufer/Verkäufer** der importierten Rechnung. Wenn dies leer ist, wird nach einer Bestellnummer in der Rechnung gesucht und dann der Verkäufer-/Einkäufercode aus der zugehörigen Bestellung verwendet, sofern vorhanden.

**Um die Sachkontonummer und mögliche andere Kontocodes zu identifizieren**, prüft Document Capture, ob unter **Buchungseinrichtung** Regeln eingerichtet wurden. Mit dieser Einrichtung kann Document Capture möglicherweise Codes für Sachkonten, Artikel, Ressourcen, Anlagen, Artikelzuschläge, [Betragsverteilungscodes](@DC-118) und/oder [Einkaufsverträge](@DC-85) anwenden.

## Informationen zum Thema

[Währungen einrichten](https://learn.microsoft.com/de-de/dynamics365/business-central/finance-set-up-currencies) (Microsoft-Artikel)  
[Mit Papier- und PDF-Belegen arbeiten](@DC-71)  
[Felder in einem Beleg erfassen](@DC-110)  
[Einkäufercodeübersetzung](@DC-128)