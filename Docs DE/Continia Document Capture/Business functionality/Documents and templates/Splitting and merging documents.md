---
title: Belege in Document Capture aufteilen und zusammenführen
date: 11-11-2024
description: Aufteilen und Zusammenführen von Dokumenten, automatisch oder manuell.
id: DC-80
lang: de
---

# Belege aufteilen und zusammenführen

Einige der Dateien, die Sie scannen oder empfangen, bestehen möglicherweise aus mehreren Belegen, die in einer einzigen Datei zusammengefasst sind. Beispielsweise kann Ihnen ein Kreditor eine PDF-Datei mit mehreren Einkaufsrechnungen senden. In solchen Fällen können Sie die PDF-Datei in Continia Document Capture in mehrere separate Dokumente aufteilen.

Es ist auch möglich, zwei oder mehr separate PDF-Dateien zu einem einzigen Dokument zusammenführen. Dies ist beispielsweise dann notwendig, wenn Sie eine Rechnung mit Verkaufsbedingungen oder anderen zur Rechnung gehörenden Anlagen erhalten. Document Capture kann diese Anhänge mit der Rechnung zusammenführen, sodass keine separaten Dokumente im Belegjournal verbleiben.

> [!NOTE]
> Durch das Aufteilen und Zusammenführen von PDF-Dokumenten verändern Sie die Originalbelege. Wenn ein Originalbeleg ein Kreditorzertifikat enthält, verliert dieses seine Gültigkeit, sobald der Originalbeleg in mehrere kleinere Dokumente aufgeteilt oder mit anderen Dokumenten zusammengeführt wird.

## Belege manuell aufteilen

So teilen Sie einen Beleg manuell auf:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, zum Beispiel **EINKAUF**, um das Belegjournal zu öffnen.
3. Klicken Sie in der Aktionsleiste auf **Dokument** und dann auf **Teilen und zusammenführen**.
4. Wählen Sie in der Belegliste das Dokument aus, das Sie teilen möchten, und die Seite, ab der das Dokument geteilt werden soll. Beachten Sie, dass Sie die erste Seite des Dokuments nicht als Trennseite auswählen können.
5. Klicken Sie in der Aktionsleiste auf **Dokumente trennen**. Das Dokument wird nun in zwei Teile geteilt und die Seite, die Sie ausgewählt haben, wird zur ersten Seite des neuen Dokuments.

Das neue Dokument wird mit einer neuen Belegnummer versehen, die unter **Belegnr.** in der Liste angezeigt wird.

> [!NOTE]
> Nur Belege mit mehreren Seiten können geteilt werden. Einzelne Seiten können nicht aufgeteilt werden.

## Belege automatisch aufteilen

Sie können Belege auch automatisch aufteilen, indem Sie die Einstellungen der Einkaufsbelegkategorie entsprechend konfigurieren. Gehen Sie hierzu wie folgt vor:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Öffnen Sie die entsprechende Belegkategorie. Um beispielsweise die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**, da dadurch das Belegjournal geöffnet wird), und wählen Sie dann **Bearbeiten** in der Aktionsleiste aus.
3. Gehen Sie im Inforegister **OCR-Verarbeitung** zum Abschnitt **PDF-Dokumente aufteilen** und aktivieren Sie **Automatisch**. Es werden dann weitere Optionen angezeigt, die in der Tabelle unten beschrieben werden.

Die zusätzlichen Optionen ermöglichen es Ihnen, genau festzulegen, wie Ihre Dokumente aufgeteilt werden sollen. Alle Optionen werden unten erläutert:

| Option                  | Definition                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Seite aufteilen**     | Mit dieser Option werden eingehende Belege aufgeteilt, wenn darin eine leere Seite erkannt wird. Als leere Seite gilt eine Seite mit weniger als 40 Zeichen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Herkunfts-ID**        | Wenn Sie diese Option aktivieren, werden eingehende Belege aufgeteilt, wenn darin eine Herkunfts-ID identifiziert wird. Die Herkunfts-ID wird auf der Seite **Belegkategorie** unter **Herkunftstabelle und Felder** in den Feldern **Tabellen** und **Primärschlüsselfeld** ausgewählt. Bei Einkaufsrechnungen ist die standardmäßige Herkunfts-ID die Kreditornummer. Das heißt, dass Document Capture eingehende Belege immer dann aufteilt, wenn ein neuer Kreditor identifiziert wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Trennzeichen Felder** | Mit dieser Option werden eingehende Belege aufgeteilt, wenn Document Capture ein Trennzeichenfeld erkennt. Sie können eigene Trennzeichenfelder wie folgt definieren: Wählen Sie auf der Seite **Belegkategorie** unter **Vorlagen** die jeweilige Vorlagenzeile > {{more-options-small}} und anschließend **Bearbeiten**. Wählen Sie unter **Felder** das Feld, dass Sie als Trennzeichenfeld verwenden möchten. Wählen Sie anschließend auf der **Vorlagenfeldkarte** unter **Allgemein** die Option **Als Belegtrenner verwenden**.<br><br>Beachten Sie, dass ein Standard-Trennzeichenfeld möglicherweise bereits zugewiesen wurde. Bei Einkaufsrechnungen ist das Standardtrennzeichenfeld die Rechnungsnummer. Das bedeutet, dass Document Capture eingehende Belege immer dann aufteilt, wenn ein anderer Wert im Feld Rechnungsnummer erkannt wird. Die Option **Herkunfts-ID** ist obligatorisch und wird automatisch aktiviert, wenn Sie **Trennzeichen Felder** aktivieren. |
| **Barcode**             | Wenn diese Option aktiviert ist, werden eingehende Belege immer dann aufgeteilt, wenn ein Barcode oder QR-Code identifiziert wird. Im darunter liegenden, optionalen Feld **Barcode Text** können Sie Informationen eingeben, die für dieses Feld angewendet werden sollen (siehe unten).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Barcode Text**        | Wenn Sie die Option **Barcode** aktivieren und einen bestimmten Text in das Feld **Barcode-Text** eingeben, teilt Document Capture eingehende Dokumente auf, wenn ein Barcode oder QR-Code mit diesem bestimmten Text identifiziert wird.<br><br>Sie können die Teilung auch anhand spezieller Symbole/Zeichen, sogenannter _Operatoren_, festlegen, zum Beispiel: <ul><li><b>DK\*</b> teilt eingehende Dokumente auf, wenn ein Barcode/QR-Code mit <b>DK</b> beginnt.</li><li><b>SHIP\*&\*2020</b> teilt eingehende Dokumente auf, wenn ein Barcode/QR-Code mit <b>SHIP</b> beginnt und mit <b>2020</b> endet.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                          |

## Belege manuell zusammenführen

So führen Sie einen Beleg manuell zusammen:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, zum Beispiel **EINKAUF**, um das Belegjournal zu öffnen.
3. Klicken Sie in der Aktionsleiste auf **Dokument** und dann auf **Teilen und zusammenführen**.
4. Wählen Sie in der Belegliste die Belege aus, die Sie zusammenführen möchten. Auf einem Computer können Sie mehrere Dokumente auswählen, indem Sie die Umschalttaste drücken und klicken.<a href="#footnote-1"><sup>1</sup></a>
5. Nachdem Sie die Belege ausgewählt haben, die zusammengeführt werden sollen, wählen Sie in der Aktionsleiste **Zusammenführen** aus. Die Belege werden zu einem Dokument zusammengeführt und die einzelnen Belege werden in der Spalte **Name** wie folgt umbenannt: Die erste Seite des zusammengeführten Belegs wird entweder in Seite 1 umbenannt oder nach dem Kreditor benannt, während alle folgenden Seiten nach der Seitenzahl benannt werden, also beispielsweise Seite 2, Seite 3 usw.
6. Optional: Sie können die Seiten des zusammengeführten Dokuments mit den Optionen **Nach oben** und **Nach unten** in der Aktionsleiste neu anordnen.<a href="#footnote-2"><sup>2</sup></a>

## Belege automatisch zusammenführen

Sie können Belege auch automatisch zusammenführen, indem Sie die Einstellungen der Vorlagenkarte entsprechend konfigurieren. Gehen Sie hierzu wie folgt vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, zum Beispiel **EINKAUF**, um das Belegjournal zu öffnen.
3. Klicken Sie in der Aktionsleiste auf **Vorlage > Vorlagenkarte**, um die Vorlagenkarte zu öffnen.
4. Aktivieren Sie im Inforegister **Allgemein** die Einstellung **Aus der gleichen E-Mail zusammenführen**.

   > [!NOTE]
   > Da es möglich ist, Rechnungen von mehreren Kreditoren an eine einzige E-Mail anzuhängen, muss Document Capture den Kreditor in jedem Beleg identifizieren können, um sie effektiv zusammenführen zu können.

   > [[!IMPORTANT]
   > **Aus der gleichen E-Mail zusammenführen** funktioniert nur, wenn Sie alle Dateien auf einmal über die Aktion **Dateien importieren** im Rollencenter importieren. Wenn Sie versuchen, mehrere Dateien zusammenzuführen, indem Sie den Stapel **Bereit zum Import** auswählen und die gewünschten Dateien auf der Seite **Scannen & OCR** auswählen, entstehen beim Import mehrere Dokumente.

<small style>

<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1">Die Belege müssen der Reihe nach zusammengeführt werden. Beispielsweise können die Belege 1, 2, 3 und 4 in der Liste zusammengeführt werden, die Belege 1 und 4 jedoch nicht.</li>
    <li id="footnote-2">Die Optionen <b>Nach oben</b> und <b>Nach unten</b> können nur zum Verschieben von Seiten innerhalb eines Dokuments verwendet werden. Einzelne Belege können mit dieser Funktion nicht in der Liste nach oben oder unten verschoben werden.</li>    
  </ol>
</div>
</small>