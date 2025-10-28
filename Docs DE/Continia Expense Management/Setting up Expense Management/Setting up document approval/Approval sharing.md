---
title: Expense Management Geteilte Genehmigung einrichten
date: 18-02-2025
description: Einrichten der automatischen geteilten Genehmigung, zum Beispiel bei Abwesenheit der Genehmiger
id: EM-64
lang: de
---

# Geteilte Genehmigung einrichten

Sie können alle Ihre Genehmigungsaufgaben automatisch an einen anderen Genehmiger weiterleiten, wenn Sie Dokumente für einen bestimmten Zeitraum nicht genehmigen können. Indem Sie Ihre Genehmigungsaufgaben an einen bestimmten Genehmiger weitergeben, kann dieser als Ihr Vertreter Ihre Genehmigungsaufgaben übernehmen, bis Sie Dokumente wieder selbst genehmigen können.

## Geteilte Genehmigung einrichten

Die Geteilte Genehmigung eignet sich gut, wenn Sie nicht im Büro sind und Engpässe bei Genehmigungsprozessen vermeiden möchten. Ein benannter Genehmiger ist ein Administrator.

So richten Sie die geteilte Genehmigung ein:

1. Suchen {{search}} Sie nach **Geteilte Genehmigung** und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Aktionsleiste **Liste bearbeiten** aus.
3. Geben Sie in der Spalte **Inhaber Benutzer-ID** die Benutzer-ID der Person ein, die Genehmigungsaufgaben teilt.
4. Geben Sie in der Spalte **Geteilt mit Benutzer-ID** die Benutzer-ID der Person ein, die die Aufgabe des Ersatzgenehmigers übernimmt.
5. Wählen Sie in der Spalte **Teilungsart** die Option **Normal** aus.
   > [!NOTE]
   > Wenn ein Administrator die Abwesenheitsgenehmigung im Namen eines Benutzers einrichten muss, muss der Administrator **Abwesend** anstelle von **Normal** auswählen, damit der Benutzer den Eintrag bei Bedarf später bearbeiten kann.
6. Geben Sie in den Spalten **Gültig von** und **Gültig bis** das Start- und Enddatum des Zeitraums ein, in dem Genehmigungsaufgaben geteilt werden sollen, oder wählen Sie die Daten aus.
7. Wenn der Ersatzgenehmiger die Grenzwerte und Berechtigungen übernehmen soll, aktivieren Sie das Kontrollkästchen **Inhaber Grenzwerte und Berechtigungen verwenden**.
8. Geben Sie an, wer während der angegebenen Zeit Genehmigungs-E-Mails erhält. Wählen Sie unter **Empfänger-E-Mail** die entsprechende Option:<br><ul><li>**Nur ursprünglicher Genehmiger**</li><li>**Nur gemeinsamer Genehmiger**</li><li>**Beide Genehmiger**</li></ul>

## Einen fiktiven Benutzer als Gruppe verwenden

In Situationen, in denen Sie Genehmigungen mehrerer Personen verwalten müssen, können Sie einen neuen fiktiven Benutzer erstellen und das Konto als Gruppengenehmiger verwenden. Verwenden Sie diese Lösung auch, wenn es eine Unternehmensrichtlinie gibt, die vorschreibt, dass Genehmiger auf höchster Ebene ihre eigenen Genehmigungsanfragen von jemand anderem als sich selbst genehmigen lassen müssen.

Das für die Gruppe (den fiktiven Benutzer) festgelegte Genehmigungslimit überschreibt das für jeden Benutzer in der Gruppe individuell festgelegte Genehmigungslimit. Sie müssen ein Administrator sein, um dies einrichten zu können.

So erstellen Sie einen neuen fiktiven Benutzer, den Sie als Gruppe verwenden können:

1. Suchen Sie {{search}} nach **Continia Benutzereinrichtung** und wählen Sie dann den entsprechenden Link.
2. Wählen Sie in der Aktionsleiste **Neu** aus.
3. Wählen Sie unter **Allgemein** im Feld **Continia-Benutzer-ID** das Menü (...). Wählen Sie dann entweder eine vorhandene Benutzer-ID aus oder wählen Sie in der Aktionsleiste **Neu** aus und erstellen Sie eine neue Benutzer-ID.
4. Füllen Sie das Feld **Name** aus.

> [!IMPORTANT]
> Die Continia-Benutzer-ID, die Sie für diesen fiktiven Benutzer erstellt oder aus der Continia-Benutzerliste ausgewählt haben, kann nur für diesen Zweck verwendet werden. Sie kann für nichts anderes verwendet werden.

4. Aktivieren Sie unter **Expense Management** > **Genehmigungslimit** entweder **Unbegrenzt** oder geben Sie das Genehmigungslimit im Feld **Betrag** an.

> [!NOTE]
> Wenn Sie im Feld **Genehmiger Name** ein Genehmigungslimit für den fiktiven Benutzer festlegen, stellen Sie sicher, dass sein Genehmigungslimit höher ist als das aller anderen in der Gruppe, oder weisen Sie ihm ein unbegrenztes Genehmigungslimit zu.

Jetzt haben Sie einen neuen fiktiven Benutzer, der als Gruppe verwendet werden kann.

### Benutzer zur Gruppe hinzufügen

So fügen Sie Benutzer zur Gruppe hinzu, die Sie gerade erstellt haben:

1. Suchen {{search}} Sie nach **Geteilte Genehmigung** und wählen Sie dann den zugehörigen Link.
2. Klicken Sie in der Aktionsleiste auf **Liste bearbeiten**.
3. Wählen Sie in der Spalte **Inhaber Benutzer-ID** den Benutzer aus, den Sie im vorherigen Schritt erstellt haben.
4. Wählen Sie in der Spalte **Geteilt mit Benutzer-ID** einen Benutzer aus, den Sie in die Gruppe für die geteilte Genehmigung aufnehmen möchten.
5. Wählen Sie in der Spalte **Teilungsart** die Option **Normal** aus.
6. Aktivieren Sie in der Spalte **Inhaber Grenzwerte und Berechtigungen verwenden** das Kontrollkästchen.
7. Wählen Sie in der Spalte **Empfänger-E-Mail** die entsprechende Option:<br><ul><li>**Nur ursprünglicher Genehmiger**</li><li>**Nur gemeinsamer Genehmiger**</li><li>**Beide Genehmiger**</li></ul>
8. Wiederholen Sie diese Schritte für jeden Benutzer, den Sie in die Gruppe aufnehmen möchten.

Sie können die Anzahl der Benutzer, die der Gruppe hinzugefügt wurden, auf der Seite Continia-Benutzer-Seite unter **Für diesen Benutzer freigegeben** sehen.

## Geteilte Genehmigung bei Abwesenheit einrichten

Um dies einzurichten, müssen Sie kein Administrator sein, da einzelne Benutzer die geteilte Genehmigung auch bei Abwesenheit einrichten können.

So richten Sie die geteilte Genehmigung selbst ein:

1. Suchen {{search}} Sie nach Expense Management Genehmigungsposten und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Aktionsleiste **Abwesenheitseinrichtung** aus.
3. Geben Sie unter **Allgemein** in den Feldern **Weiterleiten von Datum** und **Weiterleiten bis Datum** das Start- und Enddatum des Zeitraums ein, in dem Genehmigungsaufgaben geteilt werden sollen. Sie können die Daten auch auswählen.
4. Geben Sie im Feld **Weiterleiten an Name** die Benutzer-ID des Ersatzgenehmigers ein, an den Ihre Genehmigungsaufgaben weitergeleitet werden sollen.
5. Wenn Sie möchten, dass Ihre Genehmigungsaufgaben für alle Mandanten geteilt werden, in denen Sie und der stellvertretende Genehmiger vorhanden sind, aktivieren Sie das Kontrollkästchen **Kopiere in alle Mandanten**. Wenn Sie dieses Kontrollkästchen nicht aktivieren, gilt die von Ihnen eingerichtete geteilte Genehmigung bei Abwesenheit nur für den Mandanten, in dem Sie sich gerade befinden.

> [!NOTE]
> Die Felder **Inhaber Grenzwerte und Berechtigungen verwenden** und **E-Mails weiterleiten** sind auf der Seite **Abwesenheitseinrichtung** in der Benutzeroberfläche für Benutzer ausgeblendet. Sie sind jedoch standardmäßig aktiviert. Wenn Sie diese Standardeinstellungen ändern möchten, kann ein Administrator dies auf der Seite **Geteilte Genehmigung** tun.