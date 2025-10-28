---
title: Automatischer Import von Kreditkartentransaktionen
date: 22-03-2024
description: Eine Einführung in den automatischen Import von Kreditkartentransaktionen in Continia Expense Management
id: EM-202
lang: de
---

# Automatischer Import von Kreditkartentransaktionen

Der automatische Import Ihrer Kreditkartentransaktionen direkt in Continia Expense Management bietet Ihnen eine einfache Möglichkeit, Prozesse in Ihrem Unternehmen zu optimieren. Dies hilft Ihnen, alle Ausgaben Ihrer Mitarbeiter und Kreditkarten im Auge zu behalten, und ist bei weitem der einfachste Weg, um Ihre Transaktionen in Microsoft Dynamics 365 Business Central zu übertragen.

Ihre Optionen für den Import von Kreditkartentransaktionen in Expense Management hängen davon ab, welche Kreditkarte(n) Sie in Ihrem Unternehmen verwenden. Continia unterstützt alle gängigen Kreditkarten, darunter Mastercard, Visa, American Express und Eurocard, sowie eine große Anzahl weiterer Kartentypen. Um mehr über die verschiedenen Optionen sowie die erforderlichen Schritte zur Einrichtung zu erfahren, wählen Sie unten Ihren Kreditkartentyp aus:

- [Kreditkartenvereinbarungen aktivieren](Activating credit card agreements.md)
- [American Express](Importing American Express transactions.md)
- [Mastercard](@EM-279)
- [Visa](@EM-281)
- [Eurocard](@EM-162)
- [Andere Karten](Importing transactions from other cards.md)

Im Allgemeinen unterstützt Continia Tausende von Szenarien und eine Vielzahl von Banken weltweit. Sie müssen lediglich Ihre Bank bitten, sich mit [Ihrem Continia-Partner](/Continia Expense Management/Getting Started/Resellers and Partners/Find a Reseller.md) in Verbindung zu setzen, und Ihr Partner übernimmt die weitere Abwicklung, natürlich unter der Voraussetzung, dass Ihre Bank einverstanden ist und technisch in der Lage ist, Transaktionen an Expense Management zu senden.

> [!IMPORTANT]
> Wenn Sie sich nicht sicher sind, ob Ihre Bank Transaktionen in Expense Management exportieren kann, wenden Sie sich bitte an Ihre Bank und bitten Sie sie, sich an [Ihren Continia-Partner](/Continia Expense Management/Getting Started/Resellers and Partners/Find a Reseller.md) zu wenden. Ihr Continia-Partner wird dann mit Continia zusammenarbeiten, um die bestmögliche Lösung für Ihr Unternehmen zu finden.

## So richten Sie den automatischen Import von Kreditkartentransaktionen ein

Um Kreditkartentransaktionen automatisch in Expense Management zu importieren, befolgen Sie diese Schritte:

1. Kontaktieren Sie Ihre Bank, um eine Vereinbarung zu treffen, mit der sie Kreditkartentransaktionen an Expense Management senden kann.
   > [!NOTE]
   > Bevor Sie die Aktivierung in Business Central anfordern, muss eine Vereinbarung mit der Bank bestehen. Sie können innerhalb von Business Central keine Bankvereinbarung anfordern.
2. Da es für die verschiedenen Kreditkarten jeweils spezifische Vorgehensweisen gibt, informieren Sie bitte Ihre Bank, dass Sie die entsprechenden Richtlinien und Informationen zu den verschiedenen Kartentypen bei Bedarf unter den folgenden Links finden:
   - [American Express](Importing American Express transactions.md)
   - [Mastercard](@EM-279)
   - [Visa](@EM-281)
   - [Eurocard](@EM-162)
   - [Andere Karten](Importing transactions from other cards.md)
3. Warten Sie auf die Bestätigung Ihrer Bank, dass die Vereinbarung aktiviert wurde und die Bank begonnen hat, Kreditkartentransaktionen an Continia zu senden. Sobald Sie die Bestätigung erhalten haben, können Sie die Aktivierung in Business Central anfordern.
4. Um eine Vereinbarung in Expense Management zu aktivieren, gehen Sie folgendermaßen vor:
   1. Wählen Sie das Symbol {{search}}, geben Sie **Bankvereinbarungen** ein, und wählen Sie dann den zugehörigen Link.
   2. Wählen Sie in der Aktionsleiste **Neue Vereinbarung anfordern** aus, um die unterstützte Einrichtungsanleitung **Bankvereinbarung Aktivierung** zu öffnen.
   3. Wählen Sie **Weiter**.
   4. Füllen Sie alle Felder mit den relevanten Transaktionsdetails aus.
      > [!NOTE]
      > Um sicherzustellen, dass die von Ihnen übermittelte Transaktion in den von Ihrer Bank an Continia gesendeten Daten enthalten ist, achten Sie darauf, eine Transaktion auszuwählen, die ausgeführt wurde, nachdem Ihre Bank die Aktivierung der Vereinbarung bestätigt hat. Die von Ihnen gewählte Transaktion sollte mindestens 1–2 Tage nach dem Datum stattgefunden haben, an dem Ihre Bank mit der Übermittlung der Transaktionsdaten an Continia begonnen hat.
      >
      > Vermeiden Sie die Verwendung von Gebühren und anderen allgemeinen Transaktionen. Je eindeutiger der Text und der Betrag sind, desto besser.
      >
      > Wenn Sie die letzten sechs Ziffern der Kartennummer nicht kennen, reicht in der Regel die Eingabe der letzten vier Ziffern.
   5. Wenn Sie alle Angaben eingegeben haben, wählen Sie **Weiter**.
   6. Wählen Sie **Fertig**, um die unterstützte Einrichtung zu schließen.

Sie haben jetzt die Aktivierung der Vereinbarung in Business Central angefordert und Ihre Anfrage wird zur Bearbeitung an Continia gesendet. Der Status der Anfrage wird auf **Ausstehend** gesetzt.

## Anforderungsstatus anzeigen und Probleme beheben

Um den Status Ihrer Aktivierungsanforderung anzuzeigen, gehen Sie zur Seite **Bankvereinbarungen** und wählen Sie in der Aktionsleiste **Protokoll der Aktivierungsanfrage** aus, um die Seite **Bankvereinbarung Aktivierungsprotokoll** zu öffnen. Suchen Sie in der Liste der Anfragen die von Ihnen übermittelte Anfrage und überprüfen Sie ihren Status in der Spalte **Anforderungsstatus**.

Wenn die Aktivierungsanfrage genehmigt wurde, ändert sich ihr Status. Stellen Sie sicher, dass Sie die Synchronisierung mit Continia Online durchführen, bevor Sie den Status Ihrer Aktivierungsanforderung überprüfen (wählen Sie auf der Seite **Bankvereinbarungen** die Option **Erzwinge Synchronisation mit Continia Online**). Der Status wird erst aktualisiert, wenn Sie die Synchronisierung mit Continia Online durchgeführt haben. Beachten Sie, dass die Bearbeitung Ihrer Aktivierungsanfrage bis zu 48 Stunden dauern kann.

Wenn sich der Status Ihrer Aktivierungsanfrage in **Abgelehnt** ändert, prüfen Sie in der [obigen Anleitung](#so-richten-sie-den-automatischen-import-von-kreditkartentransaktionen-ein), ob Sie alle Schritte richtig ausgeführt haben.

> [!NOTE]
> Der mit Abstand häufigste Grund für eine abgelehnte Aktivierungsanforderung ist, dass die übermittelte Transaktion vor dem Datum erfolgte, an dem Ihre Bank begonnen hat, Transaktionen an Expense Management zu senden.
>
> Ein weiterer häufiger Grund ist, dass Sie von Ihrer Bank keine Bestätigung über die Aktivierung der Vereinbarung erhalten haben.

Wenn weiterhin Probleme auftreten, erstellen Sie bitte ein Support-Ticket. Ihr Support-Ticket muss die folgenden Informationen enthalten, da wir Ihnen ohne diese Angaben nicht weiterhelfen können:

- Client-ID
- Mandant GUID
- Bankname
- Bankvereinbarungsnummer (wird von Ihrer Bank angegeben)

> [!TIP]
> Beachten Sie, dass viele Banken unterschiedliche Begriffe verwenden, wie z. B. _Dateiübermittlungs-ID_, _Firmen-ID_ oder _Empfänger-ID_.
>
> Informationen, wie Sie Client-Anmeldeinformationen und Mandanten GUID ermitteln, finden Sie unter [How to find Client Credentials and Company GUID](https://continia.zendesk.com/hc/en-us/articles/360020019300-How-to-find-Client-Credentials-and-Company-GUID) (nur für Continia-Partner verfügbar).

## Informationen zum Thema

[American Express-Transaktionen importieren](Importing American Express transactions.md)  
[Mastercard-Transaktionen importieren](@EM-279)  
[Visa-Transaktionen importieren](@EM-281)  
[Transaktionen von anderen Karten importieren](Importing transactions from other cards.md)  
[Manueller Dateiimport](Manual file import.md)  
[Finden eines Partners für Continia Expense Management](/Continia Expense Management/Getting Started/Resellers and Partners/Find a Reseller.md)