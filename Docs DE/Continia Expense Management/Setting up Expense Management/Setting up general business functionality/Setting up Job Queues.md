---
title: Aufgabenwarteschlangen in Expense Management einrichten
date: 13-11-2024
description: Lernen Sie, wie Sie Aufgabenwarteschlangen in Expense Management einrichten und verwalten.
id: EM-65
lang: de
---

# Aufgabenwarteschlangen einrichten

Durch die Automatisierung regelmäßiger Aufgaben wie der Synchronisierung können Sie viel Zeit sparen. Mithilfe von Aufgabenwarteschlangen können Sie diese Prozesse automatisieren, indem Sie Aufgaben automatisch im Hintergrund ausführen lassen, wobei bei Bedarf eine manuelle Synchronisierung möglich bleibt. In diesem Artikel wird beschrieben, wie Sie Aufgabenwarteschlangen in Expense Management einrichten und verwalten, um Aufgaben wie Synchronisierungen, Genehmigungen und Erinnerungen zu automatisieren. Er umfasst eine Liste [der verfügbaren Aufgabenwarteschlangen](@EM-278), Informationen zum [Erstellen und Verwalten von Posten mit der Seite **Einrichtung Aufgabenwarteschlangenposten**](#so-verwenden-sie-die-seite-zum-einrichten-von-aufgabenwarteschlangen), um Aufgabenwarteschlangen zu verwalten, Zeitpläne anzupassen und er bietet eine schrittweise Anleitung zum [Konfigurieren von Aufgabenwarteschlangen und Verwalten der Zeitpläne auf der **Karte für Aufgabenwarteschlangenposten**](#so-richten-sie-aufgabewarteschlangen-ein). Allgemeine Informationen zum Arbeiten mit Aufgabenwarteschlangen in Business Central finden Sie im [Microsoft-Artikel zu Aufgabenwarteschlangen](https://docs.microsoft.com/de-de/dynamics365/business-central/admin-job-queues-schedule-tasks).

## So verwenden Sie die Seite zum Einrichten von Aufgabenwarteschlangen

Um das Einrichten und Verwalten wiederkehrender Aufgaben zu vereinfachen, können Sie die Seite **Einrichtung Aufgabenwarteschlangenposten** von Expense Management verwenden. Über diese Seite erhalten Administratoren direkten Zugriff auf die Standardcodeunits, um schnell Einträge für Aufgaben wie Synchronisierungen und Genehmigungen zu erstellen und zu verwalten, ohne für jede Aufgabe manuell nach Jobcodes suchen zu müssen.

So verwalten Sie Aufgabenwarteschlangen:

1. Wählen Sie das Symbol {{search}}, geben Sie **Expense Management Einrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Aktionsleiste **Einrichtung** > **Einrichtung Aufgabenwarteschlangenposten** aus.
3. Wählen Sie auf der Seite **Einrichtung Aufgabenwarteschlangenposten** in der Aktionsleiste **Alle planen** aus, wenn Sie alle Codeunits auf die Standardeinstellungen zurücksetzen möchten.
4. Über die Felder auf der Seite **Einrichtung Aufgabenwarteschlangenposten** haben Sie Zugriff auf die Standardcodeunits und können deren Zeitplan nach Bedarf anpassen. Sie können eine neue Aufgabenwarteschlange hinzufügen und die Einstellungen aktiver Aufgabenwarteschlangen ändern, beispielsweise Startzeit, Häufigkeit oder Wiederholung der Aufgabe. Nachdem Sie Ihre Anpassungen vorgenommen haben, wählen Sie **Neu starten**, um die Änderungen anzuwenden und die Codeunit zu aktivieren. Die folgenden Felder sind verfügbar:
   | Feld               | Beschreibung                                                                                                                                                                                                                                                                     |
   | ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | Continia Online    | Wählen Sie _Jetzt planen_ oder den aktuellen Wert aus, um direkten Zugriff auf die Karte für Codeunit 6086305 CEM Online Synch. Mgt. zu erhalten, mit der Sie die Synchronisierung mit Continia Online verwalten können.         |
   | Feldabhängigkeiten | Wählen Sie _Jetzt planen_ oder wählen Sie den aktuellen Wert aus, um direkten Zugriff auf die Karte für die Codeunit 6086569 CEM Update Field Dependencies zu erhalten.                                                                                          |
   | Genehmigermail     | Wählen Sie _Jetzt planen_ oder wählen Sie den aktuellen Wert aus, um direkten Zugriff auf die Karte für die Codeunit 6086313 CEM Expense Approval Email zu erhalten. Mit dieser Codeunit können Sie den Versand von Genehmigungs-E-Mails planen. |
   | Erinnerungsmail    | Wählen Sie _Jetzt planen_ oder wählen Sie den aktuellen Wert aus, um direkten Zugriff auf die Karte für die Codeunit 6086314 CEM Reminder Email zu erhalten. Mit dieser Codeunit können Sie den Versand von Erinnerungs-E-Mails planen.          |
   | Statusbericht      | Wählen Sie _Jetzt planen_ oder wählen Sie den aktuellen Wert aus, um direkten Zugriff auf die Karte für die Codeunit 6086353 CEM Send Status Report zu erhalten. Mit dieser Codeunit können Sie das Senden von Statusberichten planen.           |

## So richten Sie Aufgabewarteschlangen ein

Wie oben erwähnt, können Sie Aufgabenwarteschlangen verwenden, um viele verschiedene Aufgaben und Prozesse zu planen und auszuführen. Der Einrichtungsvorgang ist immer gleich – nur die Codeunits/Berichte sind unterschiedlich.

Um eine Aufgabenwarteschlange einzurichten, folgen Sie diesen Schritten:

1. Wählen Sie das Symbol {{search}}, geben Sie **Aufgabenwarteschlangenposten** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Aktionsleiste **Neu** aus, um die **Karte für Aufgabenwarteschlangenposten** zu öffnen. Alternativ können Sie auf der Seite **Expense Management Einrichtung** die Optionen **Einrichtung** > **Einrichtung Aufgabenwarteschlangenposten** wählen und ein Feld auswählen, um die Karte für den Aufgabenwarteschlangenposten zu öffnen.
3. Gehen Sie auf der **Karte für Aufgabenwarteschlangenposten** zu **Art des auszuführenden Objekts** und wählen Sie den entsprechenden Typ aus, je nachdem, ob Sie eine Codeunit oder einen Bericht ausführen.
4. Geben Sie im Feld **ID des auszuführenden Objekts** die entsprechende Codeunit bzw. den entsprechenden Bericht ein.
5. Geben Sie unter **Früheste(s) Startdatum/-uhrzeit** mithilfe des Datums und der Uhrzeit an, wann mit der Ausführung der Aufgabenwarteschlange begonnen werden soll. Wenn Sie ein Datum ausgewählt oder eingegeben haben, wird das Feld **Früheste(s) Startdatum/-uhrzeit** automatisch mit der Standardtageszeit ausgefüllt; Sie können dies jedoch bei Bedarf ändern.
6. Geben Sie im Inforegister **Wiederholung** die Wiederholungsrate der Aufgabenwarteschlange an, indem Sie den Schalter für jeden der Tage aktivieren, an denen sie ausgeführt werden soll. Füllen Sie die verbleibenden Felder im Inforegister **Wiederholung** nach Bedarf aus.
7. Wählen Sie in der Aktionsleiste **Status auf 'Bereit' festlegen** aus, um die Aufgabenwarteschlange zu starten.

> [!NOTE]
> Aufgabenwarteschlangen schlagen manchmal fehl, beispielsweise aufgrund einer unterbrochenen Kommunikation mit einer wichtigen externen Ressource, die nicht mehr reagiert. Dies führt schließlich zu einem Fehlerstatus. Um dies zu vermeiden, sollten Sie in den Feldern **Maximale Anzahl von Ausführungsversuchen** und **Verzögerung der erneuten Ausführung (Sek.)**, die sich auf dem Inforegister **Allgemein** befinden, einen Wert festlegen. Beachten Sie, dass Sie möglicherweise **Mehr anzeigen** auswählen müssen, damit diese Felder sichtbar werden.
