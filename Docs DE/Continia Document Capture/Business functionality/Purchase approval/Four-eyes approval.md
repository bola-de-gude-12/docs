---
title: Vier-Augen-Genehmigung
date: 04-10-2024
description: Informationen zur Vier-Augen-Genehmigung und Identifizierung von Genehmigern (manuell oder automatisch).
id: DC-35
lang: de
---

# Vier-Augen-Genehmigung

Mit der Vier-Augen-Genehmigung soll sichergestellt werden, dass jeder Beleg, der zur Genehmigung eingereicht wird, von mindestens zwei Genehmigern (vier Augen) genehmigt wird. Nach der Aktivierung gilt die Vier-Augen-Genehmigung für alle Belege – sie kann nicht für einzelne Belege aktiviert oder deaktiviert werden. Allerdings gibt es zwei Ausnahmen, in denen die Vier-Augen-Genehmigung nicht gilt, auch wenn sie aktiviert wurde:

- Wenn die Beleggenehmigung durch einen [Genehmigungsablaufcode](@DC-33) initiiert wird, wird die Vier-Augen-Genehmigung nicht angewendet.
- Wenn Sie [einen **Vier-Augen-Schwellenwert (MW)** konfigurieren](@DC-22#so-richten-sie-die-einkaufsgenehmigung-ein), der eine Vier-Augen-Genehmigung für alle Rechnungen auslöst, die diesen Schwellenwert überschreiten, wird die Vier-Augen-Genehmigung nicht für Rechnungen mit niedrigeren Werten angewendet.

Wenn ein Beleg, der genehmigt werden soll, nur einen Genehmiger hat, muss ein zweiter Genehmiger hinzugefügt werden, wenn die Vier-Augen-Genehmigung aktiviert wurde. Der zweite Genehmiger kann je nach Konfiguration manuell oder automatisch identifiziert und hinzugefügt werden:

> [!NOTE]
> Informationen zum Aktivieren und Einrichten der Vier-Augen-Genehmigung in der Document Capture Einrichtung finden Sie unter [Einkaufsgenehmigung aktivieren](@DC-22). Die Vier-Augen-Genehmigung für die erweiterte Genehmigung muss jedoch in der **Genehmigungsgruppe** eingerichtet werden. Weitere Informationen finden Sie unter [So richten Sie erweiterte Genehmigungsgruppen ein](@DC-31#so-richten-sie-erweiterte-genehmigungsgruppen-ein) und unter [Erweiterte Genehmigung](@DC-38#vier-augen-genehmigung).

## Manuelle oder automatische Identifizierung von Genehmigern

Wenn ein Beleg, der genehmigt werden soll, nur einen Genehmiger hat, muss ein zweiter Genehmiger hinzugefügt werden, wenn die Vier-Augen-Genehmigung aktiviert wurde. Die Identifizierung des zweiten Genehmigers kann so eingerichtet werden, dass sie entweder automatisch durch Continia Document Capture oder manuell durch den ersten Genehmiger erfolgt.

- Wenn bei der Einrichtung **Automatische Auswahl** gewählt wurde, identifiziert Document Capture den zweiten Genehmiger basierend auf den Einstellungen des ersten Genehmigers (mit dem Feld **4. Augen Genehmigung, 2ter. Genehmiger Name** in der **Continia Benutzereinrichtung** des ersten Genehmigers). In diesem Fall fügt Document Capture automatisch den zweiten Genehmiger hinzu, und es sind keine manuellen Aktionen erforderlich.
- Wenn bei der Einrichtung **Manuelle Auswahl** gewählt wurde, muss der erste Genehmiger den zweiten Genehmiger bei der Genehmigung des Belegs manuell auswählen. Ein Dialogfeld fordert den ersten Genehmiger auf, den Beleg an einen anderen Genehmiger mit der Aktion **Weiterleiten und genehmigen** weiterzuleiten.

## Informationen zum Thema

[Document Capture Einrichtung](@DC-22)