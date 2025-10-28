---
title: Daten aus eDokumenten erfassen
date: 23-09-2025
description:
id: DC-182
lang: de
---

# Daten aus eDokumenten erfassen

Mit Continia eDocuments können jetzt mehr Daten als zuvor erfasst werden, die Sie für die Einrichtung und Verwendung von Vorlagen verwenden können. Dadurch kann die Herkunft besser identifiziert werden und im Belegjournal stehen dadurch mehr Optionen zur Verfügung.

Vorher wurden in Continia Document Capture eingehende XML-Dokumente durch die Verwendung von XML-Pfaden verarbeitet. Sowohl für Identifikationsvorlagen als auch für Herkunftsvorlagen wurden XML-Pfade verwendet, um anzugeben, wo die verschiedenen Felder oder Zeilen in jedem eingehenden XML-Dokument zu finden sind. In Continia eDocuments wurden diese XML-Pfade durch eDocuments-Tabellen ersetzt, die eine größere Flexibilität bei elektronischen Formaten bieten.

Auf den Karten für XML-Identifikationsvorlagen wurde das Inforegister **Felder** und die Liste von Feldern mit entsprechenden XML-Pfaden durch das Inforegister **eDokument-Herkunftsidentifikation** ersetzt, das eine Liste mit eDocuments-Tabellen enthält. Auf den Karten für XML-Herkunftsvorlagen wurden die Bereiche **Rechnung** und **Gutschrift** im Inforegister **Allgemein** durch den Bereich **eDokumente** ersetzt, der Kopf- und Zeilentabellen für eDokumente anstelle von XML-Pfaden verwendet, um Daten zu identifizieren und zu erfassen.

> [!NOTE]
> Informationen zur Funktionsweise von Identifikationsvorlagen für Continia eDocuments finden Sie unter [Herkunftsidentifikation](#herkunftsidentifikation) und [So können Sie eine XML-Identifikationsvorlage anzeigen und bearbeiten](#so-konnen-sie-eine-xml-identifikationsvorlage-anzeigen-und-bearbeiten) weiter unten.
>
> Informationen über Herkunftsvorlagen und deren Anpassung finden Sie unter [Feldzuordnung und Detailseiten für Kopffelder von Herkunftsvorlagen](#feldzuordnung-und-detailseiten-fur-kopffelder-von-herkunftsvorlagen) und [So ordnen Sie Felder zu und richten Detailseiten ein](#so-ordnen-sie-felder-zu-und-richten-detailseiten-ein) weiter unten.

## Herkunftsidentifikation

XML-Identifikationsvorlagen werden zur Identifikation von Debitoren und Kreditoren verwendet, was auch als Herkunftsidentifikation bezeichnet wird. Um dies zu optimieren, wurde in Continia eDocuments in diesen Vorlagen eine neue Funktion hinzugefügt, auf die über die Vorlagenkarte der Identifikationsvorlagen im Inforegister **eDokument-Herkunftsidentifikation** zugegriffen werden kann.

Dadurch haben Sie die Möglichkeit, mehr Identifikationsparameter zu verwenden und diese Ihren Bedürfnissen und Wünschen entsprechend anzupassen. Für jeden Identifikationsparameter steht eine Vielzahl unterschiedlicher eDocuments-Tabellen zur Auswahl sowie Felder aus jeder Tabelle und Felder für Kreditoren/Debitoren. So können Sie angeben, wie Continia eDocuments den Kreditor/Debitor identifizieren soll und nach welchen Feldern hierzu in eingehenden Dokumenten gesucht werden soll.

Eine Reihe typischer eDokument-Tabellenfeldpositionen für Global Location Numbers (GLNs) und Umsatzsteuer-Identifikationsnummern wurden standardmäßig eingerichtet. Sie können diese anzeigen oder bearbeiten, indem Sie der Anleitung unter [So können Sie eine XML-Identifikationsvorlage anzeigen oder bearbeiten](#so-konnen-sie-eine-xml-identifikationsvorlage-anzeigen-oder-bearbeitene) folgen.

## So können Sie eine XML-Identifikationsvorlage anzeigen oder bearbeiten

So können Sie eine XML-Identifikationsvorlage anzeigen oder bearbeiten:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Öffnen Sie die entsprechende Belegkategorie – beispielsweise **EINKAUF** – indem Sie die Kategoriezeile (nicht den Code) auswählen und anschließend in der Aktionsleiste auf **Bearbeiten** klicken.
3. Wählen Sie im Inforegister **Vorlagen** in der Liste der Vorlagen die XML-Identifikationsvorlage aus, die Sie anzeigen oder bearbeiten möchten (wie zum Beispiel **EBILLING-ID**), und klicken Sie dann auf **Bearbeiten**, um die Vorlagenkarte zu öffnen.
4. Im Inforegister **eDokument-Herkunftsidentifikation** können Sie sehen, wie die standardmäßigen Identifikationsparameter eingerichtet sind. Sie können diese folgendermaßen bearbeiten:
   - Um einen Identifikationsparameter hinzuzufügen, klicken Sie in der Inforegister-Titelleiste auf **Neue Zeile** oder wählen Sie einfach die leere Zeile am Ende der Liste aus und füllen Sie dann die Tabellenfelder in jeder Spalte nach Bedarf aus.
   - Um einen Identifikationsparameter zu löschen, klicken Sie in der Inforegister-Titelleiste auf **Zeile löschen**.
   - Um einen vorhandenen Identifikationsparameter zu bearbeiten, wählen Sie das Tabellenfeld aus, das Sie bearbeiten möchten, und klicken Sie dann auf die drei Punkte auf der rechten Seite des Felds, um eine **Objekte**/**Felder-Lookup**-Seite zu öffnen. Wählen Sie auf dieser Seite die eDocuments-Tabelle oder das eDocuments-Feld aus, das Continia eDocuments zur Identifizierung des Kreditors/Debitors verwenden soll, und klicken Sie dann auf **OK**.

## Feldzuordnung und Detailseiten für Kopffelder von Herkunftsvorlagen

Herkunftsvorlagen sind an eine bestimmte Herkunft (zum Beispiel einen Kreditor) gebunden und werden von Document Capture zum Erfassen, Validieren und Registrieren von Dokumenten verwendet. Mit Continia eDocuments können Sie Herkunftsvorlagen beliebig anpassen, indem Sie alle Vorlagenkopffelder so einrichten, dass es bestimmte Daten aus einem eingehenden XML-Dokument erfasst werden. Sie können außerdem von jedem Kopfzeilenfeld aus eine Verknüpfung zu einer bestimmten Seite mit weiteren Details herstellen.

Um Vorlagenkopffelder zum Erfassen bestimmter Daten zu konfigurieren, verwenden Sie die Funktion **Aus eDokument erfassen**. Damit werden alle Felder aufgelistet, die die XML-Struktur zwischen einem bestimmten Dokument und den verschiedenen Tabellen zugeordnet hat. Beispielsweise stehen Ihnen möglicherweise folgende Tabellen zur Auswahl:

- **eAbrechnungskopf**
- **Parteiinformationen** – **Kreditor**
- **Parteiinformationen** – **Debitor**
- **Parteiidentifikation** – **Kreditor**
- **Parteiidentifikation** – **Debitor**
- **Zahlungsmittel**
- **MwSt.-Zwischensumme**
- **Beleghinweis**

Sie können zwischen den Feldern aller Tabellen frei wählen, wenn Sie Tabellenfelder bestimmten Vorlagenkopffeldern zuordnen. Beispielsweise können Sie das Vorlagenkopffeld **Buchungsbeschreibungszeile** dem Feld **Zahlungsbedingungshinweis** aus der Tabelle **eAbrechnungskopf** zuordnen. Dadurch wird sichergestellt, dass die **Zeilenbuchungsbeschreibung** immer die Dokumentdaten erfasst, die sich in diesem bestimmten Tabellenfeld befinden.

Um einem Kopffeld einen Link zu einer bestimmten Seite mit weiteren Details hinzuzufügen, verwenden Sie die Funktion **eDokumente-Detailseite**. Dies ermöglicht Ihnen Folgendes:

- Sie können dem Benutzer weitere Informationen zur Verfügung stellen, die für das angegebene Kopffeld relevant sind.
- Sie können es dem Benutzer ermöglichen, aus vorgegebenen Optionen auszuwählen, um ein bestimmtes Feld näher zu bestimmen.

Sie können die Funktion beispielsweise verwenden, um das Kopffeld **MwSt.-Betrag** mit einer Seite zu verknüpfen, die mehr Informationen zum Mehrwertsteuersatz, zur Mehrwertsteuersystem-ID und ähnlichen Informationen enthält. Sie können dem Benutzer mit dieser Funktion beispielsweise auch mehrere Auswahlmöglichkeiten zur Angabe der Zahlungsmethode anbieten.

> [!TIP]
> Die angegebenen Details oder Optionen stehen dem Benutzer dann jeweils im Abschnitt **Belegkopf** im Belegjournal in der Spalte **Details** der Feldtabelle zur Verfügung.

Der folgende Abschnitt [So ordnen Sie Felder zu und richten Detailseiten ein](#so-ordnen-sie-felder-zu-und-richten-detailseiten-ein) enthält eine Anleitung, wie Sie die oben beschriebene Funktion einrichten können.

## So ordnen Sie Felder zu und richten Detailseiten ein

Um Vorlagenkopfzeilenfeldern bestimmten Tabellenfelder zuzuordnen und/oder Detailseiten für bestimmte Kopfzeilenfelder einzurichten, gehen Sie folgendermaßen vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die entsprechende Belegkategorie – beispielsweise **EINKAUF** – indem Sie die Kategoriezeile (nicht den Code) auswählen und anschließend in der Aktionsleiste auf **Bearbeiten** klicken.
3. Wählen Sie im Inforegister **Vorlagen** in der Liste der Vorlagen die XML-Vorlage aus, die Sie konfigurieren möchten, und klicken Sie dann auf **Bearbeiten**, um die Vorlagenkarte zu öffnen.
4. Wählen Sie im Inforegister **Felder** das Kopffeld aus, das Sie konfigurieren möchten. Dadurch wird die Vorlagenfeldkarte geöffnet.
5. Gehen Sie im Inforegister **Allgemein** zum Abschnitt **eDokumente**.
6. Um das ausgewählte Kopfzeilenfeld einem bestimmten Tabellenfeld zuzuordnen, klicken Sie auf das Feld **Aus eDokument erfassen**, um die entsprechende Seite zu öffnen. Suchen Sie in der Liste der eDocuments-Tabellen die entsprechende Tabelle und wählen Sie dann das Tabellenfeld aus, dem Sie das Kopfzeilenfeld zuordnen möchten.
   > [!NOTE]
   > Das ausgewählte Feld wird dem Feld **Aus eDokumente erfassen** als Link hinzugefügt (der Name der ausgewählten eDokumente-Tabelle gefolgt vom Namen des ausgewählten Tabellenfelds). Durch Klicken auf diesen Link können Sie Ihre Auswahl bei Bedarf später bearbeiten.
   >
   > Wenn Sie ein Tabellenfeld aus einer eDocuments-Tabelle ausgewählt haben, das doppelt vorhanden ist, wird das Feld **Anzahl von Filtern** unten automatisch ausgefüllt, um die genaue Position des ausgewählten Felds anzugeben. Beispiel: Es gibt es zwei Tabellen **Parteiinformationen** (eine für **Buchhaltungslieferanten** und eine für **Buchhaltungskunden**. Wenn Sie aus einer dieser Tabellen ein Feld auswählen, wird im Feld **Anzahl von Filtern** angezeigt, um welches Feld es sich handelt.
7. Um einen Filter anzuwenden, klicken Sie auf das Feld **Anzahl von Filtern**, um die Seite **Tabellenfilter** zu öffnen, die alle Felder für die Tabelle auflistet, die Sie oben unter **Aus eDokument erfassen** ausgewählt haben. Suchen Sie das Feld, nach dem Sie filtern möchten, und geben Sie dann in der Spalte **Filter** den gewünschten Filter ein oder wählen Sie ihn aus.
8. Wenn der Feldwert das Ergebnis einer Operation ist, die mit anderen Dokumentdaten durchgeführt wurde, geben Sie die Art der Operation in **Wertoperation** an. Sie können zwischen drei Optionen wählen:
   | Option        | Beschreibung                                                                                                                                                           |
   | ------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | **Summe**     | Addiert die Werte des ausgewählten Felds und der entsprechenden Felder für alle Datensätze in der Tabelle, die Sie oben in Schritt 6 ausgewählt haben. |
   | **Anzahl**    | Zählt die Anzahl der Datensätze in der Tabelle, die Sie oben in Schritt 6 ausgewählt haben.                                                            |
   | **Existiert** | Gibt an, ob der Datensatz in der Tabelle vorhanden ist, die Sie oben in Schritt 6 ausgewählt haben.                                                    |
9. Geben Sie auf der **eDokumente-Detailseite** an, welche Details (sofern vorhanden) Sie den Benutzern im Abschnitt **Belegkopf** des Belegjournals anzeigen möchten:
   - Wenn es sich bei dem ausgewählten Feld um einen Feldtyp handelt, bei dem Benutzer aus mehreren Optionen auswählen können (z. B. **Zahlungsmittel**), klicken Sie auf das Feld, um eine Liste mit Optionen zu öffnen, und wählen Sie dann die Optionen aus, die den Benutzern angezeigt werden sollen.
   - Wenn es sich bei dem ausgewählten Feld um einen anderen Feldtyp handelt, klicken Sie auf das Feld, um eine Liste mit Seiten zu öffnen. Wählen Sie dann die Seite aus, auf die der Link verweisen soll, um den Benutzern weitere Informationen zu dem Feld bereitzustellen.
