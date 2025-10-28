---
title: Expense Management Upgrade von Versionen 2.60–6.50 auf Version 8.00
date: 29-09-2023
description: Eine Anleitung zum direkten Upgrade von den Versionen 2.60–6.50 auf Version 8.00
lang: de
---

# Upgrade von Versionen 2.60–6.50 auf Version 8.00

Mit Continia Document Capture 8.00 und Continia Expense Management 8.00 hat Continia Software eine kombinierte Upgrade-Anleitung veröffentlicht, mit der unsere Partner direkt von Document Capture 4.50–6.50 und/oder Expense Management 2.60–6.50 auf Document Capture 8.00 und/oder Expense Management 8.00 aktualisieren können.

> [!NOTE]
> Wenn Sie ein Upgrade von Document Capture 7.00 und/oder Expense Management 7.00 auf Version 8.00 durchführen, folgen Sie dem standardmäßigen Upgrade-Prozess unter [Manuelles Upgrade von Version 7.00 auf Version 8.00](../from-version-700/manual-upgrade) oder [Automatisiertes Datenupgrade von 7.00 auf Version 8.00](../from-version-700/automated-data-upgrade).

Diese Upgrade-Anleitung beschreibt das manuelle Aktualisieren von Document Capture (DC) und Expense Management (EM) in der Version von Microsoft Dynamics NAV/Business Central (BC), die aktuell mit Document Capture und Expense Management verwendet wird (NAV 3.70 bis BC v14).

Wenn Sie Document Capture oder Expense Management in Microsoft Dynamics 365 Business Central Online verwenden, wird das Hauptupgrade automatisch durchgeführt, wenn Sie Document Capture 8.00/Expense Management 8.00 installieren (nach der Deinstallation von Document Capture 7.00/Expense Management 7.00).

Informationen zur Migration einer FOB-basierten Version von NAV/Business Central zu einer On-Premises-Erweiterung und/oder Online, finden Sie unter [Upgrade von NAV/Business Central mit einer Installation von Expense Management](@EM-107) und [Expense Management von Business Central On-Premises zur Cloud](@EM-112).

Diese Upgrade-Anleitung kann mit den folgenden Versionen von Document Capture und Expense Management verwendet werden:

**Document Capture**

- Document Capture 4.50 mit einem beliebigen Service Pack
- Document Capture 5.00 mit einem beliebigen Service Pack
- Document Capture 5.50 mit einem beliebigen Service Pack
- Document Capture 6.00 mit einem beliebigen Service Pack
- Document Capture 6.50 mit einem beliebigen Service Pack

**Expense Management**

- Expense Management 2.60 mit einem beliebigen Service Pack
- Expense Management 3.00 mit einem beliebigen Service Pack
- Expense Management 3.50 mit einem beliebigen Service Pack
- Expense Management 4.00 mit einem beliebigen Service Pack
- Expense Management 6.50 mit einem beliebigen Service Pack

Wenn auf Ihrem System eine ältere Version läuft, müssen Sie zunächst auf die erforderlichen Versionen aktualisieren.

In dieser Version haben wir die Client- und Serverkomponenten von Document Capture aktualisiert, die Sie aktualisieren müssen, bevor Sie mit der Arbeit mit Document Capture und Expense Management beginnen. Diese Anleitung hilft Ihnen bei der richtigen Ausführung. Die Document Capture- und Expense Management-Objekte in dieser Version sind nicht abwärtskompatibel mit älteren Komponenten, ebenso wie die in dieser Version enthaltenen Komponenten nicht abwärtskompatibel mit älteren Objekten sind.

Wenn Document Capture und Expense Management noch nicht in Ihrem System installiert wurden, sollten Sie keine Informationen in diesem Dokument verwenden.

## Aufgabe 1: Mindestversionsanforderungen prüfen

Stellen Sie sicher, dass auf Ihrem aktuellen System eine der unterstützten Versionen von Document Capture oder Expense Management ausgeführt wird, die im zusammenfassenden Abschnitt aufgeführt sind. Wenn nicht, ist es sehr wichtig, dass Sie die entsprechende Upgrade-Anleitung von einer früheren Version auf Document Capture 4.50 und/oder Expense Management 2.60 befolgen. Frühere Upgrade-Anleitungen finden Sie hier:

Für Document Capture: https://continia.zendesk.com/hc/en-us/sections/201853305-Upgrade-Guides  (nur für Partner verfügbar)

Für Expense Management: https://continia.zendesk.com/hc/da/sections/360000175700-Upgrade-Guides (nur für Partner verfügbar)

## Aufgabe 2: Aktualisierte NAV-Lizenzdatei importieren

Der Upgrade-Vorgang muss mit einer Partnerentwicklerlizenz durchgeführt werden.

Achten Sie nach dem Upgrade darauf, eine neue oder aktualisierte Kundenlizenzdatei von Microsoft zu verwenden und diese in NAV zu importieren.

Wenn Sie den Microsoft Dynamics NAV Server verwenden, müssen Sie ihn neu starten, um die neue Lizenz zu nutzen.

## Aufgabe 3: Objekte zusammenführen

Wenn Sie das System Ihres Kunden geändert haben, prüfen Sie, ob die geänderten Objekte mit Document Capture- oder Expense Management-Objekten in Konflikt stehen, und führen Sie sie bei Bedarf zusammen. Sie sollten Objekte in einem Testsystem zusammenführen, damit sie für den späteren Import im Upgrade-Prozess bereit sind.

## Aufgabe 4: Pre-Upgradepaket importieren

Welches Pre-Upgradepaket Sie verwenden müssen, hängt sowohl von Ihrer NAV-/Business Central-Version als auch von der Version von Document Capture/Expense Management ab, von der Sie aktualisieren.

> [!IMPORTANT]
> Stellen Sie sicher, dass Sie das richtige Upgrade-Paket verwenden.

Beispiel eines Pre-Upgrade-Dateinamens mit Beschreibung:

- “NAV 2016 to BC14 - DC4.50 to DC8.00, EM2.60 to EM8.00 – Direct Upgrade **Pre**”.fob
  - Die NAV-Version liegt zwischen NAV 2016 und BC v14 (Business Central April 2019).
  - Die DC/EM-Version vor dem Upgrade ist DC v4.50 und EM v2.60
  - Dies ist die Pre-Upgrade-.fob-Datei

## Aufgabe 5: Pre-Upgrade-Schritt ausführen

Nachdem Sie das richtige Pre-Upgrade-Paket (alles ersetzen) importiert haben, gehen Sie entweder zu **Document Capture Einrichtung** oder **Expense Management Einrichtung** und wählen Sie dann **Daten auf neueste Version aktualisieren**. Dadurch wird das Pre-Upgrade durchgeführt.

**Stellen Sie sicher, dass Sie das Upgrade in einem Mandanten starten, in dem entweder Document Capture oder Expense Management aktiviert ist.**

> [!NOTE]
> _Folgendes ist nicht relevant, wenn Sie von DC v6.00.x oder DC v6.50.x oder von EM v4.00.x oder EM v6.50.x aktualisieren:_
>
> Stellen Sie vor dem Starten des Upgrades sicher, dass der Produktaktivierungsstatus in allen zu aktualisierenden Mandanten korrekt ist. Wenn der Upgrade-Code einen Mandanten ohne gültigen Aktivierungsstatus erkennt, wird er mit der folgenden Fehlermeldung abgebrochen:
>
> - _„Ein oder mehrere Mandanten hat/haben einen falschen Aktivierungsstatus. Führen Sie Seite 6086102 „CDC Company Registration Upg.“ aus, um den Aktivierungsstatus des Mandanten zu aktualisieren, und führen Sie dann die Pre-Migration erneut aus, um den Upgrade-Prozess fortzusetzen.“_
>
> Durch Ausführen dieser Seite/dieses Formulars (abhängig von der NAV-Version) können Sie DC und EM separat für jeden Mandanten aktivieren oder deaktivieren. Das Upgrade kann erst fortgesetzt werden, wenn alle Produkt-/Mandantenkombinationen aktiviert oder deaktiviert sind.

## Aufgabe 6: Alle Tools und Komponenten installieren

Sie müssen alle unten beschriebenen Installationen mit der ausführbaren Datei **Setup** durchführen, die sich im Stammverzeichnis des Produktordners (Setup.exe) befindet.

> [!NOTE]
> Das Installationsprogramm aktualisiert den Ordner **Add-ins** (Client und/oder Server) unter dem Standardinstallationspfad. Wenn Ihr Installationspfad also vom Standardpfad von Microsoft abweicht, kopieren Sie den neuen Ordner **Add-ins** unbedingt in den Ordner, in dem sich Ihre Installation befindet.

## Aufgabe 7: Serverkomponenten aktualisieren

Um Ihre Serverkomponenten zu aktualisieren, folgen Sie je nach Ihrer Version von NAV/Business Central einer der folgenden Anleitungen:

<br>

| Version                   | Anleitung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NAV Server 2009 – 2009 R2 | Führen Sie die folgenden Schritte nur aus, wenn Sie Dynamics NAV 2009 – 2009 R2 verwenden: <ol><li>Beenden Sie „Microsoft Dynamics NAV Server“. Richten Sie den manuellen Start ein.</li><li>Beenden Sie „Microsoft Dynamics NAV Business Web Services“ falls diese gestartet wurden. Richten Sie den manuellen Start ein.</li><li>Starten Sie den Windows-Server neu.</li><li>Deinstallieren Sie „Document Capture RTC Server Components“</li><li>Installieren Sie „Document Capture RTC Server Components“.</li><li>Wenn Sie den Microsoft Dynamics NAV Server nicht am standardmäßigen Speicherort installiert haben, müssen Sie die Add-ins manuell vom aktuellen Speicherort Ihrer Installation verschieben.</li><li>Starten Sie „Microsoft Dynamics NAV Server“ neu. Richten Sie den automatischen Start ein.</li><li>Starten Sie „Microsoft Dynamics NAV Business Web Services“ falls erforderlich. Richten Sie den automatischen Start ein.</li></ol> |
| NAV Server 2013 – BC14    | Führen Sie diese Schritte nur aus, wenn Sie Dynamics NAV 2013 – Business Central April 2019 (BC14) verwenden: <ol><li>Beenden Sie „Microsoft Dynamics NAV Server“.</li><li>Deinstallieren Sie „Document Capture RTC Server Components“.</li><li>Installieren Sie „Document Capture RTC Server Components“.</li><li>Wenn Sie den Microsoft Dynamics NAV Server nicht am standardmäßigen Speicherort installiert haben, müssen Sie die Add-ins manuell vom standardmäßigen Speicherort zum aktuellen Speicherort Ihrer Installation verschieben.</li><li>Starten Sie „Microsoft Dynamics NAV Server“.</li></ol>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| NAV Classic PC-Upgrade    | Führen Sie die folgenden Schritte nur aus, wenn Sie Dynamics NAV Classic verwenden: <ol><li>Auf dem Computer, auf dem Sie das Upgrade durchführen, müssen Sie die „Document Capture Classic Client Components“ und „Document Capture Classic Components (Scanner)“ deinstallieren.</li><li>Installieren Sie „Document Capture Classic Client Components“.</li><li>Installieren Sie „Document Capture Classic Components (Scanner)“, falls erforderlich.</li></ol>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NAV RTC PC-Upgrade        | Führen Sie diese Schritte nur aus, wenn Sie Dynamics NAV RTC verwenden: <ol><li>Auf dem Computer, auf dem Sie das Upgrade durchführen, müssen Sie „Document Capture RTC Client“ und „Document Capture RTC Components (Scanner)“ deinstallieren.</li><li>Installieren Sie „Document Capture RTC Client“.</li><li>Installieren Sie „Document Capture RTC Component (Scanner)“, falls erforderlich.</li><li>Wenn Sie den Microsoft Dynamics NAV RTC Client nicht am standardmäßigen Speicherort installiert haben, müssen Sie die Add-ins manuell vom aktuellen Speicherort in den Speicherort Ihrer Installation verschieben.</li></ol>                                                                                                                                                                                                                                                                                                                                                                                                   |

## Aufgabe 8: NAV-Objekte und -Daten aktualisieren

> [!IMPORTANT]
> Bevor Sie Objektänderungen vornehmen oder mit der Datenaktualisierung beginnen, sichern Sie unbedingt die Datenbank.

Importieren Sie die neuen DC v8.00/EM v8.00-Objekte aus dem Produktordner. Verwenden Sie **Alle ersetzen** im Import Worksheet. Beachten Sie, dass bei einigen Objekten während des Imports möglicherweise eine Warnung angezeigt wird, da einige Teile der neuen Versionsliste ein geändertes Format aufweisen. Legen Sie für NAV 2015 und höher beim Objektimport das Synchronisierungsschema auf „Später“ fest.

> [!WARNING]
> Für alle Versionen von NAV 2013 bis Business Central Oktober 2018 (BC v13) gilt: Beim Importieren des DC v8.00/EM v8.00 Objektpakets überspringen Sie die vier unten genannten Seiten. Die Seiten waren unbeabsichtigt in den Release-Paketen enthalten, werden jedoch im Service Pack 1 entfernt.
>
> - Seite 5 **Währungen**
> - Seite 10 **Länder/Regionen**
> - Seite 209 **Maßeinheiten**
> - Seite 472 **MwSt.-Buchungsmatrix Einr.**

## Aufgabe 9: Nach dem Upgrade

Befolgen Sie die nachstehende Anleitung, um die Schritte nach dem Upgrade abzuschließen:

1. Importieren Sie das Objekt-Post-Upgradepaket, das Ihrer NAV/BC-Version und der DC/EM-Version entspricht, von der Sie aktualisieren (z. B. „NAV 2016 to BC14 – DC4.50 to DC8.00, EM2.60 to EM8.00 – Direct Upgrade Post.fob“).
2. Verwenden Sie **Alle ersetzen** im Import Worksheet. Wenn Sie NAV 2015 oder eine neuere Version verwenden, setzen Sie „Schema synchronisieren“ beim Import auf „Später“.
3. Kompilieren Sie alle Document Capture- und Expense Management-Objekte (Versionslistenfilter \*DC\*|\*EM\*|\*CC\*|\*DN\*). Wenn Sie NAV 2015 oder eine neuere Version verwenden, setzen Sie „Schema synchronisieren“ auf „Später“. Einige DC/EM-Objekte werden nicht kompiliert. Sie werden später im Upgrade-Prozess gelöscht.
4. Kompilieren Sie alle MenuSuites (nicht nur DC und EM).
5. Wenn Sie NAV 2015 oder eine neuere Version verwenden, wählen Sie Tools -> **Sync. Schema For All Tables** -> **With Validation** aus.
6. Starten Sie den RTC-Client neu.
7. Stellen Sie sicher, dass Sie das Upgrade in einem Mandanten starten, in dem entweder Document Capture oder Expense Management aktiviert ist.
8. Führen Sie die Funktion **Daten auf neueste Version aktualisieren** von der **Document Capture Einrichtung Einrichtung**-Karte oder der **Expense Management Einrichtung**-Karte in einem beliebigen aktivierten Mandanten aus. Hierdurch werden:
   - Alle Mandanten mit eingeschlossen und Document Capture-Daten aktualisiert, falls erforderlich.
   - Expense Management-Daten aktualisiert, falls erforderlich.
9. Der Vorgang nach der Aktualisierung sollte ohne Fehler abgeschlossen werden.
10. Starten Sie den RTC-Client neu.
11. Überprüfen Sie, ob der Aktivierungsstatus der aktualisierten Mandanten wie erwartet ist.

## Aufgabe 10: Clientkomponenten aktualisieren

Um Ihre Clientkomponenten zu aktualisieren, folgen Sie je nach Ihrer Version von NAV/Business Central einer der folgenden Anleitungen:

<br>

| Version                     | Anleitung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| --------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NAV Classic Clients         | Führen Sie die folgenden Schritte nur durch, wenn Sie Dynamics NAV Classic verwenden: <ol><li>Deinstallieren Sie „Document Capture Classic Client Components“.</li><li>Deinstallieren Sie „Document Capture Classic Components (Scanner)“.</li><li>Installieren Sie „Document Capture Classic Client Components“.</li><li>Installieren Sie „Document Capture Classic Components (Scanner)“, falls erforderlich.</li></ol> |
| NAV RTC Clients 2009 – 2016 | Führen Sie die folgenden Schritte nur aus, wenn Sie Dynamics NAV 2009 – 2016 verwenden: <ol><li>Deinstallieren Sie „Document Capture RTC Client Components“.</li><li>Installieren Sie „Document Capture RTC Client Components“.</li></ol>                                                                                                                                                                                                                                                       |
| NAV RTC Clients 2017 – BC14 | <ol><li>Deinstallieren Sie „Document Capture RTC Client“.</li><li>Deinstallieren Sie „Document Capture RTC Components (Scanner)“.</li><li>Client-Add-ins werden jetzt automatisch an alle NAV Clients verteilt, wenn erforderlich.</li></ol>                                                                                                                                                                                                                                                                                                    |

## Aufgabe 11: Nicht verwendete Anwendungs- und Upgradeobjekte löschen

Nach Abschluss des Upgrades entfernen Sie bitte die Upgrade-Objekte (alle Objekttypen, mit Force):

Filter: 6086100..6086199

> [!NOTE]
> Bei Versionen vor NAV 2015 müssen Upgrade-Tabellen und veraltete Tabellen vor dem Löschen manuell geleert werden.

Einige Objekte, die Teil der DC/EM-Version waren, von der Sie das Upgrade durchgeführt haben, werden nicht mehr benötigt. Bitte löschen Sie daher bei jedem Upgrade von einer der folgenden Versionen die angegebenen Objekte:

- Tabellen: <br> 6085620|6085701

Die folgenden Objekte werden im Code gelöscht; daher ist es nicht notwendig, sie manuell zu löschen:

- Formulare: <br> 6085606|6085716|6085751|6086348|6086403|6086418|6192771|6192773|6192776
- Seiten: <br> 6085606|6086037|6086054|6086348|6192771|6192777|6192778|6192773|6192776
- Codeunits: <br> 6085620|6085622|6085747|6085800|6086335|6085929|6192774|6192776|6192778

### Speziell für 2009 R2 RTC

Der Support für den NAV 2009 R2 RoleTailored Client wurde ab DC v8.00 und EM v8.00 eingestellt. Es wird nur der Classic Client unterstützt.

Alle DC- und EM-Seiten, außer Webservice-Seiten, sollten gelöscht werden. Seiten, die vom Continia Web Approval Portal als Webdienste verwendet werden, enden alle mit „(WS)“ im Objektnamen.

DC enthält Modifikationen an den vier unten genannten Standardseiten. Diese Änderungen sollten nach dem Upgrade manuell entfernt werden.

- Seite 26 **Kreditorenkarte**
- Seite 138 **Gebuchte Einkaufsrechnung**
- Seite 140 **Gebuchte Einkaufsgutschrift**
- Seite 344 **Navigate**

## Aufgabe 12: Das Continia Web Approval Portal aktualisieren

Um das Continia Web Approval Portal zu aktualisieren, gehen Sie folgendermaßen vor:

1. Wenn Sie NAV-Objekte unter NAV 2009 R2 verwenden, müssen Sie die aktualisierten Web Approval Portal-Objekte aus dem Produktordner importieren. Für NAV 2009 R2 und spätere Versionen sind diese Objekte im Basispaket enthalten.
2. Kompilieren Sie alle Document Capture- und Expense Management-Objekte (Versionslistenfilter \*DC\*|\*EM\*|\*CC\*|\*DN\*).
3. Führen Sie die Funktion **Erzeuge Web Service** aus der Continia-Webportal-Liste aus. Diese Funktion muss nur in einem Mandanten ausgeführt werden.
4. Wenn Sie weiterhin das Continia Web Portal On-Premises verwenden, erstellen Sie eine neue Website in IIS oder aktualisieren Sie die vorhandene.
5. Führen Sie im Bildschirm **Continia-Benutzer** in NAV die Funktion **Benutzer exportieren** aus, um Webbenutzer zu exportieren.

## Aufgabe 13: Kreditorenvorlagen mit der Einstellung „Preise inkl. MwSt“ aktualisieren

Die folgenden Informationen sind nur relevant, wenn Sie ein Upgrade von den Versionen DC v4.50, DC v5.00 oder DC v5.50 durchführen und das System Kreditorenvorlagen mit der Einstellung„Preise inkl. MwSt.“ enthält.

Mit der Veröffentlichung von DC v6.00 wurde die Registrierung von Einkaufsbelegen mit „Preise inkl. MwSt.“ geändert. Damit Sie die neue Funktionalität in vollem Umfang nutzen können, sind einige Änderungen an vorhandenen Kreditorenvorlagen erforderlich. Die aktualisierte Funktionalität und die notwendigen Änderungen werden in [diesem Artikel](https://continia.zendesk.com/hc/da/articles/360010610879-How-to-upgrade-templates-with-Prices-Incl-VAT-when-upgrading-to-DC6-00) beschrieben (nur für Partner verfügbar).

Der Artikel erwähnt das „Template Upgrade Tool“. Sie finden dies im DC v8.00-Produkt-.fob, indem Sie die folgenden Objekte importieren:

Tabelle: 6086110 and 6086111\
Seite: 6086100 and 6086101

## Informationen zum Thema

[Manuelles Upgrade von Version 7.00 auf Version 8.00](../from-version-700/manual-upgrade)\
[Automatisiertes Datenupgrade von Version 7.00 auf Version 8.00](../from-version-700/automated-data-upgrade)

<style>
  .content table tr td:nth-child(1) {
    width: 130px;
  }
  .content table tr td:nth-child(2) {
    width: 600px;
  }  
</style>
