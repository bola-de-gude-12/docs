---
title: Projekte und Projektaufgaben verwenden
description: Erfahren Sie, wie Sie Belegen bestimmten Projekten und Aufgaben zuordnen.
date: 13-07-23
id: EM-170
lang: de
---

# Projekte und Projektaufgaben verwenden

Für jeden Belegtyp kann definiert werden, welche Felder für Expense-Benutzer in der Expense App und im Expense Portal sichtbar sind. Zusätzlich zu den Standardfeldern können Sie weitere Felder einbeziehen, beispielsweise Projekte. Um Belege bestimmten Projekten und Aufgaben zuzuordnen, können Sie die folgenden Felder hinzufügen:

- **Projektnr.** - Feld für Projekte. Wenn Sie beispielsweise Belege einem bestimmten Projekt zuordnen möchten, bezieht sich dies auf ein bestimmtes Projekt, eine Aufgabe oder einen Auftrag, der von einer Einzelperson oder einem Team innerhalb einer Organisation übernommen wurde. Es handelt sich um einen eindeutigen Arbeitsaufwand, der Ressourcen erfordert und mit entsprechenden Kosten verbunden sein kann.
- **Aufgabe** – Feld für Projektaufgaben. Dies ist beispielsweise der Fall, wenn Sie Aufwendungen für Teilaktivitäten im Rahmen der Erledigung eines Auftrags angeben möchten. Bei diesen Aufgaben kann es sich um einzelne Schritte oder Aktionen handeln, die zum Erreichen des Gesamtziels der Arbeit erforderlich sind. Mit jeder Aufgabe können eigene Kosten verbunden sein, beispielsweise für Material, Arbeitskosten oder externe Dienste.

## So fügen Sie Projekte und Aufgaben hinzu

So fügen Sie Projektnummer und Aufgabe für einen Beleg hinzu:

1. Wählen Sie das Symbol {{search}}, geben Sie **Konfigurierte Felder** ein, und wählen Sie dann den zugehörigen Link.

2. Wählen Sie in der Aktionsleiste **Pauschale**, **Fahrstrecke**, **Beleg** oder **Abrechnung** aus. Der Standardwert für die Ausgabenart wird jetzt angezeigt.

3. Wählen Sie in der Spalte **Feld Code** eine leere Zelle aus und wählen Sie **Neu**.

4. Wählen Sie aus der Dropdownliste **Projektnr.** oder **Aufgabe** aus.

## So verwenden Sie abrechenbar oder nicht abrechenbar für Projekte und Aufgaben

Wenn Sie die Felder **Projektnr.** und **Aufgabe** hinzufügen, wird der Beleg automatisch als abrechenbar gekennzeichnet. In Business Central ist auf der Beleg-Karte die **Projektzeilenart** auf _Abrechenbar_ eingestellt. Diese Funktion ist nützlich, wenn der Auftrag dem Endkunden in Rechnung gestellt werden muss. So kann beispielsweise ein Beratungsunternehmen den Auftrag in Rechnung stellen, anstatt die Kosten zu tragen. Wenn für den Auftrag jedoch keine weitere Rechnungsstellung vorgesehen ist, können Sie den Auftragspositionstyp auf **Budget** festlegen.

Das Feld **Abrechenbar** kann standardmäßig in der Expense-App und im Expense-Portal konfiguriert werden. Das Feld **Projektzeilenart** kann jedoch nur in Business Central geändert werden. Wenn Sie Benutzern in der App und im Portal die Möglichkeit geben möchten, auszuwählen, ob ein Beleg mit einem zugewiesenen Auftrag und einer zugewiesenen Aufgabe in Rechnung gestellt werden soll oder nicht, können Sie unter **Konfigurierte Felder** ein Feld hinzufügen. Dadurch können Benutzer das Feld **Projektzeilenart** direkt in der App und im Portal bearbeiten.

So zeigen Sie das Feld **Projektzeilenart** in der Expense App und im Portal an:

1. Wählen Sie das Symbol {{search}}, geben Sie **Konfigurierte Felder** ein, und wählen Sie dann den zugehörigen Link.

2. Wählen Sie in der Spalte **Feld Code** eine leere Zelle aus und wählen Sie **Neu**.

3. Wählen Sie aus der Dropdownliste **Abrechenbar** aus. Durch diese Aktion wird das Feld sowohl in der App als auch im Portal zugänglich. Der Standardwert ist dabei _False_.

   In Szenarien, in denen das Feld standardmäßig immer auf _False_ (nicht abrechenbar) eingestellt sein soll, können Sie die Felder **Sichtbar standardmäßig ausblenden** und **Bearbeitbar** auswählen. Diese Konfiguration verbirgt das Feld, behält aber den Wert _False_ bei.
