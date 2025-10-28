---
title: Zuweisen von Pauschalen zu Projekten nach Ziel
date: 30-09-2025
description: Expense-Benutzer können Projekten Pauschalen nach Zielort zuordnen
id: EM-331
lang: de
---

# Zuweisen von Pauschalen zu Projekten nach Ziel

| Funktion                                       |         Allgemeine Verfügbarkeit        |           Öffentliche Vorschau          |
| ---------------------------------------------- | :-------------------------------------: | :-------------------------------------: |
| Zuweisen von Pauschalen zu Projekten nach Ziel | {{checkmark}} Okt. 2025 | {{checkmark}} Sep. 2025 |

## Vorteile

Diese Funktion verbessert die Projektkostenverwaltung, indem sie es Benutzern ermöglicht, Projektinformationen für jedes einzelne Ziel innerhalb einer Pauschale auszuwählen. Eine detaillierte und genaue Zuordnung der Reisekosten ist besonders nützlich für Unternehmen, die komplexe Reisen mit mehreren Etappen verwalten und eine präzise Budgetverfolgung auf Projektbasis benötigen. Insgesamt sorgt diese Funktion für einen reibungsloseren Arbeitsablauf und eine höhere Betriebseffizienz bei den detailliertesten Szenarien der Kostenzuordnung.

## Details zur Funktion

Dieses Update führt die Felder **Projekt** und **Aufgabe** für Pauschalenziele ein und ermöglicht so eine detailliertere Kostenzuordnung.

- Projekt- und Aufgabenfelder – Die beiden neuen Felder für „Projekt“ und „Aufgabe“ wurden den Zielzeilen von Pauschalen hinzugefügt. Diese Felder sind auch im Expense Portal und in der Expense Mobile App verfügbar.
- Übernahme von Projektdaten – Beim Erstellen einer neuen Pauschale werden die Projekt- und Aufgabendetails aus der Kopfzeile automatisch in die Zielzeilen übernommen. Sie haben jedoch die Flexibilität, das Projekt und die Aufgabe auf einzelnen Zielzeilen zu ändern.
- Buchungslogik:
  - Wenn nicht mehrere Ziele aktiviert sind, werden das Projekt und die Aufgabe, die im Pauschalenkopf angegeben sind, für die Buchung verwendet.
  - Wenn mehrere Ziele verwendet werden, bucht das System die Ausgaben basierend auf dem Projekt und der Aufgabe, die jeder einzelnen Reiseetappe zugewiesen sind.
  - Bei Szenarien mit zwei oder mehr Zielen am selben Tag mit unterschiedlichen Projekten wird für jedes Ziel eine separate Projekt Buch.-Blattzeile erstellt. Jede Linie wird mit dem vollen Tagessatz gebucht, da der Satz durch das Endziel des jeweiligen Tages bestimmt wird.
- Konfiguration – Sie können der Ansicht in Business Central mithilfe von **Konfigurierte Felder** die neuen Felder **Projekt** und **Aufgabe** hinzufügen.
- Erweiterbarkeit für Partner – Es wurde ein Event integriert, das es Partnern ermöglicht, den gebuchten Betrag für jedes Projekt anzupassen und so für mehr Flexibilität zu sorgen.

Weitere Informationen finden Sie unter [Projekte und Projektaufgaben verwenden](@EM-170)
