---
title: Abrechnungen einrichten
date: 26-03-2025
description: Erfahren Sie, wie Sie Abrechnungen aktivieren, deaktivieren und entsprechend Ihrem Workflow einrichten.
lang: de
id: EM-306
---

# Abrechnungen einrichten

Erfahren Sie, wie Sie Abrechnungen in Microsoft Dynamics 365 Business Central aktivieren, deaktivieren und einrichten. Sie können dies auf der Seite Expense Management Einrichtung verwalten.

## Abrechnungen aktivieren oder deaktivieren

Sie müssen die Funktion für Abrechnungen aktivieren, wenn sie bei der Ersteinrichtung von Continia Expense Management nicht aktiviert wurde. Wenn Ihr Unternehmen hingegen keine Abrechnungen verwenden möchte, können Sie diese Funktion vollständig deaktivieren.

So aktivieren oder deaktivieren Sie Abrechnungen:

1. Suchen {{search}} Sie nach Expense Management Einrichtung und wählen Sie dann den zugehörigen Link.
2. Gehen Sie unter **Allgemein** in **Anwendungsbereiche** zu **Abrechnung**.
3. Wählen Sie Ihre bevorzugte Option:
   | Option          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
   | --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | **Deaktiviert** | Expense-Benutzer können keine Abrechnungen erstellen oder einreichen. Die Schaltfläche **Neue Abrechnung** ist in der Expense App nicht sichtbar und die Registerkarte **Abrechnung** ist im Expense Portal nicht sichtbar. In Business Central sind alle mit Abrechnungen verbundenen Einstellungen nicht verfügbar.                                                                                                        |
   | **Optional**    | Expense-Benutzer können Abrechnungen erstellen oder einreichen. Die Schaltfläche **Neue Abrechnung** wird in der Expense App angezeigt und die Registerkarte **Abrechnung** wird im Expense Portal zusammen mit den Schaltflächen und Registerkarten für normale Belege, Fahrstrecken und Pauschalen (sofern diese bereits aktiviert wurden) angezeigt.                                                                   |
   | **Notwendig**   | Expense-Benutzer können _nur_ Abrechnungen erstellen und einreichen, jedoch keine Belege, Fahrstrecken und Pauschalen. Die Schaltfläche **Neue Abrechnung** wird größer dargestellt, da nur diese Schaltfläche in der Expense App verfügbar ist, genauso wie die Registerkarte **Abrechnung**, die als einzige Registerkarte im Expense Portal verfügbar ist. Im Rollencenter ist nur der Stapel **Abrechnungen** verfügbar. |

Sie haben jetzt Abrechnungen entsprechend Ihren Anforderungen aktiviert oder deaktiviert.

## Abrechnungen konfigurieren

Nachdem Sie Abrechnungen aktiviert haben, können Sie einige der grundlegenden Einstellungen so konfigurieren, dass sie den Anforderungen Ihres Unternehmens entsprechen.

So konfigurieren Sie die Einstellungen für Abrechnungen:

1. Suchen {{search}} Sie nach Expense Management Einrichtung und wählen Sie dann den zugehörigen Link.
2. Bearbeiten Sie unter **Abrechnung** die Einstellungen nach Bedarf:
   - **Automatisch zur Genehmigung einreichen**: Wenn Sie diese Einstellung aktivieren, werden alle fehlerfreien Abrechnungen automatisch zur Genehmigung übermittelt.

   - **Datum und Uhrzeit der Ab- und Rückreise aktivieren**: Aktivieren Sie diese Einstellung, um die Felder **Abreise Datum/Zeit** und **Rückreise Datum/Zeit** für jede in der Expense-App und im Expense Portal erstellte Abrechnung anzuzeigen. Auf diese Weise können Expense-Benutzer Start- und Enddatum sowie -uhrzeit für alle Geschäftsreisen eingeben. Die beiden neuen Felder werden auch auf der Seite **Konfigurierte Felder** angezeigt. Sie heißen **ER-DEPARTURE DT** und **ER-RETURN DATETIME**. Um die Felder anzuzeigen oder zu bearbeiten, suchen Sie die Seite **Konfigurierte Felder** und öffnen Sie sie, und wählen Sie dann in der Aktionsleiste **Start** > **Abrechnung**.

     > [!TIP]
     > Um die Eingabe von Start- und Enddaten für Expense-Benutzer bei jeder Abrechnung _obligatorisch_ zu machen, gehen Sie zu den einzelnen Feldern in der Liste und aktivieren Sie die entsprechenden Kontrollkästchen in der Spalte **Notwendig**.

   - **Abrechnung Vorabgenehmigung**: Verwenden Sie diese Option, um festzulegen, ob und wie Ihre Abrechnungen vorab genehmigt werden sollen. Wählen Sie Ihre bevorzugte Option:

     | Option          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
     | --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
     | **Deaktiviert** | Für die Einreichung von Abrechnungen ist für Expense-Benutzer keine Vorabgenehmigung erforderlich.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
     | **Optional**    | Jedem Expense-Benutzer, der in der Expense App oder im Expense Portal eine Abrechnung erstellt, wird ein Dialogfeld mit der Frage angezeigt, ob für die Abrechnung eine Vorabgenehmigung erforderlich ist. Das Feld **Betrag der Vorabgenehmigung (MW)** wird in der App und im Portal angezeigt. Wenn derExpense-Benutzer im Dialogfeld **Nein** auswählt, ist für die Einreichung der Abrechnung keine Vorabgenehmigung erforderlich. Wenn der Benutzer **Ja** auswählt, muss er einen Vorabgenehmigungsbetrag eingeben und die Abrechnung zur Vorabgenehmigung einreichen, bevor weitere Änderungen vorgenommen werden können (nach Abschluss des Vorabgenehmigungsprozesses). |
     | **Notwendig**   | Expense-Benutzer müssen für jede Abrechnung einen vorab genehmigten Betrag eingeben. Wenn sie in der Expense App oder im Expense Portal eine Abrechnung erstellen, wird das Feld **Betrag der Vorabgenehmigung (MW)** als Pflichtfeld angezeigt, das Sie ausfüllen müssen, um die Abrechnung zur Vorabgenehmigung einzureichen. Bis zur vorläufigen Genehmigung der Abrechnung sind keine weiteren Änderungen mehr möglich.                                                                                                                                                                                                                                                                                          |

Sie haben jetzt Abrechnungen konfiguriert.

## Posten nach Abrechnung oder Belegart gruppieren

In manchen Situationen bietet es sich an, Posten zu gruppieren, anstatt sie einzeln einzureichen (beispielsweise, wenn es viele Posten für dieselbe Abrechnung gibt). Mit der Buchungsgruppierungsmethode können Sie Posten nach Abrechnung oder Dokumenttyp gruppieren.

Die Buchungsgruppierungsmethode bietet zwei Möglichkeiten zum Gruppieren von Posten:

- Einzeleintrag pro Abrechnung – erstellt einen einzelnen Posten für die Abrechnung
- Separate Einträge pro Belegart – gruppiert Posten nach Belegen, Fahrstrecken oder Pauschalen

So gruppieren Sie Posten:

1. Suchen {{search}} Sie nach **Expense Management Einrichtung** und wählen Sie dann den zugehörigen Link.
2. Navigieren Sie unter **Abrechnung** zum Feld **Buchungsgruppierungsmethode**.
3. Wählen Sie im Dropdown-Menü entweder **Einzeleintrag pro Belegart** oder **Separate Einträge pro Belegart**.

### Gruppierungsausnahmen

Derzeit können Posten nicht nach den folgenden Methoden gruppiert werden.

- Sachkonto (beispielsweise nach unterschiedliche Zahlungsarten)
- Verschiedenen Währungen
- Verschiedenen Dimensionen
- Kreditorennr.

## Zusätzliche Feldcodes hinzufügen

Möglicherweise ist es für Sie hilfreich, einer Abrechnung zusätzliche konfigurierte Felder hinzuzufügen, beispielsweise eine Projektnummer oder eine Aufgabennummer. Wenn Sie den Dokumenttypen Belege, Pauschalen und Fahrstrecken dasselbe konfigurierte Feld hinzugefügt haben, wird der Feldwert in der Abrechnung für alle Dokumente übernommen, die der Abrechnung hinzugefügt werden.

## Informationen zum Thema

Weitere Informationen zu Abrechnungen finden Sie unter:

[Vorabgenehmigung von Abrechnungen einrichten](@EM-272)

[Abrechnungen einreichen und verwalten](@EM-294)

[Mehrere Kommentare in Abrechnungen anzeigen](@EM-301)

[Überblick über Abrechnungen](@EM-44)