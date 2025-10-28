---
title: Datenpflege einrichten
date: 02-12-2024
description: null
id: EM-224
lang: de
---

# Datenpflege einrichten

Je nachdem, wo Sie ansässig sind, ist es auch wichtig, Daten zu löschen, um die Datenschutz-Grundverordnung (DSGVO) der Europäischen Union oder ähnliche Vorschriften einzuhalten. Mit der DSGVO-Datenpflegefunktion in Expense Management können Sie nicht nur Begriffe und Werte, sondern auch Belege, Belegdatensätze und alle zugehörigen Anhänge löschen.

Bevor Sie die Datenpflege durchführen können, müssen Sie wie unten beschrieben die Aufbewahrungsdauer für Suchdaten und DSGVO-Daten angeben. Sie können die Datenpflege manuell ausführen oder Aufgabenwarteschlangen einrichten, die dies automatisch erledigen.

In den Feldern **Aufbewahrungsfrist (Jahre)** und **DSGVO-Aufbewahrungsdauer (Jahre)** wird die Anzahl der abgeschlossenen _Geschäftsjahre_ angegeben, die Belegdaten gespeichert werden, wenn die Datenpflege ausgeführt wird. Das Minimum ist dabei jeweils 2 bzw. 5 Jahre.  Dieser Prozess basiert auf dem Belegstatus, das heißt, er schließt nur gebuchte Belege ein, und die Aufbewahrungsfrist wird ab dem Buchungsdatum des Belegs berechnet.

## So konfigurieren Sie die Einstellungen für die DSGVO-Konformität

Um anzugeben, wie viele Jahre DSGVO-relevante Daten (das heißt Begriffe und Werte, die Belege selbst und alle zugehörigen Anhänge) gespeichert werden, bevor sie mithilfe der Datenpflege gelöscht werden können, führen Sie die folgenden Schritte aus:

1. Wählen Sie das Symbol {{search}}, geben Sie **Expense Management Einrichtung** ein und wählen Sie dann den zugehörigen Link.

2. Gehen Sie im Inforegister **Allgemein** unter **Datenpflege** zum Feld **DSGVO-Aufbewahrungsdauer (Jahre)** und geben Sie an, wie viele Jahre die DSGVO-relevanten Daten gespeichert werden sollen.

   > [!NOTE]
   > Wenn unter **Kreditoren & Einkauf Einr.** > **Löschen des Belegs zulassen vor** ein Datum angegeben ist, wird dieses Datum auch berücksichtigt, um zu berechnen, wann die DSGVO-relevanten Daten frühestens gelöscht werden können.
   >
   > Für die DSGVO-Datenpflege sind auch die Secure Archive-Einstellungen relevant. Wenn **Secure Archive** aktiviert ist, gilt auch die im Feld **Minimaler Archivierungszeitraum** angegebene Anzahl von Jahren.
   >
   > In diesem Fall wird die Einstellung mit dem längsten Speicherungszeitraum angewendet. Wenn die **DSGVO-Aufbewahrungsdauer (Jahre)** beispielsweise auf _5 Jahre_ festgelegt ist, das Datum **Löschen des Belegs zulassen vor** eine Speicherung der Daten für _3 Jahre_ vorsieht und **Minimaler Archivierungszeitraum** auf _9 Jahre_ festgelegt ist, werden die Daten _9 Jahre_ gespeichert (sofern Secure Archive aktiviert ist).

3. Um die DSGVO-Datenpflegeaktion von der Seite **Expense Management** auszuführen, gehen Sie zu **Aktionen** > **Funktionen** und wählen Sie dann **DSGVO-Datenpflege ausführen** aus.

Informationen zum Ausführen der Datenpflege mit Aufgabenwarteschlangen finden Sie unter [Aufgabenwarteschlangen einrichten](Setting up job queues.md).

## Informationen zum Thema

[Secure Archive](@EM-189)
