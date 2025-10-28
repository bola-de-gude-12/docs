---
title: Geteilte Genehmigung
date: 24-03-2024
description: Eine Einführung in die geteilte Genehmigung
id: DC-37
lang: de
---

# Geteilte Genehmigung

Die geteilte Genehmigung ermöglicht es Ihnen, Ihre Genehmigungsaufgaben für einen bestimmten Zeitraum automatisch an einen anderen Genehmiger weiterzuleiten, falls Sie in diesem Zeitraum keine Belege genehmigen können. Der andere Genehmiger ist dann Ihr Vertreter, bis Sie wieder verfügbar sind.

Es gibt zwei Arten der geteilten Genehmigung:

- Administratoren können geteilte Genehmigung stellvertretend für andere Benutzer einrichten (für alle Benutzer und Zwecke)
- Sie können geteilte Genehmigung selbst einrichten, wenn Sie abwesend sind.

In beiden Fällen muss die geteilte Genehmigung bei Abwesenheit jedes Mal neu eingerichtet werden. Weitere Informationen dazu finden Sie unter [Geteilte Genehmigung einrichten](@DC-25).

## Unnötige Genehmigungsanforderungen vermeiden

Wenn Sie Ihre Genehmigungen an einen anderen höherrangigen Genehmiger weiterleiten, kann es sein, dass dieser Genehmiger denselben Beleg mehrmals genehmigen muss. Um dies zu vermeiden, überprüft Continia Document Capture die nächste Genehmigungsanforderung in der Genehmigungskette, um zu ermitteln, ob der Beleg vom aktuellen Genehmiger genehmigt werden kann. Wenn ja, wird er automatisch genehmigt, sodass der Genehmiger den gleichen Beleg nicht zweimal zur Genehmigung erhält.

Diese Funktionalität ist für alle unterstützten Einkaufsbelegarten aktiviert:

- Rechnungen
- Gutschriften
- Bestellungen
- Reklamationen

Die Funktion wird für die Continia-Standardgenehmigung und die Genehmigung mit Genehmigungsablaufcodes unterstützt. Sie wird nicht für die erweiterte Genehmigung und Genehmigung anhand von Berechtigungen für Konten und Dimensionen unterstützt.

> [!NOTE]
> Nur Genehmigungsanforderungen, die in der Genehmigungskette in aufeinanderfolgender Reihenfolge erscheinen, werden automatisch genehmigt.

## Informationen zum Thema

[Geteilte Genehmigung einrichten](@DC-25)