---
title: Expense Management Secure Archive
date: 20-05-2025
description: Sichern Sie und bewahren Sie Ihre Dokumente in ihrer Originalform auf
id: EM-189
lang: de
---

# Secure Archive

Mit Secure Archive können Sie alle digitalen Dokumente, die Ihr Unternehmen für Buchhaltungszwecke verwendet, sowie Dokumente, die mit Document Capture/Expense Management verarbeitet werden, sichern und in ihrer ursprünglichen Form aufbewahren. Dies schützt vor versehentlichem Löschen oder Ändern. Unter vollständiger Einhaltung der lokalen und nationalen Gesetzgebung sind alle Ihre archivierten Dokumente während des von Ihnen festgelegten Archivierungszeitraums vollständig rückverfolgbar. Darüber hinaus zeichnet die integrierte Protokollierungsfunktion automatisch jeden Schritt der Dokumentenverarbeitung auf, vom ersten Eingang bis zur endgültigen Buchung.

Wenn Sie nur an der Protokollierungsfunktion interessiert sind, können Sie diese als eigenständige Funktion unabhängig von Secure Archive aktivieren. So wird die Verarbeitung aller Microsoft Dynamics 365 Business Central-Belege automatisch nachverfolgt und protokolliert – nicht nur die der Belege, die von Continia-Lösungen verarbeitet werden. Dabei gibt es auch keine der geringfügigen Einschränkungen von Secure Archive.

Informationen zum Einrichten von Secure Archive und bzw. der Protokollierungsfunktion finden Sie unter [Secure Archive einrichten](@EM-190).

> [!NOTE]
> Secure Archive ist sowohl für die Continia Document Capture- als auch für Continia Expense Management-Lösung verfügbar. Dieser Artikel bezieht sich auf beide Lösungen.

Mit Secure Archive haben Document Capture und Expense Management in Deutschland die Zertifizierung als revisionssicheres Dokumentenmanagementsystem („AC-DMS ready“) erhalten. Die in Deutschland als „PK-DML ready“ bekannte Zertifizierung gilt seit mehr als zwei Jahrzehnten als Standard für ein gesetzlich konformes und revisionssicheres Management elektronischer Dokumente. Das Zertifikat, das Continia verliehen wurde, finden Sie hier: [VOI Compliance Certificate](https://partnerzone.blob.core.windows.net/articles/docs/dc/CERT_Urkunde_Continia_1.pdf).

## Umfang von Secure Archive

Secure Archive speichert Einkaufsdokumente, die von Document Capture/Expense Management verarbeitet wurden und die schließlich gebucht und für die Buchhaltung verwendet werden. Dazu gehören unter anderem Lieferantenrechnungen, Lieferantengutschriften, gescannte Einkaufsbelege, heruntergeladene elektronische Dokumente, per E-Mail empfangene Spesenanhänge von Mitarbeitern sowie Belege, die Document Capture oder Expense Management per Drag & Drop hinzugefügt werden.

> [!IMPORTANT]
> Das Archiv umfasst _keine_ Dokumente, die in Business Central außerhalb von Document Capture oder Expense Management verarbeitet werden. Für Document Capture ist nur die Belegkategorie **EINKAUF** im Umfang eingeschlossen, während für Expense Management keine derartigen Einschränkungen gelten.
>
> Damit Document Capture Secure Archive verwenden kann, müssen Sie Ihre Einkaufsbelege registrieren, indem Sie Rechnungen oder Gutschriften erstellen (oder den Bestellabgleich nutzen). Secure Archive steht nicht zur Verfügung, wenn Sie Ihre Belege in Buch.-Blättern registrieren.

### Speicherung von Dokumentdaten

Continia empfiehlt die Verwendung der Business Central SQL-Datenbank, die modernste Sicherheit und Dokumentenschutz bietet. Die Sicherheitseinstellungen der SQL-Datenbank liegen jedoch außerhalb der Kontrolle von Document Capture und Expense Management. Wenden Sie sich für eine Beratung an Ihren Business Central-Partner.

Wenn Ihre Organisation sich dafür entschieden hat, Ihr Belegarchiv außerhalb ihrer Datenbank zu hosten, beispielsweise mithilfe eines lokalen Dateispeichers oder Azure Blob Storage, liegt die Verantwortung für die Speichersicherheit ausschließlich bei Ihrer Organisation. Normalerweise wird diese Art des Hostings aufgrund von Unternehmensrichtlinien oder Speicherplatzbeschränkungen gewählt.

## Hauptfunktionen

Eine der Hauptfunktionen von Secure Archive besteht darin, im Archiv gespeicherte Belege vor dem Löschen durch Benutzer zu schützen. Daher kann die standardmäßige Business Central-Einkaufseinstellung **Löschen des Belegs zulassen vor \<DATUM\>** nicht innerhalb des von Ihnen definierten Archivierungszeitraums verwendet werden.

Eine weitere wichtige Funktion besteht darin, dass Secure Archive die Echtheit jedes im Archiv gespeicherten Belegs gewährleistet. Dies funktioniert mithilfe sicherer Hash-Funktionen, über die Sie im Abschnitt „Hash-Funktionen verwenden“ mehr erfahren können.

Document Capture verfügt über eine Soft-Delete-Funktion. Wenn Sie also feststellen, dass mit einem Ihrer Dokumente etwas nicht stimmt (z. B. eine schlechte Scanqualität), können Sie es löschen. Allerdings wird das Dokument dadurch nicht vollständig gelöscht. Obwohl es gelöscht zu sein scheint, wird es im Secure Archive im Hintergrund gespeichert, sodass von dort aus weiterhin vollständig darauf zugegriffen werden kann.

> [!NOTE]
> Diese Soft-Delete-Funktion ist nur für Document Capture verfügbar, nicht für Expense Management.

Wenn Sie einen Beleg nach dem Buchen hinzufügen möchten (z. B. einen besseren Scan), ist dies möglich. Der neue Beleg wird jedoch mit **Hinzufügen nach der Buchung** gekennzeichnet, um deutlich zu machen, dass es sich nicht um den ursprünglichen Beleg handelt.

Secure Archive bietet außerdem eine vollständige Rückverfolgbarkeit: Von jedem beliebigen Eintrag in **Sachposten** und **Kreditorenposten** aus können Sie mithilfe von **Posten finden** den Originalbeleg, so wie Sie ihn erhalten oder gescannt haben, zurückverfolgen. Dabei sind alle Metadaten wie Absender-E-Mail und Zeitstempel enthalten. Diese Rückverfolgbarkeit bleibt auch dann erhalten, wenn Sie Belege aufteilen oder zusammenführen.

Wenn Secure Archive aktiviert ist, wird jede mit Expense Management importierte Datei in eine digital signierte PDF-Datei umgewandelt. Die ursprüngliche Datei wird ebenfalls im Archiv aufbewahrt. Die Dateisignierung findet in den folgenden Fällen statt:

- Wenn Sie die Datei über das Expense Portal oder die Expense Mobile App hochladen, sofern **Belege signieren** vorher aktiviert und die Synchronisierung mit Continia Online durchgeführt wurde.
- Wenn die Datei aus Business Central hochgeladen wird und **Belege signieren** in der Einrichtung aktiviert ist.

## Hashfunktionen verwenden

Um die Sicherheit zu optimieren und die Echtheit von Belegen sicherzustellen, werden Hashfunktionen sowohl für Document Capture als auch für Expense Management verwendet, jedoch auf etwas unterschiedliche Weise. Die Hashfunktionalität der beiden Lösungen wird in den folgenden zwei Abschnitten beschrieben.

### Hashfunktionen für Document Capture

Jedem Beleg, der in Document Capture entweder über die Kategorie **EINKAUF** oder durch Hinzufügen mit Drag & Drop importiert wird, wird automatisch ein Hash (SHA1) zugewiesen. Dieser Hash wird neu berechnet, wenn der importierte Beleg geteilt oder zusammengeführt wird, wenn Seiten im Beleg gedreht werden oder wenn die Reihenfolge der Belegseiten geändert wird. Der neu berechnete Hashwert ersetzt dann den ursprünglichen Hashwert und bildet eine neue Vergleichsbasis – sozusagen ein neues Original.

Wenn Sie einen Beleg buchen, werden die Hashwerte aller angehängten Belege neu berechnet und mit den ursprünglichen Hashwerten verglichen. Stimmen sie nicht überein, wird die Buchung abgelehnt. In solchen Fällen müssen Sie alle Belege löschen und den Vorgang wiederholen. Diese Löschung wird zusammen mit allen anderen Belegaktivitäten im Protokoll aufgezeichnet.

Wenn Sie einen gebuchten Beleg öffnen, werden die Hashwerte wieder neu berechnet und erneut mit den ursprünglichen Hashwerten verglichen. Wenn sie nicht übereinstimmen, wird dies deutlich unter **Allgemein** > **Belegprotokoll** angezeigt. Dort wird eine Meldung in Rot angezeigt, die darauf hinweist, dass ein oder mehrere Beleg(e) nach der Buchung geändert wurde(n). Sie können diese Meldung auswählen, um die **Zusammenfassung Belegprotokoll** zu öffnen, in der dann angezeigt wird, welche Belege geändert wurden.

Wenn der ursprüngliche und der neu berechnete Hashwert übereinstimmen, wird unter **Belegprotokoll** eine Meldung mit der Anzahl der Belegprotokolleinträge angezeigt – zum Beispiel **2 Belegprotokolleinträge** – anstelle der oben erwähnten roten Warnmeldung. Wenn Sie auf diese Meldung klicken, um die **Zusammenfassung Belegprotokoll** zu öffnen, wird in der Spalte **Datei-Hash-Prüfung** durch **OK** signalisiert, dass eine perfekte Übereinstimmung zwischen den ursprünglichen und den aktuellen Hashwerten besteht. Die Belege sind unverändert und wurden in keiner Weise manipuliert.

### Hashfunktionen für Expense Management

Wie auch bei Document Capture wird jedem Beleg, der mit Expense Management importiert wird (entweder durch manuellen Import in Business Central oder durch Download über die Synchronisierung mit Continia Online) ein Hash zugeordnet (SHA1). Secure Archive nutzt solche Hashwerte als Vergleichsbasis, um sicherzustellen, dass eingehende Belege im gesamten Prozess bis zur Buchung unverändert bleiben.

Wenn Sie einen Beleg buchen, werden die Hashwerte aller angehängten Belege neu berechnet und mit den ursprünglichen Hashwerten verglichen. Wenn sie nicht übereinstimmen, wird die Buchung abgelehnt und es werden eine Fehlermeldung sowie ein Fehlerkommentar im Abschnitt **Bemerkungen** angezeigt. In solchen Fällen müssen Sie alle Belege löschen und den Vorgang wiederholen. Diese Löschung wird zusammen mit allen anderen Belegaktivitäten im Protokoll aufgezeichnet.

## Die Protokollierungsfunktion

Die Protokollierungsfunktion protokolliert automatisch die Aktivität aller Dokumente in Business Central (nicht nur die der von Document Capture/Expense Management verarbeiteten Belege) ab dem Zeitpunkt ihrer Eingabe im System bis hin zu ihrer Buchung. Bei den Dokumenten, die von einer oder beiden Lösungen von Continia verarbeitet werden, gibt es hinsichtlich der Protokollierung bestimmte Unterschiede zwischen den beiden Lösungen. Die folgenden beiden Abschnitte bieten einen Überblick über die protokollierten Aktivitäten für Document Capture bzw. Expense Management:

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

[Secure Archive einrichten](@EM-190)

<style>
  .content table tr td:nth-child(1) {
    width: 160px;
  }
  .content table tr td:nth-child(2) {
    width: 570px;
  }  
</style>