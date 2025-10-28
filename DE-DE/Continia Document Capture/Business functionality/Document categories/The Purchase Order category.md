---
title: Die Kategorie Einkaufsbestellungen in Document Capture
date: 27-08-2025
description: So erstellen und aktualisieren Sie Bestellungen in Document Capture.
id: DC-136
lang: de
---

# Die Kategorie „Einkaufsbestellungen“

Mit der Kategorie für Einkaufsbestellungen – **BESTELLUNG** – können Sie in Continia Document Capture Einkaufsbestellungen automatisch erstellen und aktualisieren, basierend auf Daten, die in einem anderen Beleg erkannt wurden (zum Beispiel in der Auftragsbestätigung eines Kreditors). Die Bestellungen werden in Microsoft Dynamics 365 Business Central erstellt, sobald Sie sie registrieren.

Wenn eine Bestellung auf diese Weise erstellt wird, können Daten wie beispielsweise Artikelnummern, Preis und Menge oder praktisch alle anderen Informationen, die für Sie im Beleg des Kreditors relevant sind, erfasst werden. Die Aktualisierung von Bestellungen umfasst jedoch nur eine begrenzte Anzahl ausgewählter Felder: **Kred.-Bestellnr.**, **Kred.-Lieferungsnr.**, **Zugesagtes Wareneingangsdatum**, **Menge** und **EK-Preis**.

> [!NOTE]
> Sie können einer vorhandenen Bestellung keine Zeilen hinzufügen; Sie können jedoch vorhandene Zeilen aktualisieren. Alternativ können Sie eine andere Bestellung erstellen.

Es ist auch möglich, Lieferscheine (bzw. Empfangsbestätigungen) in der Kategorie **Einkaufsbestellungen** zu verarbeiten. Auf diese Weise können Sie Lieferscheine von Kreditoren mit einer offenen Bestellung abgleichen, das Feld **Menge akt. Lieferung** der Bestellung aktualisieren und den Einkaufsbeleg und/oder eine Rechnung buchen.

Alle drei Prozesse, das heißt die Erstellung, Aktualisierung und der Abgleich von Bestellungen, werden in den folgenden Abschnitten beschrieben.

## So erstellen Sie eine Einkaufsbestellung

So erstellen Sie eine Business Central-Bestellung auf der Grundlage eines importierten Belegs wie einer Auftragsbestätigung:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.

2. Klicken Sie auf den Code **BESTELLUNG**, um das Belegjournal für Bestellungen zu öffnen.

3. Wählen Sie in der Liste der Belege den Beleg aus, den Sie als Grundlage für die Bestellung verwenden möchten.

4. Wenn sich der Beleg auf einen neuen Kreditor bezieht, stellen Sie sicher, dass dieser eingerichtet ist und ihm eine Vorlage zugeordnet ist. Falls dies nicht der Fall ist, erstellen Sie den Kreditor, indem Sie in der Aktionsleiste auf **Kreditor > Kreditorenkarte** klicken und die Details ausfüllen. Document Capture erstellt dann eine Kopie der zugehörigen Mastervorlage und ordnet sie dem neuen Kreditor zu.

5. Klicken Sie in der Aktionsleiste auf **Start** > **Felder erkennen**, um die Felder des ausgewählten Belegs zu erfassen.

6. Überprüfen Sie, ob alle erforderlichen Felder korrekt erfasst wurden und ob im Abschnitt **Bemerkungen** unten Warnungen oder Fehlermeldungen angezeigt werden. Wenn Informationen nicht stimmen oder fehlen, korrigieren Sie sie manuell. Wenn Sie beispielsweise nicht identifizierte Feldsuchtexte oder -werte manuell erfassen möchten, finden Sie hierzu weitere Informationen unter [Felder in einem Beleg erfassen](@DC-110).

7. Gehen Sie zu **[B]estellung / [E]mpfangsbestätigung** und überprüfen Sie, ob der Buchstabe **B** in der Spalte **Wert** angezeigt wird. Wenn nicht, geben Sie den Wert manuell ein und drücken Sie dann die **Eingabetaste**.

8. Klicken Sie in der Aktionsleiste auf **Vorlage** > **Vorlagenkarte**, um die Vorlagenkarte zu öffnen.

9. Gehen Sie im Inforegister **Einkaufsbestellungen** zu **Bestellung Reg. Schritt 1** und stellen Sie sicher, dass **Bestellung erstellen** oder **Bestellung erstellen oder aktualisieren** ausgewählt ist.
   > [!NOTE]
   > Wenn **Bestellung erstellen oder aktualisieren** ausgewählt ist, verwendet Document Capture den Wert **Bestellnummer** oder **Kred.-Bestellnr.**, um automatisch zu ermitteln, ob eine neue Bestellung erstellt oder eine bestehende Bestellung aktualisiert werden soll.

10. Klicken Sie in der Aktionsleiste auf **Start** > **Registrieren**, um die neue Bestellung zu registrieren.

Die Bestellung wird dann als Geschäftseinheit in Business Central erstellt und steht zur weiteren Verarbeitung zur Verfügung.

## So aktualisieren Sie eine Einkaufsbestellung

So aktualisieren Sie eine bestehende Einkaufsbestellung:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.

2. Klicken Sie auf den Code **BESTELLUNG**, um das Belegjournal für Bestellungen zu öffnen.

3. Wählen Sie in der Liste der Belege den Beleg aus, dessen Daten Sie zum Aktualisieren einer bestehenden Bestellung verwenden möchten.

4. Klicken Sie in der Aktionsleiste auf **Start** > **Felder erkennen**, um die Felder des ausgewählten Belegs zu erfassen.

5. Überprüfen Sie, ob alle erforderlichen Felder korrekt erfasst wurden und ob im Abschnitt **Bemerkungen** unten Warnungen oder Fehlermeldungen angezeigt werden. Wenn Informationen nicht stimmen oder fehlen, korrigieren Sie sie manuell. Wenn Sie beispielsweise nicht identifizierte Feldsuchtexte oder -werte manuell erfassen möchten, finden Sie hierzu weitere Informationen unter [Felder in einem Beleg erfassen](@DC-110).

6. Gehen Sie zu **[B]estellung / [E]mpfangsbestätigung** und überprüfen Sie, ob der Buchstabe **B** in der Spalte **Wert** angezeigt wird. Wenn nicht, geben Sie den Wert manuell ein und drücken Sie dann die **Eingabetaste**.

7. Klicken Sie in der Aktionsleiste auf **Vorlage** > **Vorlagenkarte**, um die Vorlagenkarte zu öffnen.

8. Gehen Sie im Inforegister **Einkaufsbestellungen** zu **Bestellung Reg. Schritt 1** und stellen Sie sicher, dass **Bestellung aktualisieren** oder **Bestellung erstellen oder aktualisieren** ausgewählt ist.
   > [!NOTE]
   > Wenn **Bestellung erstellen oder aktualisieren** ausgewählt ist, verwendet Document Capture den Wert **Bestellnummer** oder **Kred.-Bestellnr.**, um automatisch zu ermitteln, ob eine neue Bestellung erstellt oder eine bestehende Bestellung aktualisiert werden soll.

9. Klicken Sie in der Aktionsleiste auf **Start** > **Registrieren**, um die entsprechende Bestellung zu aktualisieren.

Die bestehende Bestellung, die mit dem ausgewählten Beleg übereinstimmt, wird dann mit den Daten des ausgewählten Belegs aktualisiert.

## So aktualisieren Sie eine Bestellung auf Basis eines Lieferscheins

So aktualisieren Sie eine bestehende Bestellung auf Basis eines Lieferscheins:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.

2. Klicken Sie auf den Code **BESTELLUNG**, um das Belegjournal für Bestellungen zu öffnen.

3. Wählen Sie in der Liste der Belege den Lieferschein aus, dessen Daten Sie zum Aktualisieren einer bestehenden Bestellung verwenden möchten.

4. Klicken Sie in der Aktionsleiste auf **Start** > **Felder erkennen**, um die Felder des ausgewählten Belegs zu erfassen.

5. Überprüfen Sie, ob alle erforderlichen Felder korrekt erfasst wurden und ob im Abschnitt **Bemerkungen** unten Warnungen oder Fehlermeldungen angezeigt werden. Wenn Informationen nicht stimmen oder fehlen, korrigieren Sie sie manuell. Wenn Sie beispielsweise nicht identifizierte Feldsuchtexte oder -werte manuell erfassen möchten, finden Sie hierzu weitere Informationen unter [Felder in einem Beleg erfassen](@DC-110).

6. Gehen Sie zu **[B]estellung / [E]mpfangsbestätigung** und überprüfen Sie, ob der Buchstabe **E** in der Spalte **Wert** angezeigt wird. Wenn nicht, geben Sie den Wert manuell ein und drücken Sie dann die **Eingabetaste**.

7. Klicken Sie in der Aktionsleiste auf **Vorlage** > **Vorlagenkarte**, um die Vorlagenkarte zu öffnen.

8. Gehen Sie im Inforegister **Einkaufsbestellungen** zu **Empfangsbestätigung Reg. Schritt 1** und wählen Sie **Aktualisiere Bestellempfangsbestätigung**.

9. **Optional:** Wenn Sie die Empfangsbestätigung auch buchen möchten, gehen Sie im Inforegister **Einkaufsbestellungen** zu **Empfangsbestätigung Reg. Schritt 2** und wählen Sie entweder **Empfangsbestätigung buchen** oder **Empfangsbestätigung und Rechnung buchen**.

   > [!NOTE]
   > Wenn **Bestellung erstellen oder aktualisieren** ausgewählt ist, verwendet Document Capture den Wert **Bestellnummer** oder **Kred.-Bestellnr.**, um automatisch zu ermitteln, ob eine Bestellung erstellt oder eine bestehende Bestellung aktualisiert werden soll.

10. Klicken Sie in der Aktionsleiste auf **Start** > **Bestellabgleich**.

11. Klicken Sie in der Aktionsleiste auf **Abgleich durchführen**. Document Capture versucht anschließend, die übereinstimmenden Artikel zu finden und aktualisiert die Spalten **Abgeglichene Menge** und **Abgeglichene Gesamtmenge**.

12. Klicken Sie in der Aktionsleiste auf **Start** > **Registrieren**, um die entsprechende Bestellung zu aktualisieren.

Hierdurch wird das Feld **Menge akt. Lieferung** der bestehenden Bestellung, die mit dem ausgewählten Beleg übereinstimmt, aktualisiert und die Rechnung gebucht, falls Sie dies in Schritt 9 ausgewählt haben.

## Informationen zum Thema

[Grundlegende Konzepte in Document Capture](@DC-83)  
[Mit Belegkategorien arbeiten](@DC-78)