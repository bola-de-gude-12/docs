---
title: Expense Management Einkaufsverträge überprüfen
date: 01-04-2023
description: null
id: EM-132
lang: de
---

# Einkaufsverträge überprüfen

Der Überprüfungsprozess ist ein zentraler Bestandteil des Einkaufsverträge-Moduls. Mit Vertragsüberprüfungen soll sichergestellt werden, dass ein Mitarbeitender im Unternehmen (der Prüfer) die aktuellen Verträge des Unternehmens prüft und darauf achtet, dass sie auf dem neuesten Stand sind oder bei Bedarf verlängert, gekündigt oder geändert werden. Sie können für die einzelnen Verträge verschiedene Prüfer oder einen Prüfer für alle Verträge bestimmen, je nachdem, was für Ihr Unternehmen am sinnvollsten ist.

Ein Einkaufsvertragsadministrator – normalerweise ein Buchhalter – startet den Prozess, indem er entweder einen Vertrag oder mehrere Verträge auf einmal an den Prüfer sendet. Dieser sieht die Verträge durch und sendet Sie dann an den Buchhalter zur Überprüfung und zum Abschluss zurück. Bei jeder Überprüfung kann der Prüfer zusätzliche Zeilen hinzufügen, nicht verwendete Zeilen entfernen und Überprüfungskommentare schreiben, die der Einkaufsvertragsadministrator berücksichtigen kann.

In den folgenden Abschnitten werden die einzelnen Schritte im Prozess genauer beschrieben.

> [!TIP]
> Außer dem Symbol {{search}}, das in den folgenden Anleitungen verwendet wird, können Prüfer und Einkaufsvertragsadministratoren den Überprüfungsprozess auch mit den Stapeln in der Stapelgruppe **Einkaufsverträge** im Microsoft Dynamics 365 Business Central-Rollencenter verwalten. Die Gruppe enthält die folgenden vier Stapel:
>
> - **Alle**: Enthält alle Verträge und bietet allen Benutzern eine gute Übersicht.
> - **Überprüfung fällig**: Enthält Verträge, die maximal eine Woche fällig sind. Dieser Stapel ist hauptsächlich für Prüfer vorgesehen.
> - **Überfällig**: Enthält Verträge, deren Datum für **Nächste Überprüfung am** mehr als eine Woche zurückliegt. Dieser Stapel ist hauptsächlich für Prüfer vorgesehen.
> - **Überprüfung eingereicht**: Enthält Verträge, die vom Prüfer geprüft und zurückgesendet wurden. Dieser Stapel ist in erster Linie für den Einkaufsvertragsadministrator vorgesehen.

## So richten Sie einen Einkaufsvertragsadministrator ein

Um Verträge zur Prüfung zu senden und verschiedene Prüfungsaktionen durchführen zu können, müssen Sie als Einkaufsvertragsadministrator eingerichtet sein. Gehen Sie dazu folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Continia Benutzereinrichtung** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Liste der Continia-Benutzer die ID des Benutzers aus, den Sie als Einkaufsvertragsadministrator einrichten möchten. Dadurch wird die **Continia Benutzereinrichtung Karte** geöffnet.
3. Aktivieren Sie im Inforegister **Allgemein** im Abschnitt **Einkaufsverträge** den Schalter **Einkaufsvertragsadministrator**.

Dadurch wird der ausgewählte Benutzer zum Einkaufsvertragsadministrator und kann Verträge zur Überprüfung versenden und Überprüfungen verwalten.

## So senden Sie einen einzelnen Vertrag zur Überprüfung

> [!NOTE]
> Nur Einkaufsvertragsadministratoren können diese Aktion ausführen. Um einen Einkaufsvertragsadministrator einzurichten, folgen Sie [der Anleitung oben](#so-richten-sie-einen-einkaufsvertragsadministrator-ein).

Als Einkaufsvertragsadministrator können Sie einen Vertrag folgendermaßen zur Überprüfung senden:

1. Wählen Sie das Symbol {{search}}, geben Sie **Einkaufsverträge** ein, und wählen Sie dann den zugehörigen Link, um die Seite **Einkaufsverträge** zu öffnen.
2. Wählen Sie in der Vertragsliste den Vertrag aus, den Sie zur Überprüfung senden möchten.
3. Wählen Sie in der Aktionsleiste **Start** > **Überprüfung beginnen**.

Dadurch wird der Vertrag zur Überprüfung gesendet und das Feld **Status** im Inforegister **Überprüfen** zeigt dann **Überprüfung ausstehend** an.

## So senden Sie mehrere Verträge zur Überprüfung

> [!NOTE]
> Nur Einkaufsvertragsadministratoren können diese Aktion ausführen. Um einen Einkaufsvertragsadministrator einzurichten, folgen Sie [der Anleitung oben](#so-richten-sie-einen-einkaufsvertragsadministrator-ein).

Als Einkaufsvertragsadministrator können Sie mehrere Verträge folgendermaßen zur Überprüfung senden:

1. Wählen Sie das Symbol {{search}}, geben Sie **Einkaufsverträge** ein, und wählen Sie dann den zugehörigen Link, um die Seite **Einkaufsverträge** zu öffnen.
2. Wählen Sie in der Aktionsleiste **Start** > **Stapelüberprüfung starten...** aus, um die Seite **Einkaufsverträge zur Überprüfung senden** zu öffnen.
3. Im Inforegister **Filter: Einkaufsvertragskopf** wird der Filter **Nächste Überprüfung am** hinzugefügt und mit dem Datumsbereich **..[heute]** automatisch gefüllt. So werden alle Verträge, die noch nicht überprüft wurden, und deren Datum in **Nächste Überprüfung am** überschritten wurde, in einem Stapel zur Überprüfung gesendet. Sie können den automatisch ausgefüllten Datumsbereich auch ändern.
4. **Optional:** Wenn Sie einen weiteren Filter hinzufügen möchten, wählen Sie **+ Filter**.
5. **Optional:** Geben Sie im Inforegister **Erweitert** alle erforderlichen Einschränkungen für den Stapelbericht hinsichtlich der Zeilengenerierungszeit und/oder der maximalen Zeilen- oder Beleganzahl ein.
6. **Optional:** Wenn Sie den Stapelbericht zu einem späteren Zeitpunkt ausführen möchten, wählen Sie **Plan…** und dann ein Startdatum/eine Startzeit und ein Ablaufdatum/eine Ablaufzeit aus. Sie können auch eine Datumsformel eingeben, die dann das Feld **Früheste(s) Startdatum/-uhrzeit** automatisch ausfüllt.
   > [!NOTE]
   > Wenn Sie **Datumsformel für nächste Ausführung** auswählen, müssen Sie eine Formel in Form einer Ganzzahl gefolgt von **T** (Tage), **WT** (Wochentage), **W** (Wochen), **M** (Monaten), **Q** (Quartale) oder **J** (Jahre) eingeben, zum Beispiel **2W** (zwei Wochen). Für komplexere Formeln können Sie auch die mathematischen Symbole + und – verwenden oder den Buchstaben **L** (laufend) als Präfix für eine der zuvor genannten Zeiteinheiten eingeben – zum Beispiel **LM+10T** (der laufende Monat plus zehn Tage).
7. Wählen Sie **OK**, wenn Sie fertig sind.

Dadurch werden alle Verträge innerhalb des angegebenen Datumsbereichs in einem Stapel zur Überprüfung gesendet, und das Feld **Status** im Inforegister **Überprüfen** zeigt dann für alle Verträge **Überprüfung ausstehend** an.

## So brechen Sie eine Vertragsüberprüfung ab

> [!NOTE]
> Nur Einkaufsvertragsadministratoren können diese Aktion ausführen. Um einen Einkaufsvertragsadministrator einzurichten, folgen Sie [der Anleitung oben](#so-richten-sie-einen-einkaufsvertragsadministrator-ein).

Um eine gestartete Überprüfung abzubrechen, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Einkaufsverträge** ein, und wählen Sie dann den zugehörigen Link, um die Seite **Einkaufsverträge** zu öffnen.
2. Wählen Sie in der Vertragsliste den Vertrag aus, dessen Überprüfung Sie abbrechen möchten.
3. Wählen Sie in der Aktionsleiste **Start** > **Überprüfung abbrechen**.
4. Ein Dialogfeld wird angezeigt, in dem Sie gefragt werden, ob Sie die Überprüfung abbrechen möchten. Wählen Sie **Ja**.

Dadurch wird die Überprüfung abgebrochen. Außerdem wird auf der Seite **Einkaufsvertrag** im Feld **Status** im Inforegister **Überprüfen** nicht mehr **Überprüfung ausstehend** angezeigt, sondern ein leeres Statusfeld.

## So reichen Sie eine Vertragsüberprüfung ein

Sobald Ihnen ein Vertrag von einem Einkaufsvertragsadministrator zur Überprüfung zugesandt wurde, können Sie den Vertrag prüfen und mit Kommentaren an den Administrator zurücksenden. Sie können dies entweder in Business Central oder im Continia Web Approval Portal vornehmen, wie in den folgenden beiden Abschnitten beschrieben:

### Mit Business Central

Um eine Überprüfung mit Business Central einzureichen, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Einkaufsverträge** ein, und wählen Sie dann den zugehörigen Link, um die Seite **Einkaufsverträge** zu öffnen.
2. Wählen Sie in der Liste der Verträge in der Spalte **Nr.** die Nummer des Vertrags aus, den Sie überprüfen möchten. Dadurch wird die Seite **Einkaufsvertrag** geöffnet.
3. Überprüfen Sie den Vertrag und nehmen Sie die erforderlichen Änderungen vor.
4. Wenn Sie den Vertrag überprüft haben, gehen Sie zum Inforegister **Überprüfen** und wählen Sie das Feld **Bemerkungen** aus.
5. Wählen Sie auf der geöffneten Seite in der Aktionsleiste **Neu** aus, um eine Kommentarzeile hinzuzufügen.
6. Geben Sie unter **Bemerkungen** Ihre Überprüfungskommentare ein. Die Felder **Datum** und **Name** werden automatisch ausgefüllt.
7. Wiederholen Sie die Schritte 5–6, wenn Sie weitere Bemerkungen hinzufügen möchten, und kehren Sie dann zur Seite **Einkaufsvertrag** zurück. Hier werden Ihre Kommentare im Feld **Bemerkungen** angezeigt.
8. Wählen Sie in der Aktionsleiste **Start** > **Überprüfung einreichen**.
9. Ein Dialogfeld wird angezeigt, in dem Sie gefragt werden, ob Sie die Überprüfung einreichen möchten. Wählen Sie **Ja**.

Dadurch wird Ihre Überprüfung an den Einkaufsvertragsadministrator gesendet und das Feld **Status** im Inforegister **Überprüfen** ändert sich in **Überprüfung eingereicht**.

### Mit dem Web Approval Portal

Um eine Überprüfung mit dem Web Approval Portal einzureichen, gehen Sie folgendermaßen vor:

1. Melden Sie sich am Web Approval Portal an.
2. Wählen Sie auf der Registerkarte **Einkauf** die Option **Verträge** aus, um die Seite **Meine ausstehenden Überprüfungen** zu öffnen.
3. Wählen Sie in der Liste der zu überprüfenden Verträge den Vertrag aus, den Sie zur Überprüfung einreichen möchten.
4. Überprüfen Sie den Vertrag und nehmen Sie die erforderlichen Änderungen vor.
5. Geben Sie im Textfeld oben rechts Ihre Bemerkungen von der Überprüfung ein und wählen Sie **Speichern** aus, wenn Sie fertig sind. Wiederholen Sie diesen Schritt, wenn Sie weitere Bemerkungen hinzufügen möchten.
6. Wählen Sie in der Aktionsleiste **Überprüfung einreichen** aus.

Dadurch wird Ihre Überprüfung an den Einkaufsvertragsadministrator übermittelt. Außerdem wird in Business Central auf der Seite **Einkaufsvertrag** im Feld **Status** im Inforegister **Überprüfen** > **Überprüfung eingereicht** angezeigt.

## So schließen Sie eine Vertragsüberprüfung ab

> [!NOTE]
> Nur Einkaufsvertragsadministratoren können diese Aktion ausführen. Um einen Einkaufsvertragsadministrator einzurichten, folgen Sie [der Anleitung oben](#so-richten-sie-einen-einkaufsvertragsadministrator-ein).

Als Einkaufsvertragsadministrator können Sie eine Vertragsüberprüfung folgendermaßen abschließen:

1. Wählen Sie das Symbol {{search}}, geben Sie **Einkaufsverträge** ein, und wählen Sie dann den zugehörigen Link, um die Seite **Einkaufsverträge** zu öffnen.
2. Wählen Sie in der Liste der Verträge in der Spalte **Nr.** die Nummer des Vertrags aus, deren Überprüfung Sie abschließen möchten. Dadurch wird die Seite **Einkaufsvertrag** geöffnet.
3. Prüfen Sie die Vertragsänderungen des Prüfers sowie die Bemerkungen im Inforegister **Überprüfen** unter **Bemerkungen**.
4. **Optional:** Wenn etwas nicht ganz richtig ist oder Sie Fragen an den Prüfer haben, können Sie unter **Bemerkungen** selbst einen Kommentar hinzufügen, um den Prüfer über Fehler oder Unklarheiten zu informieren. Senden Sie den Vertrag anschließend an den Prüfer zurück, indem Sie **Start** > **Zur Korrektur ablehnen** auswählen. Wählen Sie im Dialogfeld, das geöffnet wird, **Ja** aus.
   > [!NOTE]
   > Dadurch wird die Überprüfung an den Prüfer zurückgesendet und das Feld **Status** im Inforegister **Überprüfen** wieder in **Überprüfung ausstehend** geändert. Der Prüfer kann dann die Kommentare des Administrators prüfen, alle notwendigen Änderungen vornehmen und die Prüfung wie [oben beschrieben](#so-reichen-sie-eine-vertragsuberprufung-ein) wieder einreichen.
5. Wenn hingegen alles in Ordnung ist, können Sie die Überprüfung wie folgt abschließen: Wählen Sie in der Aktionsleiste **Start** > **Überprüfung abschließen** aus.
6. Ein Dialogfeld wird angezeigt, in dem Sie gefragt werden, ob Sie die Überprüfung abschließen möchten. Wählen Sie **Ja**.

Dadurch gibt es fünf Änderungen im Inforegister **Überprüfen**: Alle Informationen im Feld **Status** werden gelöscht, um den nächsten Überprüfungszyklus vorzubereiten, und das Feld **Nächste Überprüfung am** wird basierend auf der Überprüfungshäufigkeit aktualisiert, die Sie im Feld **Überprüfen** angegeben haben. Darüber hinaus werden alle Überprüfungsbemerkungen, die Sie möglicherweise hinzugefügt haben, im Feld **Bemerkungen** angezeigt. **Letzte Überprüfung am** wird mit dem Tagesdatum aktualisiert und anschließend wird Ihr Name unter **Letzte Überprüfung von** angezeigt.

## Informationen zum Thema

[Einkaufsverträge erstellen](@EM-131)\
[Belege basierend auf einem Vertrag genehmigen](@EM-133)\
[Das Einkaufsvertragsarchiv anzeigen](@EM-134)
