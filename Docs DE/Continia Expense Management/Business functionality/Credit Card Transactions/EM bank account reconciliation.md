---
title: Expense Management-Bankkontoabstimmung
date: 10-06-2025
description:
id: EM-91
lang: de
---

# Expense Management-Bankkontoabstimmung

Suchen Sie fehlende Transaktionen und stimmen Sie Transaktionen mit einem Kontoauszug ab, indem Sie die Funktion Bankkontoabstimmung von Expense Management verwenden.

Diese Funktion ist der Standardfunktion zur Bankabstimmung in Dynamics 365 Business Central sehr ähnlich. Allerdings bietet die Bankkontoabstimmung von Expense Management einige zusätzliche Vorteile:

- Sie können ein Bankkonto, ein Sachkonto oder einen Kreditor abgleichen
- Sie können den Status der Ausgaben sehen

Sie können monatliche Abstimmungen können durch das Vorschlagen von Zeilen, den Import von Kontoauszugstransaktionen oder die manuelle Eingabe von Informationen aus einem Kontoauszug durchführen, indem Papierauszüge von der Bank mit Transaktionen in Expense Management verglichen werden.

Sie können zwischen automatischer und manueller Abstimmung wählen.

## Automatische Abstimmung

1. Suchen Sie {{search}} nach **Bankkontoabstimmung – Expense Management**.
2. Klicken Sie in der Aktionsleiste auf **Neu**.
3. Wählen Sie unter **Allgemein** eine Bankkontoart aus.
4. Wählen Sie eine Bankkontonummer aus. Alle mit diesem Konto verbundenen Banktransaktionsposten werden automatisch angezeigt.
5. So erhalten Sie Kontoauszugszeilen mit einer der beiden Methoden:

   1. Klicken Sie in der Aktionsleiste auf **Bank** > **Bankkontoauszug importieren**.
   2. Klicken Sie im Dialogfeld auf **Neue Bankkontoauszugsdatei importieren** oder **Vorhandene Auszugsdatei im Dateisystem finden** und klicken Sie auf **OK**.

   Oder

   1. Klicken Sie in der Aktionsleiste auf **Start** > **Zeilen vorschlagen**.
   2. Klicken Sie unter **Optionen** auf die Felder und klicken Sie dann auf **OK**.
6. Klicken Sie in der Aktionsleiste auf **Abstimmung** > **Automatische Abstimmung**, und klicken Sie dann auf **OK**.
7. Nachdem Sie beide Seiten abgeglichen haben, kopieren Sie den Betrag vom **Gesamtsaldo** und fügen Sie ihn in den **Auszug Abschlussaldo** ein.
8. Klicken Sie in der Aktionsleiste auf **Start** > **Buchen**, um die Abstimmung zu buchen.

Um gebuchte Abstimmungen anzuzeigen, suchen Sie {{search}} nach **Bankkontoauszüge – Expense Management**.

## Manuelle Abstimmung

1. Suchen Sie {{search}} nach **Bankkontoabstimmung – Expense Management**.

2. Klicken Sie in der Aktionsleiste auf **Neu**.

3. Wählen Sie unter **Allgemein** eine Bankkontoart aus.

4. Wählen Sie eine Bankkontonummer aus. Alle mit diesem Konto verbundenen Banktransaktionsposten werden automatisch angezeigt.

5. So erhalten Sie Kontoauszugszeilen mit einer der beiden Methoden:
   1. Klicken Sie in der Aktionsleiste auf **Bank** > **Bankkontoauszug importieren**.

   2. Klicken Sie im Dialogfeld auf **Neue Bankkontoauszugsdatei importieren** oder **Vorhandene Auszugsdatei im Dateisystem finden** und klicken Sie auf **OK**.

      Oder

   3. Geben Sie die Informationen anhand Ihres Bankauszugs in die Felder **Transaktionsdatum**, **Art**, **Beschreibung** und **Auszugsbetrag** ein.

6. Wählen Sie die Bankauszugszeile und den Banktransaktionseintrag aus, den Sie abgleichen möchten, und klicken Sie dann in der Aktionsleiste auf **Abstimmung** > **Manuell zuweisen**. Wiederholen Sie den Vorgang für jede Kontoauszugszeile.

7. Um die Abstimmung zu buchen, klicken Sie in der Aktionsleiste auf **Start** > **Buchen**.

Um gebuchte Abstimmungen anzuzeigen, suchen Sie {{search}} nach **Bankkontoauszüge – Expense Management** und wählen Sie dann den entsprechenden Link.

## Informationen zum Thema

[Transaktionen mit benutzerdefinierten Vorlagen importieren](@EM-47)

[Überblick über Kreditkartentransaktionen](@EM-213)