---
title: Automatischer Belegabgleich
date: 13-03-2025
description: Automatischer Abgleich von Einkaufsrechnungen und Gutschriften mit zugehörigen Belegen
id: DC-70
lang: de
---

# Automatischer Belegabgleich

Wenn Sie den automatischen Abgleich einrichten, gleicht Continia Document Capture eingehende Rechnungen und Gutschriften automatisch mit den zugehörigen Belegen ab, basierend auf den Abgleichkriterien, die Sie beim Einrichten ausgewählt haben. Dies spart im Vergleich zum manuellen Abgleich viel Zeit und eignet sich besonders gut für Unternehmen, die große Mengen an eingehenden Belege erhalten.

Sie können zum Beispiel festlegen, ob Zeilen erkannt und abgeglichen werden sollen. Diese Einstellung hat erhebliche Auswirkungen auf den automatischen Abgleichprozess, da sich der Abgleich auf Zeilenebene sehr vom Abgleich mit dem Belegkopf unterscheidet. Die Unterschiede werden in den folgenden Abschnitten erläutert.

Um den Abgleich auf Kopfebene einzurichten, finden Sie Informationen unter [Automatischen Abgleich konfigurieren](@DC-68). Informationen zum Einrichten des Zeilenabgleichs finden Sie unter [Zeilenabgleich einrichten](@DC-69).

> [!TIP]
> Document Capture unterstützt den Abgleich einer Eingangsrechnung mit einer oder mehreren Einkaufslieferungen und/oder Einkaufsbestellungen, sei es auf Kopf- oder Zeilenebene. Darüber hinaus kann Document Capture Gutschriften mit einer oder mehreren Rücklieferungen und/oder Reklamationen abgleichen.

## Allgemeine Abgleichparameter

Unabhängig davon, ob Zeilenabgleich aktiviert wurde oder nicht, wendet Document Capture allgemeine Abgleichparameter an, um eine Übereinstimmung zwischen einer eingehenden Rechnung/Gutschrift und anderen zugehörigen Belegen zu ermitteln (Bestellungen/Lieferungen für Rechnungen und Reklamationen/Rücksendungen für Gutschriften). Die angewandten Filter grenzen die Anzahl potenzieller Übereinstimmungen ein, bevor andere Abgleichkriterien in Bezug auf Kopf oder Zeilen angewendet werden.

**Pflichtfilter (automatisch angewendet)**

- Kreditorennr.
- Währungscode
- Ausstehende Menge:
  - In Bestellzeilen darf die **Restbestellungsmenge** nicht Null sein.
  - In Lieferungszeilen darf **Lief. nicht fakt. Menge** nicht Null sein.
  > [!NOTE]
  > Mit diesem Filter werden Belegzeilen identifiziert, die noch nicht in Rechnung gestellt wurden.

**Optionale Filter**

- Bestellnummer – bezogen auf das Feld **Bestellnummer** im Belegjournal
- Kred.-Bestellnr.
- Kred.-Lieferungsnr.

## Kopfabgleich

Wenn Document Capture eine Rechnung oder Gutschrift mit zugehörigen Belegen auf Kopfebene abgleicht, werden die Zeilen der zugehörigen Belege mit dem Gesamtbetrag der Rechnung oder Gutschrift abgeglichen. Dabei werden die Menge und der Preis übereinstimmender Belegzeilen verwendet. Wenn Sie beispielsweise in den [Einstellungen für Zeilenabgleich](@DC-69) die Option **Menge abgleichen** auf **Ja – immer** gesetzt haben, muss jede mit einer Rechnungszeile abgeglichene Bestell- oder Einkaufslieferungszeile die gleiche Menge wie die Rechnungszeile aufweisen, um als gültiger Abgleich zu gelten.

Wenn der Gesamtrechnungsbetrag 1.005 $ betragen würde und Sie eine Abweichung von 10 $ festgelegt hätten, wäre die Einkaufslieferungszeile aus dem obigen Beispiel ebenfalls eine akzeptable Übereinstimmung. Aufgrund der Differenz von 5 $ handelt es sich jedoch nicht um eine vollständige Übereinstimmung. Daher wäre diese Zeile nur ausgewählt worden, wenn keine anderen, genaueren Übereinstimmungen identifiziert worden wären.

> [!TIP]
> In der Regel fallen die Gesamtbeträge von Eingangsrechnungen und Gutschriften sehr unterschiedlich aus. Das heißt, die Gesamtbeträge sind relativ eindeutig und der Abgleich mit dem Gesamtbetrag reicht oft aus, um eine zuverlässige Übereinstimmung sicherzustellen. Wenn es jedoch mehrere identische oder ähnliche Übereinstimmungen für einen Gesamtbetrag gibt, verwendet Document Capture einfach die erste erkannte Übereinstimmung, die aber möglicherweise nicht richtig ist. Um dies zu vermeiden, sollten Sie Ihre Kreditoren bitten, in allen Belegen an Sie immer eine Bestellreferenz anzugeben. Dadurch hat Document Capture außerdem Gesamtbetrag, der Währung und der Kreditorennummer einen zusätzlichen Abgleichparameter zur Verfügung, um Belege zuzuordnen und eine deutlich höhere Genauigkeit zu garantieren.

### Prioritätenliste der Suchmethoden

Um Übereinstimmungen für einen eingehenden Beleg auf Kopfebene zu ermitteln, durchsucht Document Capture die Belegzeilen mithilfe unterschiedlicher Suchmethoden in der unten aufgeführten Reihenfolge. Es wird die Methode angewendet, die die genaueste Übereinstimmung liefert.

> [!NOTE]
> Bei Rechnungen sucht Document Capture nach übereinstimmenden Bestell- und Lieferungszeilen, während bei Gutschriften nach übereinstimmenden Reklamations- und Rücklieferungszeilen gesucht wird. Die folgende Liste der Suchmethoden wird anhand von Rechnungen veranschaulicht.
>
> Die Einstellungen für die Suchmethoden in der Liste müssen auf der Vorlagenkarte unter **Einkaufsbelege** > **Bestellabgleich** > **Rechnungen abgleichen mit** entsprechend vorgenommen werden. Die erforderlichen Vorlageneinstellungen für die jeweilige Methode sind in der Liste angegeben.

<br>

| Priorität | Suchmethode                                                                                                                                  | Erforderliche Vorlageneinstellung |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------- |
| 1         | Alle Bestellungen und/oder Lieferungen werden mit dem Gesamtbetrag der eingehenden Rechnung abgeglichen.                     | **Lieferungen und Bestellungen**  |
| 2         | Alle Lieferungen werden mit dem Gesamtbetrag der eingehenden Rechnung abgeglichen.                                           | **Lieferungen**                   |
| 3         | Alle Lieferungen werden überprüft, um zu ermitteln, ob sie mit dem Gesamtbetrag der Eingangsrechnung übereinstimmen.         | **Lieferungen**                   |
| 4         | Alle Bestellungen werden überprüft, um zu ermitteln, ob sie mit dem Gesamtbetrag der Eingangsrechnung übereinstimmen.        | **Bestellungen**                  |
| 5         | Es wird versucht, den Gesamtbetrag der Eingangsrechnung mit einer Bestellung und allen zugehörigen Lieferungen abzugleichen. | **Lieferungen und Bestellungen**  |

Wenn die Differenz zwischen dem Rechnungs-/Gutschriftenbetrag und dem Gesamtbetrag der übereinstimmenden Belegzeilen bei einer der oben genannten Suchmethoden Null ist, überspringt Document Capture alle nachfolgenden Suchmethoden.

## Zeilenabgleich

Wenn Document Capture eine Rechnung oder Gutschrift mit zugehörigen Belegen bei aktiviertem Zeilenabgleich abgleicht, werden alle Zeilen der Rechnung oder Gutschrift nacheinander überprüft, um für jede Zeile in den zugehörigen Belegen eine übereinstimmende Zeile zu ermitteln. Dazu werden die von Ihnen angegebenen Abgleichkriterien verwendet. Wenn Sie beispielsweise in den [Einstellungen für Zeilenabgleich](@DC-69) die Option **Menge abgleichen** auf **Ja – immer** gesetzt haben, muss jede mit einer Rechnungszeile abgeglichene Bestell- oder Einkaufslieferungszeile die gleiche Menge wie die Rechnungszeile aufweisen, um als gültiger Abgleich zu gelten.

In den Einstellungen für den Zeilenabgleich stehen Ihnen mehrere Abgleichparameter zur Auswahl. Mit dem Parameter **EK-Preis abgleichen** ist es sogar möglich, einen Abweichungsbetrag oder -prozentsatz anzugeben. Wenn Sie beispielsweise in den [Einstellungen für Zeilenabgleich](@DC-69) die Option **Einstandspreis - Toleranz %** auf 5 einstellen und anschließend eine Rechnungszeile mit einem Einstandspreis von 100 $ abgleichen, identifiziert Document Capture Bestell- und Lieferungszeilen mit einem Einstandspreis zwischen 95 $ und 105 $ als gültige Übereinstimmungen, sofern andere angegebene Parameter auch zutreffen.

Der Abgleich von Belegen auf Zeilenebene in Kombination mit den verschiedenen für den Zeilenabgleich verfügbaren Parametern ermöglicht Document Capture einen genaueren Abgleich als dem auf Kopfebene. Allerdings wird dadurch auch die Komplexität des Prozesses erhöht, was für Sie möglicherweise nicht notwendig ist. Überlegen Sie sich daher, welche Konfiguration für Ihr Unternehmen die richtige ist.

## Automatischen Abgleich ausführen

Beide Arten des automatischen Abgleichs werden wie unten beschrieben durchgeführt, abhängig davon, ob Sie während der Einrichtung die Funktion **Automatischer Abgleich** aktiviert haben oder nicht:

Die Funktion **Automatischer Abgleich ist aktiviert:** Der automatische Abgleich wird ausgeführt, wenn Sie [im Belegjournal **Felder erkennen** auswählen](/continia-document-capture/business-functionality/documents-and-templates/working-with-paper-and-pdf-documents#capturing-fields). Werden beim [Import des Belegs](@DC-82) alle Belegfelder korrekt erkannt, erfolgt der Abgleich sogar automatisch beim Import. In jedem Fall wird im Bemerkungsbereich des Belegjournals bestätigt, dass der Beleg erfolgreich mit einem anderen Beleg abgeglichen wurde.

Wenn **Automatischer Abgleich** aktiviert ist, **Rechnung Reg. Schritt 1** entweder auf **Bestellung zuordnen & Rechnung erzeugen** oder **Bestellung zuordnen und aktualisieren** eingestellt ist und kein Abgleich vorliegt, werden Sie von Document Capture im Abschnitt **Bemerkungen** entsprechend benachrichtigt. Sie können den Beleg jedoch trotzdem registrieren.

> [!NOTE]
> Im Belegjournal unter **Belegkopf** können Sie den automatischen Abgleichprozess erneut auslösen, indem Sie die identifizierte **Bestellnummer** oder den **Betrag ohne MwSt.** ändern, sofern dies erforderlich ist.

Die Funktion **Automatischer Abgleich** ist deaktiviert: Der automatische Abgleich muss manuell von Ihnen ausgelöst werden. Gehen Sie hierzu wie folgt vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie den Code **EINKAUF** aus, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste den Beleg aus, den Sie automatisch mit anderen Belegen abgleichen möchten.
4. Weisen Sie dem Beleg falls nötig [einen Kreditor zu](/continia-document-capture/business-functionality/documents-and-templates/working-with-paper-and-pdf-documents#den-mit-einem-beleg-verknupften-kreditor-andern).
5. Klicken Sie in der Aktionsleiste auf **Bestellabgleich**, um die Seite **Bestellabgleich** (oder die Seite **Gutschrift Abgleich** für Gutschriften) zu öffnen.
6. Klicken Sie in der Aktionsleiste auf **Start** > **Bestellabgleich**.

Document Capture gleicht den Beleg jetzt automatisch mit anderen Belegen ab. Im Inforegister **Bestellzeilen** werden die Zeilen, die automatisch abgeglichen wurden, fett dargestellt. Im Bereich **Bemerkungen** des Belegjournals wird bestätigt, dass der Beleg erfolgreich mit einem anderen Beleg abgeglichen wurde.

## Informationen zum Thema

[Manueller Belegabgleich](@DC-62)  
[Umgang mit Abweichungen, einschließlich Teilabgleich](@DC-63)
