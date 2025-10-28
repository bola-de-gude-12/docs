---
title: Belege aus Kreditkartentransaktionen erstellen
date: 01-12-2023
description: null
id: EM-201
lang: de
---

# Belege aus Kreditkartentransaktionen erstellen

Wenn Kreditkartentransaktionen importiert wurden (entweder automatisch durch Einrichten eines automatischen Imports oder manuell), können in Expense Management automatisch neue Belege aus den Transaktionen erstellt werden. Sie können Expense Management auch so einrichten, dass Transaktionen mit Belegen abgeglichen werden sollen, die bereits vom Karteninhaber erstellt wurden. Dies wird für jede Zahlungsart individuell konfiguriert.

## Voraussetzungen

Um die automatische Erfassung von Ausgaben aus Kreditkartentransaktionen einrichten zu können, ist Folgendes erforderlich:

- Es wurde mindestens eine Zahlungsart eingerichtet.

## So erstellen Sie Belege automatisch

Wenn für eine Zahlungsart **Erstelle Beleg aus Banktransaktion** aktiviert ist, erstellt Expense Management immer automatisch neue Belege aus Transaktionen und sendet sie an den Karteninhaber, der dann Belegbilder anhängen und die Ausgabe kategorisieren kann.

Datum, Währung, Betrag und Beschreibung einer Transaktion werden dem Beleg immer hinzugefügt.

Um eine Zahlungsart so einzurichten, dass aus Transaktionen automatisch Belege erstellt werden, müssen Sie zunächst einem Benutzer eine Karte zuweisen:

1. Wählen Sie das Symbol {{search}}, geben Sie **Banktransaktionseingang** ein, und wählen Sie dann den zugehörigen Link. Sie können auf diesen Eingang auch über den Stapel **Banktransaktionseingang** im Rollencenter zugreifen.
2. Wählen Sie in der Aktionsleiste **Weise Kreditkarte dem Benutzer zu** aus.
3. Wählen Sie in der Liste der verfügbaren Continia-Benutzer-IDs den Benutzer aus, dem Sie eine Karte zuweisen möchten.
4. Im Dialogfenster mit der Frage _Der Kreditkarte muss eine Zahlungsart zugeordnet sein. Möchten Sie fortfahren?_, wählen Sie **Ja**.
5. Wählen Sie in der Liste der Zahlungsarten die Kreditkarte aus, die Sie dem in Schritt 2 ausgewählten Benutzer zuweisen möchten.

Expense Management führt nun eine Synchronisierung durch und überprüft, ob importierte Transaktionen einem der eingereichten Kreditkartenbelege zugeordnet werden können. Wenn keine Übereinstimmungen möglich sind, erstellt Expense Management neue Belege und sendet sie an die Benutzer.

Sie müssen das oben beschriebene Verfahren nur beim ersten Importieren von Transaktionen für die ausgewählte Kreditkarte durchführen.

## So erstellen Sie Belege manuell

Wenn Sie Belege lieber manuell erstellen möchten, folgen Sie der Anleitung unten. Die manuelle Methode bietet sich zum Beispiel an, wenn Sie bei der ersten Verwendung von Expense Management Kreditkartentransaktionen löschen möchten, die mit einer anderen Lösung als Expense Management verarbeitet wurden.

Dieser manuelle Prozess ermöglicht es auch, Abstimmungsregeln einzurichten, um Belegarten zuzuweisen oder Transaktionen vom Belegerstellungsprozess auszuschließen.

1. Wählen Sie das Symbol {{search}}, geben Sie **Banktransaktionseingang** ein, und wählen Sie dann den zugehörigen Link. Sie können auf diesen Eingang auch über den Stapel **Banktransaktionseingang** im Rollencenter zugreifen.
2. Wählen Sie in der Aktionsleiste **Weise Kreditkarte dem Benutzer zu** aus.
3. Wählen Sie in der Liste der verfügbaren Continia-Benutzer-IDs den Benutzer aus, dem Sie eine Karte zuweisen möchten.
4. Im Dialogfenster mit der Frage _Der Kreditkarte muss eine Zahlungsart zugeordnet sein. Möchten Sie fortfahren?_, wählen Sie **Ja**.
5. Wählen Sie in der Liste der Zahlungsarten die Kreditkarte aus, die Sie dem in Schritt 2 ausgewählten Benutzer zuweisen möchten.

Jetzt werden alle Kreditkartentransaktionen, die sich auf die ausgewählte Kreditkarte beziehen, in die Warteschlange **Nicht abgestimmt** im Rollencenter verschoben. Wenn Sie stattdessen über die Suche auf Ihre nicht abgeglichenen Transaktionen zugreifen möchten, wählen Sie das Symbol {{search}}, geben Sie **Banktransaktionen** ein und wählen Sie den entsprechenden Link.

Von hier aus können Sie die Transaktion manuell einem vorhandenen Beleg zuordnen oder einen neuen Beleg erstellen, indem Sie **Ausgaben abgleichen oder erstellen** auswählen. Der Beleg wird automatisch in der Mobile Expense App des Karteninhabers angezeigt, wo er Bilder anhängen und zusätzliche Informationen hinzufügen und den Beleg dann zur Genehmigung senden kann.

## Informationen zum Thema

[Zahlungsarten einrichten](@EM-81)  
[Automatischer Import von Kreditkartentransaktionen ](@EM-202)
