---
title: Automatische Archivierung von Einkaufsbestellungen bei Registrierung von Aktualisierungen
date: 24-12-2024
description:
id: DC-349
lang: de
---

# Automatische Archivierung von Einkaufsbestellungen bei Registrierung von Aktualisierungen

| Funktion                                                                                  |           Öffentliche Vorschau          |     Allgemeine Verfügbarkeit Online     |
| ----------------------------------------------------------------------------------------- | :-------------------------------------: | :-------------------------------------: |
| Automatische Archivierung von Einkaufsbestellungen bei Registrierung von Aktualisierungen | {{checkmark}} Sep. 2024 | {{checkmark}} Okt. 2024 |

## Vorteile

Wenn eine Bestellung von dem Kreditor, an den Sie sie gesendet haben, aktualisiert wird, möchten Sie möglicherweise den Verlauf der Bestellung einsehen, um die ursprüngliche Bestellung anzuzeigen. Dies wird durch diese Funktion erleichtert, mit der Sie alle Änderungen an Bestellungen verfolgen und frühere Versionen in einem Standardarchiv von Microsoft Dynamics 365 Business Central anzeigen können.

## Details zur Funktion

Mit dieser Funktion können Sie Ihre Einkaufsbestellungen automatisch archivieren lassen, wenn Sie Aktualisierungen einer Bestellung durch einen Kreditor registrieren. Die Funktion archiviert automatisch die Version jeder Bestellung, bevor die Änderungen vom Kreditor angewendet wurden. Alle archivierten Bestellversionen werden im standardmäßigen **Bestellungsarchiv** von Business Central gespeichert.

In folgenden Fällen werden Bestellungen je nach Belegkategorie automatisch archiviert:

- Kategorie **EINKAUF**: Wenn Sie ein Document Capture-Dokument mit den Registrierungsoptionen **Bestellung zuordnen und aktualisieren** oder **Reklamation zuordnen und aktualisieren** als Rechnung oder Gutschrift registrieren.
- Kategorie **BESTELLUNG**: Wenn Sie ein Document Capture-Dokument mit den Registrierungsoptionen **Bestellung erstellen oder aktualisieren**, **Bestellung aktualisieren** oder **Aktualisiere Bestellempfangsbestätigung** registrieren.