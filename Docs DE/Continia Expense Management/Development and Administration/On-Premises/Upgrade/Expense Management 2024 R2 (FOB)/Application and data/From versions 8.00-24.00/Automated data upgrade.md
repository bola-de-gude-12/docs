---
title: Automatisiertes Datenupgrade von Versionen 8.00–24.00 auf Version 25.00
date: 13-03-2025
description:
lang: de
---

# Automatisiertes Datenupgrade von Versionen 8.00–24.00 auf Version 25.00

Mit Document Capture Version 25.00 und Expense Management Version 25.00 veröffentlicht Continia Software eine kombinierte Upgrade-Anleitung, mit dem unsere Partner Document Capture 8.00–24.00, Expense Management 8.00–24.00 oder ein System mit sowohl Document Capture 8.00–24.00 als auch Expense Management 8.00–24.00 aktualisieren können.

In dieser Upgrade-Anleitung wird das Upgrade von Document Capture und Expense Management mit dem automatisierten Datenupgrade auf BC14 beschrieben.

Informationen zum manuellen Pre- und Post-Upgrade-Prozess finden Sie unter [Manuelles Upgrade von Versionen 8.00–24.00 auf Version 25.00](@EM-263).

Wenn Sie Document Capture oder Expense Management in Microsoft Business Central Cloud verwenden, wird das Hauptupgrade automatisch durchgeführt, wenn Sie Document Capture 25.00 und/oder Expense Management 25.00 installieren.

Informationen zur Migration von der FOB-basierten Version von NAV/BC zur On-Premises-Erweiterung und/oder Cloud finden Sie unter [Upgrade von NAV/Business Central mit einer Installation von Expense Management](@EM-107) und [Expense Management von Business Central On-Premises zur Cloud migrieren](@EM-112).

Diese Upgrade-Anleitung kann mit den folgenden Versionen von Document Capture und Expense Management verwendet werden:

**Document Capture**

- Document Capture 8.00 mit einem beliebigen Service Pack
- Document Capture 9.00 mit einem beliebigen Service Pack
- Document Capture 10.00 mit einem beliebigen Service Pack
- Document Capture 11.00 mit einem beliebigen Service Pack
- Document Capture 12.00 mit einem beliebigen Service Pack
- Document Capture 24.00 mit einem beliebigen Service Pack

**Expense Management**

- Expense Management 8.00 mit einem beliebigen Service Pack
- Expense Management 9.00 mit einem beliebigen Service Pack
- Expense Management 10.00 mit einem beliebigen Service Pack
- Expense Management 11.00 mit einem beliebigen Service Pack
- Expense Management 12.00 mit einem beliebigen Service Pack
- Expense Management 24.00 mit einem beliebigen Service Pack

Wenn auf dem System eine ältere Version läuft, müssen Sie zunächst auf die erforderlichen Versionen aktualisieren (8.00).

In dieser Version haben wir die Client- und Serverkomponenten von Document Capture aktualisiert, die Sie aktualisieren müssen, bevor Sie mit der Arbeit mit Document Capture und Expense Management beginnen. Diese Anleitung hilft Ihnen bei der richtigen Ausführung. Die Document Capture- und Expense Management-Objekte in dieser Version sind nicht abwärtskompatibel mit älteren Komponenten, ebenso wie die in dieser Version enthaltenen Komponenten nicht abwärtskompatibel mit älteren Objekten sind.

Wenn Document Capture und Expense Management noch nicht in Ihrem System installiert wurden, sollten Sie keine Informationen in diesem Dokument verwenden.

## Voraussetzungen

Document Capture 2024 R2 (25.00) und Expense Management 2024 R2 (25.00) sind nur verfügbar, wenn Sie eine der folgenden Versionen von Business Central verwenden:

- Business Central 2024 Release Wave 2 (BC v25)
- Business Central 2024 Release Wave 1 (BC v24)
- Business Central 2023 Release Wave 2 (BC v23)
- Business Central April 2019 (v14, FOB-basiert)
  Dies bedeutet, dass Kunden, die ältere NAV/BC-Versionen verwenden, nicht auf DC25.00/EM25.00 aktualisieren können. Stattdessen müssen sie auf DC8.00 aktualisieren, da diese Version weiterhin mit Service Packs unterstützt wird

## Aufgabe 1: Mindestversionsanforderungen prüfen

Stellen Sie sicher, dass auf Ihrem aktuellen System eine der unterstützten Versionen von Document Capture oder Expense Management ausgeführt wird, die im zusammenfassenden Abschnitt aufgeführt sind. Falls dies nicht der Fall ist, _müssen Sie der Upgrade-Anleitung von einer früheren Version_ auf DC8.00–24.00 und/oder EM8.00–24.00 folgen. Sie finden frühere Upgrade-Anleitungen unter [Unterstützte Upgradepfade für Continia Document Capture (FOB)](@DC-8) und [Supported Upgrade Paths for Continia Expense Management (FOB)](@EM-103).

## Aufgabe 2: Eine aktualisierte Business Central-Lizenzdatei importieren

Sie müssen eine Partnerentwicklerlizenz verwenden, um den Upgrade-Prozess durchzuführen. Achten Sie nach dem Upgrade darauf, eine neue oder aktualisierte Kundenlizenzdatei von Microsoft zu verwenden. Um die neue Lizenz zu verwenden, starten Sie den Business Central Server neu.

## Aufgabe 3: Objekte zusammenführen

Wenn Sie das System Ihres Kunden geändert haben, prüfen Sie, ob die geänderten Objekte mit Document Capture- oder Expense Management-Objekten in Konflikt stehen, und führen Sie sie bei Bedarf zusammen. Sie sollten Objekte in einem Testsystem zusammenführen, damit sie für den späteren Import im Upgrade-Prozess bereit sind.

## Aufgabe 4: Serverkomponenten aktualisieren

Sie müssen alle unten beschriebenen Installationen mit der ausführbaren Datei **Setup** durchführen, die sich im Stammverzeichnis des Produktordners (Setup.exe) befindet.

> [!NOTE]
> Das Installationsprogramm aktualisiert den Ordner **Add-ins** (Client und/oder Server) unter dem Standardinstallationspfad. Wenn Ihr Installationspfad also vom Standardpfad von Microsoft abweicht, müssen Sie den neuen Ordner **Add-ins** in den Ordner kopieren, in dem sich Ihre Installation befindet.

Um Ihre Serverkomponenten zu aktualisieren, verwenden Sie die folgende Anleitung:

| Version | Anleitung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BC14    | Führen Sie diese Schritte nur aus, wenn Sie Business Central April 2019 (BC14) verwenden: <ol><li>Beenden Sie „Business Central Server Server“.</li><li>Deinstallieren Sie „Document Capture RTC Server Components“.</li><li>Installieren Sie „Document Capture RTC Server Components“.</li><li>Wenn Sie den Microsoft Business Central Server nicht am standardmäßigen Speicherort installiert haben, müssen Sie die Add-ins manuell vom standardmäßigen Speicherort zum aktuellen Speicherort Ihrer Installation verschieben.</li><li>Starten Sie „Microsoft Business Central Server“.</li></ol> |

## Aufgabe 5: Business Central-Objekte und -Daten aktualisieren

> [!IMPORTANT]
> Bevor Sie Objektänderungen vornehmen oder mit der Datenaktualisierung beginnen, sichern Sie die Datenbank.

Importieren Sie die neuen DC25.00/EM25.00-Objekte aus dem Produktordner. Bei einigen Objekten wird während des Imports möglicherweise eine Warnung angezeigt wird, da einige Teile der neuen Versionsliste ein geändertes Format aufweisen. Verwenden Sie **Alle ersetzen** im Import Worksheet. Stellen Sie die Schemasynchronisierung beim Objektimport auf **Später** ein.

## Aufgabe 6: Datenaktualisierung

So führen Sie den Schritt nach dem Upgrade aus:

1. Importieren Sie das Objektpaket mit dem Namen “BC14 - DC8.00-D24.00 to DC25.00, EM8.00-EM24.00 to EM25.00 – Direct Upgrade Post”. Verwenden Sie **Alle ersetzen** im Import Worksheet. Stellen Sie die Schemasynchronisierung beim Import auf **Später** ein.

2. Kompilieren Sie alle Document Capture- und Expense Management-Objekte (Versionslistenfilter\*DC\*|\*EM\*|\*CC\*|\*DN\*|\*BF\*|\*CA\*). Stellen Sie die Schemasynchronisierung auf **Später** ein.

3. Wenn Sie MS Dynamics NAV 2019 Frühjahr oder früher verwenden, aktualisieren Sie die Workflow-Vorlagen. In der aktuellen Version wurden die Workflow-Vorlagen aktualisiert und müssen in jedem Mandanten manuell aktualisiert werden. Gehen Sie hierzu wie folgt vor:

  - Deaktivieren Sie die aktuellen Workflows, die mit Expense Management verknüpft sind (sie haben das Präfix CEM).
  - Führen Sie die Codeunit 6086372 – CEM-Workflow-Setup manuell aus, wodurch neue Workflow-Vorlagen generiert werden.
  - Erstellen Sie aus jeder dieser Vorlagen neue Workflows. Denken Sie daran, die Workflows nach ihrer Erstellung zu aktivieren

4. Kompilieren Sie alle MenuSuites (nicht nur Document Capture und Expense Management).

5. Wählen Sie Tools -> „Sync. Schema For All Tables“ -> **With Validation**.

6. Wählen Sie Tools -> „Data Upgrade“ -> „Start…“, um die Seite **Start Data Upgrade** zu öffnen.

7. Wählen Sie unter **Execution Mode** die Option **Serial** aus und deaktivieren Sie anschließend das Kontrollkästchen unter **Continue on Error**. Wählen Sie **OK**, um die Seite zu schließen.

Die Datenaktualisierung sollte ohne Fehler abgeschlossen werden.

### Problembehandlung beim Datenupgrade

1. Falls das Datenupgrade fehlschlägt, müssen Sie den Powershell-Befehl Get-NAVDataUpgrade [ServerInstance] -ErrorOnly ausführen, um den eigentlichen Fehler herauszufinden, oder den Debugger mit „Debug Next“ verwenden.
2. Bei der Fehlermeldung „Function 'UpdatePerDatabase' in the upgrade codeunit '6086106' has failed because of the following error: 'A call to System.Net.WebClient.DownloadData failed with this message: The remote server returned an error: (404) Not Found.“ liegt ein Problem beim Herunterladen der Control Add-in-Ressourcen vor. Dieses Problem kann auftreten, wenn unsere Services ausgefallen sind, oder es könnte ein Problem mit der Server-Firewall sein.
3. Sie können es erneut versuchen, indem Sie Tools ausführen -> “Data Upgrade” -> “Resume…”.
4. Wenn derselbe Fehler auftritt, können Sie Codeunit 6086106 erstellen und die folgende Codezeile auskommentieren: CODEUNIT.RUN(CODEUNIT::"CDC Capture RTC Library");
5. Führen Sie dann Tools -> “Data Upgrade” -> “Resume…” aus.
6. Dadurch wird das Herunterladen des Control-Add-Ins beim Upgrade übersprungen. Daher müssen Sie es nach der Datenaktualisierung von der Document Capture Einrichtung-Seite manuell herunterladen: Wählen Sie auf der Registerkarte **Aktionen** die Optionen **Continia Web Client-Add-Ins importieren** und **Client-Add-Ins importieren** aus, um alle relevanten Add-Ins zu importieren.

## Aufgabe 7: Clientkomponenten aktualisieren

Um Ihre Clientkomponenten zu aktualisieren, verwenden Sie die folgende Anleitung:

| Version | Anleitung                                                                                                                                                                                                                                   |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BC14    | <ol><li>Deinstallieren Sie „Document Capture RTC Client“.</li><li>Deinstallieren Sie „Document Capture RTC Components (Scanner)“.</li><li>Client-Add-ins werden jetzt automatisch an alle BC Clients verteilt, wenn erforderlich.</li></ol> |

## Aufgabe 8: Nicht verwendete Anwendungs- und Upgradeobjekte löschen

Nach dem Upgrade der Clientkomponenten sollten Sie sicherstellen, dass alle Objekte kompiliert werden und das Upgrade nicht versehentlich erneut gestartet wird.

So löschen Sie nicht verwendete Anwendungs- und Upgradeobjekte:

1. Entfernen Sie die Upgrade-Objekte (Alle Objekttypen, mit Force):
  Filter: 6086100..6086199
2. Nach dem Löschen der Upgrade-Objekte importieren Sie die Upgrade-Platzhalterobjekte aus der Fob-Datei, die die neuen Document Capture/Expense Management-Objekte enthält. Importieren Sie nur die Objekte im ID-Bereich: 6086100..6086199

## Aufgabe 9: Das Continia Web Approval Portal aktualisieren

So aktualisieren Sie das Continia Web Approval Portal:

1. Kompilieren Sie alle Document Capture- und Expense Management-Objekte (Versionslistenfilter\*DC\*|\*EM\*|\*CC\*|\*DN\*|\*BF\*|\*CA\*).
2. Führen Sie die Funktion **Erzeuge Web Service** aus der Continia-Webportal-Liste aus. Diese Funktion muss nur in einem Mandanten ausgeführt werden.
3. Wenn Sie weiterhin das Continia Web Portal On-Premises verwenden, erstellen Sie eine neue Website in IIS oder aktualisieren Sie die vorhandene.
4. Führen Sie die Funktion „Benutzer exportieren“ aus, um Webbenutzer von der Continia-Benutzerseite in BC zu exportieren.

<style>
  .content table tr td:nth-child(1) {
    width: 130px;
  }
  .content table tr td:nth-child(2) {
    width: 600px;
  }  
</style>