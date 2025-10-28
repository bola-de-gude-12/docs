---
title: Upgrade von Continia Core (FOB)
date: 09-07-2024
description:
id: EM-255
lang: de
---

# Upgrade von Continia Core (FOB)

Continia Core ist ein Modul, das für die ordnungsgemäße Funktion aller Continia-Lösungen unerlässlich ist. Es wird zur Aktivierung und Verbrauchserfassung verwendet, enthält aber auch eine Reihe anderer wichtiger Funktionen, die von mehreren Continia-Lösungen verwendet werden, wie etwa Frameworks zur Verwaltung der Telemetrie und Webkommunikation. Weitere Informationen finden Sie unter [Grundlegendes zu Continia Core](@DC-52).

> [!NOTE]
> Continia Core-Objekte sind in den FOB-Dateien für alle Continia-Produkte enthalten.

Obwohl das Modul abwärts- und aufwärtskompatibel ist, empfehlen wir unbedingt, immer die neueste Version zu installieren, wenn Sie eine neue Continia-Lösung installieren oder eine oder mehrere Ihrer vorhandenen Lösungen für beliebige FOB-Versionen von Microsoft Dynamics 365 Business Central aktualisieren.

## Die neueste Version von Continia Core installieren

Wenn Sie eine Continia-Lösung auf eine neuere Version oder ein neueres Service Pack aktualisieren, müssen Sie Objekte mithilfe des **Import Worksheets** importieren. Achten Sie dabei darauf, dass für alle im Arbeitsblatt angezeigten Objekte die neuste Version von Continia Core ausgewählt ist. Continia Core-Objekte haben die folgende Versionslistenstruktur:

- `CC[localization][NAV version].[major version].[service pack].[hotfix]`

Die folgende Tabelle enthält zwei Beispiele für Versionslisten:

<br>

| Version                                                                                             | Versionsliste                                                                                        |
| --------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Continia Core Version 1, Service Pack 1, für Microsoft Dynamics NAV 2018, W1 Localization           | CCW111.00.00.1.01                    |
| Continia Core Version 1, Service Pack 2, Hotfix 1, für Microsoft Dynamics NAV 2018, DK Localization | CCDK11.00.00.1.02.01 |

<br>

Normalerweise empfehlen wir, beim Importieren von Objekten im Zusammenhang mit einem Continia-Produkt-Upgrade **Alle ersetzen** auszuwählen. Dies ist jedoch bei Continia Core-Objekten nicht unbedingt der Fall, da Sie immer die neuesten Versionen dieser Objekte installiert haben müssen und Produktpakete manchmal ältere Continia Core-Objekte enthalten. Sie können die integrierte Intelligenz des **Import Worksheets** nutzen, um zu bestimmen, wann Sie alle Objekte ersetzen sollten und wann nicht, wie in den folgenden Beispielen:

### Beispiel 1

In diesem Szenario besteht die Aufgabe darin, Continia Document Capture auf Version 6.50.03 in einem System zu aktualisieren, auf dem die folgenden Anwendungen installiert sind:

- Continia Document Capture 6.00.05
- Continia Document Output 4.00
- Continia Payment Management 4.01
- Continia Core 4.01

Das Produktpaket Document Capture 6.50.03 enthält Objekte für Version 3.00.03 von Continia Core. Dies bedeutet, dass die Objekte des Produktpakets älter sind als die, die bereits im System installiert sind. Das **Import Worksheet** erkennt dies automatisch und setzt die **Aktion** auf **Überspringen** (anstatt auf **Ersetzen**), damit Sie _nicht_ alle Continia Core-Objekte ersetzen, sondern stattdessen einfach **OK** auswählen müssen.

### Beispiel 2

In diesem Szenario besteht die Aufgabe darin, Document Capture auf Version 8.01. in einem System zu aktualisieren, auf dem die folgenden Anwendungen installiert sind:

- Document Capture version 7.01
- Document Output 4.00
- Payment Management 4.01
- Continia Core 4.01

Das Produktpaket Document Capture 8.01 enthält Objekte für Version 5.01 von Continia Core. Dies bedeutet, dass die Objekte des Produktpakets neuer sind als die, die bereits im System installiert sind. Das **Import Worksheet** erkennt dies automatisch und setzt die **Aktion** auf **Ersetzen** (anstatt **Überspringen**), damit Sie **Alle ersetzen** auswählen können, um alle Continia Core-Objekte zu ersetzen.

## Informationen zum Thema

[Grundlegendes zu Continia Core](@DC-52)