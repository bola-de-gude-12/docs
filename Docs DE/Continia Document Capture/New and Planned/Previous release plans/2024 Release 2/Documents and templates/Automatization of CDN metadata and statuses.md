---
title: Automatische Aktualisierung von CDN-Metadaten und -Status
date: 24-12-2024
description:
id: DC-315
lang: de
---

# Automatische Aktualisierung von CDN-Metadaten und -Status

| Funktion                                                  |           Öffentliche Vorschau          |     Allgemeine Verfügbarkeit Online     |
| --------------------------------------------------------- | :-------------------------------------: | :-------------------------------------: |
| Automatische Aktualisierung von CDN-Metadaten und -Status | {{checkmark}} Sep. 2024 | {{checkmark}} Okt. 2024 |

## Vorteile

Mit dieser Funktion stehen Ihnen immer die aktuellsten Metadaten des Continia Delivery Network (CDN) zur Verfügung, beispielsweise Netzwerkdaten, Identifikationstypen, Netzwerkprofile und verschiedene Dokumentdaten. Die Funktion stellt außerdem sicher, dass der Status von Dokumenten, die über das Continia Delivery Network gesendet werden, automatisch aktualisiert wird, sodass Sie die Seite **Gesendete Netzwerkdokumente** hierfür nicht manuell öffnen müssen.

## Details zur Funktion

Die folgenden Aufgabenwarteschlangen werden hinzugefügt, um die Aktualisierung von Metadaten und Status für das Continia Delivery Network zu automatisieren:

- **eDocuments metadata update**
- **eDocuments document update**

Die Aufgabenwarteschlange **eDocuments metadata update** wird für die Aktualisierung von Teilnahmen und Netzwerkdaten verwendet. Die Ausführung ist einmal täglich zu einer beliebigen Uhrzeit zwischen 18:00 und 5:00 Uhr geplant.

Die Aufgabenwarteschlange **eDocuments document update** wird verwendet, um die Dokumentenstatus zu aktualisieren und um neue Belege und Lieferscheine herunterzuladen. Sie wird alle 30 Minuten ausgeführt.