---
title: E-Mail-Benachrichtigungen
date: 25-06-2025
description: Einrichten, Anpassen und Senden von Status- und Erinnerungs-E-Mails
id: DC-26
lang: de
---

# E-Mail-Benachrichtigungen

Sie können Genehmiger per E-Mail benachrichtigen, wenn sie eine Genehmigungsaktion in Continia Document Capture oder im Continia Web Approval Portal durchführen müssen, z. B. einen Beleg genehmigen, ablehnen oder stornieren. Sie können diese Benachrichtigung entweder [manuell](#so-senden-sie-status-e-mails-manuell) oder [automatisch über Aufgabenwarteschlangen](#so-senden-sie-status-e-mails-mithilfe-von-aufgabenwarteschlangen) senden.

Bei Bedarf können Sie [die E-Mails anpassen](#so-passen-sie-benachrichtigungs-e-mails-an) und es ist auch möglich, [Erinnerungs-E-Mails einzurichten](#so-richten-sie-erinnerungs-e-mails-ein), wenn die Genehmigung von Belegen dringlich ist.

Bevor Sie Benachrichtigungs-E-Mails senden können, müssen Sie mithilfe der unterstützten Einrichtung ein E-Mail-Konto konfigurieren:

1. Suchen Sie {{search}} nach **E-Mail einrichten** und wählen Sie dann den entsprechenden Link aus.
2. Folgen Sie den Anweisungen auf dem Bildschirm, um das E-Mail-Konto einzurichten.

## So senden Sie Status-E-Mails manuell

So benachrichtigen Sie Genehmiger manuell, dass Belege auf ihre Genehmigung warten:

1. Gehen Sie im Rollencenter zu **Continia Document Capture Aktivitäten**.
2. Klicken Sie unter **Aktionen** auf **Status-E-Mail an Genehmiger senden**.

Anschließend werden E-Mails an alle Genehmiger gesendet, die ausstehende Genehmigungsanforderungen haben. Jede E-Mail enthält eine Tabelle mit allen zur Genehmigung ausstehenden Belegen und einen Link zum Genehmigungs-Client, der für den Empfänger [für die Genehmigung von Belegen konfiguriert wurde](@DC-23#so-richten-sie-benutzer-als-genehmiger-ein) (entweder Document Capture oder das Web Approval Portal). Der Genehmigungs-Client zeigt dann alle Genehmigungsanforderungen an, die an diesem Tag noch nicht bearbeitet wurden.

> [!NOTE]
> Wenn eine Status-E-Mail an einen Genehmiger gesendet wird, wird dies von Document Capture protokolliert. Das Programm verwendet die Informationen, um zu bestimmen, wann weitere Benachrichtigungen gesendet werden sollen. Beim ersten Ausführen des Status-E-Mail-Prozesses an einem beliebigen Tag – ob manuell oder automatisch mithilfe von Aufgabenwarteschlange – wird eine E-Mail mit allen Belegen, deren Genehmigung noch aussteht, an den Genehmiger gesendet. Wenn der Prozess am selben Tag erneut ausgeführt wird, erhält der Genehmiger nur dann Status-E-Mails, wenn seit dem ersten Ausführen des Prozesses neue Genehmigungsanforderungen für diesen Genehmiger hinzugefügt wurden.

## So senden Sie Status-E-Mails mithilfe von Aufgabenwarteschlangen

Es besteht auch die Möglichkeit, Status-E-Mails mithilfe von Aufgabenwarteschlangen automatisch an Genehmiger zu senden. Weitere Informationen finden Sie unter [Aufgabenwarteschlangen einrichten](@DC-16).

Jede E-Mail enthält eine Tabelle mit allen zur Genehmigung ausstehenden Belegen und einen Link zum Genehmigungs-Client, der für den Empfänger [für die Genehmigung von Belegen konfiguriert wurde](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#so-richten-sie-benutzer-als-genehmiger-ein) (entweder Document Capture oder das Web Approval Portal). Der Genehmigungs-Client zeigt dann alle Genehmigungsanforderungen an, die an diesem Tag noch nicht bearbeitet wurden.

> [!TIP]
> Um doppelte Benachrichtigungen zu vermeiden, wird empfohlen, die Standardbenachrichtigungen von Microsoft Dynamics NAV/Business Central zu deaktivieren. Andernfalls werden die Genehmiger sowohl von Document Capture als auch NAV/Business Central über dieselben Genehmigungsanforderungen benachrichtigt.
>
> So deaktivieren Sie die Standardbenachrichtigungen:
>
> 1. Suchen Sie {{search}} nach **Document Capture Einrichtung** und wählen Sie dann den entsprechenden Link aus.
> 2. Klicken Sie im Inforegister **Allgemein** unter **Einkaufsgenehmigung** auf den Link im Feld **Status**.
> 3. Deaktivieren Sie auf der Seite **Document Capture Einrichtung / Einkaufsgenehmigungen** die Einstellung **Standardbenachrichtigung aktivieren**.

## So passen Sie Benachrichtigungs-E-Mails an

Sie können bestimmte Teile der E-Mails, die an Genehmiger gesendet werden, ganz einfach anpassen, einschließlich der Standardbetreffzeilen und des eigentlichen Texts, den sie enthalten:

1. Suchen Sie {{search}} nach **Document Capture Einrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie im Inforegister **Allgemein** unter **Einkaufsgenehmigung** auf den Link im Feld **Status**.
3. Füllen Sie auf der Seite **Document Capture Einrichtung / Einkaufsgenehmigung** unter **E-Mail-Einrichtung** die Felder nach Bedarf aus.
4. **Optional**: Um eine benutzerdefinierte HTML-Vorlage beispielsweise mit anderem Text und einer anderen Formatierung als die Standardvorlage zu importieren, gehen Sie zur Aktionsleiste und wählen Sie **Status-E-Mail** > **Vorlage importieren**. Wählen Sie dann die HTML-Vorlage aus, die Sie importieren möchten.

   > [!TIP]
   > Das Document Capture-Installationspaket enthält eine HTML-Vorlage für Status-E-Mails, die Sie bearbeiten und als Grundlage für Ihre eigene benutzerdefinierte Vorlage verwenden können. Sie finden dies hier: [Laufwerk]\Support Files\Document Capture\Other.
   >
   > Beachten Sie, dass Sie beim Erstellen Ihrer eigenen benutzerdefinierten Vorlage die beiden Schlüsselwörter #DOCUMENTS# und #APPROVALFORMLINK# beibehalten müssen. Beim Erstellen der Benachrichtigungs-E-Mail ersetzt Document Capture diese beiden Schlüsselwörter durch eine Liste aller relevanten Belege zur Genehmigung und einen Link zum entsprechenden Genehmigungs-Client.

   > [!NOTE]
   > Wenn Sie keine eigene benutzerdefinierte HTML-Vorlage importieren, verwendet Document Capture die Standardvorlage, die in einer Textvariablen in der Codeunit **CDC Purch. Approval E-Mail** hardcodiert wurde.
   >
   > Falls zuvor eine benutzerdefinierte Vorlage importiert wurde und Sie stattdessen die Standardvorlage verwenden möchten, können Sie die importierte Vorlage löschen, indem Sie die folgenden Schritte ausführen:
   >
   > 1. Klicken Sie auf der Seite **Document Capture Einrichtung / Einkaufsgenehmigungen** in der Aktionsleiste auf **Aktionen** > **E-Mail** > **Vorlage löschen**.
   > 2. In einem Dialogfeld werden Sie gefragt, ob Sie die Vorlage löschen möchten. Klicken Sie auf **Ja**, um die zuvor importierte Vorlage zu löschen und die Standardvorlage wiederherzustellen.

## So richten Sie Erinnerungs-E-Mails ein

Um den Benachrichtigungs-E-Mails an die Genehmiger eine zusätzliche Dringlichkeitsstufe zu verleihen, richten Sie eine oder mehrere benutzerdefinierte Erinnerungs-E-Mails ein.

Alle Einstellungen, die Sie beim Einrichten von Erinnerungs-E-Mails mit der Anleitung unten festlegen (zum Beispiel der Textkörper oder die Betreffzeilen von Erinnerungs-E-Mails) überschreiben alle Einstellungen, die Sie möglicherweise auf der Seite **Document Capture Einrichtung / Einkaufsgenehmigungen** konfiguriert haben.

So richten Sie Erinnerungs-E-Mails ein:

1. Suchen Sie {{search}} nach **E-Mail Einrichtung für Genehmigungserinnerung** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie in der Aktionsleiste auf **Neu**, um einen neuen Erinnerungs-E-Mail-Eintrag zu erstellen.
3. Geben Sie in der Spalte **Mahnstufe** die Stufe der Erinnerung an, indem Sie eine Ganzzahl eingeben. Da die Spalte **Mahnstufe** die Reihenfolge bestimmt, in der Erinnerungs-E-Mails versendet werden, ist die erste Stufe normalerweise mit **1** gekennzeichnet, und alle nachfolgenden Stufen werden mit fortlaufenden Nummern (**2**, **3** usw.) gekennzeichnet.
4. Geben Sie in der Spalte **Fälligkeitsformel** die Zeit ein, die vergehen soll, bevor eine Erinnerungs-E-Mail dieser Stufe versendet wird. Dieser Wert wird ab dem Zeitpunkt berechnet, an dem die Genehmigungsanfrage an den Genehmiger gesendet wird.
   > [!NOTE]
   > Ihr Eintrag muss eine Ganzzahl sein, gefolgt von **T** (Tage), **WT** (Wochentage), **W** (Wochen), **M** (Monate), **Q** (Quartale) oder **J** (Jahre) – zum Beispiel **2W** (zwei Wochen). Für komplexere Formeln können Sie auch die Operatoren + und - verwenden oder den Buchstaben **L** (laufend) als Präfix für eine der zuvor genannten Zeiteinheiten eingeben – zum Beispiel **LM+10T** (der laufende Monat plus zehn Tage).
5. **Optional**: Geben Sie in der Spalte **Sende an CC** an, ob Kopien der Erinnerungs-E-Mails an den Manager des aktuellen Genehmigers oder des ursprünglichen Genehmigers gesendet werden sollen.
6. **Optional**: Geben Sie in der Spalte **Sende CC an Benutzer-ID** die ID eines beliebigen anderen Benutzers ein, der Kopien der Erinnerungs-E-Mails erhalten soll.
7. Geben Sie in der Spalte **E-Mail-Betreff** den Text ein, der in der Betreffzeile aller auf dieser Stufe gesendeten Erinnerungs-E-Mails angezeigt werden soll.
8. **Optional**: Um den Textkörper einer der Erinnerungs-E-Mails anzupassen, wählen Sie die entsprechende Mahnstufe aus, gehen Sie zur Aktionsleiste und klicken Sie auf **Vortext** und/oder **Nachtext**. Geben Sie dann den Text ein, der im Text aller auf dieser Stufe gesendeten Erinnerungs-E-Mails angezeigt werden soll.

   > [!NOTE]
   > Erinnerungs-E-Mails werden pro Beleg gesendet, nicht als Liste mit allen Belegen, die genehmigt werden müssen. Bedenken Sie dies beim Einrichten von Erinnerungs-E-Mails.

## Informationen zum Thema

[Continia Benutzereinrichtung für Genehmigungen](@DC-23)