---
title: eDocuments-Tabellenstrukturen in Document Capture
date: 07-03-2025
description: Eine kurze Beschreibung der Tabellenstrukturen von eDocuments.
id: DC-181
lang: de
---

# eDocuments-Tabellenstrukturen

Mit Continia eDocuments werden Dokumentdaten mithilfe einer Reihe vordefinierter Tabellen strukturiert gespeichert. Dadurch kann Continia Document Capture die Dokumente in den bekannten Seiten- und Tabellenformaten darstellen, die allen Benutzern von Microsoft Dynamics 365 Business Central vertraut sind.

Wenn Sie also eine XML-Datei mit Continia eDocuments empfangen (importieren) oder senden (exportieren), wird die Datei wie gewohnt als Business Central-Datensatz mit drei allgemeinen Bereichen für die Dokumentenkarte angezeigt:

- Ein Inforegister **Allgemein** mit verschiedenen Kopffeldern.
- Ein Inforegister **Zeilen** mit einer Übersicht aller Belegzeilen im Tabellenformat.
- Zusätzliche Dokumentendetails, einschließlich Inforegistern wie **Bestelldetails**, **Versand und Zahlung**, **Lieferung**, **Referenz** und **Technische Informationen**.

Anstatt einer XML-Datei, die im Allgemeinen nicht gut lesbar und nicht einfach zu bearbeiten ist, können Sie in Continia eDocuments mit einer Dokumentenkarte arbeiten, die wie die anderen Standardseiten für Dokumente bzw. Belege in Business Central formatiert sind. Solche Dokumentenkarten – oder Datensätze – sind für eAbrechnungsdokumente, eBestellungsdokumente, eAbrechnung-Antwortdokumente und eBestellung-Antwortdokumente verfügbar.

> [!NOTE]
> Wenn Datensätze erstellt werden, werden Sie in Continia eDocuments mit den Nummernserien benannt, die sie beim [Einrichten von Continia eDocuments](@DC-179) angegeben haben.

Einer der Hauptvorteile von diesem Ansatz besteht darin, dass Sie Dokumentdetails direkt in der Benutzeroberfläche hinzufügen oder korrigieren können, wenn die Validierung eines Dokuments aufgrund fehlender oder falscher Daten fehlschlägt. Sie müssen keine komplexen XML-Dateien bearbeiten oder Ihren Partner um Unterstützung bitten, wenn ein Dokument Fehler enthält. Geben Sie stattdessen die korrekten oder fehlenden Daten in das entsprechende Feld auf der Dokumentenkarte des Dokuments ein, dessen Validierung fehlgeschlagen ist.

Durch die Darstellung von XML-Dateien als standardmäßige Business Central-Dokumentenseiten können Sie (oder Ihr Partner) zusätzliche Felder hinzufügen oder nach bestimmten Werten filtern, um das Gesuchte zu finden. Im Allgemeinen können Sie XML-Dateien auf dieselbe Weise verwenden und bearbeiten wie andere Dokumente Business Central in auch.