---
title: Suchtexte zu PDF-Mastervorlagen hinzufügen
date: 03-08-2023
description:
id: DC-117
lang: de
---

# Suchtexte zu PDF-Mastervorlagen hinzufügen

Um die Erkennungsgenauigkeit von PDF-Mastervorlagen zu verbessern, kann Continia Document Capture Suchtexte für die Vorlagen basierend auf Suchtexten vorschlagen, die bereits in vorhandenen Herkunftsvorlagen (z. B. Kreditorenvorlagen) verwendet werden. Die Vorschläge können anschließend den Feldern der Mastervorlagen hinzugefügt werden.

Diese kreditorenspezifischen Suchtexte, die mit der Zeit der Standardeinrichtung hinzugefügt werden, verbessern die Erkennung der Felder importierter PDF-Belege von neuen Kreditoren in Document Capture (oder die Erstellung einer neuen Vorlage für einen vorhandenen Kreditor), was zu einer höheren Gesamtgenauigkeit führt.

## So fügen Sie Mastervorlagenfeldern vorgeschlagene Suchtexte hinzu

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.

2. Um die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**) und dann **Bearbeiten** in der Aktionsleiste, um die Karte **Belegkategorie** zu öffnen.

3. Wählen Sie im Inforegister **Vorlagen** in der Vorlagenliste die Mastervorlage für PDF-Dateien (**EINKAUF-DE**) aus.

   > [!NOTE]
   > Wenn es in der Kategorie mehr als eine PDF-Mastervorlage gibt und Sie keine bestimmte auswählen, wird standardmäßig die erste in der Liste verwendet.

4. Klicken Sie in der Aktionsleiste auf **Suchtextvorschläge**, um die entsprechende Seite zu öffnen.

5. Sie haben die folgenden Optionen:
   1. Klicken Sie in der Aktionsleiste auf **Vorschläge erstellen** und wählen Sie dann im angezeigten Dialogfeld **Vorschläge für alle Felder erzeugen** > **OK** aus.
   2. Wählen Sie in der Liste der Felder das Feld aus, für das Sie Vorschläge erstellen möchten, und wählen Sie dann in der Aktionsleiste **Vorschläge erstellen** aus. Wählen Sie im angezeigten Dialogfeld **Erzeuge Vorschläge für [ausgewähltes Feld]** > **OK**.

6. Ein Dialogfeld wird angezeigt, in dem bestätigt wird, dass mehrere Suchtexte vorgeschlagen wurden. Wählen Sie **OK**, um dies zu schließen.

7. Wählen Sie in der Liste der Felder in der Spalte **Anzahl der Vorschläge** die angezeigte Zahl für das Feld aus, für das Sie Vorschläge anzeigen möchten.

8. Aktivieren Sie in der Liste der vorgeschlagenen Suchtexte in der Spalte **Auswählen** die Kontrollkästchen der Suchtexte, die Sie der Mastervorlage hinzufügen möchten. Wählen Sie **Schließen**, um zur Seite **Suchtextvorschläge** zurückzukehren.

   > [!TIP]
   > Wenn Sie einige oder alle vorgeschlagenen Suchtexte ignorieren möchten, aktivieren Sie einfach das Kontrollkästchen **Ignorieren** für jeden Suchtext, den Document Capture nicht berücksichtigen soll. Alle ignorierten Suchtexte werden nicht mehr vorgeschlagen, wenn Sie die Funktion **Vorschläge erstellen** in Zukunft ausführen.

9. Wiederholen Sie die Schritte 7 und 8 für alle weiteren Felder, die Sie mit vorgeschlagenen Suchtexten in der Mastervorlage aktualisieren möchten.

10. Sie haben die folgenden Optionen:
    1. Klicken Sie in der Aktionsleiste auf **Vorlage aktualisieren** und wählen Sie dann im angezeigten Dialogfeld **Aktualisieren Sie alle Vorlagenfelder** > **OK** aus.
    2. Wählen Sie in der Liste der Felder das Feld aus, für das Sie Vorschläge in der Mastervorlage aktualisieren möchten, und wählen Sie dann in der Aktionsleiste **Vorlage aktualisieren** aus. Wählen Sie im angezeigten Dialogfeld **Aktualisieren Sie das [ausgewähltes Feld]-Vorlagenfeld** > **OK**

11. Ein Dialogfeld wird angezeigt, in dem bestätigt wird, dass mehrere Suchtexte erstellt wurden. Wählen Sie **OK**, um dies zu schließen.

Hierdurch werden die ausgewählten Suchtexte der PDF-Mastervorlage hinzugefügt, entweder für alle relevanten Vorlagenfelder (Schritt 10a) oder für das von Ihnen speziell ausgewählte Feld (Schritt 10b).

## So zeigen Sie hinzugefügte Suchtexte an

Um die Suchtexte anzuzeigen, die Sie mit der obigen Anleitung hinzugefügt haben, gehen Sie folgendermaßen vor:

1. Öffnen Sie die Karte **Belegkategorie** (wie in den Schritten 1–2 der Anleitung oben beschrieben).
2. Wählen Sie im Inforegister **Vorlagen** die entsprechende PDF-Mastervorlage in der Liste aus, und wählen Sie dann **Bearbeiten** aus, um die Vorlagenkarte zu öffnen.
3. Wählen Sie im Inforegister **Felder** in der Liste der Vorlagenfelder das Feld aus, das Sie anzeigen möchten. Dadurch wird die Vorlagenfeldkarte geöffnet.
4. Wählen Sie im Inforegister **Allgemein** unter **Suchtext** den angezeigten Suchtext aus, um die Seite **Bearbeiten – Feld Suchtexte** zu öffnen.

Dadurch wird eine Liste aller registrierten Suchtexte für das ausgewählte Vorlagenfeld angezeigt, einschließlich der Suchtexte, die Sie selbst hinzugefügt haben.

## Informationen zum Thema

[Mit Vorlagen arbeiten](@DC-18)\
[Neue Vorlagenfelder einrichten](@DC-19)