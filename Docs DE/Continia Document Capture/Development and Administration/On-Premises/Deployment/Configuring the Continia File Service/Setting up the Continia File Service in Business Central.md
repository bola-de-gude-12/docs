---
title: Den Continia File Service in Business Central einrichten
date: 07-08-2023
description:
id: DC-126
lang: de
---

# Den Continia File Service in Business Central einrichten

Wenn Sie für den Continia File Service [ein Repository und einen Autorisierungsschlüssel eingerichtet haben](@DC-125), müssen Sie den Dienst in Microsoft Dynamics 365 Business Central konfigurieren. Hierfür gibt es zwei Möglichkeiten:

- Für die [Standardkonfiguration](#standard-configuration), verwenden Sie den Konfigurationsassistenten.
- Für [erweiterte Einrichtungsoptionen](#advanced-setup) verwenden Sie die **Document Capture Einrichtung**.

Beide Methoden werden in den Abschnitten unten ausführlicher beschrieben.

> [!IMPORTANT]
> Die Details, die Sie im Konfigurationstool [bei der Konfiguration des Continia File Service](@DC-125) eingegeben haben, müssen bei der Einrichtung des Dienstes in Business Central wiederverwendet werden. Achten Sie daher darauf, dass Sie dieselben Details verwenden, wenn Sie den Anleitungen unten folgen.

> [!NOTE]
> Wenn Sie vom Dateisystem zum File Service migrieren, ändert sich der tatsächliche Speicherort der Dateien normalerweise nicht. Nur die Art und Weise, wie auf die Dateien zugegriffen wird, ändert sich. Aus diesem Grund verschiebt Continia Document Capture bei einer Migration zum Dateidienst keine Dateien automatisch. Wenn Dateien verschoben werden müssen, müssen Sie dies manuell durchführen.

## Standardkonfiguration

Um den Continia File Service in Business Central mithilfe des Konfigurationsassistenten zu konfigurieren, führen Sie die folgenden Schritte aus:

1. Wählen Sie das Symbol {{search}}, geben Sie **Speichermigrationsassistent** ein, und wählen Sie dann den zugehörigen Link.
2. Folgen Sie den Anweisungen auf dem Bildschirm.
3. Wenn Sie fertig sind, wählen Sie **Beenden**, um den Assistenten zu schließen und Ihre Einstellungen zu übernehmen.

Der Continia File Service ist jetzt vollständig konfiguriert und kann als Ihr standardmäßiger Dokumentspeichertyp verwendet werden.

## Erweiterte Einrichtung

Um den Continia File Service in Business Central mithilfe der **Document Capture Einrichtung** für erweiterte Einstellungen zu konfigurieren, führen Sie diese Schritte aus:

1. Suchen Sie ({{search}}) nach **Document Capture Einrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie im Inforegister **Allgemein** unter **Dokumentspeichertyp** die Option **File Service** aus.
3. Ein Dialogfeld wird angezeigt, in dem Sie gefragt werden, ob Sie Ihre Dateien zum **File Service** migrieren möchten. Wählen Sie **Ja**, um zu bestätigen und das Dialogfeld zu schließen. Die Seite **Speichereinstellungen aktualisieren – File Service** wird geöffnet.
4. Füllen Sie die Felder **Server**, **Server-Port**, **Repository** und **Autorisierungsschlüssel** aus und ändern Sie bei Bedarf die Pfade und die **Datei Verzeichnisstruktur**.
   > [!IMPORTANT]
   > Ihre Einträge für **Server Port**, **Repository** und **Autorisierungsschlüssel** müssen mit den entsprechenden Einträgen identisch sein, die Sie im Konfigurationstool hinzugefügt haben [als Sie den Continia File Service konfiguriert haben](@DC-125). Außerdem müssen die Pfade dem Stammordner entsprechen, den Sie im Konfigurationstool angegeben haben.
5. **Optional**: Wenn Ihre Serverkonfiguration eine sichere Verbindung mithilfe von Kryptografie, SSL oder ähnlichem erfordert, aktivieren Sie **Sichere Verbindung verwenden**.
6. **Optional**: Um die Einrichtung zu überprüfen, wählen Sie die drei Punkte oben und dann **Verbindung testen** aus. Ein Dialogfeld mit Verbindungsdetails wird angezeigt. Wählen Sie **OK**, um es zu schließen.
7. Wählen Sie auf der Seite **Speichereinstellungen aktualisieren – File Service** **OK** aus, um fortzufahren.
8. Befolgen Sie die Anweisungen auf dem Bildschirm, um die Einrichtung abzuschließen.

Der Continia File Service ist jetzt vollständig konfiguriert und kann als Ihr standardmäßiger Dokumentspeichertyp verwendet werden.