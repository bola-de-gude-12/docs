Mit Document Capture Version 8.00 und Expense Management Version 8.00 veröffentlicht Continia Software eine kombinierte Upgrade-Anleitung, mit der unsere Partner Document Capture 7.00, Expense Management 7.00 oder ein System mit sowohl Document Capture 7.00 als auch Expense Management 7.00 aktualisieren können.

> [!IMPORTANT]
> Diese Upgrade-Anleitung kann nur mit den Versionen von Dynamics NAV verwendet werden, die die neuen Data Upgrade Tools von Microsoft unterstützen. (Microsoft Dynamics NAV 2016 und höher).

Diese Upgrade-Anleitung beschreibt das Upgrade von Document Capture and Expense Management mit dem automatisierten Datenupgrade auf die NAV-Version (NAV 2016 bis BC14), die aktuell mit Document Capture and Expense Management verwendet wird.

Wenn die Dynamics NAV-Version kein Datenupgrade unterstützt oder Sie nach dem manuellen Prozess vor und nach dem Upgrade suchen, finden Sie weitere Informationen unter [Manuelles Upgrade von Version 7.00 auf Version 8.00](@EM-30).

Wenn Sie Document Capture oder Expense Management in Microsoft Dynamics Business Central Cloud verwenden, wird das Hauptupgrade automatisch durchgeführt, wenn Sie Document Capture 8.00 installieren.

Migration von der FOB-basierten Version von NAV/BC zur On-Premises-Erweiterung und/oder Online finden Sie in [diesem Artikel in der Continia PartnerZone](https://continia.zendesk.com/hc/da/articles/360015942380-Overview-Migrating-from-BC14-FOB-based-to-BC15-or-newer-versions-On-Premises-and-or-Cloud-).

Diese Upgrade-Anleitung kann mit den folgenden Versionen von Document Capture und Expense Management verwendet werden:

**Document Capture**

- Document Capture 7.00 mit einem beliebigen Service Pack

**Expense Management**

- Expense Management 7.00 mit einem beliebigen Service Pack

Wenn auf dem System eine ältere Version läuft, müssen Sie zunächst auf die erforderlichen Versionen aktualisieren.

In dieser Version haben wir die Client- und Serverkomponenten von Document Capture aktualisiert, die Sie aktualisieren müssen, bevor Sie mit der Arbeit mit Document Capture und Expense Management beginnen. Diese Anleitung hilft Ihnen bei der richtigen Ausführung. Die Document Capture- und Expense Management-Objekte in dieser Version sind nicht abwärtskompatibel mit älteren Komponenten, ebenso wie die in dieser Version enthaltenen Komponenten nicht abwärtskompatibel mit älteren Objekten sind.

Wenn Document Capture und Expense Management noch nicht in Ihrem System installiert wurden, sollten Sie keine Informationen in diesem Dokument verwenden. Informationen zur Installation von Document Capture oder Expense Management finden Sie im Schnelleinstieg.

## Aufgabe 1: Mindestversionsanforderungen prüfen

Stellen Sie sicher, dass auf Ihrem aktuellen System eine der unterstützten Versionen von Document Capture oder Expense Management ausgeführt wird, die im zusammenfassenden Abschnitt aufgeführt sind. Wenn nicht, ist es sehr wichtig, dass Sie der Upgrade-Anleitung von einer früheren Version auf DC7.00 und/oder EM7.00 folgen. Frühere Upgrade-Anleitungen finden Sie hier:

Für Document Capture: https://continia.zendesk.com/hc/en-us/sections/201853305-Upgrade-Guides

Für Expense Management: https://continia.zendesk.com/hc/da/sections/360000175700-Upgrade-Guides

## Aufgabe 2: Aktualisierte NAV-Lizenzdatei importieren

Der Upgrade-Vorgang muss mit einer Entwicklerlizenz durchgeführt werden.

Achten Sie nach dem Upgrade darauf, eine neue oder aktualisierte Kundenlizenzdatei von Microsoft zu verwenden und diese in NAV zu importieren.

Wenn Sie den Dynamics NAV-Server verwenden, müssen Sie den Dynamics NAV-Server neu starten, um die neue Lizenz zu verwenden.

## Aufgabe 3: Objekte zusammenführen

Wenn Sie das System Ihres Kunden geändert haben, prüfen Sie, ob die geänderten Objekte mit Document Capture- oder Expense Management-Objekten in Konflikt stehen, und führen Sie sie bei Bedarf zusammen. Sie sollten Objekte in einem Testsystem zusammenführen, damit sie für den späteren Import im Upgrade-Prozess bereit sind.

## Aufgabe 4: Alle Tools und Komponenten installieren

Sie müssen alle unten beschriebenen Installationen mit der ausführbaren Document Capture **Setup**-Datei durchführen, die sich im Stammverzeichnis des Produktordners (Setup.exe) befindet.

> [!NOTE]
> Das Installationsprogramm aktualisiert den Ordner **Add-ins** (Client und/oder Server) unter dem Standardinstallationspfad. Wenn Ihr Installationspfad also vom Standardpfad von Microsoft abweicht, müssen Sie den neuen Ordner **Add-ins** in den Ordner kopieren, in dem sich Ihre Installation befindet.

## Aufgabe 5: Serverkomponenten aktualisieren

Um Ihre Serverkomponenten zu aktualisieren, folgen Sie je nach Ihrer Version von NAV/Business Central einer der folgenden Anleitungen:

<br>

| Version                 | Anleitung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NAV Server 2016 -> BC14 | Führen Sie die folgenden Schritte nur aus, wenn Sie Dynamics NAV 2016 -> Microsoft Dynamics 365 Business Central Frühjahr 2019 Update (BC14) verwenden: <ol><li>Beenden Sie &ldquo;Microsoft Dynamics NAV Server&rdquo;.</li><li>Deinstallieren Sie „Document Capture RTC Server Components“.</li><li>Installieren Sie „Document Capture RTC Server Components“.</li><li>Wenn Sie den Microsoft Dynamics NAV Server nicht am Standardspeicherort installiert haben, Sie müssen die Add-ins manuell vom Standardspeicherort an den aktuellen Speicherort Ihrer Installation verschieben.</li><li>Starten Sie „Microsoft Dynamics NAV Server“.</li></ol> |
| NAV RTC Upgrade PC      | Führen Sie die folgenden Schritte nur aus, wenn Sie Dynamics NAV RTC verwenden: <ol><li>Auf dem Computer, auf dem Sie das Upgrade durchführen, müssen Sie „Document Capture RTC Client“ und „Document Capture RTC Components (Scanner)“ deinstallieren.</li><li>Installieren Sie „Document Capture RTC Client“.</li><li>Installieren Sie „Document Capture RTC Component (Scanner)“, falls erforderlich.</li><li>Wenn Sie den Microsoft Dynamics NAV RTC Client nicht am Standardspeicherort installiert haben, Sie müssen die Add-ins manuell vom Standardspeicherort an den aktuellen Speicherort Ihrer Installation verschieben.</li></ol>                                               |

## Aufgabe 6: NAV-Objekte und -Daten aktualisieren

> [!IMPORTANT]
> Bevor Sie Objektänderungen vornehmen oder mit der Datenaktualisierung beginnen, sichern Sie unbedingt die Datenbank.

Importieren Sie die neuen DC8.00/EM8.00-Objekte aus dem Produktordner. Beachten Sie, dass bei einigen Objekten während des Imports möglicherweise eine Warnung angezeigt wird, da einige Teile der neuen Versionsliste ein geändertes Format aufweisen. Verwenden Sie **Alle ersetzen** im Import Worksheet. Stellen Sie die Schemasynchronisierung beim Objektimport auf **Später** ein.

> [!WARNING]
> Für alle Versionen von NAV 2013 bis Business Central Oktober 2018 (BC v13) gilt: Beim Importieren des DC8.00/EM8.00-Objektpakets überspringen Sie die vier unten genannten Seiten. Die Seiten waren unbeabsichtigt in den Release-Paketen enthalten, werden jedoch im Service Pack 1 entfernt.
>
> - Seite 5 **Währungen**
> - Seite 10 **Länder/Regionen**
> - Seite 209 **Maßeinheiten**
> - Seite 472 **MwSt.-Buchungsmatrix Einr.**

## Aufgabe 7: Datenaktualisierung

Befolgen Sie die nachstehende Anleitung, um die Schritte nach dem Upgrade abzuschließen:

1. Importieren Sie das Objektpaket mit der folgenden Bezeichnung: “(Ihre NAV-Version) - Document Capture 8.00, Expense Management 8.00 - DataUpgrade.fob”. Verwenden Sie **Alle ersetzen** im Import Worksheet. Stellen Sie die Schemasynchronisierung beim Import auf **Später** ein.
2. Kompilieren Sie alle Document Capture- und Expense Management-Objekte (Versionslistenfilter \*DC\*|\*EM\*|\*CC\*|\*DN\*). Stellen Sie die Schemasynchronisierung auf **Später** ein.
3. Kompilieren Sie alle MenuSuites (nicht nur DC und EM).
4. Wählen Sie Tools -> „Sync. Schema For All Tables“ -> **With Validation**.
5. Wählen Sie Tools -> „Data Upgrade“ -> „Start…“, um die Seite **Start Data Upgrade** zu öffnen.
6. Wählen Sie unter **Execution Mode** die Option **Serial** aus und deaktivieren Sie anschließend das Kontrollkästchen unter **Continue on Error**. Wählen Sie **OK**, um die Seite zu schließen.

Die Datenaktualisierung sollte ohne Fehler abgeschlossen werden.

### Problembehandlung beim Datenupgrade

1. Falls das Datenupgrade fehlschlägt, müssen Sie den Powershell-Befehl Get-NAVDataUpgrade [ServerInstance] -ErrorOnly ausführen, um den eigentlichen Fehler herauszufinden, oder den Debugger mit „Debug Next“ verwenden.
2. Bei einer Fehlermeldung wie “Function 'UpdatePerDatabase' in the upgrade codeunit '6086102' has failed because of the following error: 'A call to System.Net.WebClient.DownloadData failed with this message: The remote server returned an error: (404) Not Found.'.” liegt ein Problem beim Herunterladen der Control Add-in-Ressourcen vor. Dieses Problem kann auftreten, wenn unsere Services ausgefallen sind, oder es könnte ein Problem mit der Server-Firewall sein.
3. Sie können es erneut versuchen, indem Sie Tools ausführen -> “Data Upgrade” -> “Resume…”.
4. Wenn derselbe Fehler auftritt, können Sie Codeunit 6086102 erstellen und die folgende Codezeile auskommentieren:  CODEUNIT.RUN(CODEUNIT::"CDC Capture RTC Library");
5. Führen Sie dann Tools -> “Data Upgrade” -> “Resume…” aus.
6. Dadurch wird das Herunterladen des Control-Add-Ins beim Upgrade übersprungen. Daher müssen Sie es nach der Datenaktualisierung von der Document Capture Einrichtung-Seite manuell herunterladen: Wählen Sie auf der Registerkarte **Aktionen** die Optionen **Continia Web Client-Add-Ins importieren** und **Client-Add-Ins importieren** aus, um alle relevanten Add-Ins zu importieren.

## Aufgabe 8: Clientkomponenten aktualisieren

Um Ihre Clientkomponenten zu aktualisieren, folgen Sie je nach Ihrer Version von NAV/Business Central einer der folgenden Anleitungen:

<br>

| Version                      | Anleitung                                                                                                                                                                                                                                                                          |
| ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NAV RTC Clients 2016         | Führen Sie die folgenden Schritte nur aus, wenn Sie Dynamics NAV 2016 verwenden: <ol><li>Deinstallieren Sie „Document Capture RTC Client Components“.</li><li>Installieren Sie „Document Capture RTC Client Components“.</li></ol> |
| NAV RTC Clients 2017 -> BC14 | <ol><li>Deinstallieren Sie „Document Capture RTC Client“.</li><li>Deinstallieren Sie „Document Capture RTC Components (Scanner)“.</li><li>Client-Add-Ins werden jetzt bei Bedarf automatisch an alle NAV-Clients verteilt.</li></ol>                                               |

## Aufgabe 9: Upgrade-Objekte löschen

Nach Abschluss des Upgrades entfernen Sie bitte die Upgrade-Objekte (alle Objekttypen, mit Force):

Filter: 6086100..6086199

> [!NOTE]
> Bei Versionen vor NAV 2015 müssen Upgrade-Tabellen vor dem Löschen manuell geleert werden.

## Aufgabe 10: Das Continia Web Approval Portal aktualisieren

Um das Continia Web Approval Portal zu aktualisieren, gehen Sie folgendermaßen vor:

1. Wenn Sie NAV-Objekte unter NAV 2009 R2 verwenden, müssen Sie die aktualisierten Web Approval Portal-Objekte aus dem Produktordner importieren. Für NAV 2009 R2 und spätere Versionen sind diese Objekte im Basispaket enthalten.
2. Kompilieren Sie alle Document Capture- und Expense Management-Objekte (Versionslistenfilter \*DC\*|\*EM\*|\*CC\*|\*DN\*).
3. Führen Sie die Funktion **Erzeuge Web Service** aus der Continia-Webportal-Liste aus. Diese Funktion muss nur in einem Mandanten ausgeführt werden.
4. Wenn Sie weiterhin das Continia Web Portal On-Premises verwenden, erstellen Sie eine neue Website in IIS oder aktualisieren Sie die vorhandene.
5. Führen Sie die Funktion „Benutzer exportieren“ aus, um Webbenutzer von der Continia-Benutzerseite in NAV zu exportieren.

## Informationen zum Thema

[Manuelles Upgrade von Version 7.00 auf Version 8.00](@EM-30)

<style>
  .content table tr td:nth-child(1) {
    width: 130px;
  }
  .content table tr td:nth-child(2) {
    width: 600px;
  }  
</style>