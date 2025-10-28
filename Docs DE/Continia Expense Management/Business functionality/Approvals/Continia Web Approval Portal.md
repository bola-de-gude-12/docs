---
title: Continia Web Approval Portal für Expense Management
date: 01-11-2024
description: Eine Beschreibung des Continia Web Approval Portals und seiner Verwendung zur Verarbeitung von Ausgaben.
id: EM-34
lang: de
---

# Continia Web Approval Portal

Das Continia Web Approval Portal ermöglicht die Genehmigung von Einkaufsdokumenten, Ausgaben und Verkaufsdokumenten in allen Mandanten, auf die Sie Zugriff haben. Im Web Approval Portal stehen zwei Ansichten zur Verfügung: klassisch und mandantenübergreifend. Genehmiger mit Zugriff auf mehrere Mandanten können alle relevanten Ausgaben an einem Ort anzeigen. Sie können nach Mandant oder Dokumenttyp filtern und so Genehmigungen effizient priorisieren, ohne zwischen Mandanten wechseln zu müssen, was wertvolle Zeit spart.

Im oberen blauen Menüband des Portals finden Sie Registerkarten für **Einkauf**, **Expense Management**, **Verträge** und **Verkauf**, sofern Sie die erforderlichen Module aktiviert haben. In diesem Artikel geht es um die Registerkarte **Belege** und die Genehmigung von Ausgaben.

> [!NOTE]
> Informationen zum Einrichten des Web Approval Portals und zum Konfigurieren von Benutzern finden Sie unter [Web-Genehmigung einrichten](@EM-52). Benutzer müssen außerdem [als Genehmiger eingerichtet sein](@EM-53), um das Portal verwenden zu können.

## Die verfügbaren Ansichten

Auf den Registerkarten im blauen Menüband wird angezeigt, wie viele Dokumente jeweils auf den entsprechenden Registerkarten zur Genehmigung ausstehen. Die grünen Optionen in den Untermenüs (zum Beispiel **Belege**, **Fahrstrecken**, **Pauschalen** und **Abrechnungen** im Menü **Expense Management**) zeigen die Anzahl der zu genehmigenden Belege für den jeweiligen Dokumenttyp an. Diese Anzahl wird auch im Mandantenübersichtsmenü oben rechts wiedergegeben. Dort sehen Sie die Gesamtanzahl der ausstehenden Dokumente für jeden Mandanten und wie sich diese auf die einzelnen Kategorien aufteilen.

Die Seite **Meine offenen Genehmigungen** ist die wichtigste Seite im Abschnitt **Genehmigungen** und bietet ein mandantenübergreifendes Dashboard, das alle Ausgaben anzeigt, die auf Ihre Genehmigung warten. Auf dieser Seite können Sie allgemeine Genehmigungsaktionen durchführen. Um auf andere Übersichtsseiten zuzugreifen, klicken Sie auf **Meine offenen Genehmigungen**, um ein Dropdown-Menü mit den folgenden Optionen zu öffnen:

| <div style="width:150px">Option</div> | Beschreibung                                                                                                                                                                     |
| ------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Systemansicht                         | Gruppiert alle Übersichtsseiten für die Ausgabengenehmigung.                                                                                                     |
| Genehmigungen in Vorbereitung         | Listet Ausgaben auf, denen Sie als Genehmiger zugewiesen sind, jedoch nicht als erster Genehmiger im Ablauf. Hier sind keine Aktionen verfügbar. |
| Meine offenen Genehmigungen           | Zeigt alle Ausgaben an, die auf Ihre Genehmigung warten, sodass Sie Dokumente genehmigen, ablehnen, weiterleiten oder zurückstellen können.                      |
| Meine bearbeiteten Genehmigungen      | Zeigt zuvor genehmigte oder abgelehnte Ausgaben an. Auf dieser Seite sind keine Genehmigungsaktionen verfügbar.                                  |

> [!TIP]
> Durch Klicken auf das Home-Symbol oder den Text **Continia Web Approval Portal** oben links im blauen Menüband können Sie jederzeit schnell zur Seite **Meine offenen Genehmigungen** zurückkehren.

## Filtern und Navigieren

Die meisten Übersichtsseiten enthalten dieselben Genehmigungsaktionen, wie zum Beispiel Genehmigen, Ablehnen, Weiterleiten, auf Abwarten setzen (und genehmigen), und Sie können darauf mehr Details über die einzelnen Ausgaben anzeigen und zusätzliche Genehmigungsaktionen ausführen.

Um die Anzahl der Genehmigungsposten pro Seite einzugrenzen, filtern Sie mit **Typ auswählen** nach dem Dokumenttyp oder mit **Mandanten auswählen** nach dem Mandanten. Das Portal zeigt an, wie viele Posten pro Belegart und Mandant vorhanden sind.

Durch Auswahl einer bestimmten Dokumentenart oder eines Mandanten aus dem Menü werden die entsprechenden Ausgaben zur Genehmigung geöffnet. Sie können auch auf den Mandantennamen klicken, um die Ausgaben mit der höchsten Priorität und ausstehender Genehmigung anzuzeigen.

## So arbeiten Sie mit offenen Genehmigungen

Die Aktionsleiste der Seite **Meine offenen Genehmigungen** enthält die folgenden Genehmigungsaktionen: Genehmigen, Ablehnen, Weiterleiten, Auf Abwarten setzen und Genehmigen und auf Abwarten setzen. Diese Aktionen ermöglichen Ihnen es, Ausgaben direkt von der Startseite aus zu bearbeiten. In der Liste der Genehmigungsposten finden Sie die wichtigsten Details aller Dokumente, die zur Genehmigung anstehen. Dazu gehören zum Beispiel die Dokumentnummer, der Kreditorenname, die aktuellsten Genehmigungskommentare und die Gesamtbeträge der Dokumente. Darüber hinaus können Sie in der Spalte **Aktionen** die Original-PDF- oder XML-Datei anzeigen oder herunterladen.

So können Sie die gewünschte Genehmigungsaktion im Web Approval Portal durchführen:

1. Wählen Sie in der Liste den gewünschten Genehmigungsposten ganz links in der Spalte mit dem Häkchen in der Kopfzeile aus. Dadurch wird der gesamte Eintrag hervorgehoben.
2. Wählen Sie in der Aktionsleiste die Aktion aus, die Sie für den ausgewählten Eintrag ausführen möchten.
3. Sie haben die folgenden Optionen:
   1. Wenn Sie **Ablehnen**, **Auf Abwarten setzen und genehmigen** oder **Auf Abwarten setzen** auswählen, wird ein Dialogfeld geöffnet. Wählen Sie einen Ursachencode aus (falls solche Codes eingerichtet wurden), fügen Sie einen Freitextkommentar hinzu, und wählen Sie dann **Weiter**, um die Aktion zu bestätigen.
   2. Wenn Sie **Weiterleiten** wählen, öffnet sich ein anderes Dialogfeld. Wählen Sie den Namen des Benutzers aus, an den Sie die Genehmigungsanforderung weiterleiten möchten, oder geben Sie ihn ein, und wählen Sie dann die gewünschte Weiterleitungsaktion aus. Wenn erforderlich, fügen Sie unten einen Freitextkommentar hinzu und wählen Sie dann **Weiter**, um die Aktion zu bestätigen.

> [!TIP]
> Sie können in der Liste der Genehmigungsposten mehrere Einträge gleichzeitig auswählen, um Genehmigungsaktionen für alle ausgewählten Einträge auf einmal durchzuführen. Wenn Sie alle Einträge auf einmal auswählen möchten, wählen Sie das Kontrollkästchen ganz links in der Kopfzeile aus. Mit diesem Häkchen können Sie außerdem die Auswahl aller Einträge aufheben.
