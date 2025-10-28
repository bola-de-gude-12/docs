---
title: Häufig gestellte Fragen zur Continia Expense App
date: 18-06-2025
description: Häufig gestellte Fragen zur Continia Expense App
id: EM-245
lang: de
---

# Häufig gestellte Fragen zur Continia Expense App

Hier finden Sie Antworten auf einige der am häufigsten gestellten Fragen zur Continia Expense App.

## Kann ich eine Benachrichtigungs-E-Mail erhalten, wenn ein Expense-Dokument genehmigt oder abgelehnt wird?

Nein, E-Mail-Benachrichtigungen für genehmigte oder abgelehnte Dokumente sind derzeit in Expense Management nicht verfügbar. Sie können den Status von Dokumenten jedoch mithilfe der [Push-Benachrichtigungen der Continia Expense Mobile App](@EM-46) überwachen oder diesen im Expense Web Portal unter **Belege** > **Historie** einsehen (abgelehnte Dokumente sehen Sie unter **Abrechnung** > **Offen**). Sie können den Status auch mit Ihren [Expense Management-Aufgabenwarteschlangen](@EM-278) anzeigen.

## Warum funktioniert das Feld **Teilnehmer** in der Continia Expense App/im Expense Portal nicht richtig?

Wenn bei einer Belegart das Eintragen von **Teilnehmern** erforderlich ist, dies in der Expense Mobile App oder im Expense Portal jedoch nicht wie erwartet funktioniert, wurden wahrscheinlich einige Schritte im Einrichtungsprozess ausgelassen.

Überprüfen Sie, ob Sie die folgenden Schritte ausgeführt haben:

1. Gehen Sie in Business Central zu **Belegarten**.
2. Aktivieren Sie unter **Teilnehmer erforderlich** die Kontrollkästchen für die Belegarten, für die Teilnehmer angegeben werden müssen.
3. Gehen Sie zu **Feldtypabhängigkeiten**.
4. Wählen Sie **Start** > **Systemabhängigkeiten aktualisieren**. Jetzt werden auf der Seite Zeilen angezeigt, wodurch die Funktion ordnungsgemäß funktioniert.
5. Wählen Sie **Continia Online** > **Erzwinge Synchronisation mit Continia Online**, um die Änderungen auf die Geräte der Benutzer zu übertragen.

Das Feld **Teilnehmer** ist normalerweise erst verfügbar, wenn die jeweilige Belegart im Expense Portal oder in der mobilen Expense App ausgewählt wird.