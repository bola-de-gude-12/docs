---
title: Identifikationstexte für eine Vorlage in Document Capture einrichten
date: 27-06-2025
description: So richten Sie Suchtexte als Identifikationsmethode ein.
id: DC-108
lang: de
---

# Identifikationstexte für eine Vorlage einrichten

Sie können Identifikationstexte entweder direkt in einer Kreditorenvorlage oder im Belegjournal einrichten. Normalerweise richten Sie Suchtexte im Belegjournal beim Verarbeiten von Belegen ein, da hier normalerweise festgestellt wird, dass Document Capture nicht den richtigen Kreditor für einen Beleg identifiziert hat.

Um Identifikationstexte für eine Vorlage im Belegjournal einzurichten, gehen Sie folgendermaßen vor:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, zum Beispiel **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste den Beleg aus, dessen Vorlage Sie Identifikationstexte hinzufügen möchten. Klicken Sie auf die Belegzeile, _nicht_ die Nummer in der Spalte **Nr.**, da dadurch die Dokumentenkarte geöffnet wird.
4. Klicken Sie auf das Feld **Identifikationstext** für die ausgewählte Belegzeile. Zum Anzeigen der Spalte **Identifikationstext** müssen Sie möglicherweise mithilfe des Bildlauffelds in der Belegliste nach rechts navigieren (abhängig von Ihrer Bildschirmgröße).
5. Für PDF-Dokumente können Sie eine der beiden Möglichkeiten verwenden:

   - Geben Sie manuell beliebige Stichwörter ein, die Sie als Identifikationstext verwenden möchten.

   - Verwenden Sie vorhandenen Text aus dem Dokumentenbild, indem Sie mit der linken Maustaste klicken und die Schaltfläche gedrückt halten, um einen blauen Rahmen um den relevanten Text im Bild zu zeichnen (wie beim Erfassen von Vorlagenfeldwerten).
6. Für XML-Dokumente müssen Sie manuell einen Suchbegriff eingeben, da die Erfassung von Bildtext nicht möglich ist.
7. Um mehr als einen Identifikationstext hinzuzufügen, klicken Sie auf die drei Punkte rechts neben dem Feld **Identifikationstext**, um die Seite **Vorlage Identifikationstexte** zu öffnen.
8. Wählen Sie eine neue Zeile aus und geben Sie den neuen Text in die Spalte **Vorlage Identifikationstexte** ein. Wiederholen Sie diesen Vorgang für jeden weiteren Text, den Sie hinzufügen möchten, und klicken Sie abschließend auf **Schließen**.

> [!NOTE]
> Wenn Sie einer Vorlage zwei oder mehr Suchtexte hinzufügen, müssen alle gleichzeitig im Dokument vorhanden sein, damit der Kreditor erkannt wird.

Die Wörter, die Sie als Identifikationstexte verwenden, müssen sorgfältig gewählt werden, da es sonst zur falschen Übereinstimmung von Kreditoren kommen kann. Wenn Sie beispielsweise den Identifikationstext „Fracht“ für den Kreditor DHL verwendet haben, erkennt Document Capture dieses Wort möglicherweise auch in Belegen von anderen Kreditoren als DHL, beispielsweise UPS. In diesem Fall würde dieselbe Vorlage für zwei unterschiedliche Kreditoren verwendet werden, was ungünstig ist.

Um dieses Problem zu vermeiden sollten Sie Identifikationstexte verwenden, die für Kreditoren eindeutig sind, beispielsweise deren Bankkonto- oder Telefonnummer oder sogar deren Adresse.

Alternativ können Sie Suchtexte in mehreren Vorlagen einrichten. Wenn Document Capture dann in mehr als einer Vorlage eine Übereinstimmung findet, werden Sie in einem Dialogfeld aufgefordert, die richtige auszuwählen. Dies geschieht nur, wenn Felder in einem einzelnen Dokument erkannt werden, nicht beim Dokumentimport und nicht, wenn Sie im Belegjournal mehrere Dokumente auswählen.

## Informationen zum Thema

[Belegherkunft und -vorlage identifizieren](@DC-109)