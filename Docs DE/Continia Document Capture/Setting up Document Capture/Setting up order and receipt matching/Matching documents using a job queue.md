---
title: Abgleichen von Dokumenten mithilfe einer Aufgabenwarteschlange in Document Capture
date: 16-06-2025
id: DC-479
description:
lang: de
---

# Belege mit einer Aufgabenwarteschlange abgleichen

Der automatische Abgleich kann durch andere Geschäftsprozesse blockiert oder behindert werden. Beispielsweise kann eine verspätete Warenlieferung den automatischen Abgleich einer Rechnung in Continia Document Capture mit einem Wareneingang aufhalten, wenn der Wareneingang zum Zeitpunkt des Rechnungseingangs in Ihrer Kreditorenbuchhaltung noch nicht erfolgt ist. In solchen Fällen ist die Ausführung der sogenannten „Batch Match“-Aufgabenwarteschlange (d. h. Stapelabgleich) praktisch, da diese in regelmäßigen Abständen versucht, den automatischen Abgleich wiederholt durchzuführen. Im obigen Beispiel würde man mit der Aufgabenwarteschlange sicherstellen, dass die Rechnung mit dem entsprechenden Wareneingang abgeglichen wird, sobald die Ware eingetroffen ist.

Um diese Aufgabenwarteschlange auszuführen, müssen Sie Codeunit 6086022 **CDC Batch Match Documents** verwenden. Weitere Informationen zum Einrichten der Aufgabenwarteschlange finden Sie unter [Aufgabenwarteschlangen einrichten](/Continia Document Capture/Setting up Document Capture/Setting up general business functionality/Setting up job queues.md).
