---
title: Expense Management Speicher anpassen
date: 22-08-2022
description: Passen Sie Ihren Expense Management-Speicher an, indem Sie die Methode erweitern oder überschreiben, wie Dokumente gespeichert und abgerufen werden.
id: EM-92
lang: de
---

# Speicher anpassen

Expense Management bietet Unterstützung für drei verschiedene Speichermodelle: **Dateisystem**, **Datenbank** und **Azure Blob Storage**. Sie können Ihren Speicher aber auch anpassen, indem Sie die Methode erweitern oder überschreiben, wie Dokumente in Expense Management gespeichert und abgerufen werden. Sie können dies mithilfe von vier verschiedenen Publisher Events, die in der Codeunit **CEM Doc. File Events** bereitgestellt werden, überschreiben oder erweitern.

- **SetAttachment**: Wird aufgerufen, wenn die Speicherung einer Datei angefordert wird.
- **GetAttachment**: Wird aufgerufen, wenn eine Datei angefordert wird.
- **HasAttachment**: Wird aufgerufen, wenn überprüft wird, ob eine Datei vorhanden ist.
- **ClearAttachment**: Wird aufgerufen, wenn die Löschung einer Datei angefordert wird, beispielsweise wenn ein mit der entsprechenden Datei verknüpftes Dokument gelöscht oder importiert wird.

PDF-Dokumente werden in Seiten aufgeteilt, die im Add-In angezeigt werden. Sie können mit den Bildern mit den folgenden Events interagieren:

- **SetPage**: Wird aufgerufen, wenn die Speicherung einer Datei angefordert wird.
- **GetPage**: Wird aufgerufen, wenn eine Datei angefordert wird.
- **HasPage**: Wird aufgerufen, wenn überprüft wird, ob eine Datei vorhanden ist.
- **ClearPage**: Wird aufgerufen, wenn die Löschung einer Datei angefordert wird, beispielsweise wenn ein mit der entsprechenden Datei verknüpftes Dokument gelöscht oder importiert wird.

In mehreren Lokalisierungen ist eine Dokumentsignatur erforderlich. In diesen Fällen können die folgenden Events zur Interaktion mit digital signierten PDF-Dokumenten verwendet werden:

- **SetPDF**: Wird aufgerufen, wenn die Speicherung einer Datei angefordert wird.
- **GetPDF**: Wird aufgerufen, wenn eine Datei angefordert wird.
- **HasPDF**: Wird aufgerufen, wenn überprüft wird, ob eine Datei vorhanden ist.
- **ClearPDF**: Wird aufgerufen, wenn die Löschung einer Datei angefordert wird, beispielsweise wenn ein mit der entsprechenden Datei verknüpftes Dokument gelöscht oder importiert wird.

In Expense Management werden alle Dateien zunächst von Continia Online in einen Puffer mit der Bezeichnung Attachment Inbox heruntergeladen. Aus diesem Grund stehen alle Events auch für Posteingangsprozesse zur Verfügung. Dazu gehören:

- **SetInboxAttachment**: Wird aufgerufen, wenn die Speicherung einer Datei angefordert wird.
- **GetInboxAttachment**: Wird aufgerufen, wenn eine Datei angefordert wird.
- **HasInboxAttachment**: Wird aufgerufen, wenn überprüft wird, ob eine Datei vorhanden ist.
- **ClearInboxAttachment**: Wird aufgerufen, wenn die Löschung einer Datei angefordert wird, beispielsweise wenn ein mit der entsprechenden Datei verknüpftes Dokument gelöscht oder importiert wird.
- **SetInboxPage**: Wird aufgerufen, wenn die Speicherung einer Datei angefordert wird.
- **GetInboxPage**: Wird aufgerufen, wenn die Speicherung einer Datei angefordert wird.
- **HasInboxPage**: Wird aufgerufen, wenn überprüft wird, ob eine PDF-Seite vorhanden ist.
- **ClearInboxPage**: Wird aufgerufen, wenn die Löschung einer PDF-Seite angefordert wird, beispielsweise wenn ein mit der entsprechenden Datei verknüpftes Dokument gelöscht oder importiert wird.
- **SetInboxPDF**: Wird aufgerufen, wenn die Speicherung einer digital signierten PDF-Datei angefordert wird.
- **GetInboxPDF**: Wird aufgerufen, wenn eine digital signierte PDF-Datei angefordert wird.
- **HasInboxPDF**: Wird aufgerufen, wenn überprüft wird, ob eine digital signierte PDF-Datei vorhanden ist.
- **ClearInboxPDF**: Wird aufgerufen, wenn die Löschung einer digital signierten PDF-Datei angefordert wird, beispielsweise wenn ein mit der entsprechenden Datei verknüpftes Dokument gelöscht oder importiert wird.

Alle oben genannten Methoden verwenden ein _handled_-Pattern, das es Programmierern ermöglicht, das Verhalten zu überschreiben oder zu erweitern. Wenn _Handled_ auf _true_ gesetzt ist, erfolgen in Expense Management keine Aktionen, da erwartet wird, dass der Dateivorgang vom Erweiterungscode gehandhabt wird. Wenn für _Handled_ kein Wert festgelegt ist, führt der Code den Dateivorgang gemäß dem in der Expense Management Einrichtung Einrichtung ausgewählten Speichermodell aus. Auf diese Weise ist es möglich, eine Teilmenge der Dateien zu erweitern und extern zu speichern und die Dateispeicherung dennoch von Expense Management verwalten zu lassen.

Alle Methoden haben die folgenden Argumente:

- EMAttachment: Ein Verweis auf den Anhangsdatensatz, der alle Informationen zum Anhang enthält.

- Success: Ein Boolescher Wert, der angibt, ob der Vorgang erfolgreich war. Dieser Wert wird nur weitergegeben, wenn der Wert für _Handled_ ebenfalls auf _true_ gesetzt ist.

**OnSet()** und **OnGet()** haben einen zusätzlichen Parameter, _TempFile_, bei dem es sich um einen **CDC Temp File** Datensatz handelt. Der **CDC Temp File**-Datensatz ist als Dateiobjekt zu betrachten, da er Dateiinformationen und den Inhalt der Datei enthält. Das Feld **Data** im Datensatz enthält die Daten der Datei, die entweder gespeichert oder abgerufen werden. Wenn Sie also **OnSet()** abonnieren, enthält das Feld **Data** den Inhalt der zu speichernden Datei, während bei **OnGet()** der Inhalt der angeforderten Datei im Feld **Data** angezeigt werden sollte.

> [!NOTE]
> Da die oben genannten Vorgänge von verschiedenen Routinen in Expense Management aufgerufen werden, wie z. B. dem Dokumentimport, dürfen im ausgeführten Code keine Fehler vorhanden sein, da dies die vorhandene Funktionalität beeinträchtigen oder unterbrechen würde.

> [!IMPORTANT]
> Die Erweiterung der Dokumentenspeicherung ist mit Risiken verbunden. Continia Software kann nicht für verloren gegangene oder fehlende Dokumente haftbar gemacht werden, wenn dieser Teil von Expense Management erweitert wird.