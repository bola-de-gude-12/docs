---
title: Einen Kreditor als Buchungskontoart für Kreditkartentransaktionen verwenden
date: 04-07-2024
description: Erfahren Sie, wie Sie einen Kreditor als Buchungskontoart für Kreditkartentransaktionen festlegen
id: EM-248
lang: de
---

# Einen Kreditor als Buchungskontoart für Kreditkartentransaktionen verwenden

Mit Expense Management ist es möglich, Kreditkartentransaktionen auf einen Kreditor zu buchen. Folgendes ist dabei jedoch _nicht_ möglich:

- Sie können keine Spesenabrechnungen verwenden.
- Buchen im Fibu Buch.-Blatt ist nicht möglich. Alle Dokumente (Belege, Fahrstrecken, Pauschalen) werden als Einkaufsrechnungen und nicht im Fibu Buch.-Blatt verbucht. Das System erstellt Einkaufsrechnungen, die den Status OFFEN haben und anschließend genehmigt und gebucht werden müssen. Für alle mit Kreditkartentransaktionen verbundenen Ausgaben wird eine Einkaufsrechnung für die Bank/den Kreditor erstellt und für alle Fahrstrecken, Pauschalen und Bar-/Privatausgaben wird für jeden Continia-Benutzer (deren Kreditor) eine Einkaufsrechnung erstellt.

## Einen Kreditor als Buchungskontoart für Kreditkartentransaktionen einrichten

So richten Sie einen Kreditor als Buchungskontoart für Kreditkartentransaktionen ein:

1. Gehen Sie zu **Expense Management Einrichtung**.
2. Deaktivieren Sie im Inforegister **Allgemein** die Option **Abrechnung**.
3. Legen Sie im Inforegister **Einkauf Belegbuchung** die Option **Beleg Buchungsart** auf **Bevorzugt Einkaufsrechnung** fest.

Anschließend sehen Sie möglicherweise folgende Meldung: _Wenn Sie „Bevorzugt Einkaufsrechnung“ aktivieren, deaktivieren Sie „Banktransaktionen beim Import buchen“. Möchten Sie fortfahren?_

Wählen Sie **Ja**. Dadurch wird die Buchung beim Import deaktiviert.

Jetzt müssen Sie die Buchungskontoart für die Zahlungsart ändern, für die Sie einen Kreditor als Buchungskonto verwenden wollen:

1. Gehen Sie zu **Zahlungsarten**.
2. Wählen Sie die Zahlungsart aus, für die Sie einen Kreditor als Buchungskonto verwenden möchten.
3. Legen Sie im Inforegister **Buchung** die **Methode** auf **Buchung auf ein Buchungskonto** fest.
4. Legen Sie unter **Buchungskonto** die **Art** auf **Kreditor** fest.
5. Wählen Sie unter **Nr.** einen Kreditor mit der Lookup-Funktion aus.