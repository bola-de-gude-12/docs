---
title: Belegdaten mit der KI-Belegerkennung erfassen
date: 20-03-2025
description: Belegdaten mit der KI-Belegerkennung erfassen
lang: de
---

# Belegdaten mit der KI-Belegerkennung erfassen

Die KI-Belegerkennung ist eine erweiterte Funktion, die Daten aus gescannten Anhängen wie Quittungen und Rechnungen erkennt und erfasst, wodurch die manuelle Eingabe erheblich reduziert wird. Machen Sie ein Foto von Ihrem Beleg oder senden Sie eine PDF-Rechnung aus anderen Apps oder Geräten. Anschließend übernimmt die KI-Belegerkennung die automatische Identifizierung und Extraktion relevanter Daten. Durch die direkte Erfassung von Daten aus gescannten Belegen und PDF-Anhängen mithilfe modernster optischer Zeichenerkennung (OCR) spart Ihnen die KI-Belegerkennung viel Zeit, minimiert Fehler und rationalisiert den Spesenabrechnungsprozess im Allgemeinen.

Unabhängig davon, ob Sie sie für die eigentlichen Anhänge oder digitale PDFs verwenden, sorgt die KI-Belegerkennung dafür, dass die Spesenabrechnung schnell, genau und problemlos erfolgt. Sie ist für die Verwendung mit Belegen aus allen Ländern konzipiert, unabhängig von der Herkunft, und funktioniert sowohl mit der [Continia Expense App](#to-capture-data-using-the-expense-app) als auch mit dem [Continia Expense Portal](#to-capture-data-using-the-expense-portal).

## Welche Daten werden erfasst?

Für jeden Beleg identifiziert und füllt die KI-Belegerkennung automatisch Daten für die folgenden Felder aus:

- **Betrag**
- **Währung**
- **Belegdatum**
- **Zahlungsart**
- **Beschreibung** (Händler)
- **MwSt.-Betrag** (wenn dieses Feld auf der Seite **Konfigurierte Felder** hinzugefügt wurde, finden Sie weitere Informationen unter [Abrechnungen einrichten](@EM-80) in Continia Expense Management).
- Verschiedene ESG-Felder, abhängig vom Wert des Felds **Belegart**:
   - **Strom (kWh)**
   - **Teilnehmer**
   - **Kraftstoffmenge**
   - **Anzahl der Nächte**
   - **Zurückgelegte Entfernung**
   - **Abflugflughafen**
   - **Zielflughafen**
   - **Rückfahrt**
   - **Abfahrtshafen**
   - **Zielhafen**
   - **Vom Bahnhof**
   - **Zum Bahnhof**
   > [!NOTE]
   > Die ESG-Felder sind in den Benutzeroberflächen der Expense App und im Expense Portal nur sichtbar, wenn im Feld **Belegart** bestimmte Werte ausgewählt wurden, wie z. B. **ELECTRICY**, **FUEL-PETROL** oder **TRAVEL-FLIGHT**.

## Automatische Aufteilung der differenzierten Mehrwertsteuer

Wenn Sie möchten, dass die KI-Belegerkennung die Mehrwertsteuerdaten in Ihren gescannten Anhängen automatisch erfasst, müssen Sie das Feld **MwSt.-Betrag** auf der Seite **Konfigurierte Felder** in Continia Expense Management hinzufügen. Informationen zum Hinzufügen dieses Felds finden Sie unter [Felder einrichten](@EM-80).

Nachdem Sie das Feld **MwSt.-Betrag** hinzugefügt haben, identifiziert die KI-Belegerkennung alle relevanten Mehrwertsteuerdaten in den gescannten Anhängen und füllt das Feld automatisch aus. Wenn auf einen Anhang außerdem zwei oder mehr verschiedene Mehrwertsteuerarten ausgewiesen wurden, teilt die KI-Belegerkennung die Mehrwertsteuer automatisch mithilfe des Felds **Verteilungen** auf. Beispielsweise würde ein Anhang mit einem Gesamtwert von 34,90 $ folgendermaßen aufgeteilt:

| MwSt. % | MwSt. | Preis ohne MwSt. | Gesamtbetrag |
| ----------------------- | --------------------- | -------------------------------- | ------------ |
| 12,00 %                 | 2,40                  | 20,00                            | 22,40        |
| 25,00 %                 | 2,50                  | 10,00                            | 12,50        |
|                         | 4,90                  | 30,00                            | 34,90        |

Wenn dieser Anhang einer Ausgabe in der Expense App hinzugefügt wird, wird im Feld **Verteilung** der Text **Verteilungszeilen: 2** angezeigt, um zu signalisieren, dass die Summe in zwei Zeilen aufgeteilt ist. Wenn Sie dann das Feld **Verteilung** auswählen, um die Seite **Verteilungen** zu öffnen, wird oben der Gesamtbetrag von 34,90 $ angezeigt, gefolgt von den beiden Verteilungszeilen von 22,40 $ (12,00 %) bzw. 12,50 $ (25,00 %).

## So erfassen Sie Daten mit der Expense App

Mit der KI-Belegerkennung können Sie Belegdaten mithilfe der Expense App erfassen, indem Sie in der App ein Foto Ihrer Belege machen. Gehen Sie dazu folgendermaßen vor:

1. Öffnen Sie die Expense App und wählen Sie **Neuer Beleg**.
2. Wählen Sie in der Symbolreihe oben das Kamerasymbol aus, um auf die Kamera Ihres Telefons zuzugreifen.
3. Machen Sie ein Foto des Belegs und wählen Sie **Foto verwenden**. Anschließend wird das Foto im Beleg beigefügt, und die Belegdaten werden automatisch erfasst und in die entsprechenden Felder des Belegs eingetragen.
4. Wählen Sie **Belegart** aus, um die Liste der Belegarten zu öffnen, und wählen Sie dann die entsprechende aus.
5. Wischen Sie über die Schaltfläche **Übertragen**, um den Beleg zu übermitteln.

Der Beleg wird anschließend zur Genehmigung eingereicht.

## So erfassen Sie Daten mit dem Expense Portal

Es ist im Expense Portal nicht möglich, Ihre Belege abzufotografieren. Darüberhinaus funktioniert die Erfassung der Belegdaten im Portal aber genauso reibungslos wie in der App. Um Daten im Expense Portal mithilfe der KI-Belegerkennung zu erfassen, gehen Sie folgendermaßen vor:

1. Wählen Sie oben im blauen Band **Belege** aus.
2. Wählen Sie in der oberen linken Ecke **Neu** aus, um einen Beleg zu erstellen.
3. Sie haben die folgenden Optionen:
   - Suchen Sie den entsprechenden Beleg in Ihrem Dateibrowser und ziehen Sie ihn in das Drag-and-Drop-Feld auf der rechten Seite.
   - Wählen Sie in der Aktionsleiste **Anhänge** aus, um die Liste der hochgeladenen Anhänge zu öffnen. Suchen Sie in der Liste nach dem Beleg, den Sie der Ausgabe hinzufügen möchten, und wählen Sie dann **Hinzufügen** aus, um den Beleg hinzuzufügen.
4. Die Belegdaten werden automatisch erfasst und in die entsprechenden Felder des Belegs eingetragen. Füllen Sie die restlichen Angaben manuell aus.
5. Wählen Sie in der Aktionsleiste **Einreichen** aus, um den Beleg einzureichen.

Der Beleg wird anschließend zur Genehmigung eingereicht.