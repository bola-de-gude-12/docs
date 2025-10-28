---
title: Expense Management: Einkaufsverträge erstellen
date: 18-02-2025
description: null
id: EM-131
lang: de
---

# Einkaufsverträge erstellen

Ähnlich wie Continia Expense Management und die meisten anderen Lösungen und Module von Continia lässt sich das Einkaufsverträge-Modul direkt in Microsoft Dynamics 365 Business Central integrieren. Sie können darauf über das Symbol {{search}} zugreifen, wenn Sie Einkaufsverträge erstellen möchten.

Sie können Einkaufsverträge folgendermaßen erstellen:

- [Von Grund auf](#einen-neuen-einkaufsvertrag-erstellen), von der Seite **Einkaufsverträge** aus
- [Basierend auf einem Beleg](#einen-einkaufsvertrag-auf-der-grundlage-eines-belegs-erstellen)

Welche Methode Sie verwenden, hängt von Ihren Anforderungen und der Seite ab, von der aus Sie navigieren. Beide Methoden werden weiter unten ausführlich beschrieben.

## Einen neuen Einkaufsvertrag erstellen

Sie können einen ganz neuen Einkaufsvertrag ohne einen vorhandenen Beleg erstellen.

So erstellen Sie einen neuen Einkaufsvertrag:

1. Suchen {{search}} Sie nach **Einkaufsverträge**, und wählen Sie dann den zugehörigen Link, um die Seite **Einkaufsverträge** zu öffnen.
   > [!NOTE]
   > Sie können diese Seite auch vom Business Central-Rollencenter aus öffnen: Unter **Continia Expense Management Aktivitäten** > **Einkaufsverträge** > **Alle**.
1. Wählen Sie in der Aktionsleiste **Neu**, um die Seite für Einkaufsverträge zu öffnen.
1. Füllen Sie die Felder unter **Allgemein** nach Bedarf aus. In der folgenden Tabelle werden die verschiedenen Felder erläutert.

   | Feld | Beschreibung   |
   | --- | --- |
   | **Einkäufercode (Prüfer)**                  | Geben Sie in diesem Feld den Code der Person ein, die den neuen Vertrag überprüfen soll, ein oder wählen Sie sie aus.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
    | **Preistyp**                                                   | Geben Sie an, ob die Beträge der Vertragszeilen _genau_ mit den Beträgen der zugehörigen Belege übereinstimmen müssen, damit die Belege automatisch genehmigt werden (**Fester Betrag**), oder ob eine gewisse Betragsabweichung akzeptabel ist (**Variabler Betrag**). <br> Wenn Sie **Variabler Betrag** auswählen, ermittelt Expense Management anhand der unter **Max. erlaubte Zeilenabweichung %** eingegebenen Werte für die entsprechenden Zeilen (unter **Zeilen**), ob die zugehörigen Belegbeträge innerhalb der zulässigen Abweichung liegen. Wenn Sie **Fester Betrag** auswählen, ignoriert Expense Management alle unter **Max. erlaubte Zeilenabweichung %** eingegebenen Werte.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
    | **Abrechnungszeit-Code**                                       | Geben Sie an, wie oft Sie Belege für diesen Vertrag von den Mitarbeitern erwarten. Mit dieser Angabe wird der **Jährliche Betrag** für jede Zeile im Inforegister **Zeilen** zusammen mit den Feldern **Menge** und **Einstandspreis** berechnet. <div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Hinweis</span></p><p>Sie können Ihre eigenen Codes für Abrechnungszeiträume erstellen, indem Sie das Dropdown-Menü des Felds öffnen und **+ Neu** auswählen. Als nächstes füllen Sie die Felder nach Bedarf aus. Unter **Periodendatumsformel** müssen Sie eine Ganzzahl eingeben, gefolgt von <b>T</b> (Tage), <b>WT</b> (Wochentage), <b>W</b> (Wochen), <b>M</b> (Monate), <b>Q</b> (Quartale) oder <b>Y</b> (Jahre) – zum Beispiel <b>2W</b> (zwei Wochen). <br>Sie können auch angeben, wie oft der Vertrag überprüft werden muss, indem Sie das Feld <b>Überprüfen</b> bearbeiten. Wenn Sie hier <b>Datumsformel</b> auswählen, geben Sie die Formel unter <b>Überprüfen der Datumsformel</b> anhand der oben genannten Richtlinien ein. Basierend auf Ihrer Eingabe in diesen beiden Feldern werden die entsprechenden Felder unter <b>Überprüfen</b> automatisch ausgefüllt (siehe Schritt 4 unten).</p></div> |
    | **Autom. bestätigen innerhalb der Abweichung** | Wählen Sie **Ja** aus, wenn Expense Management Belege automatisch genehmigen soll. Der Belegbetrag muss dann mit dem entsprechenden Betrag der Vertragszeile innerhalb der Abweichung übereinstimmen, die unter **Max. erlaubte Zeilenabweichung %** unter **Zeilen** definiert ist. <br><br> Je nachdem, ob Sie **Ja** oder **Nein** auswählen, gelten folgende Regeln: <ul><li><b>Ja</b>: Wenn Sie unter <b>Preistyp</b> > <b>Fester Betrag</b> ausgewählt und/oder unter <b>Max. erlaubte Zeilenabweichung %</b> keinen Wert eingegeben haben, muss der Belegbetrag genau mit dem Betrag der Vertragszeile übereinstimmen, damit der Beleg automatisch genehmigt wird.</li><li><b>Nein</b>: Wenn Sie unter <b>Preistyp</b> > <b>Variabler Betrag</b> ausgewählt und/oder einen Wert unter <b>Max. erlaubte Zeilenabweichung %</b> eingegeben haben, werden diese Einstellungen ignoriert.</li></ul> |
1. Füllen Sie die Felder unter **Allgemein** nach Bedarf aus. In der folgenden Tabelle werden die verschiedenen Felder erläutert.

   | Feld | Beschreibung   |
   | --- | --- |
   | **Genehmigung**                | Geben Sie an, wie oft der Einkaufsvertrag überprüft werden muss. Die Standardoption ist jährlich. Sie können dies jedoch im Dropdown-Menü **Genehmigung** ändern. Alle Änderungen, die Sie an den Feldern **Genehmigung** und **Datumsformel Genehmigung** unter **Abrechnungszeit-Code** vornehmen, werden in dieses Feld automatisch eingetragen. <div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Hinweis</span></p><p>Wenn Sie <b>Datumsformel</b> auswählen, wird das Feld <b>Datumsformel Genehmigung</b> angezeigt. Geben Sie eine Formel ein. Geben Sie dafür eine Ganzzahl ein, gefolgt von<b>T</b> (Tage), <b>WT</b> (Wochentage), <b>W</b> (Wochen), <b>M</b> (Monate), <b>Q</b> (Vierteljahr) oder <b>J</b> (Jahre) zum Beispiel, <b>2W</b> (zwei Wochen). Für komplexere Formeln können Sie auch + und – verwenden oder den Buchstaben **L** (laufend) als Präfix für eine der zuvor genannten Zeiteinheiten eingeben, zum Beispiel **LM+10T** (der laufende Monat plus zehn Tage).</p></div> |
    | **Nächstes Genehmigungsdatum** | Geben Sie an, wann der Vertrag das nächste Mal überprüft werden soll. Der Standardwert hängt davon ab, was Sie unter **Genehmigung** ausgewählt haben. Wenn Sie beispielsweise **Jährlich** ausgewählt haben, ist der Standardwert das Startdatum des Vertrags plus ein Jahr minus einen Monat.  |
1. Erstellen Sie unter **Zeilen** eine Zeile für jeden Mitarbeiter, für den Sie Belege erwarten, indem Sie alle Felder nach Bedarf ausfüllen. In der folgenden Tabelle werden die verschiedenen Felder erläutert.

   | Feld | Beschreibung   |
   | --- | --- |
   | **Expense-Benutzer**                                 | Wählen Sie den Expense-Benutzer aus, der dieser Zeile zugeordnet werden soll.                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
   | **Einstandspreis**                                   | Die Felder **Betrag ohne MwSt.** und **Jährlicher Betrag** (die beide nicht bearbeitet werden können) werden automatisch anhand der Informationen ausgefüllt, die Sie im Feld **Einstandspreis** eingeben. Außerdem werden die beiden Felder automatisch ausgefüllt, wenn Sie das Feld **Menge** bearbeiten. <br />Der Wert des Felds **Jährlicher Betrag** basiert auf Ihrer Auswahl im Feld **Abrechnungszeit-Code** unter **Allgemein**.                                 |
   | **Max. erlaubte Zeilenabweichung %** | Der Ausgabenbetrag wird automatisch genehmigt, wenn er mit dem Vertragszeilenbetrag innerhalb der prozentualen Abweichung übereinstimmt, die Sie in diesem Feld eingeben. <br> <div class="alarm alarm-important"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Wichtig</span></p><p>Dies gilt nur, wenn unter <b>Allgemein</b> die Einstellungen <b>Preistyp</b> auf <b>Variabler Betrag</b> und <b>Autom. bestätigen innerhalb der Abweichung</b> auf <b>Ja</b> festgelegt sind.</p></div> |

## Einen Einkaufsvertrag auf der Grundlage eines Belegs erstellen

Sie können einen Einkaufsvertrag auch auf Basis eines Belegs erstellen.

So erstellen Sie einen Einkaufsvertrag auf der Grundlage eines Belegs:

1. Suchen {{search}} Sie nach **Belege** und wählen Sie dann den zugehörigen Link.

2. Wählen Sie in der Liste der Belege den Beleg aus, den Sie als Grundlage für Ihren Einkaufsvertrag verwenden möchten.

3. Wählen Sie **Bearbeiten** aus.

4. Wählen Sie in der Aktionsleiste **Aktionen** > **Einkaufsverträge** > **Erstelle Einkaufsvertrag**, um die Seite **Erstelle Einkaufsvertrag** zu öffnen.
  > [!NOTE]
  > Die folgenden Felder werden mit Daten aus der Kopfzeile des ausgewählten Belegs automatisch ausgefüllt:
  >
  > - **Beschreibung** wird automatisch mit dem Wert aus dem Feld **Beschreibung** des Belegs ausgefüllt.
  > - Der **Einkäufercode (Prüfer)** wird automatisch mit dem Wert **Verkäufer/Einkäufer** aus dem Feld **Expense-Genehmiger-ID** ausgefüllt, das Sie auf der Seite **Continia Benutzereinrichtung** finden.
  > - **Genehmigung** wird automatisch mit der Standardoption **Jährlich** ausgefüllt.
  > - **Kreditornr.** wird automatisch mit dem Wert aus dem Feld **Kreditornr.** des Belegs ausgefüllt.

5. Überprüfen Sie die automatisch ausgefüllten Felder und bearbeiten Sie sie, falls erforderlich. Füllen Sie dann die restlichen Felder nach Bedarf aus.

6. Wählen Sie **OK**, um die Seite zu schließen und den Vertrag zu erstellen.

Dadurch wird der Vertrag auf der Seite **Einkaufsverträge** geöffnet, wo Sie Änderungen vornehmen und weitere Felder ausfüllen können. Eine detaillierte Beschreibung dieses Vorgangs finden Sie in den Schritten 3–5 im obigen Abschnitt.

### Einen Beleg einem bestehenden Vertrag hinzufügen

Sie können einem bestehenden Einkaufsvertrag einen Beleg hinzufügen:

1. Suchen {{search}} Sie nach **Belege** und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Liste der Belege den Beleg aus, den Sie als Grundlage für Ihren Einkaufsvertrag verwenden möchten.
3. Wählen Sie **Bearbeiten** aus.
4. Wählen Sie unter **Einkaufsverträge** im Feld **Einkaufsvertragsnummer** den Vertrag aus, dem Sie den Beleg hinzufügen möchten.
5. Wählen Sie unter **Einkaufsverträge** im Feld **Einkaufsvertragszeilennr.** das Menü aus (...). Es wird ein Dialogfeld mit der Frage angezeigt, ob Sie basierend auf diesem Beleg eine neue Vertragszeile erstellen möchten. Wählen Sie **Ja**, um eine Vertragszeile zu erstellen.
  > [!NOTE]
  > Wenn der Vertrag bereits eine Zeile für diesen Mitarbeiter enthält, können Sie aus einer Liste mit Vertragszeilen auswählen, die nach dieser Mitarbeiternummer gefiltert sind.

## Informationen zum Thema

[Einkaufsverträge überprüfen](@EM-132)\
[Belege basierend auf einem Vertrag genehmigen](@EM-133)\
[Das Einkaufsvertragsarchiv anzeigen](@EM-134)

<style>
  .content table tr td:nth-child(1) {
    width: 120px;
  }
  .content table tr td:nth-child(2) {
    width: 610px;
  }  
</style>