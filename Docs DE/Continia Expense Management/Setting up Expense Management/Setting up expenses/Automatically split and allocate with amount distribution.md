---
title: Automatisches Aufteilen und Zuweisen mithilfe der Betragsverteilung
date: 15-04-2024
description: Erfahren Sie, wie Sie die automatische Aufteilung und Zuordnung von Ausgaben in abzugsfähige und nicht abzugsfähige Zeilen einrichten.
id: EM-216
lang: de
---

# Automatisches Aufteilen und Zuweisen mithilfe der Betragsverteilung

In dieser Anleitung wird erläutert, wie Sie Ausgaben mithilfe von Verteilungscodes in Continia Expense Management aufteilen und zuordnen. Dies ist in Ländern nützlich, in denen beispielsweise ein Teil der Mehrwertsteuer/Umsatzsteuer für bestimmte Arten von Ausgaben abzugsfähig ist.

Wenn ein Expense-Benutzer eine Ausgabe für eine Belegart registriert, wird diese Ausgabe aufgeteilt und mithilfe eines Verteilungscodes den verschiedenen Belegarten zugewiesen: der ursprünglichen Belegart und der, die beim Einrichten des Verteilungscodes angegeben wurde. Letztere Belegart ist für Expense-Benutzer nicht sichtbar. Daher ändert sich aus Sicht eines Expense-Benutzers beim Einreichen von Ausgaben nichts. Die Kostenaufteilung kann nur in Business Central angezeigt werden. <br> <br>

<iframe src="https://player.vimeo.com/video/917147014?h=9793ae1a3e&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" title="Automatically Split and Allocate with amount distribution in Expense Management"></iframe>

## Voraussetzungen

Um die automatische Aufteilung und Zuordnung mittels Betragsverteilung einrichten zu können, ist folgendes erforderlich:

- Die Einstellung **Betragsverteilung aktivieren** muss in der **Expense Management Einrichtung** im Inforegister **Beleg** aktiviert sein. Wenn diese Einstellung aktiviert ist, wird die Spalte **Verteilungscode** auf der Seite **Belegarten** angezeigt.
- Eine neue oder vorhandene Belegart, für den Expense-Benutzer Ausgaben registrieren, zum Beispiel **BEWIRTUNG**. Informationen hierzu finden Sie unter [Belegarten einrichten](@EM-41).
- Eine neue Belegart, die nur für die Zuweisung verwendet wird, z. B. **BEWIRTUNG OHNE ABZUG**.

## So richten Sie die Betragsverteilung ein

Sie müssen einen Verteilungscode für eine Belegart einrichten (z. B. **BEWIRTUNG**).

1. Wählen Sie das Symbol {{search}}, geben Sie **Belegarten** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Aktionsleiste **Liste bearbeiten** aus.
3. Wählen Sie eine Belegart aus (zum Beispiel **BEWIRTUNG**).
4. Wählen Sie im Feld **Verteilungscode** im Dropdown-Menü **Neu** aus und erstellen Sie einen neuen Verteilungscode, indem Sie die folgenden Felder ausfüllen:
   - **Verteilungscode** – Der Name des Verteilungscodes.
   - **Beschreibung** – Eine kurze Beschreibung des Verteilungscodes.
5. Unter **Verteilungszeilen** legen Sie fest, wie die Ausgabe prozentual verteilt wird und auf welche Belegarten. Hier werden die Belegarten angewendet, die oben unter den Voraussetzungen aufgeführt sind.

Ein Beispiel für Aufteilungen gemäß der Betragsverteilung:1. Zeile: 70 % | **BEWIRTUNG**
2. Zeile: 30 % | **BEWIRTUNG OHNE ABZUG**

## Informationen zum Thema

[Belegarten einrichten](@EM-41)
