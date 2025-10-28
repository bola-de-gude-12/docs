---
title: Dokumentenkontrollprotokoll
date: 18-04-2024
description:
id: DC-212
lang: de
---

# Dokumentenkontrollprotokoll

Die Protokollierungsfunktion von [Secure Archive](@DC-154) zeichnet automatisch jeden Schritt bei der Verarbeitung von Dokumenten auf, die in Continia Document Capture und/oder Continia Expense Management importiert und darin verarbeitet wurden. Wenn solche Dokumente gebucht werden, wird im Inforegister **Allgemein** der Dokumentenkarte unter **Dokumentenprotokoll** eine Meldung angezeigt, die die Anzahl der Protokolleinträge angibt. Wenn an einem Dokument nach der Genehmigung und/oder Buchung Änderungen vorgenommen wurden, wird hier stattdessen eine rote Warnmeldung angezeigt, um darauf hinzuweisen, dass das Dokument und/oder die Anhänge geändert wurden.

Sie können den Status eines einzelnen gebuchten Dokuments jederzeit anzeigen, indem Sie dessen Dokumentenkarte öffnen und die Meldung unter **Dokumentenprotokoll** sowie die Seite **Zusammenfassung Belegprotokoll** prüfen. In vielen Fällen kann es jedoch vorzuziehen sein, stattdessen eine Stapelprüfung _aller_ relevanten Dokumente auszuführen, um einen schnellen Überblick darüber zu erhalten, welche Dokumente Ihre Aufmerksamkeit erfordern. Eine solche Übersicht bietet das **Dokumentenkontrollprotokoll**. Wenn Sie damit eine Stapelprüfung durchführen, werden für alle von Ihnen gefilterten Dokumente die folgenden Prüfungen durchgeführt:

- Es wird eine [Hashprüfung](@DC-154#hashfunktionen-fur-document-capture) durchgeführt, um zu ermitteln, ob die Dokumente nach der Buchung geändert wurden.
- Es wird geprüft, ob Anhänge zwischen der Genehmigung und Buchung geändert wurden.
- Es überprüft, ob Drag-and-Drop-Anhänge nach dem Buchen gelöscht wurden.

Anschließend werden alle Dokumente, die die definierten Filterkriterien erfüllen, in eine farbcodierte Liste aufgenommen, wobei Dokumente, die eine oder mehrere Prüfungen nicht bestanden haben, rot markiert sind. Auf diese Weise können Sie Probleme bei Dokumenten leichter identifizieren und die richtigen Maßnahmen zur Behebung der Probleme ergreifen. Durch die Verwendung des **Dokumentenkontrollprotokolls** müssen Sie nicht manuell zu jedem einzelnen gebuchten Beleg und seiner **Zusammenfassung Belegprotokoll** navigieren, um sich über mögliche Probleme zu informieren. Stattdessen können Sie jederzeit ganz einfach und proaktiv eine Liste abrufen.

Die auf der Seite **Dokumentenkontrollprotokoll** angezeigte Liste der Dokumente enthält mehrere Spalten mit relevanten Dokumentendetails sowie mehrere Spalten, die sich auf die Dokumentenprüfungen beziehen:

<br>

| Spalte                                  | Beschreibung                                                                                                                                                                                                                                                                                                                            |
| --------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Prüfung fehlgeschlagen**              | Gibt an, ob das Dokument eine Prüfung nicht bestanden hat. Wenn **Ja** angezeigt wird, ist der Text sowohl in dieser Spalte als auch in der Spalte **Letzte durchgeführte Prüfung** rot markiert.                                                                                                       |
| **Letzte durchgeführte Prüfung**        | Gibt an, wann die letzte Prüfung durchgeführt wurde. Wenn Sie in der Aktionsleiste **Dokumentenüberprüfungen durchführen** auswählen, wird dieses Datum aktualisiert.                                                                                                                                   |
| **Fehlermeldung prüfen**                | Gibt an, warum das Dokument eine Prüfung nicht bestanden hat. Dies ist die gleiche Meldung wie die, die unter **Dokumentenprotokoll** im Inforegister **Allgemein** des gebuchten Dokuments angezeigt wird.                                                                                             |
| **Fehlgeschlagene Prüfung abgeglichen** | Gibt an, ob eine fehlgeschlagene Prüfung abgestimmt wurde, von wem und wann. Wenn Sie in der Aktionsleiste **Abstimmen** auswählen, wird der Text in dieser Spalte aktualisiert und der Text in den Spalten **Prüfung fehlgeschlagen** und **Letzte Prüfung durchgeführt** wechselt von Rot zu Schwarz. |

## So führen Sie eine Stapelprüfung durch

Um eine Stapelprüfung durchzuführen und einen Filter für die zu prüfenden Dokumente zu definieren, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Dokumentenkontrollprotokoll** ein, und wählen Sie dann den zugehörigen Link.
2. Um eine Stapelprüfung durchzuführen, gehen Sie zur Aktionsleiste und wählen Sie **Dokumentenprüfungen durchführen**. Dadurch wird die Seite **Kontrollprotokolleinträge erstellen** geöffnet.
3. Um die Anzahl der Dokumente einzugrenzen, für die Sie die Prüfung durchführen möchten, können Sie einen Filter anwenden. Unter **Ergebnisse anzeigen** werden folgende Felder als Standardfilterkombination angezeigt:
   - **Buchungsdatum**
   - **Kreditorenbuchungsgruppe**
     Wenn Sie nach verschiedenen Feldern filtern möchten, wählen Sie jedes Feld aus, um ein Dropdown-Menü mit allen verfügbaren Feldern zu öffnen, und wählen Sie dann die entsprechenden Felder aus.
4. Um ein neues Filterfeld hinzuzufügen, wählen Sie **Filter hinzufügen** und wählen Sie dann einen Filter aus der Liste aus.
5. Geben Sie rechts neben jedem ausgewählten Feld unter **Geben Sie einen Wert ein** den Wert ein, den Sie als Filter verwenden möchten.
   > [!TIP]
   > Beispielsweise können Sie für das Feld **Buchungsdatum** **0101..T** eingeben, um Dokumente anzuzeigen, die zwischen dem 1. Januar des laufenden Jahres und dem heutigen Datum gebucht wurden.
6. **Optional**: Die Durchführung der Prüfung kann lange dauern, wenn Sie viele Dokumente haben. Falls Sie den Vorgang für einen späteren Zeitpunkt planen möchten, um Unterbrechungen in Ihrem Arbeitsablauf zu vermeiden, wählen Sie **Plan...**, um die Seite **Bericht planen** zu öffnen, und wählen Sie anschließend einen geeigneten Zeitpunkt aus. Wählen Sie **OK**, um die Seite zu schließen.
7. Wählen Sie **OK**, um die Prüfung durchzuführen und zur Seite **Dokumentenkontrollprotokoll** zurückzukehren.

Nun wird die Prüfung durchgeführt und eine Dokumentenliste erstellt. Wenn Sie oben in Schritt 6 **Planen** ausgewählt haben, wird die Prüfung zum ausgewählten Zeitpunkt durchgeführt.

## So erhalten Sie weitere Informationen zu Listeneinträgen

Weitere Informationen zu den einzelnen Einträgen in der Liste finden Sie auf der Seite **Dokumentenkontrollprotokoll**. Gehen Sie dazu folgendermaßen vor:

1. Befolgen Sie die Anleitung oben unter [So führen Sie eine Stapelprüfung durch](#so-fuhren-sie-eine-stapelprufung-durch), um eine Liste mit Dokumenten zu erstellen.
2. Um den Verlauf eines aufgelisteten Dokuments und vorgenommene Prüfungen mit der Aktion **Dokumentenüberprüfungen durchführen** anzuzeigen, gehen Sie wie folgt vor:
   1. Wählen Sie das Dokument aus, dessen Prüfverlauf Sie anzeigen möchten.
   2. Klicken Sie in der Aktionsleiste auf **Kontrollprotokolleinträge**, um die Seite **Anzeigen – Dokumentenkontrollprotokolleinträge** zu öffnen.
   3. Wählen Sie **Schließen**, nachdem Sie die Prüfung durchgeführt haben, um zur Seite **Dokumentenkontrollprotokoll** zurückzukehren.
3. Um alle weiteren Einträge zu einem Dokument in der Liste anzuzeigen, gehen Sie wie folgt vor:
   1. Wählen Sie das Dokument aus, für das Sie Einträge anzeigen möchten.
   2. Klicken Sie in der Aktionsleiste auf **Einträge finden**, um die Seite zum Bearbeiten zu öffnen.
   3. Wählen Sie die Einträge aus, die Sie anzeigen möchten, und navigieren Sie zurück zur Seite **Dokumentenkontrollprotokoll**, wenn Sie fertig sind.
4. Um die Seite **Zusammenfassung Belegprotokoll** zu öffnen, auf die Sie sonst über die Dokumentenkarte des gebuchten Dokuments zugreifen würden, gehen Sie wie folgt vor:
   1. Wählen Sie das Dokument aus, für das Sie die **Zusammenfassung Belegprotokoll** anzeigen möchten.
   2. Klicken Sie in der Aktionsleiste auf **Zusammenfassung Belegprotokoll**.
   3. Wenn Sie fertig sind, wählen Sie **Schließen**, um zur Seite **Zusammenfassung Belegprotokoll** zurückzukehren.

## So filtern Sie die Liste und stimmen fehlgeschlagene Dokumente ab

Mit der Aktion **Abstimmen** können Sie bestätigen, dass Sie über eine fehlgeschlagene Prüfung informiert wurden und dieser nachgegangen sind. Wenn Sie ein fehlgeschlagenes Dokument abstimmen, wird es von allen zukünftigen Prüfungen ausgeschlossen und nicht mehr als fehlgeschlagen markiert (rot formatiert). Bei Bedarf können Sie mit derselben Aktion auch problemlos die Abstimmung eines abgestimmten Dokuments aufheben.

Es ist auch möglich, die Liste zu filtern, um nur fehlgeschlagene Dokumente anzuzeigen, die rot formatiert sind. Und Sie können ganz einfach wieder zur Anzeige aller Dokumente zurückkehren.

Um Dokumente abzugleichen oder die Abstimmung aufzuheben und/oder die Liste so zu filtern, dass nur fehlgeschlagene Dokumente angezeigt werden, führen Sie die folgenden Schritte aus:

1. Befolgen Sie die Anleitung oben unter [So führen Sie eine Stapelprüfung durch](#so-fuhren-sie-eine-stapelprufung-durch), um eine Liste mit Dokumenten zu erstellen.
2. Wählen Sie in der Liste der Dokumente das Dokument aus, das Sie abstimmen oder deren Abstimmung Sie aufheben möchten.
3. Klicken Sie in der Aktionsleiste auf **Abstimmen**.
4. Um nur fehlgeschlagene Dokumente anzuzeigen, die rot formatiert sind, wählen Sie in der Aktionsleiste **Fehlerhafte Zeilen anzeigen** aus. Um alle Dokumente anzuzeigen, wählen Sie die Option erneut aus.
