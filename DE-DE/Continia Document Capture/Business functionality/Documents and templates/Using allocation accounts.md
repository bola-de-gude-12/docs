---
title: Umlagekonten verwenden
date: 05-03-2025
description:
id: DC-226
lang: de
---

# Umlagekonten verwenden

In diesem Artikel wird beschrieben, wie Umlagekonten in Continia Document Capture funktionieren.

Umlagekonten sind [eine Standardfunktion von Microsoft Dynamics 365 Business Central](https://learn.microsoft.com/de-de/dynamics365/business-central/finance-allocate-revenue-costs), mit der Sie Kosten auf zwei oder mehr Sachkonten oder Dimensionen innerhalb eines Mandanten aufteilen können. Dies ist sinnvoll, da Kosten beispielsweise nicht immer direkt einer bestimmten Abteilung zugeordnet werden können.

Beim Erkennen von Feldern ist es möglich, das **Umlagekonto** als **Art** auf Kopfebene und auf Zeilenebene als **Übersetze nach Art** festzulegen. Anschließend können Sie unter **Nr.** oder **Übersetze nach Nr.** eine Kontonummer festlegen und auf der Seite **Umlagekonto** definieren, wie die erfassten Beträge oder Mengen auf die verschiedenen Zielkonten aufgeteilt werden.

> [!NOTE]
> **Umlagekonten** müssen mit den festen Kontotypen konfiguriert werden, nicht mit variablen. Andernfalls erfolgt eine gleichmäßige Verteilung der Beträge auf die Konten anstatt einer proportionalen Verteilung entsprechend der Konfiguration des Umlagekontos. Es ist außerdem nicht möglich, Bestellzeilen mit dem auf **Umlagekonto** eingestellten Kontotyp abzugleichen; und der Zielkontotyp **Vom übergeordneten Element erben** wird nicht unterstützt.

Beispielsweise kann ein Umlagekonto so konfiguriert werden, dass die von einem bestimmten Kreditor in Rechnung gestellten Beträge gleichmäßig zwischen den Abteilungen Content und Marketing aufgeteilt werden (also 50 % und 50 %). Ein anderes Konto kann so konfiguriert werden, dass 80 % der Rechnung eines Internetdienstanbieters als Internetabonnement und der Rest als Mobilfunkabonnement zugeordnet werden.

Um eine konfigurierte Zuweisung zu testen, wählen Sie auf der Seite **Umlagekonto** in der Aktionsleiste **Verteilung testen**. Anschließend wird die **Umlagekonto - Vorschau** angezeigt, die anhand der Daten des ausgewählten Dokuments anzeigt, wie der im Dokument enthaltene Betrag aufgeteilt wird.

Beim Registrieren von Dokumenten werden Einkaufszeilen mit der Kontoart **Umlagekonto** automatisch auf die entsprechenden Kontoarten mit der Standardfunktion **Zeilen aus Zuordnungskontozeile generieren** übertragen. Diese Funktion ist auf den Standardseiten für Einkaufsbelege verfügbar ist.

> [!NOTE]
> Die Validierung des **Gesamtbetrags inkl. MwSt.**/**GST** erfolgt bei Verwendung von Umlagekonten nicht. Dies liegt daran, dass Business Central den MwSt.-/GST-Betrag nicht für Dokumente berechnet, die Zeilen mit Umlagekonten enthalten.