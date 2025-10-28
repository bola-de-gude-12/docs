---
title: Zu-/Abschläge für Artikel automatisch zuweisen
date: 30-04-2023
description: So weisen Sie den Zeilen eingehender Belege Artikelzu-/abschläge  anhand vordefinierter Methoden automatisch zu
id: DC-137
lang: de
---

# Zu-/Abschläge für Artikel automatisch zuweisen

Continia Document Capture kann den Zeilen eines eingehenden Belegs automatisch Zu- bzw. Abschläge gemäß einer Methode zuweisen, die in der entsprechenden Belegvorlage definiert wird. Auf diese Weise können Artikelzuschläge bzw. -abschläge in einem importierten Beleg auf die Zeilen dieses Belegs aufgeteilt werden, je nachdem, wie Sie dies in der Vorlage eingerichtet haben. Zu-/Abschläge können folgendermaßen zugewiesen werden:

- **Zu gleichen Teilen**
- **Nach Betrag**
- **Nach Gewichtung**
- **Nach Volumen**

Im Folgenden werden diese Methoden genauer erläutert und auch die allgemeine Funktionsweise wird näher beschrieben. Die tatsächlichen Kosten werden bei der Registrierung der Belege automatisch zugeordnet.

> [!NOTE]
> Der Abgleich mit Zu-/Abschlägen wird nur unterstützt, wenn Sie den Abgleich mit Wareneingangs-/Rücklieferungszeilen durchführen.

## So richten Sie die Zuweisung von Zu-/Abschlägen ein

Um Zu-/Abschläge automatisch auf die Zeilen eingehender Belege aufzuteilen, gehen Sie folgendermaßen vor:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Um die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**), und wählen Sie dann **Bearbeiten** in der Aktionsleiste.
3. Wählen Sie auf der Seite **Belegkategorie** im Inforegister **Vorlagen** die Vorlage aus, die Sie konfigurieren möchten.
4. Wählen Sie in der Titelleiste des Inforegisters **Bearbeiten** aus, um die Vorlagenkarte zu öffnen.
5. Gehen Sie im Inforegister **Einkaufsbelege** zu **Artikel Zu-/Abschl.-Zuweisungsmethode** und wählen Sie dann die Methode aus, die Document Capture zum Zuweisen von Zu-/Abschlägen verwenden soll. Weitere Informationen zu den Zuweisungsmethoden finden Sie unter [Grundlegendes zu den Methoden](#grundlegendes-zu-den-methoden) weiter unten.

Ihre ausgewählte Methode wird anschließend für jede Zuweisung von Zu-/Aschlägen in Belegen mit dieser Vorlage verwendet, sobald Sie die Belege registrieren. In den folgenden Abschnitten wird erläutert, wie die [Zu-/Abschläge bei der Zuweisung auf die Zeilen in jedem Beleg verteilt werden](#grundlegendes-zu-den-methoden) und wie Sie [diese Verteilung anzeigen](#so-zeigen-sie-zugewiesene-zu-abschlage-an) können.

## So zeigen Sie zugewiesene Zu-/Abschläge an

Sobald Sie einen Beleg mit einem Artikelzuschlag registriert haben, wird der Artikelzuschlag automatisch (entsprechend Ihren Einstellungen in der Einrichtung) den Zeilen des Belegs zugeordnet. Anschließend wird die Belegseite (zum Beispiel die Seite **Einkaufsrechnung** für Rechnungen) geöffnet. Um die Zuweisung der Zu-/Abschläge anzuzeigen und zu überprüfen, ob diese korrekt sind, gehen Sie folgendermaßen vor:

1. Wählen Sie im Inforegister **Zeilen** in der Liste der Belegzeilen unter **Art** die Zeile mit der Bezeichnung **Zu-/Abschlag (Artikel)** aus.
2. Wählen Sie in der Titelleiste des Inforegisters **Zeile** > **Verwandte Informationen** > **Artikel Zu-/Abschlagszuweisung** aus.
3. Dadurch wird die Seite **Artikel Zu-/Abschl.-Zuw. (EK)** geöffnet. Überprüfen Sie in der Spalte **Betrag für Zuweisung**, ob der Zu-/Abschlag wie vorgesehen auf die Zeilen verteilt wurde.

## Grundlegendes zu den Methoden

Zur Erklärung der verschiedenen Methoden zur Zuweisung von Zu-/Abschlägen für Artikel finden Sie im Folgenden ein Beispiel eines eingehenden Belegs mit einem Zuschlag:

- Drei Artikelzeilen
- Gesamtbetrag ohne MwSt.: 1,000.00 €
- Gesamtgewicht aller Positionen: 100,00 kg
- Gesamtvolumen aller Positionen: 10,00 m<sup>3</sup>
- Eine Zuschlagszeile mit einer Menge von 1 und einem Betrag von 200,00 €

Bei Registrierung dieses Belegs erfolgt die Verteilung des Zuschlags auf die Artikelzeilen des Belegs in den verschiedenen Szenarien folgendermaßen:

> [!NOTE]
> Die Verteilung ist gleich, auch wenn sich der Zuschlag auf Kopfebene anstatt auf Zeilenebene befinden würde. Zu-/Abschläge werden den Belegzeilen gleichermaßen zugewiesen, unabhängig davon, ob sie sich auf Zeilenebene oder Kopfebene befinden.

### Zuweisung zu gleichen Teilen

Wenn Sie als Zuweisungsmethode für Zu-/Abschläge in [der Einrichtung](#so-richten-sie-die-zuweisung-von-zu-abschlagen-ein) **Zu gleichen Teilen** auswählen, erfolgt die Zuweisung folgendermaßen:

<br>

| Nr. |  Menge für Zuweisung | Betrag für Zuweisung |
| ------------------- | :------------------: | :------------------: |
| Artikel 1           | 0.33 |        66,67 €       |
| Artikel 2           | 0.33 |        66,67 €       |
| Artikel 3           | 0.33 |        66,67 €       |

Die Zuschlagszeile hat einen Betrag von 200,00 € und eine Menge von 1, und beides wird durch drei geteilt, da drei Artikelzeilen vorhanden sind. Durch diese gleichmäßige Verteilung wird den einzelnen Artikelpositionen ein Zuschlag von jeweils 66,67 € zugeordnet.

### Zuweisung nach Betrag

Wenn Sie als Zuweisungsmethode für Zu-/Abschläge in [der Einrichtung](#so-richten-sie-die-zuweisung-von-zu-abschlagen-ein) **Nach Betrag** auswählen, erfolgt die Zuweisung folgendermaßen:

<br>

| Nr. | Zeilenbetrag ohne MwSt. | Menge für Zuweisung | Betrag für Zuweisung |
| ------------------- | :-------------------------------------: | :-----------------: | :------------------: |
| Artikel 1           |                 500,00 €                |         0,50        |       100,00 €       |
| Artikel 2           |                 200,00 €                |         0,20        |        40,00 €       |
| Artikel 3           |                 300,00 €                |         0,30        |        60,00 €       |

Der zugewiesene Betrag für jede Position wird basierend auf dem Volumen des Artikels und seinem Verhältnis zum Gesamtvolumen aller Positionen berechnet. Beispielsweise hat Artikel 1 einen Zeilenbetrag von 500,00 €, was genau der Hälfte des Gesamtbetrags von 1,000.00 € entspricht. Die Zuschlagszeile hat einen Betrag von 200,00 € und eine Menge von 1. Da von 1 die Hälfte 0,50 ist, beträgt der zuzuweisende Betrag 0,50 × 200,00 € = 100,00 €.

### Zuweisung nach Gewicht

Wenn Sie als Zuweisungsmethode für Zu-/Abschläge in [der Einrichtung](#so-richten-sie-die-zuweisung-von-zu-abschlagen-ein) **Nach Gewicht** auswählen, erfolgt die Zuweisung folgendermaßen:

<br>

| Nr. | Bruttogewicht | Menge akt. Lieferung (Basis) | Menge für Zuweisung | Betrag für Zuweisung |
| ------------------- | :-----------: | :-------------------------------------------------------------: | :-----------------: | :------------------: |
| Artikel 1           |      2,00     |                                5                                |         0,10        |        20,00 €       |
| Artikel 2           |     10,00     |                                4                                |         0,40        |        80,00 €       |
| Artikel 3           |      5,00     |                                10                               |         0,50        |       100,00 €       |

Der zugewiesene Betrag für jede Position wird basierend auf dem Volumen des Artikels und seinem Verhältnis zum Gesamtvolumen aller Positionen berechnet. Beispiel: Artikel 1 hat ein Gesamtgewicht von 2,00 kg × 5 = 10,00 kg (das Bruttogewicht jeder Artikeleinheit multipliziert mit der Anzahl der Einheiten, die in **Menge akt. Lieferung** angegeben ist), was genau einem Zehntel des Gesamtgewichts aller Positionen (100,00 kg) entspricht. Die Zuschlagszeile hat einen Betrag von 200,00 € und eine Menge von 1. Da von 1 ein Zehntel 0,10 ist, beträgt der zuzuweisende Betrag 0,10 × 200,00 € = 20,00 €.

### Zuweisung nach Volumen

Wenn Sie als Zuweisungsmethode für Zu-/Abschläge in [der Einrichtung](#so-richten-sie-die-zuweisung-von-zu-abschlagen-ein) **Nach Volumen** auswählen, erfolgt die Zuweisung folgendermaßen:

<br>

| Nr. | Volumen | Menge akt. Lieferung (Basis) | Menge für Zuweisung | Betrag für Zuweisung |
| ------------------- | :-----: | :-------------------------------------------------------------: | :-----------------: | :------------------: |
| Artikel 1           |   1,00  |                                5                                |         5,00        |       100,00 €       |
| Artikel 2           |   0,25  |                                4                                |         1,00        |        20,00 €       |
| Artikel 3           |   0,50  |                                8                                |         4,00        |        80,00 €       |

Der zugewiesene Betrag für jede Position wird basierend auf dem Anteil berechnet, den der Positionsbetrag am Gesamtbetrag hat. Beispielsweise hat Artikel 1 ein Gesamtvolumen von 1,00 m<sup>3</sup> × 5 = 5,00 m<sup>3</sup> (das Volumen jeder Artikeleinheit multipliziert mit der Anzahl der Einheiten, die in **Menge akt. Lieferung** angegeben ist), was genau der Hälfte des Gesamtvolumens aller Positionen entspricht (10,00 m<sup>3</sup>). Die Zuschlagszeile hat einen Betrag von 200,00 € und eine Menge von 1. Da von 1 die Hälfte 0,50 ist, beträgt der zuzuweisende Betrag 0,50 × 200,00 € = 100,00 €.

## Informationen zum Thema

[Automatischer Belegabgleich](@DC-70)