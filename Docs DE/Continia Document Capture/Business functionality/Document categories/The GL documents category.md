---
title: Die Kategorie für Sachbelege in Document Capture
date: 27-08-2025
description: So verarbeiten Sie Dokumente mit OCR und hängen durchsuchbare Dokumente an Sachposten in Document Capture an.
id: DC-352
lang: de
---

# Die Kategorie „Sachbeleg“

Die Kategorie „Dokumente an Sachposten anhängen“ – **SACHBELEG** – ermöglicht Continia Document Capture die OCR-Verarbeitung und das Anhängen von Dokumenten an Sachposten, sodass sie durchsuchbar werden. Die Sachposten werden in Microsoft Dynamics 365 Business Central aktualisiert, sobald Sie das Dokument registrieren.

> [!NOTE]
> Die Kategorie „Dokumente an Sachposten anhängen“ kann nicht zum Erstellen von Fibu. Buch-Blattzeilen aus Dokumenten verwendet werden. Hierzu müssen Sie die Kategorie „Einkaufsbestellungen“ verwenden. Weitere Informationen finden Sie unter [Registrierung von Belegen als Fibu. Buch.-Blattzeilen einrichten](@DC-112) und [Belege als Fibu. Buch-Blattzeilen registrieren](@DC-67#belege-als-fibu-buch-blattzeilen-registrieren).

Bevor Sie die Kategorie „Dokumente an Sachposten anhängen“ verwenden können, müssen Sie eine neue Vorlage einrichten.

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie auf der Seite **Belegkategorien** die Kategorie „Dokumente an Sachposten anhängen“ aus und klicken Sie in der Aktionsleiste auf **Bearbeiten**.
3. Wählen Sie im Inforegister **Vorlagen** die Mastervorlage aus und klicken Sie in der zugehörigen Aktionsleiste auf **Kopieren**.
4. Setzen Sie im Dialogfeld **Vorlage kopieren** das Feld **Neuer Typ** auf den leeren Wert. Klicken Sie dann auf **OK**.

## So arbeiten Sie mit der Kategorie „Dokumente an Sachposten anhängen“

Nachdem Sie die Kategorie „Dokumente an Sachposten anhängen“ eingerichtet haben, können Sie Dokumente verarbeiten, die in diese Kategorie importiert wurden.

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Klicken Sie auf der Seite **Belegkategorien** auf den Code **SACHBELEG**, um die Kategorie „Dokumente an Sachposten anhängen“ zu öffnen.
3. Wählen Sie im Belegjournal das gewünschte Dokument aus, und klicken Sie in der Aktionsleiste auf **Aktionen > Funktionen > Vorlage erstellen/auswählen**.
4. Wählen Sie im sich öffnenden Dialogfeld die gewünschte Vorlage aus. Klicken Sie dann auf **OK**.
5. Geben Sie im Inforegister **Belegkopf** die Belegnummer in das Feld **Dokumentnr.** ein. Alternativ können Sie auf die drei Punkte neben diesem Feld klicken, um die Rechnung auszuwählen, an die Sie das eingehende Dokument anhängen möchten.
6. **Optional**: Um Text im Feld **Beschreibung** zu erkennen, wählen Sie ihn entsprechend im Dokument aus.
7. Klicken Sie in der Aktionsleiste auf **Start > Registrieren**, um den Beleg zu registrieren.

## Informationen zum Thema

[Die Kategorie „Einkaufsbestellungen“](@DC-136)