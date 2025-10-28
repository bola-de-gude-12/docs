---
title: Übersicht über den Bestell- und Lieferabgleich in Document Capture
date: 29-10-2024
description: Eine Übersicht über die Grundlagen des Belegabgleichs, einschließlich einer Reihe von Links zu anderen Artikeln mit Informationen über Abgleich.
id: DC-61
lang: de
---

# Überblick über Bestell- und Lieferabgleich

Beim Belegabgleich werden Belege verglichen, um deren Übereinstimmung sicherzustellen. So können Sie die Kontrolle darüber behalten, dass Sie beispielsweise nicht mehr bezahlen als Sie erhalten haben oder dass Sie nicht mehr Waren versenden als vereinbart. Mit Continia Document Capture können Sie eingehende Rechnungen und Gutschriften mit zugehörigen Belegen wie Bestellungen und Lieferungen abgleichen. Sie können dies manuell durchführen oder von Document Capture automatisch ausführen lassen.

Während das manuelle Verfahren keinerlei Einrichtung erfordert, muss der automatische Abgleich entsprechend Ihren Anforderungen aktiviert und konfiguriert werden. Informationen hierzu finden Sie unter [Bestell- und Lieferabgleich einrichten](@DC-60).

> [!NOTE]
> Abgleich ist in der Kategorie **EINKAUF** verfügbar und mit den folgenden Belegtypen möglich:
>
> - Einkaufsrechnungen können mit Einkaufsbestellungen, Einkaufslieferungen oder beidem abgeglichen werden.
> - Einkaufsgutschriften können mit Reklamationen, Rücklieferungen oder beidem abgeglichen werden.
>
> Außerdem ist ein Abgleich mit Einkaufsbelegen und Rücklieferungen mit Sendungsverfolgung möglich; Bestellzeilen und Rücklieferungszeilen mit Sendungsverfolgung werden jedoch nicht unterstützt.

Damit ein Abgleich erfolgreich ist, müssen die Belege, die miteinander abgeglichen werden, in der Regel die **gleiche Währung** haben und die **Kreditorennummern müssen identisch sein**. Hierbei gibt es jedoch zwei nennenswerte Ausnahmen:

- Wenn der Währungscode eines eingehenden Belegs mit dem Mandantenwährungscode (**MW**) übereinstimmt und der abzugleichende Beleg überhaupt keinen Währungscode enthält, wird dieser trotz der Währungsabweichung als Übereinstimmung akzeptiert. Wenn eine Rechnung beispielsweise in Euro ausgestellt ist und in der entsprechenden Bestellung keine Währung angegeben ist, können die beiden Belege erfolgreich abgeglichen werden, wenn auch die Mandantenwährung Euro ist.
- Wenn Sie beispielsweise eine Rechnung von einer Filiale erhalten, deren Kreditorennummer nicht mit der Nummer der Filiale übereinstimmt, bei der Sie die Bestellung aufgegeben haben, kann trotz dieser Abweichung eine Zuordnung von Rechnung und Bestellung erfolgen, sofern Sie auf der Kreditorenkarte beide Kreditorennummern eingetragen haben. Die Nummer des Kreditors, bei dem Sie kaufen, wird im Inforegister **Allgemein** unter **Nr.** angegeben, während Sie die Nummer des Kreditors, an den Sie zahlen, im Inforegister **Fakturierung** unter **Zahlung an Kred.-Nr.** eingeben können.

Jede Bestellung, die teilweise mit einer Rechnung abgeglichen ist, wird gesperrt, bis die Rechnung gebucht wurde. Dies bedeutet, dass Sie keine zusätzlichen Waren oder Dienstleistungen für diese Bestellung erhalten oder in Rechnung stellen können, bis die entsprechende Rechnung gebucht wurde. Dies gilt auch für Gutschriften, jedoch für Reklamationen anstelle von Bestellungen. Diese Einschränkung wurde als Sicherheitsmaßnahme implementiert, um sicherzustellen, dass die Bestellung (oder Reklamation) nicht plötzlich vollständig gebucht wird und die ursprünglich abgeglichene Rechnung (oder Gutschrift) nicht mehr gebucht werden kann.

Weitere Informationen zu verschiedenen Aspekten des Belegabgleichs finden Sie unter den Links in der folgenden Tabelle:

<br>

| Thema                                                                   | Siehe                                                          |
| ----------------------------------------------------------------------- | -------------------------------------------------------------- |
| Belege manuell abgleichen                                               | [Manueller Belegabgleich](@DC-62)                              |
| Belege automatisch abgleichen lassen, einschließlich Zeilenabgleich     | [Automatischer Belegabgleich](@DC-70)                          |
| Belege teilweise abgleichen und Preis- und Mengenabweichungen verwalten | [Umgang mit Abweichungen, einschließlich Teilabgleich](@DC-63) |
| Filter mit verschiedenen Kriterien beim Zeilenabgleich anwenden         | [Zeilen beim Abgleich filtern](@DC-64)                         |

## Informationen zum Thema

[Bestell- und Lieferabgleich einrichten](@DC-60)