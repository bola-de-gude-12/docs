---
title: Fahrstreckenfahrzeuge einrichten
date: 31-03-2025
description:
id: EM-27
lang: de
---

# Fahrstreckenfahrzeuge einrichten

Fahrzeuge werden zur Identifizierung unterschiedlicher Fahrstreckensätze und zur Unterscheidung verschiedener Buchungseinrichtungen verwendet. In einigen Ländern gelten beispielsweise unterschiedliche Tarife für Elektrofahrzeuge und Fahrzeuge, die mit fossilen Brennstoffen betrieben werden.

Fahrzeuge werden mit einem Sachkonto, Buchungsgruppen und Mehrwertsteuer-Buchungsgruppen in Microsoft Dynamics 365 Business Central verknüpft und Sie können auch [Unternehmensrichtlinien für Fahrtstrecken](@EM-40) angeben.

## Ein Fahrzeug einrichten

Es ist möglich, ein Standardfahrzeug zu definieren, das automatisch ausgewählt wird, wenn Sie Fahrstrecken einreichen, entweder basierend auf einem Expense-Benutzer oder einer Expense-Benutzergruppe. Sie können sowohl vorhandene Expense-Benutzer als auch Expense-Benutzergruppen verwenden oder neue erstellen. Informationen zum Einrichten von Expense-Benutzern und Expense-Benutzergruppen finden Sie [hier](@EM-36) und [hier](@EM-35).

### Buchung

Nachdem Sie ein neues Fahrzeug erstellt haben, müssen Sie festlegen, wo die Fahrstrecken für dieses Fahrzeug gebucht werden. Sie können bei Bedarf für jeden Fahrzeugtyp ein anderes Buchungskonto einrichten oder dasselbe Konto wählen.

Um einem Fahrzeugtyp ein Buchungskonto hinzuzufügen, folgen Sie den folgenden Schritten.

1. Suchen {{search}} Sie nach **Fahrzeugliste** und wählen Sie dann den zugehörigen Link.
2. Wählen Sie das Fahrzeug aus, für das Sie ein Buchungskonto hinzufügen möchten, und wählen Sie dann in der Aktionsleiste **Einrichtung** aus.
3. Wählen Sie unter **Buchungskontoart** einen Kontotyp aus.
4. Wählen Sie unter **Buchungskonto Nr.** das Konto aus, auf das die Fahrstrecken gebucht werden sollen.

Wenn Sie mit der Einrichtung der Fahrzeuge fertig sind, müssen Sie für diese Fahrzeuge [Fahrstreckensätze festlegen](Setting up mileage rates.md), bevor Sie mit der Verarbeitung der Fahrstreckenkosten beginnen können.

## Erweiterte Fahrzeugeinrichtung

Sie können Standardfahrzeuge (zum Beispiel ein Firmenwagen) sowohl einzelnen Benutzern als auch Benutzergruppen zuweisen.

### So richten Sie ein Fahrzeug für eine Expense-Benutzergruppe ein

Um ein Standardfahrzeug für eine Expense-Benutzergruppe einzurichten, führen Sie die folgenden Schritte aus:

1. Suchen Sie {{search}} nach **Continia Standard-Benutzereinrichtung** und wählen Sie dann den entsprechenden Link.
2. Wählen Sie in der Aktionsleiste **Neu** aus.
3. Wählen Sie in der neuen Zeile unter **Einrichtungsart** die Option **Gruppe** aus.
4. Wählen Sie unter **Code** eine Expense-Benutzergruppe aus.
5. Wählen Sie unter **Fahrzeugcode** das Fahrzeug aus, das Sie als Standardfahrzeug für die Expense-Benutzergruppe festlegen möchten.
6. Füllen Sie die übrigen Felder nach Bedarf aus.

### So richten Sie ein Fahrzeug für einen Expense-Benutzer ein

Um ein Standardfahrzeug für einen Expense-Benutzer einzurichten, führen Sie die folgenden Schritte aus:

1. Suchen Sie {{search}} nach **Continia Standard-Benutzereinrichtung** und wählen Sie dann den entsprechenden Link.
2. Wählen Sie in der Aktionsleiste **Neu** aus.
3. Wählen Sie in der neuen Zeile unter **Einrichtungsart** die Option **Benutzer** aus.
4. Wählen Sie unter **Code** einen Expense-Benutzer aus.
5. Wählen Sie unter **Fahrzeugcode** das Fahrzeug aus, das Sie als Standardfahrzeug für den Expense-Benutzer festlegen möchten.
6. Füllen Sie die übrigen Felder nach Bedarf aus.

## Informationen zum Thema

[Continia Standard Benutzereinrichtung](/Continia Expense Management/Setting up Expense Management/Setting up General Business Functionality/Setting up the Continia Users Default Setup.md)  
[Expense-Benutzer für Expense Management einrichten](@EM-36)  
[Expense-Benutzergruppen für Expense Management einrichten](@EM-35)

