---
title: Administratoren über offene Belege benachrichtigen
date: 10-07-2024
description:
id: DC-158
lang: de
---

# Administratoren über offene Belege benachrichtigen

Es ist möglich, E-Mails an bestimmte Administratoren bzw. Sachbearbeiter zu senden (z. B. Manager der Kreditorenbuchhaltung), um sie darüber zu benachrichtigen, dass Belege in Continia Document Capture registriert werden müssen. Um diese Benachrichtigungs-E-Mails (auch Status-E-Mails genannt) zu senden, müssen Sie zuerst [einen Adminstrator als Kategorie-Manager](#so-ordnen-sie-kategorie-manager-zu) (für jede Belegkategorie) bestimmen und [das manuelle oder automatische Versenden von E-Mails](#so-senden-sie-status-e-mails) einrichten.

Sie können auch [benutzerdefinierte Erinnerungs-E-Mails](#so-richten-sie-erinnerungs-e-mails-ein) mit unterschiedlicher Dringlichkeitsstufe einrichten, je nachdem, wie lange sich die einzelnen Belege bereits im Belegjournal befinden. Für jede Stufe können Sie einen spezifischen Text eingeben, der die zunehmende Wichtigkeit der Registrierung der Dokumente hervorhebt. Anschließend werden in festgelegten Abständen Erinnerungs-E-Mails mit Ihrem eingegebenen Text an den zuständigen Administrator versendet, bis die Dokumente registriert wurden.

> [!NOTE]
> Obwohl diese Art der Benachrichtigung [Genehmigungsbenachrichtigungen](@DC-26) im Hinblick auf Einrichtung und Funktionalität sehr ähnlich ist, handelt sich jedoch um eine andere Art von Benachrichtigungs-E-Mails, die in unterschiedlichen Phasen des gesamten Dokumentenprozesses gesendet werden.

## So ordnen Sie Kategorie-Manager zu

Um einen Administrator als Kategoriemanager einzurichten, der Benachrichtigungs-E-Mails über nicht registrierte Belege erhält, gehen Sie folgendermaßen vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Kategorie aus, für die Sie einen Kategorie-Manager einrichten möchten. Beispielsweise die Kategorie **EINKAUF** (die Kategoriezeile, nicht der Code).
3. Klicken Sie in der Aktionsleiste auf **Bearbeiten**, um die Seite **Belegkategorie** zu öffnen.
4. Gehen Sie im Inforegister **Allgemein** zu **Kategorie-Manager**.
5. Wählen Sie im Dropdown-Menü den Benutzer aus, der über offene Belege benachrichtigt werden soll.
6. Schließen Sie die Seite **Belegkategorie** und wiederholen Sie die Schritte 2 bis 5 für alle weiteren Kategorien, für die Sie einen Kategorie-Manager einrichten möchten.

Die ausgewählten Benutzer werden jetzt über Belege benachrichtigt, deren Registrierung im Belegjournal ausstehend ist, sofern Sie [das manuelle oder automatische Versenden von Status-E-Mails eingerichtet haben](#so-senden-sie-status-e-mails).

## So richten Sie Erinnerungs-E-Mails ein

Nachdem Sie einen oder mehrere Kategorie-Manager zugewiesen haben, können Sie eine oder mehrere benutzerdefinierte Erinnerungs-E-Mails einrichten, damit die Empfänger zum Handeln aufgefordert werden. So richten Sie Erinnerungs-E-Mails ein:

1. Wählen Sie das Symbol {{search}}, geben Sie **E-Mail-Einrichtung für Erinnerung an offene Dokumente** ein, und wählen Sie dann den zugehörigen Link.
2. Klicken Sie in der Aktionsleiste auf **Neu**, um einen neuen Erinnerungs-E-Mail-Eintrag zu erstellen.
3. Geben Sie in der Spalte **Mahnstufe** die Stufe der Erinnerung an, indem Sie eine Ganzzahl eingeben. Da die Spalte **Mahnstufe** die Reihenfolge bestimmt, in der Erinnerungs-E-Mails versendet werden, ist die erste Stufe normalerweise mit **1** gekennzeichnet, und alle nachfolgenden Stufen werden mit fortlaufenden Nummern (**2**, **3** usw.) gekennzeichnet.
4. Geben Sie in der Spalte **Fälligkeitsformel** die Zeit ein, die vergehen soll, bevor eine Erinnerungs-E-Mail dieser Stufe versendet wird. Dies wird ab dem Zeitpunkt des Dokumentimports berechnet.
   > [!NOTE]
   > Ihr Eintrag muss eine Ganzzahl sein, gefolgt von **T** (Tage), **WT** (Wochentage), **W** (Wochen), **M** (Monate), **Q** (Quartale) oder **J** (Jahre) – zum Beispiel **2W** (zwei Wochen). Für komplexere Formeln können Sie auch die mathematischen Symbole + und – verwenden oder den Buchstaben **L** (laufend) als Präfix für eine der zuvor genannten Zeiteinheiten eingeben. Zum Beispiel **LM+10T** (der laufende Monat plus zehn Tage).
5. **Optional**: Wenn Sie Kopien der Erinnerungs-E-Mails an andere Benutzer senden möchten, geben Sie entweder die ID dieses Benutzers in der Spalte **Sende CC an Benutzer-ID** ein oder wählen Sie sie aus.
6. Geben Sie in der Spalte **E-Mail-Betreff** den Text ein, der in der Betreffzeile aller auf dieser Stufe gesendeten Erinnerungs-E-Mails angezeigt werden soll.
7. **Optional**: Um den Textkörper einer der Erinnerungs-E-Mails anzupassen, wählen Sie die entsprechende Mahnstufe aus, gehen Sie zur Aktionsleiste und wählen Sie **Vortext** und/oder **Nachtext** aus.

   > [!TIP]
   > Unter **Vortext** eingegebener Text wird oben in der E-Mail über der Tabelle mit den zur Registrierung ausstehenden Dokumenten angezeigt. Unter **Nachtext** eingegebener Text wird unten in der E-Mail unter der Dokumententabelle angezeigt.

## So senden Sie Status-E-Mails

Status-E-Mails können entweder manuell von Ihnen oder automatisch über Aufgabenwarteschlangen versendet werden. Beide Methoden werden nachfolgend beschrieben:

**So senden Sie Status-E-Mails manuell**:

1. Wählen Sie das Symbol {{search}}, geben Sie **Status E-Mails an Kategorie-Manager senden** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **OK**.

Status-E-Mails werden dann an die von Ihnen zugewiesenen Kategorie-Manager gesendet.

**Um Status-E-Mails automatisch mithilfe von Aufgabenwarteschlangen zu senden**, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Status E-Mails an Kategorie-Manager senden** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **Planen** aus.
3. Füllen Sie die Felder nach Bedarf aus. Weitere Informationen finden Sie unter [Planen der späteren oder regelmäßigen Ausführung eines Berichts](https://learn.microsoft.com/de-de/dynamics365/business-central/ui-work-report#scheduling-a-report-to-run-later-or-periodically) (Microsoft-Artikel).

Anschließend werden Status-E-Mails, entsprechend Ihrer festgelegten Einstellungen, an die von Ihnen zugewiesenen Kategorie-Manager gesendet.

> [!NOTE]
> Sie können die Aufgabenwarteschlange auch von der Seite **Aufgabenwarteschlangenposten** aus einrichten. Weitere Informationen dazu finden Sie unter [Aufgabenwarteschlangen einrichten](@DC-16).

## Informationen zum Thema

[E-Mail-Benachrichtigungen](@DC-26)