Mit Document Capture Version 8.00 und Expense Management Version 8.00 veröffentlicht Continia Software eine Upgrade-Anleitung, mit der unsere Partner Document Capture 7.00, Expense Management 7.00 oder ein System mit sowohl Document Capture 7.00 als auch Expense Management 7.00 aktualisieren können.

Diese Upgrade-Anleitung beschreibt das manuelle Upgrade von Document Capture and Expense Management auf die NAV-Version (NAV 3.70 bis BC14), die aktuell mit Document Capture and Expense Management verwendet wird.

Wenn Sie einen automatisierten Prozess suchen, finden Sie weitere Informationen unter [Automatisiertes Datenupgrade von Version 7.00 auf Version 8.00](../automated-data-upgrade). In diesem Dokument wird beschrieben, wie Sie Document Capture oder Expense Management mit den neuen Data Upgrade-Tools von Microsoft aktualisieren.

Wenn Sie Document Capture oder Expense Management in Microsoft Business Central Online verwenden, wird das Hauptupgrade automatisch durchgeführt, wenn Sie Document Capture 8.00 installieren (nach der Deinstallation von Document Capture 7.00).

Informationen zur Migration von der FOB-basierten Version von NAV/BC zur On-Premises-Erweiterung und/oder Online finden Sie unter [Upgrade von NAV/Business Central mit einer Installation von Document Capture](@DC-7) und [Document Capture von Business Central On-Premises zur Cloud migrieren](@DC-106).

Diese Upgrade-Anleitung kann mit den folgenden Versionen von Document Capture und Expense Management verwendet werden:

**Document Capture**

- Document Capture 7.00 mit einem beliebigen Service Pack.

**Expense Management**

- Expense Management 7.00 mit einem beliebigen Service Pack.

Wenn auf dem System eine ältere Version läuft, müssen Sie zunächst auf die erforderlichen Versionen aktualisieren.

In dieser Version haben wir die Client- und Serverkomponenten von Document Capture aktualisiert, die Sie aktualisieren müssen, bevor Sie mit der Arbeit mit Document Capture und Expense Management beginnen. Diese Anleitung hilft Ihnen bei der richtigen Ausführung. Die Document Capture- und Expense Management-Objekte in dieser Version sind nicht abwärtskompatibel mit älteren Komponenten, ebenso wie die in dieser Version enthaltenen Komponenten nicht abwärtskompatibel mit älteren Objekten sind.

Wenn Document Capture und Expense Management noch nicht in Ihrem System installiert wurden, sollten Sie keine Informationen in diesem Dokument verwenden.

## Aufgabe 1: Mindestversionsanforderungen prüfen

Stellen Sie sicher, dass auf Ihrem aktuellen System eine der unterstützten Versionen von Document Capture oder Expense Management ausgeführt wird, die im zusammenfassenden Abschnitt aufgeführt sind. Wenn nicht, ist es sehr wichtig, dass Sie der Upgrade-Anleitung von einer früheren Version auf DC7.00 und/oder EM7.00 folgen. Frühere Upgrade-Anleitungen finden Sie hier:

Für Document Capture: https://continia.zendesk.com/hc/en-us/sections/201853305-Upgrade-Guides

Für Expense Management: https://continia.zendesk.com/hc/da/sections/360000175700-Upgrade-Guides

## Aufgabe 2: Aktualisierte NAV-Lizenzdatei importieren

Der Upgrade-Vorgang muss mit einer Partnerentwicklerlizenz durchgeführt werden.

Achten Sie nach dem Upgrade darauf, eine neue/aktualisierte Kundenlizenzdatei von Microsoft zu verwenden und diese in NAV zu importieren.

Wenn Sie den Dynamics NAV-Server verwenden, müssen Sie den Dynamics NAV-Server neu starten, um die neue Lizenz zu verwenden.

## Aufgabe 3: Objekte zusammenführen

Wenn Sie das System Ihres Kunden geändert haben, prüfen Sie, ob die geänderten Objekte mit Document Capture- oder Expense Management-Objekten in Konflikt stehen, und führen Sie sie bei Bedarf zusammen. Sie sollten Objekte in einem Testsystem zusammenführen, damit sie für den späteren Import im Upgrade-Prozess bereit sind.

## Aufgabe 4: Pre-Upgradepaket prüfen

In Version 8.00 gibt es keinen Schritt vor dem Upgrade.

## Aufgabe 5: Alle Tools und Komponenten installieren

Sie müssen alle unten beschriebenen Installationen mit der ausführbaren Document Capture **Setup**-Datei durchführen, die sich im Stammverzeichnis des Produktordners (Setup.exe) befindet.

> [!NOTE]
> Das Installationsprogramm aktualisiert den Ordner **Add-ins** (Client und/oder Server) unter dem Standardinstallationspfad. Wenn Ihr Installationspfad also vom Standardpfad von Microsoft abweicht, müssen Sie den neuen Ordner **Add-ins** in den Ordner kopieren, in dem sich Ihre Installation befindet.

## Aufgabe 6: Serverkomponenten aktualisieren

Um Ihre Serverkomponenten zu aktualisieren, folgen Sie je nach Ihrer Version von NAV/Business Central einer der folgenden Anleitungen:

<br>

| Version                    | Anleitung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NAV Server 2009 -> 2009 R2 | Führen Sie die folgenden Schritte nur aus, wenn Sie Dynamics NAV 2009 -> 2009 R2 verwenden: <ol><li>Beenden Sie „Microsoft Dynamics NAV Server“. Richten Sie den manuellen Start ein.</li><li>Beenden Sie „Microsoft Dynamics NAV Business Web Services“, falls gestartet. Richten Sie den manuellen Start ein.</li><li>Starten Sie den Windows-Server neu.</li><li>Deinstallieren Sie „Document Capture RTC Server Components“.</li><li>Installieren Sie „Document Capture RTC Server Components“.</li><li>Wenn Sie den Microsoft Dynamics NAV Server nicht am Standardspeicherort installiert haben, Sie müssen die Add-ins manuell vom Standardspeicherort an den aktuellen Speicherort Ihrer Installation verschieben.</li><li>Starten Sie „Microsoft Dynamics NAV Server“. Richten Sie den automatischen Start ein.</li><li>Starten Sie „Microsoft Dynamics NAV Business Web Services“, falls erforderlich. Richten Sie den automatischen Start ein.</li></ol> |
| NAV Server 2013 -> BC14    | Führen Sie die folgenden Schritte nur aus, wenn Sie Dynamics NAV 2013 -> Microsoft Dynamics 365 Business Central Frühjahr 2019 Update (BC14) verwenden: <ol><li>Beenden Sie „Microsoft Dynamics NAV Server“.</li><li>Deinstallieren Sie „Document Capture RTC Server Components“.</li><li>Installieren Sie „Document Capture RTC Server Components“.</li><li>Wenn Sie den Microsoft Dynamics NAV Server nicht am Standardspeicherort installiert haben, Sie müssen die Add-ins manuell vom Standardspeicherort an den aktuellen Speicherort Ihrer Installation verschieben.</li><li>Starten Sie „Microsoft Dynamics NAV Server“.</li></ol>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NAV Classic Upgrade PC     | Führen Sie die folgenden Schritte nur aus, wenn Sie Dynamics NAV Classic verwenden: <ol><li>Auf dem Computer, auf dem Sie das Upgrade durchführen, müssen Sie die „Document Capture Classic Client Components“ und „Document Capture Classic Components (Scanner)“ deinstallieren.</li><li>Installieren Sie „Document Capture Classic Client Components“.</li><li>Installieren Sie „Document Capture Classic Components (Scanner)“, falls erforderlich.</li></ol>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| NAV RTC Upgrade PC         | Führen Sie die folgenden Schritte nur aus, wenn Sie Dynamics NAV RTC verwenden: <ol><li>Auf dem Computer, auf dem Sie das Upgrade durchführen, müssen Sie „Document Capture RTC Client“ und „Document Capture RTC Components (Scanner)“ deinstallieren.</li><li>Installieren Sie „Document Capture RTC Client“.</li><li>Installieren Sie „Document Capture RTC Component (Scanner)“, falls erforderlich.</li><li>Wenn Sie den Microsoft Dynamics NAV RTC Client nicht am Standardspeicherort installiert haben, Sie müssen die Add-ins manuell vom Standardspeicherort an den aktuellen Speicherort Ihrer Installation verschieben.</li></ol>                                                                                                                                                                                                                                                                                                                                                                                                                 |

## Aufgabe 7: NAV-Objekte und -Daten aktualisieren

> [!IMPORTANT]
> Bevor Sie Objektänderungen vornehmen oder mit der Datenaktualisierung beginnen, sichern Sie unbedingt die Datenbank.

Importieren Sie die neuen DC8.00/EM8.00-Objekte aus dem Produktordner.  Verwenden Sie **Alle ersetzen** im Import Worksheet. Bei einigen Objekten wird während des Imports möglicherweise eine Warnung angezeigt wird, da einige Teile der neuen Versionsliste ein geändertes Format aufweisen. Legen Sie für NAV 2015 und höher beim Objektimport das Synchronisierungsschema auf „Später“ fest.

> [!WARNING]
> Für alle Versionen von NAV 2013 bis Business Central Oktober 2018 (BC v13) gilt: Beim Importieren des DC8.00/EM8.00-Objektpakets überspringen Sie die vier unten genannten Seiten. Die Seiten waren unbeabsichtigt in den Release-Paketen enthalten, werden jedoch im Service Pack 1 entfernt.
>
> - Seite 5 **Währungen**
> - Seite 10 **Länder/Regionen**
> - Seite 209 **Maßeinheiten**
> - Seite 472 **MwSt.-Buchungsmatrix Einr.**

## Aufgabe 8: Nach dem Upgrade

Befolgen Sie die nachstehende Anleitung, um die Schritte nach dem Upgrade abzuschließen:

1. Importieren Sie das Objektpaket mit der folgenden Bezeichnung: “(Ihre NAV-Version) - Document Capture 8.00, Expense Management 8.00 - PostUpgrade.fob”. Verwenden Sie **Alle ersetzen** im Import Worksheet. Wenn Sie NAV 2015 oder eine neuere Version verwenden, setzen Sie „Schema synchronisieren“ beim Import auf „Später“.
2. Kompilieren Sie alle Document Capture- und Expense Management-Objekte (Versionslistenfilter \*DC\*|\*EM\*|\*CC\*|\*DN\*). Wenn Sie NAV 2015 oder eine neuere Version verwenden, setzen Sie „Schema synchronisieren“ auf „Später“. Einige Document Capture/Expense Management-Objekte werden nicht kompiliert; sie werden später im Upgrade-Prozess gelöscht.
3. Kompilieren Sie alle MenuSuites (nicht nur Document Capture und Expense Management).
4. Wenn Sie NAV 2015 oder eine neuere Version verwenden, wählen Sie **Tools** > \*\*Sync. Schema For All Tables“ -> **With Validation**.
5. Starten Sie den RTC-Client neu.
6. Führen Sie die Funktion **Daten auf neueste Version aktualisieren** von der **Document Capture Einrichtung**-Karte oder **Expense Management Einrichtung**-Karte in einem beliebigen Mandanten aus. Die Routine schließt alle Mandanten ein und aktualisiert bei Bedarf die Document Capture-Daten und die Expense Management-Daten.
7. Der Vorgang nach der Aktualisierung sollte ohne Fehler abgeschlossen werden.

## Aufgabe 9: Clientkomponenten aktualisieren

Um Ihre Clientkomponenten zu aktualisieren, folgen Sie je nach Ihrer Version von NAV/Business Central einer der folgenden Anleitungen:

<br>

| Version                      | Anleitung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NAV Classic Clients          | Führen Sie die folgenden Schritte nur aus, wenn Sie Dynamics NAV Classic verwenden: <ol><li>Deinstallieren Sie „Document Capture Classic Client Components“.</li><li>Deinstallieren Sie „Document Capture Classic Components (Scanner)“.</li><li>Installieren Sie „Document Capture Classic Client Components“.</li><li>Installieren Sie „Document Capture Classic Components (Scanner)“, falls erforderlich.</li></ol> |
| NAV RTC Clients 2009 -> 2016 | Führen Sie die folgenden Schritte nur aus, wenn Sie Dynamics NAV 2009 -> 2016 verwenden: <ol><li>Deinstallieren Sie „Document Capture RTC Client Components“.</li><li>Installieren Sie „Document Capture RTC Client Components“.</li></ol>                                                                                                                                                                                                                                                    |
| NAV RTC Clients 2017 -> BC14 | <ol><li>Deinstallieren Sie „Document Capture RTC Client“.</li><li>Deinstallieren Sie „Document Capture RTC Components (Scanner)“.</li><li>Client-Add-Ins werden jetzt bei Bedarf automatisch an alle NAV-Clients verteilt.</li></ol>                                                                                                                                                                                                                                                                                                          |

## Aufgabe 10: Upgrade-Objekte löschen

Nach Abschluss des Upgrades entfernen Sie die Upgrade-Objekte (alle Objekttypen, mit Force):

Filter: 6086100..6086199

> [!NOTE]
> Bei Versionen vor NAV 2015 müssen Upgrade-Tabellen vor dem Löschen manuell geleert werden.

## Aufgabe 11: Das Continia Web Approval Portal aktualisieren

Um das Continia Web Approval Portal zu aktualisieren, gehen Sie folgendermaßen vor:

1. Wenn Sie NAV-Objekte unter NAV 2009 R2 verwenden, müssen Sie die aktualisierten Web Approval Portal-Objekte aus dem Produktordner importieren. Für NAV 2009 R2 und spätere Versionen sind diese Objekte im Basispaket enthalten.
2. Kompilieren Sie alle Document Capture- und Expense Management-Objekte (Versionslistenfilter \*DC\*|\*EM\*|\*CC\*|\*DN\*).
3. Führen Sie die Funktion **Erzeuge Web Service** aus der Continia-Webportal-Liste aus. Diese Funktion muss nur in einem Mandanten ausgeführt werden.
4. Wenn Sie weiterhin das Continia Web Portal On-Premises verwenden, erstellen Sie eine neue Website in IIS oder aktualisieren Sie die vorhandene.
5. Führen Sie die Funktion „Benutzer exportieren“ aus, um Webbenutzer von der Continia-Benutzerseite in NAV zu exportieren.

## Informationen zum Thema

[Automatisiertes Datenupgrade von Version 7.00 auf Version 8.00](../automated-data-upgrade)

<style>
  .content table tr td:nth-child(1) {
    width: 130px;
  }
  .content table tr td:nth-child(2) {
    width: 600px;
  }  
</style>