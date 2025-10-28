---
title: Grundlegendes zu Priorität und Übernahme von Dimensionen in Expense Management
date: 14-05-2025
description: Erfahren Sie, wie Dimensionen priorisiert und übernommen werden
id: EM-318
lang: de
---

# Grundlegendes zu Priorität und Übernahme von Dimensionen in Expense Management

Expense Management verwendet Übernahme und Priorität von Dimensionen für verschiedene Belegarten. In den folgenden Tabellen finden Sie mehr Informationen über die Priorität der Dimensionen und Verteilungen für Belege, Fahrstrecken und Pauschalen. Die Dimensionsarten werden von der höchsten Priorität (P1) bis zur niedrigsten Priorität aufgelistet.

## Dimensionsarten und Prioritäten von Belegen

Belege haben die folgenden Dimensionsarten, aufgelistet in der Reihenfolge ihrer Priorität von der höchsten (P1) bis zur niedrigsten (P5).

| <span style="white-space: nowrap;">Priorität</span> | Beschreibung                                                                                             |
| --------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| P1                                                  | Ein Projekt hat die höchste Priorität. Dies ist höher als eine Belegart. |
| P2                                                  | Eine Belegart hat Vorrang vor einem Sachkonto.                                           |
| P3                                                  | Ein Sachkonto hat Vorrang vor einem Kreditor.                                            |
| P4                                                  | Ein Kreditor hat Vorrang vor einem Verkäufer/Einkäufer.                                  |
| P5                                                  | Ein Verkäufer/Einkäufer hat die niedrigste Priorität.                                    |

## Verteilungen

Eine Verteilung übernimmt ihre Dimensionen vom Beleg.

## Dimensionsarten und Prioritäten von Fahrstrecken

Fahrstrecken haben die folgenden Dimensionstypen, aufgelistet in der Reihenfolge ihrer Priorität von der höchsten (P1) bis zur niedrigsten (P5).

| <span style="white-space: nowrap;">Priorität</span> | Beschreibung                                                                            |
| --------------------------------------------------- | --------------------------------------------------------------------------------------- |
| P1                                                  | Ein Projekt hat die höchste Priorität. Dies ist höher als ein Sachkonto |
| P2                                                  | Ein Sachkonto hat Vorrang vor einem Kreditor.                           |
| P3                                                  | Ein Kreditor hat Vorrang vor einem Verkäufer/Einkäufer.                 |
| P4                                                  | Ein Verkäufer/Einkäufer hat die niedrigste Priorität.                   |

## Dimensionsarten und Prioritäten von Pauschalen

Pauschalen haben die folgenden Dimensionstypen, aufgelistet in der Reihenfolge ihrer Priorität von der höchsten (P1) bis zur niedrigsten (P3).

> [!NOTE]
> Pauschalen übernehmen ihre Dimensionen nicht von Sachkonten des Buchungstyps Unterkunft und Verpflegung.

| <span style="white-space: nowrap;">Priorität</span> | Beschreibung                                                                                            |
| --------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| P1                                                  | Ein Projekt hat die höchste Priorität. Dies ist höher als ein Kreditor. |
| P2                                                  | Ein Kreditor hat Vorrang vor einem Verkäufer/Einkäufer.                                 |
| P3                                                  | Ein Verkäufer/Einkäufer hat die niedrigste Priorität.                                   |

## Dimensionsarten und Prioritäten von Abrechnungen

Das manuelle Festlegen einer Dimension für eine Abrechnung hat keine Auswirkungen auf die zugrunde liegenden Dokumente. Belege, Fahrstrecken und Pauschalen in der Abrechnung übernehmen keine Dimensionen aus der Kopfzeile der Abrechnung.

> [!NOTE]
> Abrechnungen sind nicht mit einer Buchungsart verknüpft und übernehmen keine Einstellungen von Sachkonten.

Abrechnungen haben die folgenden Dimensionstypen, aufgelistet in der Reihenfolge ihrer Priorität von der höchsten (P1) bis zur niedrigsten (P3).

| <span style="white-space: nowrap;">Priorität</span> | Beschreibung                                                                                            |
| --------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| P1                                                  | Ein Projekt hat die höchste Priorität. Dies ist höher als ein Kreditor. |
| P2                                                  | Ein Kreditor hat Vorrang vor einem Verkäufer/Einkäufer.                                 |
| P3                                                  | Ein Verkäufer/Einkäufer hat die niedrigste Priorität.                                   |

## Informationen zum Thema

[Belegarten einrichten](@EM-41)

[Unternehmensrichtlinien für Belege einrichten](@EM-39)

[Unternehmensrichtlinien für Fahrstrecken einrichten](@EM-40)

