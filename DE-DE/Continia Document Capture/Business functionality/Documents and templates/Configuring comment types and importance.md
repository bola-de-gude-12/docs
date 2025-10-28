---
title: Bemerkungsarten und deren Wichtigkeit konfigurieren
date: 07-10-2022
description:
id: DC-72
lang: de
---

# Bemerkungsarten und deren Wichtigkeit konfigurieren

Das Belegjournal von Continia Document Capture verfügt über einen Bereich, in dem verschiedene Bemerkungen zu dem ausgewählten Beleg angezeigt werden. Es gibt drei verschiedene Arten von Bemerkungen:

<br>

| Art der Bemerkung | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Informationen** | Hiermit werden Sie normalerweise darüber informiert, dass ein bestimmter Prozess abgeschlossen wurde, ohne dass eine Aktion von Ihnen erforderlich war. Beispiele: <ul><li>„Fälligkeitsdatum wurde auf Basis von Belegdatum berechnet“.</li><li>„Automatisch abgeglichen“.</li></ul>                                                                                                                                                                                                                                           |
| **Warnung**       | Informiert Sie darüber, dass im Beleg möglicherweise eine manuelle Bearbeitung oder Anpassung erforderlich ist. Belege mit Bemerkungen dieser Art werden vom Stapelregistrierungsprozess ausgeschlossen. Beispiele: <ul><li>„ACHTUNG: Zahlungsbedingungen (CM) nicht korrekt.“</li><li>„Bestellnr. = '[Bestellnummer]' existiert, aber mit einer anderen Währung."</li></ul>                            |
| **Fehler**        | Weist darauf hin, dass der Beleg nicht registriert werden kann. Fehler werden im Bemerkungsbereich fett und in roter Schrift angezeigt. Beispiele: <ul><li>"Beträge stimmen nicht überein."</li><li>"Kreditor-Rechnungsnummer. [Rechnungsnummer] ist bereits vorhanden (im Kreditorenposten, Lfd. Nr. = [Postennummer])."</li></ul> |

## Konfigurierbare Bemerkungen

Viele der Bemerkungen, die im Belegjournal angezeigt werden, sind konfigurierbar und können folgendermaßen bearbeitet werden:

- Sie können die Bemerkungsart ändern.
- Bei Fehlerbemerkungen können Sie angeben, ob Belege mit diesem Fehler automatisch einem Benutzer zugewiesen werden sollen, der das Problem beheben kann.

Wenn eine Bemerkung konfigurierbar ist, wird in der Spalte **Konfigurierbar** der Bemerkung**Ja** angezeigt; andernfalls wird **Nein** angezeigt.

Änderungen an der Bemerkungskonfiguration können angewendet werden auf:

1. Eine bestimmte Kreditorenvorlage. Dies ist auf der **Belegkategorie**-Karte möglich (oder direkt vom Belegjournal aus). Verwenden Sie hierzu die [Anleitung unten](#so-konfigurieren-sie-bemerkungen-fur-bestimmte-vorlagen).
2. Alle Vorlagen im aktuellen Mandanten. Dies ist unter **Benachrichtigungscenter Einrichtung** möglich. Verwenden Sie hierzu die [Anleitung unten](#so-konfigurieren-sie-bemerkungen-fur-alle-vorlagen-in-einem-mandanten).

> [!NOTE]
> Änderungen, die Sie mit Option 1 an einzelnen Vorlagen vorgenommen haben, überschreiben alle Bemerkungsänderungen, die Sie mit Option 2 auf alle Mandantenvorlagen angewendet haben.

## So konfigurieren Sie Bemerkungen für bestimmte Vorlagen

Um Bemerkungen für eine bestimmte Kreditorenvorlage zu konfigurieren, gehen Sie folgendermaßen vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.

2. Wählen Sie die entsprechende Belegkategorie aus, beispielsweise **EINKAUF**, und wählen Sie dann in der Aktionsleiste **Bearbeiten** aus, um die Karte **Belegkategorie** zu öffnen.

3. Wählen Sie im Inforegister **Vorlagen** die entsprechende Vorlage in der Liste aus, und wählen Sie dann **Bearbeiten** aus, um die Vorlagenkarte zu öffnen.

4. Klicken Sie in der Aktionsleiste auf **Zugehörig** > **Vorlage** > **Benachrichtigungscenter Einrichtung**, um die Seite **Benachrichtigungscenter Einrichtung** für die ausgewählte Vorlage zu öffnen.

5. Konfigurieren Sie die Bemerkungen nach Bedarf in den entsprechenden Feldern:

   <br>

   | Feld                                 | Beschreibung                                                                                                                                                                                                                                                                                            |
   | ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | **Benutzerdefinierte Bemerkungsart** | Ermöglicht Ihnen, den Bemerkungstyp zu ändern. Sie können den Schweregrad einer Bemerkung erhöhen, indem Sie ihn beispielsweise von **Warnung** zu **Fehler** ändern. Eine Herabstufung von **Fehler** auf **Warnung** ist normalerweise nicht möglich. |
   | **Bei Fehler zuweisen**              | Hiermit können Sie festlegen, dass ein Beleg automatisch einem bestimmten Benutzer zugewiesen wird, wenn die ausgewählte Bemerkung in einem Beleg angezeigt wird, um das Problem zu lösen. Das Feld ist nur für **Fehler**-Bemerkungen auswählbar.                      |
   | **Benutzer ID zuweisen**             | Hiermit können Sie die ID des Benutzers angeben, dem Belege mit der ausgewählten Bemerkung zugewiesen werden sollen. Das Feld kann nur bearbeitet werden, wenn **Bei Fehler zuweisen** ausgewählt wurde.                                                                |

   > [!NOTE]
   > Wenn Sie eine Bemerkung konfigurieren, wird der Text der gesamten Bemerkungszeile in der Einrichtung fett dargestellt, um die Änderung hervorzuheben, und in der Spalte **Vorlagennr.** wird die Nummer der Vorlage angezeigt, auf die die Änderung angewendet wird. Das Feld **Vorlagennr.** kann nicht bearbeitet werden kann. Es dient lediglich zu Informationszwecken.

6. Wählen Sie **Schließen**, wenn Sie fertig sind.

## So konfigurieren Sie Bemerkungen für alle Vorlagen in einem Mandanten

Um Bemerkungen für alle Vorlagen im aktuellen Mandanten zu konfigurieren, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Benachrichtigungscenter Einrichtung** ein, und wählen Sie dann den zugehörigen Link.

2. Klicken Sie in der Aktionsleiste auf **Liste bearbeiten**.

3. Wählen Sie in der Bemerkungsliste die Bemerkung, die Sie konfigurieren möchten. Konfigurieren Sie sie dann mit einem der folgenden Felder nach Bedarf:

   <br>

   | Feld                                 | Beschreibung                                                                                                                                                                                                                                                                                            |
   | ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | **Benutzerdefinierte Bemerkungsart** | Ermöglicht Ihnen, den Bemerkungstyp zu ändern. Sie können den Schweregrad einer Bemerkung erhöhen, indem Sie ihn beispielsweise von **Warnung** zu **Fehler** ändern. Eine Herabstufung von **Fehler** auf **Warnung** ist normalerweise nicht möglich. |
   | **Bei Fehler zuweisen**              | Hiermit können Sie festlegen, dass ein Beleg automatisch einem bestimmten Benutzer zugewiesen wird, wenn die ausgewählte Bemerkung in einem Beleg angezeigt wird, um das Problem zu lösen. Das Feld ist nur für **Fehler**-Bemerkungen auswählbar.                      |
   | **Benutzer ID zuweisen**             | Hiermit können Sie die ID des Benutzers angeben, dem Belege mit der ausgewählten Bemerkung zugewiesen werden sollen. Das Feld kann nur bearbeitet werden, wenn **Bei Fehler zuweisen** ausgewählt wurde.                                                                |

   <br>

4. Wiederholen Sie Schritt 3 für alle weiteren Bemerkungen, die Sie konfigurieren möchten.

> [!TIP]
> Sie können Bemerkungen für alle Vorlagen auch konfigurieren, indem Sie die Seite **Benachrichtigungscenter Einrichtung** direkt aus einer Bemerkung aufrufen: Suchen Sie im Bemerkungsbereich des Belegjournals eine konfigurierbare Bemerkung, und wählen Sie **Ja**, um die Seite **Benachrichtigungscenter Einrichtung** zu öffnen. Wählen Sie dann **Standard-Setup anzeigen** in der Aktionsleiste, um die allgemeine Einrichtungsseite zu öffnen. Alle Änderungen, die Sie hier vornehmen, werden dann auf alle Vorlagen im aktuellen Mandanten angewendet.