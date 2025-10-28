---
title: Datenpflege in Document Capture einrichten
date: 21-01-2025
description: So richten Sie die Datenpflege für Document Capture-Tabellen ein
id: DC-187
lang: de
---

# Datenpflege einrichten

Bei der Belegverarbeitung mit OCR in Continia Document Capture fallen mit der Zeit große Datenmengen an. Diese Daten können für Freitextsuchen im Belegjournal verwendet werden (z. B. die Suche nach Kontaktnamen auf einer Rechnung). Der Großteil dieser Daten wird jedoch meist nicht benötigt. Ab einem bestimmten Punkt kann das Speichern großer Datenmengen sogar die Suchfunktion beeinträchtigen und andere Prozesse verlangsamen, wie zum Beispiel das Importieren von Dokumenten und das Erkennen von Feldern. Es empfiehlt sich daher, nicht mehr benötigte Daten zu löschen.

Je nachdem, wo Sie ansässig sind, ist es auch wichtig, Daten zu löschen, um die Datenschutz-Grundverordnung (DSGVO) der Europäischen Union oder ähnliche Vorschriften einzuhalten. Mit der DSGVO-Datenpflegefunktion in Document Capture können Sie nicht nur Begriffe und Werte, sondern auch Belege, Belegdatensätze und alle zugehörigen Anhänge löschen.

Bevor Sie die Datenpflege durchführen können, müssen Sie wie unten beschrieben die Aufbewahrungsdauer für Suchdaten und DSGVO-Daten angeben. Sie können die Datenpflege manuell ausführen oder Aufgabenwarteschlangen einrichten, die dies automatisch erledigen.

In den Feldern **Aufbewahrungsfrist (Jahre)** und **DSGVO-Aufbewahrungsdauer (Jahre)** wird die Anzahl der abgeschlossenen _Geschäftsjahre_ angegeben, die Belegdaten gespeichert werden, wenn die Datenpflege ausgeführt wird. Das Minimum ist dabei jeweils 2 bzw. 5 Jahre.  Dieser Prozess basiert auf dem Belegstatus, das heißt, er schließt nur gebuchte Belege ein, und die Aufbewahrungsfrist wird ab dem Buchungsdatum des Belegs berechnet.

Das folgende Video beschreibt die wichtigsten Datenpflegefunktionen:

<br>

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src=https://player.vimeo.com/video/924643920?h=b599c81bb3&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479 frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="DC_Data maintenance_produced"></iframe></div><script src=https://player.vimeo.com/api/player.js></script>

## So konfigurieren Sie Datenpflegeeinstellungen

Um festzulegen, wie viele Jahre die Suchdaten gespeichert werden, bevor sie mit der Datenpflege gelöscht werden können, gehen Sie folgendermaßen vor:

1. Suchen Sie ({{search}}) nach **Document Capture Einrichtung** und wählen Sie dann den entsprechenden Link aus.

2. Gehen Sie im Inforegister **Allgemein** unter **Datenpflege** zum Feld **Aufbewahrungsfrist (Jahre)** und geben Sie an, wie viele Jahre die Suchdaten gespeichert werden sollen.

   > [!NOTE]
   > Wenn unter **Kreditoren & Einkauf Einr.** > **Löschen des Belegs zulassen vor** ein Datum angegeben ist, wird dieses Datum auch berücksichtigt, um zu berechnen, wann Suchdaten frühestens gelöscht werden können.
   >
   > In diesem Fall wird die Einstellung mit dem längeren Speicherungszeitraum angewendet. Wenn die **Aufbewahrungsfrist (Jahre)** beispielsweise auf _2 Jahre_ festgelegt ist, das Datum **Löschen des Belegs zulassen vor** jedoch eine Speicherung der Daten für _3 Jahre_ vorsieht, werden die Daten _3 Jahre_ gespeichert.

3. Um die Datenpflegeaktion von der Seite **Document Capture Einrichtung** auszuführen, gehen Sie zu **Aktionen** > **Funktionen** und wählen Sie dann **Datenpflege ausführen** aus.

   > [!IMPORTANT]
   > Die in Dokumenten erfassten eigentlichen Werte werden nicht gelöscht, nur ihre Suchtexte. Somit kann die Funktion **Dokumentsuche** für alle erfassten Daten verwendet werden und die Werte sind weiterhin vorhanden, bis das Dokument über die DSGVO-Datenpflegefunktion gelöscht wird. Darüber hinaus wird ein minimaler Speicherverbrauch sichergestellt, während die Suchfunktion für alle erfassten Informationen verfügbar bleibt.

## So konfigurieren Sie die Einstellungen für die DSGVO-Konformität

Um anzugeben, wie viele Jahre DSGVO-relevante Daten (das heißt Begriffe und Werte, die Belege selbst und alle zugehörigen Anhänge) gespeichert werden, bevor sie mithilfe der Datenpflege gelöscht werden können, führen Sie die folgenden Schritte aus:

1. Suchen Sie ({{search}}) nach **Document Capture Einrichtung** und wählen Sie dann den entsprechenden Link aus.

2. Gehen Sie im Inforegister **Allgemein** unter **Datenpflege** zum Feld **DSGVO-Aufbewahrungsdauer (Jahre)** und geben Sie an, wie viele Jahre die DSGVO-relevanten Daten gespeichert werden sollen.

   > [!NOTE]
   > Wenn unter **Kreditoren & Einkauf Einr.** > **Löschen des Belegs zulassen vor** ein Datum angegeben ist, wird dieses Datum auch berücksichtigt, um zu berechnen, wann die DSGVO-relevanten Daten frühestens gelöscht werden können.
   >
   > Für die DSGVO-Datenpflege sind auch die Secure Archive-Einstellungen relevant. Wenn **Secure Archive** aktiviert ist, gilt auch die im Feld **Minimaler Archivierungszeitraum** angegebene Anzahl von Jahren.
   >
   > In diesem Fall wird die Einstellung mit dem längsten Speicherungszeitraum angewendet. Wenn die **DSGVO-Aufbewahrungsdauer (Jahre)** beispielsweise auf _5 Jahre_ festgelegt ist, das Datum **Löschen des Belegs zulassen vor** eine Speicherung der Daten für _3 Jahre_ vorsieht und **Minimaler Archivierungszeitraum** auf _9 Jahre_ festgelegt ist, werden die Daten _9 Jahre_ gespeichert (sofern Secure Archive aktiviert ist).

3. Um die DSGVO-Datenpflegeaktion von der Seite **Document Capture Einrichtung** auszuführen, gehen Sie zu **Aktionen** > **Funktionen** und wählen Sie dann **DSGVO-Datenpflege ausführen** aus.

Informationen zum Ausführen der Datenpflege mit Aufgabenwarteschlangen finden Sie unter [Aufgabenwarteschlangen einrichten](Setting up job queues.md).

## Informationen zum Thema

[Aufgabewarteschlangen einrichten](Setting up job queues.md)  
[Secure Archive](@DC-154)

