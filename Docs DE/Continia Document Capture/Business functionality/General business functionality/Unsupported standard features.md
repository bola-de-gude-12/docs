---
title: Nicht unterstützte Standardfunktionen in Document Capture
date: 23-06-2025
description: Eine Liste der Funktionen, die derzeit von Document Capture nicht unterstützt werden.
id: DC-134
lang: de
---

# Nicht unterstützte Standardfunktionen

Continia Document Capture bietet umfangreiche und komplexe Funktionen, die den meisten Anforderungen und Wünschen von Unternehmen gerecht werden. In Kombination mit der insgesamt herausragenden Leistungsfähigkeit steht Ihnen hiermit die sicherlich fortschrittlichste Lösung auf dem Markt für den Import, die OCR-Verarbeitung, die Registrierung, die Genehmigung und die Archivierung von Geschäftsbelegen in Microsoft Dynamics 365 Business Central zur Verfügung.

Allerdings gibt es auch einige Standardfunktionen, die derzeit in Document Capture nicht unterstützt werden. Dazu gehören die [unten erwähnten Funktionen](#unten-erwahnten-funktionen).

## Derzeit nicht unterstützte Funktionen

Die folgenden Funktionen werden derzeit weder unterstützt noch sind sie für die zukünftige Entwicklung geplant (obwohl sie langfristig jedoch möglicherweise hinzugefügt werden):

- Buchung im Hintergrund (bzw. Buchung über Aufgabenwarteschlangen) von Rechnungen/Gutschriften, die mit Bestellungen/Reklamationen abgeglichen wurden.
- Wenn Sie einen Abgleich mit einer Bestellung durchführen, erhält Continia die Bestellung, bevor die Rechnung ausgestellt wird. Da im Empfangsprozess Commits durchgeführt werden, wurde die Vorschaufunktion blockiert. Wenn Sie die Vorschaufunktion benötigen, müssen Sie einen Abgleich mit einer Lieferung durchführen.
- Abgrenzungscodes in Zuordnungen.
- Bestimmte Workflow-Optionen:
  - Für die Workflow-Antwortoption **Genehmigertyp** unterstützt Document Capture nicht die Optionen **Genehmiger** und **Workflow-Benutzergruppe** – nur **Verkäufer/Einkäufer** wird akzeptiert. Für die erweiterte Genehmigung wird nur der Typ **Genehmiger** unterstützt.
  - Für die Workflow-Antwortoption **Einschränkungsart Genehmiger** unterstützt Document Capture nicht die Optionen **Direkter Genehmiger**, **Erster qualifizierter Genehmiger** und **Spezifischer Genehmiger** – nur **Genehmigerkette** wird akzeptiert.

## Neu unterstützte Funktionen

Die folgenden bisher nicht unterstützten Funktionen werden jetzt in Document Capture unterstützt:

- Ab Document Capture 2023 R1 (v11) werden Vorauszahlungen unterstützt. Weitere Informationen finden Sie unter [So registrieren Sie Vorauszahlungsrechnungen](@DC-67#so-registrieren-sie-vorauszahlungsrechnungen).
- Ab Document Capture 2024 R1 SP2 (v24) hat die in Business Central verfügbare Standardfunktion **Doppelte Datensätze zusammenführen** folgende Auswirkung: es werden die Document Capture-Dokumente zusammengeführt, die mit den zusammengeführten Debitoren/Kreditoren verknüpft sind.
- Ab Document Capture 2024 R2 (v25) ist es möglich, die festen Umlagekonten von Business Central zu verwenden. Weitere Informationen finden Sie unter [Umlagekonten verwenden](@DC-226).
- Ab Document Capture 2025 R1 (v26): an die gebuchte Einkaufsrechnung angehängte Belege werden als Drag-and-Drop-Anhänge in das resultierende Dokument kopiert, wenn Sie **Korrigieren**, **Stornieren** oder **Korrekturgutschrift erstellen** für die gebuchte Einkaufsrechnung verwenden. Beachten Sie, dass dies ab Document Capture 2025 R1 SP2 (v26.2) nicht für Belege gilt, die einer gebuchten Einkaufsrechnung aus einer Bestellung beigefügt sind.

## Informationen zum Thema

[Geschäftsfunktionen](@DC-50)