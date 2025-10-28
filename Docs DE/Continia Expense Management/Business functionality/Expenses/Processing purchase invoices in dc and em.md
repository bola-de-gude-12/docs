---
title: Einkaufsrechnungen in Document Capture und Expense Management verarbeiten
date: 17-03-2025
description: Erfahren Sie, wie Sie doppelte Buchungen in EM und DC vermeiden.
id: EM-277
lang: de
---

# Einkaufsrechnungen in Document Capture und Expense Management verarbeiten

Kunden, die sowohl Document Capture als auch Expense Management verwenden, können ihren Arbeitsablauf jetzt optimieren, indem sie denselben Einkauf in beiden Lösungen abwickeln. Document Capture bietet eine einfache Möglichkeit für die Einkaufsabwicklung und die Nutzung der optischen Zeichenerkennung (OCR), und Expense Management übernimmt die Zahlungsabwicklung und Rückerstattungen.

Durch die Integration von Document Capture und Expense Management wird sichergestellt, dass nach der Verarbeitung eines Einkaufs mit Document Capture in Expense Management nur noch die Zahlung und Rückerstattung vorgenommen wird. Dadurch wird vermieden, dass eine doppelte Einkauftransaktion erstellt wird. Integrierte Prüfungen in den Anwendungen machen Sie darauf aufmerksam, wenn ähnliche Einkäufe erkannt werden, und vermeiden so Doppelbuchungen.

Einen kurzen Überblick gibt das folgende Video.

<iframe src=https://player.vimeo.com/video/1020171075?h=ad9b32a8ca&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479 width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media" title="EM_Process invoices with DC"></iframe>

## Einkaufsrechnungen in beiden Lösungen verarbeiten

So verarbeiten Sie eine Einkaufsrechnung in Document Capture und Expense Management:

1. Öffnen Sie Expense Management in Business Central.
2. Suchen {{search}} Sie nach **Belege** und wählen Sie dann den zugehörigen Link.
3. Wird eine Rechnung erkannt, erscheint automatisch ein Kommentar. Das System identifiziert das Dokument als Rechnung anhand von OCR-Daten, die von der Expense App und dem Expense Portal extrahiert wurden, und synchronisiert das Dokument dann mit Business Central.
4. Senden Sie die Rechnung an Document Capture. Wählen Sie in der Aktionsleiste **Start** > **Verarbeiten mit Document Capture**.
5. Nach der OCR-Verarbeitung kann der Beleg wie jeder andere DC-Beleg über den Stapel für den Belegimport importiert werden. Weitere Informationen finden Sie unter [Belege in Document Capture registrieren](@DC-67).
6. Setzen Sie den Genehmigungsprozess für den Beleg in Expense Management fort und buchen Sie den Beleg.
7. Gehen Sie in Document Capture zur Seite **Geb. Einkaufsrechnungen** und verwenden Sie die Funktion **Posten suchen**, um zu bestätigen, dass die Rechnung nur einmal als Document Capture-Rechnung und als Beleg in Expense Management verarbeitet wurde. Alternativ können Sie zur Seite **Gebuchte Belege** in Expense Management gehen.

Die Rückerstattung an den Benutzer erfolgt nach der Buchung des Document Capture-Belegs und der zugehörigen Rechnung.

## Grundlegendes zur Konvertierung von Bildern in PDF

Sie können bildbasierte Rechnungen automatisch in PDFs konvertieren, um eine nahtlose Integration mit Document Capture zu ermöglichen.

Wenn Sie Belege verarbeiten und **Verarbeiten mit Document Capture** auswählen, werden unterstützte Dokumente im Bildformat automatisch in PDF konvertiert, bevor sie an Document Capture gesendet werden. Dies führt zu einer effizienteren und genaueren Rechnungsverarbeitung.

## Informationen zum Thema

[Belege buchen](@EM-11)