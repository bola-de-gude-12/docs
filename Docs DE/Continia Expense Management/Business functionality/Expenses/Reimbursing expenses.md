---
title: Belege erstatten
date: 25-04-2025
description: Erfahren Sie, wie Sie Belege erstatten.
id: EM-14
lang: de
---

# Belege erstatten

Wenn Sie in Ihrem Unternehmen ein externes Lohn- und Gehaltsabrechnungssystem zur Erstattung von Belegen an Benutzer verwenden, empfiehlt es sich, im Gehaltsabrechnungssystem eine Ansicht zu erstellen, in der Sie sehen können, wie viel bei jedem Expense-Benutzer aussteht. Übertragen Sie die Daten dann in das Gehaltsabrechnungssystem und merken Sie an, welche Benutzer eine Erstattung erhalten haben.

Sie können die Erstattungsansichten nach Datumsintervallen filtern und sich die Gesamtsumme zum Beispiel als Betrag und Menge anzeigen lassen. Alle Belegarten werden als Spalten auf der Erstattungsseite angezeigt. Für jede Belegart werden die Gesamtausgaben angegeben. Der Betrag für die Belegarten (falls verwendet) wird auch für jeden einzelnen Expense-Benutzer angezeigt.

Wenn Ihr Unternehmen kein externes Lohn- und Gehaltsabrechnungssystem verwendet, sind diese Ansichten nicht relevant und der Beleg wird unmittelbar nach der Buchung als **Erstattet** gekennzeichnet.

Für jedes Dokument wird mit der Erstattungsmethode festgelegt, ob ein externes Abrechnungssystem verwendet wird oder nicht. Weitere Informationen finden Sie unter [Erstattungsmethoden einrichten](@EM-177).

In diesem Artikel wird Folgendes beschrieben:

- [Die Verwendung der Felder auf der Erstattungsseite für Belege](#die-felder-auf-der-erstattungsseite-fur-belege)
- [Die Rückerstattung von Belegen eines Benutzers](#belege-eines-benutzers-zuruckerstatten)

## Die Felder auf der Erstattungsseite für Belege

| **Feld**                      | **Beschreibung**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ----------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Datumsfilter**              | Bietet die Möglichkeit, Daten nach einem Datumsintervall zu filtern. Zum Beispiel, wenn Sie nur die erstattungsfähigen Beträge für den aktuellen Monat angezeigt bekommen möchten.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Anzeigen als**              | Zeigt die Gesamtsumme als Betrag oder Menge an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Angesehen von**             | Bietet verschiedene Filteroptionen basierend auf dem Status des Belegs: Warten auf Buchung, Bereit zur Rückerstattung, Gebucht und Rückerstattet, Alles                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Benutzer**                  | Die ID des Expense-Benutzers.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Name**                      | Der Name des Expense-Benutzers.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Saldo**                     | Der Saldo des aktuellen Benutzers. Dabei handelt es sich um die Summe aller Belege für den angegebenen Zeitraum, unabhängig von ihrem Status. Der Saldo zeigt die Beträge so an, wie sie eingereicht wurden. Er berechnet nicht, wie viel dem Benutzer zurückerstattet werden sollte. Beispielsweise erfolgt für Ausgaben in Höhe von 100 EUR, die mit einer Firmenkreditkarte bezahlt wurden, keine Rückerstattung an den Benutzer (da die Zahlung mit der Firmenkreditkarte erfolgte). In diesem Fall beträgt der **Saldo** 100. |
| **Erstattungsfähiger Betrag** | Der erstattungsfähige Saldo des aktuellen Benutzers. Dies ist der Betrag, der dem Expense-Benutzer erstattet werden soll. Beispielsweise erfolgt für Ausgaben in Höhe von 100 EUR, die mit einer Firmenkreditkarte bezahlt wurden, keine Rückerstattung an den Benutzer (da die Zahlung mit der Firmenkreditkarte erfolgte). In einem solchen Szenario beträgt der **erstattungsfähige Betrag** 0.                                                                                                                                                                 |
| **Belegarten**                | Der Gesamtbetrag oder die Gesamtzahl der damit verbundenen Ausgaben, die für einen bestimmten Benutzer erstattet werden können. Sie können spezifische Belegarten erstellen, die Ihren Unternehmensrichtlinien entsprechen. Beispielsweise können Belege für Hotels, Motels und Bed & Breakfasts alle nach der Ausgabenart **Unterkunft** gruppiert werden.                                                                                                                                                                                                                       |

## Belege eines Benutzers erstatten

Im folgenden Beispiel wird beschrieben, wie Ausgaben für einen Expense-Benutzer oder eine Expense-Benutzergruppe erstattet werden.

So erstatten Sie einem Benutzer die Ausgaben:

1. Suchen {{search}} Sie nach **Erstattung der Belege** und wählen Sie dann den zugehörigen Link.
2. Setzen Sie einen **Datumsfilter** für den Zeitraum, für den Sie die Übersicht haben möchten. Setzen Sie beispielsweise Filter für den vorherigen Monat.
3. Stellen Sie sicher, dass **Angesehen von** auf **Bereit zur Rückerstattung** eingestellt ist.
4. Stellen Sie sicher, dass **Anzeigen als** auf **Betrag** eingestellt ist.
5. Überprüfen Sie im Abschnitt **Erstattung der Belege**, ob Sie mit den angezeigten Beträgen einverstanden sind.
6. Jetzt möchten Sie die erstattungsfähigen Beträge möglicherweise manuell oder automatisch an ein externes Lohn- und Gehaltsabrechnungssystem übertragen:
   1. Sie können das externe System manuell eingeben.
   2. Sie können dies in der Aktionsleiste automatisieren, indem Sie **In Excel exportieren** auswählen. Die generierte Excel-Datei können Sie an die entsprechenden Empfänger versenden.
7. Wenn Sie im externen Gehaltsabrechnungssystem eine Bestätigung erhalten, dass dem Expense-Benutzer die Ausgaben für den Beleg erstattet wurden, markieren Sie die Ausgaben in der aktuellen Ansicht als **Erstattet**. Wählen Sie in der Aktionsleiste **Erstatten** aus. Dadurch wird eine versehentliche Erstattung beim nächsten Mal vermieden.

## Informationen zum Thema

Weitere Informationen zur Erstattung von Belegen und Ausgaben im Allgemeinen finden Sie unter:

[Überblick über Belege](@EM-8)  
[Pauschalen erstatten](@EM-16)  
[Fahrstrecken erstatten](@EM-15)

