---
title: Manuelles Upgrade von Versionen 8.00–24.00 auf Version 25.00
date: 22-04-2025
description: Eine Anleitung zum direkten Upgrade der Versionen 8.00–24.00 auf Version 25.00.
lang: de
---

# Manuelles Upgrade von Versionen 8.00–24.00 auf Version 25.00

Mit Continia Document Capture 25.00 und Continia Expense Management 25.00 hat Continia Software eine kombinierte Anleitung veröffentlicht, mit dem unsere Partner direkt von Document Capture 8.00–24.00 und/oder Expense Management 8.00–24.00 auf Document Capture 25.00 und/oder Expense Management 25.00 aktualisieren können.

In dieser Anleitung wird das manuelle Upgrade von Document Capture und Expense Management beschrieben. Wenn Sie einen automatisierten Prozess suchen, finden Sie weitere Informationen unter [Automatisches Datenupgrade von Versionen 8.00–24.00 auf Version 25.00](Automated data upgrade.md). In diesem Dokument wird beschrieben, wie Sie Document Capture oder Expense Management mit den neuen Data Upgrade-Tools von Microsoft aktualisieren.

> [!IMPORTANT]
> Beachten Sie, dass Document Capture 2024 R2 (25.00) und Expense Management R2 (25.00) nur verfügbar sind, wenn Sie eine der folgenden Versionen von Microsoft Dynamics 365 Business Central verwenden:
>
> - Business Central 2025 Release Wave 1 (BC v24)
> - Business Central 2023 Release Wave 1 (BC v23)
> - Business Central 2023 Release Wave 1 (BC v22)
> - Business Central April 2019 (v14, FOB-basiert)
>   Dies bedeutet, dass Kunden, die ältere NAV/BC-Versionen verwenden, nicht auf DC25.00/EM25.00 aktualisieren können. Stattdessen müssen sie auf DC8.00 aktualisieren, da diese Version weiterhin mit Service Packs unterstützt wird.

Wenn Sie Document Capture oder Expense Management in Business Central Online verwenden, wird das Hauptupgrade automatisch durchgeführt, wenn Sie DC25.00/EM25.00 installieren.

Informationen zur Migration von der FOB-basierten Version von NAV/BC zur On-Premises-Erweiterung und/oder Online finden Sie unter [Upgrade von NAV/Business Central mit einer Installation von Document Capture](@DC-7) und [Document Capture von Business Central On-Premises zur Cloud migrieren](@DC-106).

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

Wenn auf dem System eine ältere Version läuft, müssen Sie zunächst auf die erforderlichen Versionen aktualisieren.

In dieser Version hat Continia ein Upgrade der Client- und Serverkomponenten von Document Capture durchgeführt, die Sie aktualisieren, bevor Sie mit der Arbeit mit Document Capture und Expense Management beginnen. Diese Anleitung hilft Ihnen bei der richtigen Ausführung. Die Document Capture- und Expense Management-Objekte in dieser Version sind nicht abwärtskompatibel mit älteren Komponenten, ebenso wie die in dieser Version enthaltenen Komponenten nicht abwärtskompatibel mit älteren Objekten sind.

Wenn Document Capture und Expense Management noch nicht in Ihrem System installiert wurden, sollten Sie keine der Informationen in diesem Dokument verwenden.

## Aufgabe 1: Mindestversionsanforderungen prüfen

Stellen Sie sicher, dass auf Ihrem aktuellen System eine der unterstützten Versionen von Document Capture oder Expense Management ausgeführt wird, die im zusammenfassenden Abschnitt aufgeführt sind. Wenn nicht, ist es sehr wichtig, dass Sie der Upgrade-Anleitung von einer früheren Version auf DC4.50 und/oder EM2.60 folgen. Frühere Upgrade-Anleitungen finden Sie unter [Upgrade auf Continia Document Capture 2023 R2 (12.00) für FOB-Versionen](@DC-157).

## Aufgabe 2: Aktualisierte BC-Lizenzdatei importieren

Der Upgrade-Vorgang muss mit einer Partnerentwicklerlizenz durchgeführt werden.

Achten Sie nach dem Upgrade darauf, eine neue oder aktualisierte Kundenlizenzdatei von Microsoft zu verwenden.

Sie müssen den Business Central Server neu starten, um die neue Lizenz zu verwenden.

## Aufgabe 3: Objekte zusammenführen

Wenn Sie das System Ihres Kunden geändert haben, prüfen Sie, ob die geänderten Objekte mit Document Capture- oder Expense Management-Objekten in Konflikt stehen, und führen Sie sie bei Bedarf zusammen. Sie sollten Objekte in einem Testsystem zusammenführen, damit sie für den späteren Import im Upgrade-Prozess bereit sind.

## Aufgabe 4: Pre-Upgradepaket prüfen

In Version 24.00 gibt es keinen Schritt vor dem Upgrade.

## Aufgabe 5: Serverkomponenten aktualisieren

Sie müssen alle unten beschriebenen Installationen mit der ausführbaren Datei **Setup** durchführen, die sich im Stammverzeichnis des Produktordners (Setup.exe) befindet.

> [!NOTE]
> Das Installationsprogramm aktualisiert den Ordner **Add-ins** (Client und/oder Server) unter dem Standardinstallationspfad. Wenn Ihr Installationspfad also vom Standardpfad von Microsoft abweicht, müssen Sie den neuen Ordner **Add-ins** in den Ordner kopieren, in dem sich Ihre Installation befindet.

So aktualisieren Sie Ihre Serverkomponenten:

<br>

| Version | Anleitung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BC14    | Führen Sie diese Schritte nur aus, wenn Sie Business Central April 2019 (BC14) verwenden: <ol><li>Beenden Sie „Business Central Server Server“.</li><li>Deinstallieren Sie „Document Capture RTC Server Components“.</li><li>Installieren Sie „Document Capture RTC Server Components“.</li><li>Wenn Sie den Microsoft Business Central Server nicht am standardmäßigen Speicherort installiert haben, müssen Sie die Add-ins manuell vom standardmäßigen Speicherort zum aktuellen Speicherort Ihrer Installation verschieben.</li><li>Starten Sie „Microsoft Business Central Server“.</li></ol> |

## Aufgabe 6: BC-Objekte und -Daten aktualisieren

> [!IMPORTANT]
> Bevor Sie Objektänderungen vornehmen oder mit der Datenaktualisierung beginnen, sichern Sie unbedingt die Datenbank.

Importieren Sie die neuen DC24.00/EM24.00-Objekte aus dem Produktordner. Verwenden Sie **Alle ersetzen** im Import Worksheet. Bei einigen Objekten wird während des Imports möglicherweise eine Warnung angezeigt wird, da einige Teile der neuen Versionsliste ein geändertes Format aufweisen. Stellen Sie die Schemasynchronisierung beim Objektimport auf **Später** ein.

> [!NOTE]
> Wenn in [Aufgabe 3: Objekte zusammenführen](#aufgabe-3-objekte-zusammenfuhren) ein geänderter Objektsatz erstellt wurde, achten Sie darauf, diesen zu importieren – und nicht die im Produktordner gefundenen Objekte.

## Aufgabe 7: Nach dem Upgrade

> [!IMPORTANT]
> Wenn einer Ihrer Mandanten Genehmigungen in Expense Management verwaltet, konsultieren Sie [Aufgabe 7: Nach dem Upgrade](@EM-263#aufgabe-7-nach-dem-upgrade) im [entsprechenden Expense Management-Artikel](@EM-263).

Führen Sie den Schritt nach dem Upgrade aus:

1. Importieren Sie das nach dem Upgrade erforderliche Objektpaket, das Ihrer BC-Version entspricht (BC14 - DC8.00-DC24.00 to DC25.00, EM8.00-EM24.00 to EM25.00 – Direct Upgrade Post.fob).
2. Verwenden Sie **Alle ersetzen** im Import Worksheet. Stellen Sie die Schemasynchronisierung beim Import auf **Später** ein.
3. Kompilieren Sie alle Document Capture- und Expense Management-Objekte (Versionslistenfilter\*DC\*|\*EM\*|\*CC\*|\*DN\*|\*BF\*|\*CA\*). Stellen Sie die Schemasynchronisierung auf **Später** ein. Einige DC/EM-Objekte werden möglicherweise nicht kompiliert. Sie werden später im Upgrade-Prozess gelöscht.
4. Kompilieren Sie alle MenuSuites (nicht nur DC und EM).
5. Wählen Sie Tools -> „Sync. Schema For All Tables“ -> **With Validation**.
6. Starten Sie den RTC-Client neu.
7. Stellen Sie sicher, dass Sie das Upgrade in einem Mandanten starten, in dem entweder Document Capture oder Expense Management aktiviert ist.
8. Führen Sie die Funktion **Daten auf neueste Version aktualisieren** von der **Document Capture Einrichtung**-Karte oder **Expense Management Einrichtung**-Karte in einem beliebigen aktivierten Mandanten aus. Die Routine schließt alle Mandanten ein und aktualisiert bei Bedarf die Document Capture-Daten und die Expense Management-Daten.
9. Der Vorgang nach der Aktualisierung sollte ohne Fehler abgeschlossen werden.
10. Starten Sie den RTC-Client neu.
11. Überprüfen Sie, ob der Aktivierungsstatus der aktualisierten Mandanten wie erwartet ist.

## Aufgabe 8: Clientkomponenten aktualisieren

So aktualisieren Sie Ihre Clientkomponenten:

<br>

| Version | Anleitung                                                                                                                                                                                                                                                                         |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BC14    | <ol><li>Deinstallieren Sie Document Capture RTC Client und Document Capture RTC Components (Scanner) mithilfe der Funktion **Programme hinzufügen oder entfernen** in Windows.</li><li>Client-Add-Ins werden jetzt bei Bedarf automatisch an alle NAV-Clients verteilt.</li></ol> |

## Aufgabe 9: Nicht verwendete Anwendungs- und Upgradeobjekte löschen

Nach Abschluss des Upgrades entfernen Sie bitte die Upgrade-Objekte (alle Objekttypen, mit Force):

Filter: 6086100..6086199

Nach dem Löschen der Upgrade-Objekte importieren Sie die Upgrade-Platzhalterobjekte aus der Fob-Datei, die die neuen DC/EM-Objekte enthält. Importieren Sie nur die Objekte im ID-Bereich: 6086100..6086199.

Dadurch wird sichergestellt, dass alle Objekte kompiliert werden und das Upgrade nicht versehentlich erneut gestartet wird.

## Aufgabe 10: Das Continia Web Approval Portal aktualisieren

So aktualisieren Sie das Continia Web Approval Portal:

1. Kompilieren Sie alle Document Capture- und Expense Management-Objekte (Versionslistenfilter \*DC\*|\*EM\*|\*CC\*|\*DN\*|\*BF\*).
2. Führen Sie die Funktion „Erzeuge Web Service“ aus der Continia-Webportal-Liste aus. Diese Funktion muss nur in einem Mandanten ausgeführt werden.
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