---
title: Umgang mit Abweichungen, einschließlich Teilabgleich
date: 31-08-2022
description: So verwalten Sie Preis- und Mengenabweichungen und führen Teilabgleich von Belegen durch
id: DC-63
lang: de
---

# Umgang mit Abweichungen, einschließlich Teilabgleich

Auch der in Rechnung gestellte Preis der bestellten Waren kann gelegentlich von dem Preis in der Bestellung abweichen. Für solche Abweichungen gibt es unterschiedliche Lösungen, je nach Art der Abweichung (in Bezug auf [Menge](#teilabgleich-mengenabweichungen) oder [Preis](#preisabweichungen)) und je nachdem, ob Ihr Unternehmen Belege manuell oder automatisch abgleicht.

> [!NOTE]
> Der Einfachheit halber werden in diesem Artikel alle Mengenabweichungen als _Teilabgleich bzw. teilweiser Abgleich_ bezeichnet, obwohl Kunden in den meisten Fällen weniger Artikel in Rechnung gestellt werden, als sie bestellt/erhalten haben, und nicht mehr.

## Teilabgleich (Mengenabweichungen)

Beim Abgleich zweier Belege wird in Continia Document Capture standardmäßig davon ausgegangen, dass die gesamte ausstehende Menge jeder relevanten Zeile mit dem zugehörigen Beleg übereinstimmt. Weicht die gelieferte Menge jedoch von der fakturierten Menge ab, muss stattdessen ein Teilabgleich durchgeführt werden. Wenn Sie beispielsweise 10 Laptops bestellt und erhalten haben, Ihnen aber nur 7 Laptops in Rechnung gestellt wurden, sollte die abgeglichene Menge 7 und nicht die gesamte ausstehende Menge von 10 Laptops betragen.

Ein Teilabglich kann entweder [manuell](#manueller-teilabgleich) oder [automatisch](#automatischer-teilabgleich) ausgeführt werden, je nachdem, wie Sie Ihren Belegabgleich abwickeln. Dies unterscheidet sich bei beiden Methoden erheblich.

### Manueller Teilabgleich

Wenn Belege in Ihrem Unternehmen manuell abgeglichen werden, können Sie einen Teilabgleich folgendermaßen ausführen:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Wählen Sie den Code **EINKAUF** aus, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste den Beleg aus (Rechnung oder Gutschrift), den Sie mit anderen Belegen abgleichen möchten.
4. Klicken Sie in der Aktionsleiste auf **Start** > **Bestellabgleich**.
5. Unter **Abgleich Übersicht** werden in zwei Zeilenabschnitten relevante Zeilen aus zugehörigen Belegen aufgelistet, abhängig davon, welchen Belegtyp Sie oben in Schritt 3 ausgewählt haben. Wählen Sie in einem dieser Abschnitte die Belegzeile aus, die Sie manuell bearbeiten möchten.
6. Geben Sie im Feld **Abgeglichene Menge** die richtige Menge ein (normalerweise die Menge der entsprechenden Zeile in der Rechnung oder Gutschrift, die Sie in Schritt 3 ausgewählt haben).
7. Wiederholen Sie die Schritte 5 bis 6 für alle anderen relevanten Zeilen in diesem Zeilenabschnitt und/oder im anderen Abschnitt.

Wenn Sie den Abgleichvorgang abgeschlossen haben, können Sie zurück zum Belegjournal navigieren, um den abgeglichenen Beleg zu registrieren oder anderweitig zu verarbeiten.

> [!TIP]
> Allgemeine Informationen zum manuellen Abgleich finden Sie unter [Manueller Belegabgleich](@DC-62).

### Automatischer Teilabgleich

Wenn Belege in Ihrem Unternehmen automatisch abgeglichen werden, gibt es in Document Capture zwei Möglichkeiten, Mengenabweichungen automatisch zu verarbeiten, je nachdem, ob Sie bei der Einrichtung Zeilenabgleich aktiviert haben oder nicht:

[**Wenn Zeilenabgleich aktiviert wurde**](@DC-69), verwendet Document Capture die in der Rechnung oder Gutschrift erkannten Zeilenwerte, um die Menge in den entsprechenden Belegzeilen abzugleichen. Die abgeglichene Menge entspricht immer der erkannten Menge der entsprechenden Rechnungs-/Gutschriftenzeile. Um einen Teilabgleich zu ermöglichen, muss die Option **Menge abgleichen** in der Einrichtung auf **Nein** gesetzt werden.

**Wenn Kopfabgleich verwendet wird und in der Einrichtung eine Abweichung definiert wurde**, fügt Document Capture der Rechnung oder Gutschrift eine neu erstellte Abweichungszeile hinzu, wenn die Differenz zwischen dem Gesamtbetrag der Rechnung/Gutschrift und dem des abzugleichenden Belegs innerhalb der definierten Abweichung liegt. Die Abweichungszeile erhält dann einen Betrag, der der Differenz zwischen dem Gesamtbetrag der Rechnung/Gutschrift und dem Gesamtbetrag der übereinstimmenden Zeilen aus dem Beleg entspricht. Wenn die Abweichungszeile dazugerechnet wird, stimmen die Beleggesamtbeträge genau wie vorgesehen überein.

> [!TIP]
> Allgemeine Informationen zum automatischen Abgleich finden Sie unter [Automatischer Belegabgleich](@DC-70).

## Preisabweichungen

Genau wie beim Abgleich von Mengen geht Document Capture standardmäßig davon aus, dass der Preis der gelieferten Waren dem Preis entspricht, zu dem die Waren bestellt wurden. Dies ist jedoch nicht immer der Fall und daher kann es erforderlich sein, Preisabweichungen bearbeiten zu müssen. Dies kann entweder [manuell](#preisabweichungen-manuell-ausgleichen) oder [automatisch](#preisabweichungen-automatisch-ausgleichen) erfolgen, je nachdem, wie Sie den Belegabgleich in Ihrem Unternehmen abwickeln. Dies unterscheidet sich bei beiden Methoden erheblich.

### Preisabweichungen manuell verarbeiten

Wenn Belege in Ihrem Unternehmen manuell abgeglichen werden, gehen Sie folgendermaßen vor, um Preisabweichungen im Abgleichprozess manuell zu bearbeiten:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.

2. Wählen Sie den Code **EINKAUF** aus, um das Belegjournal zu öffnen.

3. Wählen Sie in der Belegliste den Beleg aus (Rechnung oder Gutschrift), den Sie mit anderen Belegen abgleichen möchten.

4. Klicken Sie in der Aktionsleiste auf **Start** > **Bestellabgleich**.

5. Unter **Abgleich Übersicht** werden in zwei Zeilenabschnitten relevante Zeilen aus zugehörigen Belegen aufgelistet, abhängig davon, welchen Belegtyp Sie oben in Schritt 3 ausgewählt haben. Wählen Sie in einem dieser Abschnitte die Belegzeile aus, die Sie manuell bearbeiten möchten.

6. Geben Sie im Feld **EK-Preis (Rechnung)** oder **EK-Preis (Gutschrift)** (wenn Sie in Schritt 3 eine Gutschrift ausgewählt haben) den korrekten Preis für jeden gelieferten Artikel in der ausgewählte Zeile ein. Normalerweise handelt es sich dabei um den Preis der entsprechenden Zeile der Rechnung oder Gutschrift, die Sie in Schritt 3 ausgewählt haben.

7. Geben Sie im Feld **Zeilenrabatt %** bei Bedarf den korrekten Prozentsatz für den Zeilenrabatt ein.

   > [!NOTE]
   > Das Feld **Zeilenrabatt %** muss möglicherweise zuerst hinzugefügt werden, damit es sichtbar ist. [Personalisieren](https://docs.microsoft.com/de-de/dynamics365/business-central/ui-personalization-user) Sie die Seite hierzu folgendermaßen: Wählen Sie das Symbol {{settings}} > **Personalisieren** > **+ Feld**, um den Bereich **Feld der Seite hinzufügen** zu öffnen. Wählen Sie den entsprechenden Zeilenbereich und ziehen Sie dann das Feld **Zeilenrabatt %** aus dem Bereich in die Tabelle im ausgewählten Zeilenbereich. Wählen Sie **Fertig**, um das Banner **Personalisierung** zu schließen.

8. Wiederholen Sie die Schritte 5 bis 7 für alle anderen relevanten Zeilen in diesem Zeilenabschnitt und/oder im anderen Abschnitt.

Wenn Sie den Abgleichvorgang abgeschlossen haben, können Sie zurück zum Belegjournal navigieren, um den abgeglichenen Beleg zu registrieren oder anderweitig zu verarbeiten.

> [!TIP]
> Allgemeine Informationen zum manuellen Abgleich finden Sie unter [Manueller Belegabgleich](@DC-62).

### Preisabweichungen automatisch verarbeiten

Wenn Belege in Ihrem Unternehmen automatisch abgeglichen werden, gibt es in Document Capture zwei Möglichkeiten, Preisabweichungen automatisch zu verarbeiten, je nachdem, ob Sie bei der Einrichtung Zeilenabgleich aktiviert haben oder nicht:

[**Wenn Zeilenabgleich aktiviert wurde**](@DC-69), verwendet Document Capture den Einstandspreis aus der erkannten Rechnungs- oder Gutschriftenzeile. Wenn Sie in der Einrichtung unter **Zeilenabgleich** die Option **EK-Preis abgleichen** auf **Ja – immer** oder **Ja – wenn vorhanden** gesetzt haben, müssen der Einstandspreis der Rechnungs-/Gutschriftenzeile und der Einstandspreis der zugehörigen Belegzeile übereinstimmen; andernfalls können die Belegzeilen nicht automatisch abgeglichen werden. Sie können jedoch in den Einstellungen einen Abweichungsbetrag oder -prozentsatz angeben, wodurch die beiden Einstandspreise innerhalb der angegebenen Varianz voneinander abweichen dürfen.

**Wenn Kopfzeilenabgleich statt Zeilenabgleich verwendet wird**, sind die Zeilendetails der Rechnung oder Gutschrift unbekannt. Bei möglichen Abweichungen beim Gesamtbetrag (zum Beispiel aufgrund einer Mengenabweichung) fügt Document Capture der registrierten Rechnung/Gutschrift eine neue Zeile (eine Abweichungszeile) hinzu. Die abgeglichene Menge der Rechnung/Gutschrift entspricht immer der Menge der zugehörigen Belegzeile. Wenn die Abweichungszeile dazugerechnet wird, stimmen die Beleggesamtbeträge genau wie vorgesehen überein.

> [!NOTE]
> Wenn Kopfabgleich verwendet wird und _keine Abweichung in der Einrichtung definiert wurde_, kann Document Capture die Preisabweichung nicht verarbeiten und der Abgleich kann nicht durchgeführt werden.

> [!TIP]
> Allgemeine Informationen zum automatischen Abgleich finden Sie unter [Automatischer Belegabgleich](@DC-70).

## Informationen zum Thema

[Zeilen beim Abgleich filtern](@DC-64)