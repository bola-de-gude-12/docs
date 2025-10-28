---
title: Bearbeitungsgebühren
date: 13-07-2023
description: null
id: EM-163
lang: de
---

# Bearbeitungsgebühren

Für im Ausland getätigte Käufe im Rahmen von Finanztransaktionen erheben Banken üblicherweise Jahres- oder Transaktionsgebühren. Diese Gebühren sind häufig in regulären Belegen und Kauftransaktionen enthalten, sodass es schwierig ist, sie voneinander zu unterscheiden.

Expense Management kann bestimmte Transaktionen von der Buchung ausschließen, indem Abstimmungsregeln angewendet werden und diese einer bestimmten Belegart zugewiesen werden. Mit dieser Funktion können Transaktionen anhand bestimmter Schlüsselwörter identifiziert und von Expense Management vom Buchungsprozess ausgeschlossen werden.

Diese Funktionalität ist insbesondere bei Transaktionen mit Gebühren nützlich. Kreditkartengebühren gelten beispielsweise nicht als Ausgaben und der Buchhalter möchte sie möglicherweise vorübergehend ausschließen und sie beim Erhalt der Rechnungen von den Kreditkartenanbietern separat behandeln.

Continia Expense Management bietet zwei Methoden zum Ausschließen von Gebühren:

1. Sie werden von Continia Expense Management ausgeschlossen und manuell in der Finanzabteilung verarbeitet.
2. Sie können sie so konfigurieren, dass keine Anhänge erforderlich sind, und der Prozess mithilfe von Unternehmensrichtlinien automatisch abgewickelt wird.

## So schließen Sie bestimmte Transaktionen mit Abstimmungsregeln aus

Um Gebühren automatisch auszuschließen, können Sie eine separate Belegart speziell für Gebühren erstellen und so konfigurieren, dass Transaktionen ausgeschlossen werden. Darüber hinaus können Sie die Funktion **Ausblenden für Expense Benutzer** aktivieren, um zu verhindern, dass Benutzer versehentlich Belege für Gebühren erstellen.

Um dies einzurichten, müssen Sie zunächst die Gebühr ermitteln. Sie können beispielsweise nach dem Text suchen, der das Wort „Gebühr“ enthält, oder nach einer Eintrags-ID mit einer eindeutigen Kennung. Hier sind zwei Beispiele:

- **Mastercard Smartdata-Gebühren** – diese Gebühren werden als _Finanzielle Anpassungen_ bezeichnet; Sie können nach diesem bestimmten Wert oder dem Eintragstyp 5900 filtern.
- **Danske Bank Telekort-Gebühren** – Gebühren, einschließlich Kreditkartengebühren für Käufe außerhalb der EU, werden unter Buchungsart 5100 gebucht. Darüber hinaus sendet die Danske Bank veraltete Transaktionen mit einer bestimmten Kartennummer, die als Filterkriterium verwendet werden kann.

So schließen Sie Gebühren automatisch aus:

1. Wählen Sie das Symbol {{search}}, geben Sie **Belegarten** ein, und wählen Sie dann den zugehörigen Link.

2. Wählen Sie in der Aktionsleiste **Neu** aus, um eine separate Belegart für Gebühren hinzuzufügen. Fügen Sie einen Namen und eine Beschreibung hinzu und aktivieren Sie das Kontrollkästchen in der Spalte **Transaktionen ausschließen**. Zum Beispiel:
   - **Code** – Geben Sie den Code an, zum Beispiel _GEBÜHR_.
   - **Beschreibung** – Fügen Sie eine Beschreibung hinzu. Beispiel: _Gebühren und Kosten_.
   - **Suchbegriff** – Fügen Sie einen Suchbegriff hinzu. Beispiel: _Gebühren und Kosten_.
   - **Ausblenden für Expense Benutzer** – wenn diese Option ausgewählt ist, wird die Belegart in der App und im Portal ausgeblendet. Zum Beispiel, wenn Sie möchten, dass die Gebühr nur von Buchhaltern bearbeitet wird.
   - **Transaktionen ausschließen** – wenn diese Option ausgewählt ist, wird der Betrag der Banktransaktion vom Beleg ausgeschlossen. Aktivieren Sie für dieses Beispiel das Kontrollkästchen.

3. Um die Gebühr zu identifizieren, müssen Sie eine Regel hinzufügen. Wählen Sie das Symbol {{search}}, geben Sie **Banktransaktionen** ein, und wählen Sie dann den zugehörigen Link.

4. Wählen Sie in der Aktionsleiste **Abstimmungsregeln** aus.

5. Auf der Seite **Bankenabstimmungsregeln** können Sie mit einer Kennung eine neue Regel zum Ermitteln der Gebühr hinzufügen. Um beispielsweise die Telekort-Gebühren der Dansk Bank auszuschließen, definieren Sie folgende Regel:

   - **Regelnr.** – Fügen Sie die Regelnummer hinzu, um festzulegen, wann die Regel angewendet werden soll.

   - **Feldnr.** – Fügen Sie die Feldnummer hinzu, auf die die Regel angewendet werden soll.

   - **Feldname** - Gibt den Namen des Felds an, das für die Regel ausgewählt wurde.

   - **Wert** – Fügen Sie den Wert hinzu, für den die Regel gelten soll. In diesem Beispiel 5100.

   - **Belegart** – Fügen Sie GEBÜHR hinzu, um die Ausgabe zu kategorisieren.

Wenn ein Beleg mit dem Suchbegriff _Gebühr_ oder der angegebenen Regel für die Buchungsart übereinstimmt, wird ihr automatisch die Belegart **Gebühr** zugewiesen und sie wird von der weiteren Verarbeitung im System ausgeschlossen. Obwohl sie in der Tabelle für Banktransaktionen verbleibt, wird sie durch den voreingestellten Filter ausgeblendet und es werden für diese ausgeschlossenen Transaktionen keine Buchungen im Hauptbuch generiert.

So zeigen Sie die ausgeschlossenen Transaktionen an:

1. Wählen Sie das Symbol {{search}}, geben Sie **Banktransaktionen** ein, und wählen Sie dann den zugehörigen Link.

2. Wählen Sie in der Aktionsleiste **Filterbereich anzeigen** aus.

3. Navigieren Sie im Bereich „Ansichten“ zu **Eintrag ausschließen** und stellen Sie das Dropdown-Feld auf **Nein** ein.

## So schließen Sie Gebühren aus, indem Sie Anhänge optional machen

Der Prozess zum Verwalten von Gebühren kann automatisiert werden. Passen Sie hierfür die Einstellungen an, sodass keine Anhänge mehr erforderlich sind, und Unternehmensrichtlinien angewendet werden.

So schließen Sie Gebühren mithilfe optionaler Anhänge aus:

1. Wählen Sie das Symbol {{search}}, geben Sie **Belegarten** ein, und wählen Sie dann den zugehörigen Link.

2. Wählen Sie in der Aktionsleiste **Neu** aus, um eine separate Belegart für Gebühren hinzuzufügen. Fügen Sie einen Namen und eine Beschreibung hinzu und stellen Sie sicher, dass die Spalte **Anhang** auf _Optional_ gesetzt ist. Zum Beispiel:
   - **Code** – Geben Sie den Code an, zum Beispiel _ZU BUCHENDE GEBÜHREN_.
   - **Beschreibung** – Fügen Sie eine Beschreibung hinzu. Beispiel: _Zu buchende Gebühren_.
   - **Suchname** – Fügen Sie einen Suchnamen hinzu. Beispiel: _Zu buchende Gebühren_.
   - **Anhang** – Gibt an, ob das Unternehmen einen Anhang verlangt. Die Optionen sind: _Empfohlen_, _Obligatorisch_ und _Optional_. Um Gebühren automatisch auszuschließen, wählen Sie _Optional_ aus.
   - **Ausblenden für Expense Benutzer** – Wählen Sie diese Option, wenn Sie verhindern möchten, dass Benutzer sie versehentlich verwenden.

3. Wählen Sie das Symbol {{search}}, geben Sie **Unternehmensrichtlinien** ein, und wählen Sie dann den zugehörigen Link.

4. Fügen Sie eine neue Richtlinie hinzu, um Ausgaben unter einem bestimmten Betrag automatisch zu genehmigen. Zum Beispiel:
   - **Benutzertyp** – Benutzergruppe
   - **Benutzercode** - INT
   - **Aktion** - Belege unter 1000 Euro automatisch genehmigen.
   - **Betrag** - 1.000, 00

5. Wählen Sie das Symbol {{search}}, geben Sie **Banktransaktionen** ein, und wählen Sie dann den zugehörigen Link.

6. Wählen Sie in der Aktionsleiste **Abstimmungsregeln** aus.

7. Auf der Seite **Bankenabstimmungsregeln** können Sie mit einer Kennung eine neue Regel zum Ermitteln der Gebühr hinzufügen. Um beispielsweise die Telekort-Gebühren der Dansk Bank auszuschließen, definieren Sie folgende Regel:

   - **Regelnr.** – Fügen Sie die Regelnummer hinzu, um festzulegen, wann die Regel angewendet werden soll.

   - **Feldnr.** – Fügen Sie die Feldnummer hinzu, auf die die Regel angewendet werden soll.

   - **Feldname** - Gibt den Namen des Felds an, das für die Regel ausgewählt wurde.

   - **Wert** – Fügen Sie den Wert hinzu, für den die Regel gelten soll. In diesem Beispiel _Gebühr_.

   - **Belegart** – Fügen Sie ZU BUCHENDE GEBÜHREN hinzu, um die Ausgabe zu kategorisieren.

Expense Management scannt alle Banktransaktionen und gleicht sie anhand des Schlüsselworts _Gebühr_ oder einer anderen angegebenen Buchungstypregel ab. Nach der Zuordnung wird den Transaktionen die Belegart zugewiesen, z. B. die Belegart ZU BUCHENDE GEBÜHREN. Entsprechend Ihren Einstellungen ist kein Anhang erforderlich. Daher werden die Beträge für diese Belegart nicht an den Expense-Benutzer gesendet.

Anschließend wird die konfigurierte Unternehmensrichtlinie angewendet und sowohl der Beleg als auch die Banktransaktion werden auf _Freigegeben_ gesetzt. Sie können dann gebucht werden.
