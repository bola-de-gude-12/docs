---
title: Rabatte verwalten
date: 01-10-2024
description:
id: DC-227
lang: de
---

# Rabatte verwalten

In diesem Artikel wird der Umgang mit Rabatten in Continia Document Capture beschrieben.

Obwohl Rabatte eine Standardfunktion von Microsoft Dynamics 365 Business Central sind, müssen bei ihrer Verwendung entweder die Felder **Rechnungsrab.-Betrag** oder **Rechnungsrabatt in %** manuell ausgefüllt werden.

Mit Document Capture können Sie einen Rabattbetrag in einem Dokument erfassen und automatisch in die Standardrabattfelder für Rechnungen übertragen.

## Rabatte erfassen

Die folgenden Anweisungen setzen voraus, dass Sie das Feld **Rechnungsrab.-Betrag** bereits zur gewünschten Vorlage hinzugefügt haben und dass Sie wissen, wie Sie Document Capture trainieren, um Werte zu finden. Weitere Informationen finden Sie unter [Kopffelder in einem Beleg erfassen](@DC-110).

So erfassen Sie einen Rabatt:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, in diesem Fall **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste den Beleg aus, den Sie registrieren möchten.
4. Klicken Sie in der Aktionsleiste auf **Start** > **Felder erkennen** und stellen Sie sicher, dass alle Werte, einschließlich des Rabatts, korrekt erfasst wurden.
   > [!NOTE]
   > Standardmäßig werden Rabatte als negative Beträge erfasst. Wenn ein erfasster Rabatt bereits das Minuszeichen enthält, gehen Sie zur Vorlagenfeldkarte **Rechnungsrab.-Betrag** und deaktivieren Sie die Einstellung **Vorzeichen ändern** im Inforegister **Allgemein**.
5. Wenn es keine Fehler gibt, wählen Sie **Start** > **Registrieren**, um die Rechnung zu registrieren.
6. Überprüfen Sie auf der Seite **Einkaufsrechnung** die in die Felder **Rechnungsrab.-Betrag** und **Rechnungsrabatt in %** übertragenen Werte unten im Inforegister **Allgemein**.
   > [!NOTE]
   > Rabatte werden vom **Betrag ohne MwSt.** abgezogen.

## Informationen zum Thema

[Umgang mit Abweichungen, einschließlich Teilabgleich](@DC-63)