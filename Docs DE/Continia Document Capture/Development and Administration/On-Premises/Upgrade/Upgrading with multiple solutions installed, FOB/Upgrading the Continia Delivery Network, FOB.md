---
title: Upgrade des Continia Delivery Networks (FOB)
date: 23-12-2024
description: So aktualisieren Sie das Continia Delivery Network (FOB).
lang: de
---

# Upgrade des Continia Delivery Networks (FOB)

Das Continia Delivery Network ist ein Modul, das derzeit von Continia Document Capture und Continia Document Output verwendet wird. Das Modul ermöglicht Ihnen die Integration in das Peppol eDelivery Network und ermöglicht Ihren Kreditoren, Geschäftsdokumente darüber zu importieren oder exportieren. Beispielsweise kann jeder Kreditor, der mit dem Peppol eDelivery Network verbunden ist, über dieses Netzwerk Dokumente an Continia Document Capture senden und dabei das Continia Delivery Network nutzen. Weitere Informationen finden Sie unter [Grundlegendes zum Continia Delivery Network](@DC-53).

> [!NOTE]
> Continia Delivery Network-Objekte sind in den FOB-Dateien für Document Capture und Document Output enthalten.

Obwohl das Modul abwärts- und aufwärtskompatibel ist, empfehlen wir unbedingt, immer die neueste Version zu installieren, wenn Sie eine neue Continia-Lösung installieren oder eine oder mehrere Ihrer vorhandenen Lösungen für beliebige FOB-Versionen von Microsoft Dynamics 365 Business Central aktualisieren.

## Die neueste Version des Continia Delivery Network installieren

Wenn Sie eine Continia-Lösung auf eine neuere Version oder ein neueres Service Pack aktualisieren, müssen Sie Objekte mithilfe des **Import Worksheets** importieren. Achten Sie dabei darauf, dass für alle im Arbeitsblatt angezeigten Objekte die neuste Version des Continia Delivery Networks ausgewählt ist. Continia Delivery Network-Objekte haben die folgende Versionslistenstruktur:

- `DN[localization][NAV version].[major version].[service pack].[hotfix]`

Die folgende Tabelle enthält zwei Beispiele für Versionslisten:

<br>

| Version                                                                                                         | Versionsliste                                                                                        |
| --------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Continia Delivery Network Version 1, Service pack 1, für Microsoft Dynamics NAV 2018, W1 Localization           | DNW111.00.00.1.01                    |
| Continia Delivery Network Version 1, Service Pack 2, Hotfix 1, für Microsoft Dynamics NAV 2018, DK Localization | DNDK11.00.00.1.02.01 |

<br>

Normalerweise empfehlen wir, beim Importieren von Objekten im Zusammenhang mit einem Continia-Produkt-Upgrade **Alle ersetzen** auszuwählen. Dies ist jedoch bei Continia Delivery Network-Objekten nicht unbedingt der Fall, da Sie immer die neuesten Versionen dieser Objekte installiert haben müssen und Produktpakete manchmal ältere Continia Delivery Network-Objekte enthalten. Sie können die integrierte Intelligenz des **Import Worksheets** nutzen, um zu bestimmen, wann Sie alle Objekte ersetzen sollten und wann nicht, wie in den folgenden Beispielen:

### Beispiel 1

In diesem Szenario besteht die Aufgabe darin, Continia Document Output auf Version 3.27 in einem System zu aktualisieren, auf dem die folgenden Anwendungen installiert sind:

- Continia Document Capture 7.01
- Continia Delivery Network 1.01
- Continia Document Output 3.26

Das Produktpaket Document Output 3.27 enthält Objekte für Version 1.00.02 des Continia Delivery Networks. Dies bedeutet, dass die Objekte des Produktpakets älter sind als die, die bereits im System installiert sind. Das **Import Worksheet** erkennt dies automatisch und setzt die **Aktion** auf **Überspringen** (anstatt auf **Ersetzen**), damit Sie _nicht_ alle Continia Delivery Network-Objekte ersetzen, sondern stattdessen einfach **OK** auswählen müssen.

### Beispiel 2

In diesem Szenario besteht die Aufgabe darin, Document Output auf Version 5.01 in einem System zu aktualisieren, auf dem die folgenden Anwendungen installiert sind:

- Document Capture 7.01
- Continia Delivery Network 1.01
- Document Output 3.27

Das Produktpaket Document Output 5.01 enthält Objekte für Version 2.01 des Continia Delivery Networks. Dies bedeutet, dass die Objekte des Produktpakets neuer sind als die, die bereits im System installiert sind. Das **Import Worksheet** erkennt dies automatisch und setzt die **Aktion** auf **Ersetzen** (anstatt **Überspringen**), damit Sie **Alle ersetzen** auswählen können, um alle Continia Delivery Network-Objekte zu ersetzen.

## Informationen zum Thema

[Grundlegendes zum Continia Delivery Network](@DC-53)