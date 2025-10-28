---
title: Erinnerungscodes einrichten
date: 21-03-2025
description:
lang: de
---

# Erinnerungscodes einrichten

Sie können Continia Expense Management ganz einfach so konfigurieren, dass jedem Expense-Benutzer, der eine Aufgabe für ein Dokument ausführen muss, Erinnerungen gesendet werden. Dies könnte beispielsweise eine Kreditkartentransaktion sein, die abgeschlossen werden muss, oder ein Beleg, der von einem Genehmiger abgelehnt wurde und daher vom Expense-Benutzer bearbeitet werden muss.

> [!NOTE]
> Diese Funktion ist nur für Expense-Benutzer, _nicht_ für Genehmiger. Sie wird sehr häufig – aber nicht ausschließlich – im Zusammenhang mit Belegen verwendet, die automatisch aus Firmenkreditkartentransaktionen erstellt werden und von den entsprechenden Expense-Benutzern abgeschlossen werden müssen.

Das Senden von Erinnerungs-E-Mails wird von der Codeunit **6086314 CEM Reminder Email** ausgeführt. Weitere Informationen finden Sie unter [Aufgabenwarteschlangen einrichten](@EM-65).

Um Beleg-Erinnerungscodes einzurichten, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Continia Benutzereinrichtung** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Benutzerliste in der Spalte **Continia Benutzer-ID** den Benutzer aus, für den Sie Erinnerungscodes einrichten möchten. Die **Continia Benutzereinrichtung Karte** wird geöffnet.
3. Gehen Sie auf dem Inforegister **Expense Management** zu **Spesen Erinnerung** und wählen Sie die drei Punkte auf der rechten Seite des Feldes aus, um die Seite **Erinnerungscodes** zu öffnen.
4. Sie haben die folgenden Optionen:
   - Wählen Sie in der Liste der Codes einen der vorhandenen Codes aus (wählen Sie die Codezeile aus, nicht den Code selbst).
   - Einen neuen Code erstellen: Wählen Sie in der Aktionsleiste **Neu** aus, geben Sie einen Namen für den neuen Code ein und wählen Sie dann **OK** oder verlassen Sie das Feld. Geben Sie in der Spalte **Maximal Anzahl von Erinnerungen** die maximale Anzahl Erinnerungen an, die für diesen Code versendet werden sollen.
5. Wählen Sie in der Aktionsleiste die drei Punkte und dann **Mahnstufen** aus, um die Seite **Erinnerungsstufen** zu öffnen.
6. Geben Sie in der Spalte **Nr.** die Stufe der Erinnerung an, indem Sie eine Ganzzahl eingeben. Da die Spalte **Nr.** die Reihenfolge bestimmt, in der Erinnerungs-E-Mails versendet werden, ist die erste Stufe normalerweise mit **1** gekennzeichnet, und alle nachfolgenden Stufen werden mit fortlaufenden Nummern (**2**, **3** usw.) gekennzeichnet.
7. Geben Sie in der Spalte **Karenzzeit** die Zeit ein, die vergehen soll, bevor eine Erinnerungs-E-Mail dieser Stufe versendet wird.
   > [!TIP]> Ihre Eingabe muss eine [Datumsformel](https://learn.microsoft.com/en-us/dynamics365/business-central/ui-enter-date-ranges#use-date-formulas) sein. Informationen zum Startdatum der jeweiligen Erinnerungsfrist finden Sie unter [Erinnerungsfristen festlegen](#erinnerungsfristen-festlegen) weiter unten.
8. Geben Sie in der Spalte **Erinnerungstext** einen Text ein, der intern zur Identifizierung der Stufe verwendet werden kann.
9. Wiederholen Sie die Schritte 6–8 für alle weiteren Erinnerungsstufen, die Sie hinzufügen möchten, und schließen Sie dann die Seite, um zur Seite **Erinnerungscodes** zurückzukehren.
10. Stellen Sie sicher, dass der von Ihnen erstellte oder angepasste Code in der Liste ausgewählt ist, und wählen Sie dann **OK** aus, um die Seite zu schließen.

Der ausgewählte Erinnerungscode wird nun dem Feld **Spesen Erinnerung** auf der **Continia Benutzereinrichtung Karte** hinzugefügt, und der Benutzer, den Sie in Schritt 2 der Anleitung ausgewählt haben, erhält Erinnerungs-E-Mails gemäß Ihrer Einrichtung.

## Erinnerungsfristen festlegen

In der Tabelle auf der Seite **Erinnerungsstufen** gibt die Datumsformel, die Sie in der Spalte **Karenzzeit** für eine bestimmte Stufe festlegen, an, wann eine Erinnerungs-E-Mail dieser Stufe versendet wird. Für die erste Stufe wird dies aus einem Startdatum berechnet, das auf einem der folgenden Felder basiert:

- **Erstelldatum**
- **Belegdatum**/**Registrierungsdatum**/**Abreisedatum** (für Belege, Pauschalen und Fahrstrecken)

Wenn eines dieser Felder leer ist, wird das andere verwendet. Wenn beide Felder einen Datumswert haben, wird das frühere Datum verwendet. Wenn beide Felder leer sind, wird jeweils das aktuelle Datum verwendet.

Die obigen Informationen gelten nur für die erste Stufe in der Tabelle. Für die nachfolgenden Stufen wird die Zeitspanne, nach der eine Erinnerungs-E-Mail versendet wird, ab dem Zeitpunkt berechnet, an dem die vorherige Erinnerung versendet wurde.