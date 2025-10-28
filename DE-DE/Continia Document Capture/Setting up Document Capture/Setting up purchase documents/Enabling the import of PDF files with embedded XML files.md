---
title: Den Import von PDF-Dateien mit eingebetteten XML-Dateien (ZUGFeRD, XRechnung) in Document Capture aktivieren
date: 09-10-2025
description: So aktivieren Sie den Import von PDF-Dateien mit eingebetteten XML-Dokumenten in Document Capture.
id: DC-40
lang: de
---

# Import von PDF-Dateien mit eingebetteten XML-Dateien aktivieren (ZUGFeRD, XRechnung)

Für den deutschen Markt unterstützt Continia Document Capture den Import und die Verarbeitung von PDF-Dateien, in die XML-Dokumente eingebettet sind, zum Beispiel Formate wie ZUGFeRD und XRechnung.

Wenn derartige Dateien an den OCR-Dienst gesendet und in Document Capture importiert werden, werden die eingebetteten XML-Dokumente beim Import automatisch extrahiert und verarbeitet. Bei jeder importierten Datei wird auch die Original-PDF-Datei in der Belegkategorie **XMLATTACH** an den Beleg angehängt.

> [!IMPORTANT]
>
> - Um Daten aus extrahierten XML-Dokumenten verarbeiten zu können, müssen Sie die Master- und Identifikationsvorlagen XRECHNUNG-CII XML entweder von Continia Online oder aus dem Document Capture-Produktpaket importieren.
> - Wenn die Belegkategorie **XMLATTACH** nicht angezeigt wird, importieren Sie sie über die unterstützte Einrichtung **Document Capture einrichten**.

## So aktivieren Sie den Import eingebetteter XML-Dateien

> [!NOTE]
> Die folgenden Voraussetzungen und Anforderungen müssen hierfür erfüllt sein:
>
> - Sie müssen Version 8 (oder später) des Document Capture-Dienstes (OCR) ausführen.
> - Bei On-Premises-Bereitstellungen von Microsoft Dynamics NAV/Business Central müssen Sie über eine aktive Lizenz für das XML-Importmodul in Document Capture verfügen.
>
> Eine Liste der derzeit unterstützten Formate finden Sie unter [Unterstützte ektronische Dokumentformate](@DC-55).

Um den Import eingebetteter XML-Dateien zu aktivieren und die allgemeine OCR-Verarbeitung eingehender Dokumente zu konfigurieren, gehen Sie folgendermaßen vor:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Öffnen Sie die entsprechende Belegkategorie. Um beispielsweise die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**) aus, und klicken Sie auf **Bearbeiten** in der Aktionsleiste.
3. Konfigurieren Sie im Inforegister **OCR-Verarbeitung** die Einstellungen nach Bedarf, und aktivieren Sie die Einstellung **PDF mit eingebetteten XML-Dateien verarbeiten**.

## Informationen zum Thema

[Elektronische Dokumente in Deutschland importieren](@DC-195)