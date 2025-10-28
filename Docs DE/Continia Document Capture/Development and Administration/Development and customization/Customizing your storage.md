---
title: Anpassen des Speichers in Document Capture
date: 16-06-2025
description: Passen Sie Ihren Document Capture-Speicher an, indem Sie die Methode erweitern oder überschreiben, wie Dokumente gespeichert und abgerufen werden.
id: DC-73
lang: de
---

# Speicher anpassen

Document Capture bietet Unterstützung für drei verschiedene Speichermodelle: **Dateisystem**, **Datenbank** und **Azure Blob Storage**. Sie können Ihren Speicher aber auch anpassen, indem Sie die Methode erweitern oder überschreiben, wie Dokumente in Document Capture gespeichert und abgerufen werden. Sie können dies mithilfe von vier verschiedenen Publisher Events, die in der Codeunit **CDC Doc. File Events** bereitgestellt werden, überschreiben oder erweitern.

- **OnSetFile**: Wird aufgerufen, wenn die Speicherung einer Datei angefordert wird.
- **OnGetFile**: Wird aufgerufen, wenn eine Datei angefordert wird.
- **OnHasFile**: Wird aufgerufen, wenn die Existenz einer Datei überprüft wird.
- **OnClearFile**: Wird aufgerufen, wenn die Löschung einer Datei angefordert wird, beispielsweise wenn ein mit der entsprechenden Datei verknüpftes Dokument gelöscht oder importiert wird.

Alle oben genannten Methoden verwenden ein _handled_-Pattern, das es Programmierern ermöglicht, das Verhalten zu überschreiben oder zu erweitern. Wenn _Handled_ auf _true_ gesetzt ist, erfolgen in Document Capture keine Aktionen, da erwartet wird, dass der Dateivorgang vom Erweiterungscode gehandhabt wird. Wenn für _Handled_ kein Wert festgelegt ist, führt der Code den Dateivorgang gemäß dem in der Document Capture Einrichtung ausgewählten Speichermodell aus. Auf diese Weise ist es möglich, eine Teilmenge der Dateien zu erweitern und extern zu speichern und die Dateispeicherung dennoch von Document Capture verwalten zu lassen.

Alle Methoden haben die folgenden Argumente:

- _Filename_: Der Name der Datei, die gespeichert oder abgerufen wird. Der Dateiname wird von Document Capture festgelegt und ist eine eindeutige Dateikennung innerhalb des aktuellen Mandanten.
- _Company_: Der Name des Mandanten, in dem der Dateivorgang stattfindet. Zusammen identifizieren _Filename_ und _Company_ eine Datei eindeutig innerhalb einer bestimmten Datenbank.
- _DocumentNo_: Das Feld **Nr.** des **CDC Document**-Datensatzes, für den der Dateivorgang ausgeführt wird.
- _FileType_: Identifiziert den Typ der gespeicherten oder abgerufenen Datei. Dies kann verwendet werden, wenn nur bestimmte Dateitypen vom Benutzercode verarbeitet werden sollen. Die möglichen Typen werden in der Codeunit **CDC Document File Interface** aufgelistet und können folgendermaßen identifiziert werden: _TiffFileType_, _PdfFileType_, _MiscFileType_, _PageFileType_, _EmailFileType_, _HtmlFileType_, _XmlOriginalFileType_ und _XmlTrimmedFileType_.
- _Result_: Ein Boolescher Wert, der angibt, ob der Vorgang erfolgreich war. Dieser Wert wird nur weitergegeben, wenn der Wert für _Handled_ ebenfalls auf _true_ gesetzt ist.

**OnSetFile** und **OnGetFile** haben einen zusätzlichen Parameter, _TempFile_, der ein **CDC Temp File**-Datensatz ist. Der **CDC Temp File**-Datensatz ist als Dateiobjekt zu betrachten, da er Dateiinformationen und den Inhalt der Datei enthält. Das Feld **Data** im Datensatz enthält die Daten der Datei, die entweder gespeichert oder abgerufen werden. Wenn Sie also **OnSetFile** abonnieren, enthält das Feld **Data** den Inhalt der zu speichernden Datei, während bei **OnGetFile** der Inhalt der angeforderten Datei im Feld **Data** erscheinen sollte.

> [!NOTE]
> Da die oben genannten Vorgänge von verschiedenen Routinen in Document Capture aufgerufen werden, wie z. B. dem Dokumentimport, dürfen im ausgeführten Code keine Fehler vorhanden sein, da dies die vorhandene Funktionalität beeinträchtigen oder unterbrechen würde.

> [!IMPORTANT]
> Die Erweiterung der Dokumentenspeicherung ist mit Risiken verbunden. Continia Software kann nicht für verloren gegangene oder fehlende Dokumente haftbar gemacht werden, wenn dieser Teil von Document Capture erweitert wird.