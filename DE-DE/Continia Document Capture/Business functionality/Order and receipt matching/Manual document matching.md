---
title: Manueller Belegabgleich
date: 07-07-2022
description: So gleichen Sie eingehende Einkaufsrechnungen und Gutschriften manuell mit zugehörigen Belegen ab
id: DC-62
lang: de
---

# Manueller Belegabgleich

Beim manuellen Belegabgleich können Sie die Belege manuell auswählen, die miteinander abgeglichen werden sollen. Sie können beispielsweise bei einer eingehenden Einkaufsrechnung die abzugleichende Bestellung aus einer Liste offener Einkaufsbestellungen auswählen und so den Abgleichprozess selbst durchführen. Dies bietet sich besonders in Unternehmen an, in denen meist nur wenige Belege eingehen.

Abgleich ist nur in der Kategorie **EINKAUF** verfügbar und wird entweder auf der Seite **Bestellabgleich** oder der Seite **Gutschrift Abgleich** durchgeführt, je nachdem, welchen Belegtyp Sie im Belegjournal abgleichen möchten.

## So gleichen Sie Belege manuell ab

Wenn Sie einen eingehenden Beleg (entweder eine Rechnung oder eine Gutschrift) mit zugehörigen Belegen abgleichen möchten, gehen Sie folgendermaßen vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.

2. Wählen Sie den Code **EINKAUF** aus, um das Belegjournal zu öffnen.

3. Wählen Sie in der Belegliste den Beleg aus, den Sie mit anderen Belegen abgleichen möchten.

   > [!NOTE]
   > Der von Ihnen ausgewählte Beleg bestimmt, wo der Abgleich durchgeführt wird, mit welchen Belegtypen ein Abgleich durchgeführt werden kann und welche Zeilenabschnitte unter **Abgleich Übersicht** in Schritt 5 unten angezeigt werden:
   >
   > - Wenn Sie eine Rechnung auswählen, können Sie auf der Seite **Bestellabgleich** einen Abgleich mit _Bestellungen_ und _Einkaufslieferungen_ durchführen. Dies wird dann in den angezeigten Abschnitten entsprechend reflektiert.
   > - Wenn Sie eine Gutschrift auswählen, können Sie auf der Seite **Gutschrift Abgleich** einen Abgleich mit _Reklamationen_ und _Rücksendungen_ durchführen. Dies wird dann in den angezeigten Abschnitten entsprechend reflektiert.

4. Klicken Sie in der Aktionsleiste auf **Start** > **Bestellabgleich**.

5. Unter **Abgleich Übersicht** werden in zwei Zeilenabschnitten relevante Zeilen aus zugehörigen Belegen aufgelistet, abhängig davon, welchen Belegtyp Sie oben in Schritt 3 ausgewählt haben. Wählen Sie in einem der Abschnitte die entsprechende(n) Belegzeile(n) aus und wählen Sie dann **Zeile** > **Zeilen abgleichen**.

   > [!NOTE]
   > Mit der Aktion **Zeilen abgleichen** wird das Feld **Abgeglichene Menge** der ausgewählten Zeile(n) mit der ausstehenden Menge aktualisiert. Wenn dieses Feld bereits einen Wert enthält, wird der Wert durch Auswahl von **Zeilen abgleichen** auf Null zurückgesetzt.

6. Wenn Sie Anpassungen an einigen Werten vornehmen müssen, beispielsweise aufgrund von [Mengen- oder Preisabweichungen](@DC-63), können Sie die folgenden Felder manuell bearbeiten:
   - **Abgeglichene Menge**
   - **EK-Preis (Rechnung)** oder **EK-Preis (Gutschrift)**
   - **Zeilenrabatt % (Rechnung)** oder **Zeilenrabatt % (Gutschrift)**

7. Wiederholen Sie die Schritte 5 bis 6 für den anderen Zeilenabschnitt. Dies ist relevant, wenn Sie einen Abgleich mit beiden Zeilentypen durchführen müssen und wenn in beiden Abschnitten Zeilen zur Auswahl stehen.

   > [!TIP]
   > Wenn Sie weitere Informationen zu einer Belegzeile anzeigen möchten, wählen Sie die Zeile im entsprechenden Zeilenabschnitt aus und wählen Sie dann **Zeile** > **Karte**, um die Dokumentenkarte für diese Zeile zu öffnen.

Jede Zeile, für die Sie **Zeilen abgleichen** auswählen oder manuell einen Wert eingeben, wird fett dargestellt, um anzuzeigen, dass sie mit dem Beleg abgeglichen wurde. Darüber hinaus wird der abgeglichene Zeilenbetrag dem Betrag im Abschnitt **Abgleich Übersicht** oben hinzugerechnet, um den Status des Abgleichprozesses anzuzeigen:

<br>

| Feld                     | Beschreibung                                                                                                                                                                                                                                                                                         |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Rechnungsbetrag**      | Der in diesem Feld angezeigte Betrag entspricht dem Gesamtrechnungsbetrag, sofern in der Rechnung keine Frachtkosten, Umweltabgaben o. Ä. Solche Gebühren und Kosten werden normalerweise vom Rechnungsbetrag im Feld **Rechnungsbetrag** abgezogen. |
| **Abgeglichener Betrag** | Der Wert in **Abgeglichener Betrag** beträgt zunächst null und erhöht sich, wenn Zeilen abgeglichen werden. Die Beträge in den Feldern **Abgeglichener Betrag** und **Rechnungsbetrag** sollten nach Abschluss des Abgleichs übereinstimmen.                         |
| **Differenz**            | Dieses Feld gibt die Differenz zwischen **Rechnungsbetrag** und **Abgeglichener Betrag** an. Sobald der Abgleich abgeschlossen ist, sollte die Differenz Null betragen.                                                                                              |

Wenn die **Differenz** Null beträgt (oder innerhalb der von Ihnen festgelegten Abweichung liegt), haben Sie den Abgleichvorgang abgeschlossen. Sie können jetzt zurück zum Belegjournal navigieren, wo im Bemerkungsbereich unten ein neuer Eintrag **Manueller Abgleich** angezeigt wird.

Der Beleg kann jetzt zur weiteren Verarbeitung [registriert](@DC-67) werden.

## Informationen zum Thema

[Zeilen beim Abgleich filtern](@DC-64)\
[Umgang mit Abweichungen, einschließlich Teilabgleich](@DC-63)