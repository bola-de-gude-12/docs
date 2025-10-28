---
title: Dokumente ohne Mandant (UIC) in Document Capture verwalten
date: 03-10-2025
description: So aktivieren und verwalten Sie Dokumente ohne Mandant in Document Capture.
id: DC-492
lang: de
---

# Dokumente ohne Mandant (UIC) verwalten

Wenn Ihre Microsoft Dynamics 365 Business Central-Umgebung aus mehr als einem Mandanten besteht, kann Continia Document Capture [importierte Dokumente automatisch in den richtigen Mandanten verschieben](@DC-74). Wenn der richtige Mandant nicht identifiziert werden kann, haben Sie die Möglichkeit, das zugehörige Dokument automatisch in das Buch.-Blatt **Dokumente (UIC)** zu verschieben.

> [!NOTE]
> Das Buch.-Blatt **Dokumente (UIC)** kann nur von Benutzern mit Vollzugriff auf alle Mandanten verwendet werden.

## So aktivieren Sie Dokumente ohne Mandant

1. Suchen Sie ({{search}}) nach **Document Capture Einrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Aktivieren Sie auf dem Inforegister **Allgemein** die Einstellung **Dokumente ohne Mandant (UIC) verwenden**.

## So verwalten Sie Dokumente ohne Mandant

1. Suchen Sie ({{search}}) nach **Dokumente (UIC)** und wählen Sie dann den entsprechenden Link aus.
2. Verwenden Sie bei Bedarf die **Belegkategorie** und den **Statusfilter**, um die Liste der Dokumente ohne Mandant einzugrenzen.
3. Wählen Sie das gewünschte Dokument aus und wählen Sie unter der Spalte **Verschiebe in Mandant** den Zielmandanten aus. Wiederholen Sie diesen Schritt für jedes unbekannte Dokument, das Sie verschieben möchten.
4. Klicken Sie in der Aktionsleiste auf **Start** > **In Mandant verschieben**. Alternativ können Sie <kbd>F9</kbd>drücken.

