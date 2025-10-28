---
title: Die Kategorie „Verkaufsaufträge und -gutschriften“
date: 27-08-2025
description: So erstellen und aktualisieren Sie Verkaufsaufträge und Gutschriften in Document Capture.
id: DC-459
lang: de
---

# Die Kategorie „Verkaufsaufträge und -gutschriften“

Mit der Kategorie „Verkaufsaufträge und -gutschriften“ – **VERKAUF** – in Continia Document Capture können Sie Verkaufsaufträge und Gutschriften automatisch erstellen und aktualisieren, basierend auf Daten, die in einem anderen Dokument erkannt wurden (normalerweise eine Bestellung eines Debitors). Die Verkaufsaufträge und Gutschriften werden in Microsoft Dynamics 365 Business Central erstellt, sobald Sie sie registrieren.

Wenn ein Verkaufsauftrag auf diese Weise erstellt wird, können Daten wie beispielsweise Bestell- und Lieferdaten, Artikelnummern und Menge oder praktisch alle anderen Informationen, die für Sie im Beleg des Debitors relevant sind, erfasst werden.

Dieser Artikel konzentriert sich auf Verkaufsaufträge; die darin enthaltenen Anweisungen gelten jedoch auch für Gutschriften.

## So erstellen Sie einen Verkaufsauftrag

So erstellen Sie einen Business Central-Verkaufsauftrag basierend auf einem importierten Dokument:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.

2. Klicken Sie auf den Code **VERKAUF**, um das Belegjournal für Verkaufsaufträge und Gutschriften zu öffnen.

3. Wählen Sie in der Liste der Belege den Beleg aus, den Sie als Grundlage für den Verkaufsauftrag verwenden möchten.

4. Wenn sich der Beleg auf einen neuen Debitor bezieht, stellen Sie sicher, dass diesem eine Vorlage zugeordnet ist. Falls dies nicht der Fall ist, erstellen Sie den Debitor, indem Sie in der Aktionsleiste auf **Debitor > Debitorenkarte** klicken und die Details ausfüllen. Document Capture erstellt dann eine Kopie der zugehörigen Mastervorlage und ordnet sie dem neuen Debitor zu.

5. Klicken Sie in der Aktionsleiste auf **Start > Felder erkennen**, um die Felder des ausgewählten Belegs zu erfassen.

6. Überprüfen Sie, ob alle erforderlichen Felder korrekt erfasst wurden und ob im Abschnitt **Bemerkungen** unten Warnungen oder Fehlermeldungen angezeigt werden. Wenn Informationen nicht stimmen oder fehlen, korrigieren Sie sie manuell. Wenn Sie beispielsweise nicht identifizierte Feldsuchtexte oder -werte manuell erfassen möchten, finden Sie hierzu weitere Informationen unter [Felder in einem Beleg erfassen](@DC-110).

   > [!NOTE]
   > In den meisten Fällen ist die Erfassung von Beträgen nicht erforderlich, da Ihre Preise und andere betragsbezogene Werte direkt aus Business Central stammen sollten.

7. **Optional:** Bei Bedarf können Sie auch eine manuelle oder KI-gestützte Zeilenerkennung in den Verkaufsaufträgen durchführen. Weitere Informationen finden Sie unter [Zeilenfelder in einem Beleg erfassen (Zeilenerkennung)](@DC-147).

8. Klicken Sie in der Aktionsleiste auf **Start** > **Registrieren**, um den neuen Verkaufsauftrag zu registrieren.

Der Verkaufsauftrag wird dann als Geschäftseinheit in Business Central erstellt und steht zur weiteren Verarbeitung zur Verfügung.

## Informationen zum Thema

[Grundlegende Konzepte in Document Capture](@DC-83)  
[Mit Belegkategorien arbeiten](@DC-78)