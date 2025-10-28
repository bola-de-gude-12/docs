---
title: Secure Archive
date: 27-12-2024
description:
id: DC-154
lang: de
---

# Secure Archive

Mit Secure Archive können alle digitalen Belege, die Ihr Unternehmen für Buchhaltungszwecke verwendet und die mit Document Capture und/oder Expense Management verarbeitet werden, in ihrer ursprünglichen Form gesichert und aufbewahrt werden, sodass sie nicht versehentlich gelöscht oder auf unerwünschte Weise verändert werden können. Unter vollständiger Einhaltung lokaler und nationaler Gesetzgebung sind alle Ihre archivierten Belege während des von Ihnen definierten Archivierungszeitraums vollständig rückverfolgbar, und die integrierte Protokollierungsfunktion zeichnet automatisch jeden Schritt bei der Verarbeitung der Belege auf, vom ersten Eingang bis zur abschließenden Buchung.

Wenn Sie nur an der Protokollierungsfunktion interessiert sind, können Sie diese problemlos als eigenständige Funktion unabhängig von Secure Archive aktivieren. So wird die Verarbeitung aller Microsoft Dynamics 365 Business Central-Belege automatisch nachverfolgt und protokolliert – nicht nur die der Belege, die von Continia-Lösungen verarbeitet werden. Dabei gibt es auch keine der geringfügigen Einschränkungen von Secure Archive.

Informationen zum Einrichten von Secure Archive und/oder der Protokollierungsfunktion finden Sie unter [Secure Archive einrichten](@DC-155).

> [!NOTE]
> Secure Archive ist sowohl für Continia Document Capture als auch für Continia Expense Management verfügbar. Dieser Artikel bezieht sich auf beide Lösungen.

Mit Secure Archive haben Document Capture und Expense Management in Deutschland die Zertifizierung als revisionssicheres Dokumentenmanagementsystem („AC-DMS ready“) erhalten. Die in Deutschland als „PK-DML ready“ bekannte Zertifizierung gilt seit mehr als zwei Jahrzehnten als Standard für ein gesetzlich konformes und revisionssicheres Management elektronischer Dokumente. Das Zertifikat, das Continia verliehen wurde, finden Sie hier: [VOI Compliance Certificate](https://partnerzone.blob.core.windows.net/articles/docs/dc/CERT_Urkunde_Continia_1.pdf).

## Umfang von Secure Archive

Secure Archive speichert Einkaufsbelege, die von Document Capture und/oder Expense Management verarbeitet wurden und die schließlich gebucht und für die Buchhaltung verwendet werden. Dazu gehören unter anderem Lieferantenrechnungen, Lieferantengutschriften, gescannte Einkaufsbelege, heruntergeladene elektronische Dokumente, per E-Mail empfangene Spesenanhänge von Mitarbeitern sowie Belege, die Document Capture oder Expense Management per Drag & Drop hinzugefügt werden.

> [!IMPORTANT]
> Das Archiv umfasst keine Belege, die in Business Central außerhalb von Document Capture oder Expense Management verarbeitet werden. Für Document Capture ist nur die Belegkategorie **EINKAUF** im Umfang eingeschlossen, während für Expense Management keine derartigen Einschränkungen gelten.
>
> Damit Document Capture Secure Archive verwenden kann, müssen Sie Ihre Einkaufsbelege registrieren, indem Sie Rechnungen oder Gutschriften erstellen (oder den Bestellabgleich nutzen). Es kann auch verwendet werden, wenn Sie Ihre Belege in Buch.-Blättern registrieren.

> [!WARNING]
> Die physische Speicherung von Belegdaten liegt außerhalb der Kontrolle von Document Capture und Expense Management. Secure Archive schützt Ihre eigentlichen Belegdateien _nicht_ vor Änderung oder Löschung, stellt jedoch sicher, dass Sie über solche Aktionen benachrichtigt werden, wenn Sie einen Beleg buchen oder aufrufen. Der Schutz vor unbefugtem Zugriff auf Ihre Belegdateien liegt in der alleinigen Verantwortung der IT-Abteilung Ihres Unternehmens.

Aufgrund von Unternehmensrichtlinien, Speicherplatzbeschränkungen oder aus anderen Gründen hat sich Ihr Unternehmen möglicherweise dafür entschieden, Ihr Belegarchiv außerhalb der Datenbank zu hosten (z. B. in einem lokalen Dateispeicher oder Azure Blob Storage). In solchen Fällen ist die Speichersicherheit alleinige Verantwortung Ihres Unternehmens.

## Hauptfunktionen

Eine der Hauptfunktionen von Secure Archive besteht darin, im Archiv gespeicherte Belege vor dem Löschen durch Benutzer zu schützen. Daher kann die standardmäßige Business Central-Einkaufseinstellung **Löschen des Belegs zulassen vor \<DATUM\>** nicht innerhalb des von Ihnen definierten Archivierungszeitraums verwendet werden.

Eine weitere sehr wichtige Funktion besteht darin, dass Secure Archive die Echtheit jedes im Archiv gespeicherten Belegs gewährleistet. Hierfür werden Hashfunktionen verwendet, über die Sie unter [Die Verwendung von Hashfunktionen](#die-verwendung-von-hashfunktionen) weitere Informationen finden.

Wenn Sie in Document Capture feststellen, dass einer Ihrer Belege Probleme aufweist (z. B. weil die Qualität des Scans schlecht ist), können Sie ihn als gelöscht markieren. Dadurch wird der Beleg jedoch nicht vollständig gelöscht: Obwohl er auf den ersten Blick tatsächlich gelöscht zu sein scheint, wird er in Secure Archive aufbewahrt, wo Sie vollständigen Zugriff darauf haben.

> [!NOTE]
> Diese Soft-Delete-Funktion ist nur für Document Capture verfügbar, nicht für Expense Management.

Wenn Sie einen Beleg nach dem Buchen hinzufügen möchten (z. B. einen besseren Scan), können Sie dies ganz einfach tun. Der neue Beleg wird jedoch mit **Hinzufügen nach der Buchung** gekennzeichnet, um deutlich zu machen, dass es sich nicht um den ursprünglichen Beleg handelt.

Secure Archive bietet außerdem eine vollständige Rückverfolgbarkeit. Von jedem beliebigen Eintrag in **Sachposten** und **Kreditorenposten** aus können Sie mithilfe von **Posten finden** den Originalbeleg, so wie Sie ihn erhalten oder gescannt haben, zurückverfolgen. Dabei sind alle Metadaten wie Absender-E-Mail und Zeitstempel enthalten. Diese Rückverfolgbarkeit bleibt auch dann erhalten, wenn Sie Belege aufteilen oder zusammenführen.

Wenn Secure Archive aktiviert ist, wird jede mit Expense Management importierte Bilddatei in eine digital signierte PDF-Datei umgewandelt. Die ursprüngliche Datei wird ebenfalls im Archiv aufbewahrt. Die Dateisignierung findet in den folgenden Fällen statt:

- Wenn Sie die Datei über das Expense Portal oder die Expense App (mobile App) hochladen, sofern **Belege signieren** aktiviert ist und die Synchronisierung mit Continia Online durchgeführt wurde.
- Wenn die Datei aus Business Central hochgeladen wird und **Belege signieren** in der Einrichtung aktiviert wurde.

## Die Verwendung von Hashfunktionen

Um die Sicherheit zu optimieren und die Echtheit von Belegen sicherzustellen, werden Hashfunktionen sowohl für Document Capture als auch für Expense Management verwendet, jedoch auf etwas unterschiedliche Weise. Die Hashfunktionalität der beiden Lösungen wird in den folgenden zwei Abschnitten beschrieben.

### Hashfunktionen für Document Capture

Jedem Beleg, der in Document Capture entweder über die Kategorie **EINKAUF** oder durch Hinzufügen mit Drag & Drop importiert wird, wird automatisch ein Hash (SHA1) zugewiesen. Dieser Hash wird neu berechnet, wenn der importierte Beleg geteilt oder zusammengeführt wird, wenn Seiten im Beleg gedreht werden oder wenn die Reihenfolge der Belegseiten geändert wird. Der neu berechnete Hashwert ersetzt dann den ursprünglichen Hashwert und bildet eine neue Vergleichsbasis – sozusagen ein neues Original.

Wenn Sie einen Beleg buchen, werden die Hashwerte aller angehängten Belege neu berechnet und mit den ursprünglichen Hashwerten verglichen. Stimmen sie nicht überein, wird die Buchung abgelehnt. In solchen Fällen müssen Sie alle Belege löschen und den Vorgang wiederholen. Diese Löschung wird zusammen mit allen anderen Belegaktivitäten im Protokoll aufgezeichnet.

Wenn Sie einen gebuchten Beleg einsehen, werden die Hashwerte wieder neu berechnet und erneut mit den ursprünglichen Hashwerten verglichen. Wenn sie nicht übereinstimmen, wird dies deutlich im Inforegister **Allgemein** unter **Belegprotokoll** angezeigt. Dort wird eine Meldung in Rot angezeigt, die darauf hinweist, dass ein oder mehrere Beleg(e) nach der Buchung geändert wurde(n). Sie können diese Meldung auswählen, um die **Zusammenfassung Belegprotokoll** zu öffnen, in der dann angezeigt wird, welche Belege geändert wurden.

Wenn der ursprüngliche und der neu berechnete Hashwert übereinstimmen, wird unter **Belegprotokoll** einfach eine Meldung mit der Anzahl der Belegprotokolleinträge angezeigt – zum Beispiel **2 Belegprotokolleinträge** – anstelle der oben erwähnten roten Warnmeldung. Wenn Sie auf diese Meldung klicken, um die **Zusammenfassung Belegprotokoll** zu öffnen, wird in der Spalte **Datei-Hash-Prüfung** durch **OK** signalisiert, dass eine perfekte Übereinstimmung zwischen den ursprünglichen und den aktuellen Hashwerten besteht. Die Belege sind unverändert und wurden in keiner Weise manipuliert.

### Hashfunktionen für Expense Management

Wie auch bei Document Capture wird jedem Beleg, der mit Expense Management importiert wird (entweder durch manuelles Hinzufügen in Business Central oder durch Download über die Synchronisierung mit Continia Online) ein Hash zugeordnet (SHA1). Secure Archive nutzt solche Hashwerte als Vergleichsbasis, um sicherzustellen, dass eingehende Belege im gesamten Prozess bis zur Buchung unverändert bleiben.

Wenn Sie einen Beleg buchen, werden die Hashwerte aller angehängten Belege neu berechnet und mit den ursprünglichen Hashwerten verglichen. Wenn sie nicht übereinstimmen, wird die Buchung abgelehnt und es werden eine Fehlermeldung sowie ein Fehlerkommentar im Abschnitt **Bemerkungen** angezeigt. In solchen Fällen müssen Sie alle Belege löschen und den Vorgang wiederholen. Diese Löschung wird zusammen mit allen anderen Belegaktivitäten im Protokoll aufgezeichnet.

## Die Protokollierungsfunktion

Sowohl für Document Capture als auch Expense Management gibt es zwei verschiedene Protokollierungssysteme:

- Das Systemprotokoll
- Das Belegprotokoll

**Das Systemprotokoll** protokolliert automatisch jede Änderung, die in der [Einrichtung von Secure Archive](@DC-155) vorgenommen wird. Wenn ein Benutzer also eine der folgenden Einrichtungseinstellungen konfiguriert, werden die Änderungen sofort im Systemprotokoll protokolliert:

- **Secure Archive aktivieren**
- **Belegaktivitäten protokollieren**
- **Art des Archivzeitraums**
- **Minimaler Archivierungszeitraum**
- **Belege signieren** (trifft nur für Expense Management zu)

> [!TIP]
> Sie können auf das Systemprotokoll über die Seiten **Document Capture Einrichtung** und **Expense Management Einrichtung** zugreifen, indem Sie **Aktionen** > **Secure Archive** > **System-Log** auswählen. Auf der angezeigten Seite wird eine ungefilterte Liste aller Änderungen angezeigt, die in der Einrichtung vorgenommen wurden.

**Das Belegprotokoll** protokolliert automatisch die Aktivität aller von Document Capture und/oder Expense Management verarbeiteten Belege ab dem Zeitpunkt ihrer Eingabe im System bis hin zu ihrer Buchung.

> [!TIP]
> Sie können auf das Belegprotokoll folgendermaßen zugreifen:
>
> - Von den Seiten **Document Capture Einrichtung** und **Expense Management Einrichtung**: Wählen Sie **Aktionen** > **Secure Archive** > **Belegprotokoll**, um die Seite **Belegprotokoll** zu öffnen. Hier wird eine ungefilterte Liste aller Belegaktivitäten angezeigt.
> - Von der Dokumentenkarte: Wählen Sie **Aktionen** > **Dokument** > **Belegprotokoll**, um die Seite **Belegprotokoll** zu öffnen, die eine gefilterte Liste von Aktivitäten für den ausgewählten Beleg anzeigt.
> - Von einer gebuchten Einkaufsrechnung oder Gutschrift: Wählen Sie im Inforegister **Allgemein** das Feld **Belegprotokoll** aus, um die **Zusammenfassung Belegprotokoll** zu öffnen. Darin wird eine gefilterte Liste von Aktivitäten der Document Capture-Belege angezeigt, die mit dem gebuchten Business Central-Beleg verknüpft sind.

Es gibt einige Unterschiede zwischen Document Capture und Expense Management im Hinblick darauf, was im Belegprotokoll aufgezeichnet wird. Die folgenden beiden Abschnitte bieten einen Überblick über die protokollierten Aktivitäten für Document Capture bzw. Expense Management:

### Protokollierte Aktivitäten für Document Capture-Belege

| Aktivität           | Beschreibung                                                                                                                                                                                                                                                                           |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Empfangen           | Ein Protokolleintrag wird hinzugefügt, wenn ein Beleg importiert wird und wenn ein Beleg vor dem Import gelöscht wird. Der Eintrag enthält die Absender-E-Mail-Adresse (**Von**) und den Namen der Datei in der eingehenden E-Mail. |
| Gelöscht vor Import | Ein Protokolleintrag wird hinzugefügt, wenn ein Beleg von der Seite **Bereit zum Import** gelöscht wird.                                                                                                                                                               |
| Importiert          | Ein Protokolleintrag wird hinzugefügt, wenn ein neuer Beleg während des Importvorgangs oder durch Ziehen in Document Capture per Drag & Drop erstellt wird.                                                                                        |
| Gelöscht            | Ein Protokolleintrag wird hinzugefügt, wenn ein Beleg gelöscht wird.                                                                                                                                                                                                   |
| Aufgeteilt          | Ein Protokolleintrag wird hinzugefügt, wenn ein Beleg in mehrere Dokumente aufgeteilt wird.                                                                                                                                                                            |
| Zusammengeführt     | Ein Protokolleintrag wird hinzugefügt, wenn mehrere Dokumente zu einem zusammengeführt werden.                                                                                                                                                                         |
| Registriert         | Ein Protokolleintrag wird hinzugefügt, wenn ein Beleg registriert wird. Der Eintrag gibt an, als welcher Standardbeleg (Rechnung/Gutschrift) der Document Capture-Beleg registriert wurde.                                          |
| Gebucht             | Ein Protokolleintrag wird hinzugefügt, wenn ein Standardbeleg, der aus einem Document Capture-Beleg erstellt wurde, gebucht wird. Der Protokolleintrag enthält Angaben zur Nummer des gebuchten Belegs.                                                |
| Geöffnet            | Ein Protokolleintrag wird hinzugefügt, wenn ein registrierter Beleg wieder geöffnet wird.                                                                                                                                                                              |

### Protokollierte Aktivitäten für Expense Management-Belege

| Aktivität                                               | Beschreibung                                                                                                                                                                                                                                                                                   |
| ------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Empfangen                                               | Ein Protokolleintrag wird hinzugefügt, wenn eingehende Belege (Ausgaben, Fahrtkosten, Pauschalen, Spesenabrechnungen oder Transaktionen) von Continia Online heruntergeladen oder unter Expense Management Aktivitäten in Business Central erstellt werden. |
| Anhänge hinzugefügt/entfernt                            | Ein Protokolleintrag wird hinzugefügt, wenn Spesen und Fahrtkosten Beleganhänge hinzugefügt bzw. von diesen entfernt werden.                                                                                                                                   |
| Doppelte Transaktionen beim Import verworfen            | Ein Protokolleintrag wird hinzugefügt, wenn eine Transaktion verworfen wird, weil sie eine doppelte ID hat.                                                                                                                                                                    |
| Gelöscht                                                | Ein Protokolleintrag wird hinzugefügt, wenn ein Beleg gelöscht wird.                                                                                                                                                                                                           |
| Aufgeteilt                                              | Ein Protokolleintrag wird hinzugefügt, wenn eine Spesenzuordnung eine neue Ausgabe erstellt.                                                                                                                                                                                   |
| Zusammengeführt                                         | Ein Protokolleintrag wird hinzugefügt, wenn mehrere Belege zu einem zusammengeführt werden.                                                                                                                                                                                    |
| Übereinstimmend/nicht übereinstimmend                   | Protokolleinträge werden hinzugefügt, wenn Spesen und Transaktionen abgeglichen bzw. nicht abgeglichen werden.                                                                                                                                                 |
| Zur Abrechnung hinzugefügt/aus Abrechnung entfernt      | Ein Protokolleintrag wird hinzugefügt, wenn einer Spesenabrechnung ein Beleg hinzugefügt oder aus dieser entfernt wird.                                                                                                                                                        |
| Genehmigt                                               | Ein Protokolleintrag wird hinzugefügt, wenn ein Beleg genehmigt wird.                                                                                                                                                                                                          |
| Gebucht                                                 | Ein Protokolleintrag wird hinzugefügt, wenn ein Beleg gebucht wird.                                                                                                                                                                                                            |
| Aktualisierungen gebuchter Rechnungen oder Gutschriften | Ein Protokolleintrag wird hinzugefügt, wenn Expense Management eine Einkaufsrechnung oder Gutschrift erstellt. Wichtige Änderungen an diesen Belegen werden protokolliert.                                                                                     |

## Informationen zum Thema

[Secure Archive einrichten](@DC-155)

<style>
  .content table tr td:nth-child(1) {
    width: 160px;
  }
  .content table tr td:nth-child(2) {
    width: 570px;
  }  
</style>