---
title: Verwenden der Dokumentensuche in Document Capture
date: 30-06-2025
description: So suchen Sie nach Belegen in Document Capture.
id: DC-475
lang: de
---

# Dokumentensuche verwenden

Mit der Dokumentensuchfunktion in Continia Document Capture können Sie Dokumente anhand eines oder mehrerer Schlüsselwörter finden. Bei diesen Schlüsselwörtern kann es sich um Werte handeln, die in Belegen und XML-Dateien erkannt, automatisch übersetzt oder manuell von einem Benutzer eingegeben wurden – darunter Sachkonten, Genehmigungsablaufcodes, Formelergebnisse usw.

## So verwenden Sie die Dokumentensuche

1. Suchen Sie ({{search}}) nach **Beleg suchen** und wählen Sie dann den entsprechenden Link aus.
2. Geben Sie auf der Seite **Beleg suchen** die gewünschten Schlüsselwörter in das Feld **Suche nach** ein.

> [!NOTE]
> Die Suchergebnisse werden angezeigt, sobald Sie das Feld Suche nach verlassen oder in der Aktionsleiste auf Suchen klicken. Sie können die Ergebnisse jedoch verfeinern, indem Sie die anderen Felder konfigurieren.

3. Legen Sie im Feld **Suchmodus** fest, wie nach den gewünschten Schlüsselwörtern gesucht werden soll.
   - **Muss alle Wörter enthalten** – es werden nur Ergebnisse angezeigt, die alle Schlüsselwörter enthalten. Beispiel: Wenn Sie im Feld **Suche nach** „Fracht Versand Lieferung“ eingeben, sucht Document Capture nach „Fracht UND Versand UND Lieferung“.
   - **Muss mindestens ein Wort enthalten** – Ergebnisse, die eines der Schlüsselwörter enthalten, werden angezeigt. Beispiel: Wenn Sie im Feld **Suche nach** „Fracht Versand Lieferung“ eingeben, sucht Document Capture nach „Fracht ODER Versand ODER Lieferung“.
4. **Optional**: Wählen Sie im Feld **Belegkategorie** die Belegkategorie aus, in der gesucht werden soll.

Um weitere Informationen zu einem Suchergebnis anzuzeigen, wählen Sie es aus und klicken Sie in der Aktionsleiste auf eine der folgenden Optionen:

- **Dokumentenkarte** – öffnet die Dokumentenkarte des ausgewählten Dokuments.
- **Datei anzeigen** – öffnet das zugehörige Dokument mit der mit dem Dateityp verknüpften Standardanwendung.
- **Eingehende E-Mail** – öffnet die E-Mail mit der PDF- oder XML-Datei, die zum Erstellen des Dokuments verwendet wurde.
- **Posten finden** – öffnet das Dokument, das bei der Registrierung des Originaldokuments erstellt wurde, sofern das neue Dokument nicht gebucht ist. Wenn das neue Dokument gebucht wurde, wird es stattdessen vom Standard-Business Central verarbeitet.
