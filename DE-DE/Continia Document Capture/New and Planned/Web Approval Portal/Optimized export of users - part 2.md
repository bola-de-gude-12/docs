---
title: Optimierter Export von Benutzern – Teil 2
date: 24-12-2024
description:
id: DC-431
lang: de
---

# Optimierter Export von Benutzern – Teil 2

| Funktion                                  | Öffentliche Vorschau | Allgemeine Verfügbarkeit Online |
| ----------------------------------------- | :------------------: | :-----------------------------: |
| Optimierter Export von Benutzern – Teil 2 |           -          |               N/A               |

> [!NOTE]
> Die erste Stufe dieser Funktion, die im April 2024 implementiert wurde, hat die meisten Probleme mit Bezug auf die Benutzeraktualisierung behoben. Daher ist es nicht mehr erforderlich, den zweiten Teil der Optimierung zu implementieren.

## Vorteile

Die Optimierung der Benutzerexportfunktion wird für Unternehmen mit einer großen Anzahl von Benutzern eine enorme Zeitersparnis bedeuten. Derzeit können solche Kunden Continia Document Capture möglicherweise über längere Zeiträume nicht verwenden, wenn sie Benutzer exportieren, da das System während des Exports gesperrt sein kann. Durch die neue, optimierte Funktion werden die Systemausfallzeiten und die daraus resultierenden Auswirkungen drastisch reduziert.

## Details zur Funktion

Um Benutzerberechtigungen und ähnliche Daten zwischen Document Capture und dem Continia Web Approval Portal abzugleichen, ist es gelegentlich erforderlich, Benutzerdaten in Continia Online zu exportieren – beispielsweise mit der Aktion **Benutzer exportieren** auf der Seite **Continia-Benutzer**.

Dieses Benutzerexportfunktion wird nun in verschiedener Hinsicht verbessert. Die Verbesserungen werden in zwei Phasen wie folgt umgesetzt:

**Verbesserung Teil 1:** Vor dem Exportieren aller Benutzerinformationen prüft Document Capture, ob bei Benutzern Änderungen vorgenommen wurden. Nur in diesem Fall werden sämtliche Benutzerinformationen exportiert und Sie vermeiden so einen unnötigen Datenexport. Diese Änderung wurde in Document Capture 2024 R1 implementiert, veröffentlicht im April 2024.

**Verbesserung Teil 2:** Anstatt bei jeder oder mehreren kleineren Änderungen alle Benutzerdaten zu exportieren, werden nur die geänderten Informationen exportiert. Dadurch wird nicht nur die zu exportierende Datenmenge, sondern auch die Exportzeit reduziert.