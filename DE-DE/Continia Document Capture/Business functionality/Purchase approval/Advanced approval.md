---
title: Erweiterte Genehmigung in Document Capture
date: 07-07-2025
description: Eine Beschreibung der erweiterten Genehmigung und deren Funktionsweise, einschließlich anschaulicher Beispiele.
id: DC-38
lang: de
---

# Erweiterte Genehmigung

Bei der [Standardeinkaufsgenehmigung](Standard purchase approval.md) und bei [Genehmigungsabläufen](@DC-33) in Continia Document Capture ist der Genehmigungsvorgang festgelegt und basiert ausschließlich auf Rechnungsbeträgen. Als Alternative dazu bietet die erweiterte Genehmigung einen schnelleren und flexibleren Genehmigungsprozess, der sowohl auf Rechnungsbeträgen als auch auf [Dimensionen](https://docs.microsoft.com/de-de/dynamics365/business-central/finance-dimensions) basiert. Dies hat folgende Vorteile:

- Sie können die Dimensionen, mit denen Genehmiger für Rechnungen identifiziert werden, definieren.
- Der nächste Genehmiger wird erst identifiziert, wenn der aktuelle Genehmiger alle relevanten Rechnungszeilen genehmigt hat.
- Belegzeilen, die vom aktuellen Genehmiger genehmigt werden müssen, sind sowohl auf der Seite **Genehmigungsposten** in Microsoft Dynamics 365 Business Central als auch im Continia Web Approval Portal fett markiert.

Das Konzept der erweiterten Genehmigung lässt sich am besten anhand von Szenarien erklären, die [unten](#beispielszenarien-fur-die-erweiterte-genehmigung) beschrieben werden. In diesem Artikel werden zur Veranschaulichung Rechnungen verwendet; die Funktionalität kann jedoch auch für Gutschriften verwendet werden.

> [!NOTE]
> Um die erweiterte Genehmigung verwenden zu können, muss diese aktiviert und eingerichtet werden. Dies wird unter [Erweiterte Genehmigung einrichten](@DC-31) beschrieben.

## Beispielszenarien für die erweiterte Genehmigung

Bei der erweiterten Genehmigung werden die Genehmiger von Rechnungen anhand der von Ihnen definierten Dimensionen bestimmt zusammen mit den Rechnungszeilenbeträgen.

> [!NOTE]
> Wenn in einem Beleg keine Werte für die in der erweiterten Genehmigung angegebenen Dimensionen aufweist, berücksichtigt Document Capture bei der Auswahl des Genehmigers nur den Gesamtzeilenbetrag.

In diesen Szenarien wird eine erweiterte Genehmigungsgruppe mit der Dimension **Abteilung** verwendet, und die Benutzer Bernhard Kohler, Louisa Günther und Detlef Hembrock wurden als Genehmiger hinzugefügt. Sie haben unterschiedliche Genehmigungslimits für die beiden Dimensionswerte **Produktion** und **Verkauf**:

<br>

| Genehmiger(in) | Abteilung           | Genehmigungslimit        |
| --------------------------------- | ------------------- | ------------------------ |
| Bernhard Kohler                   | Produktion          | 25.000 $ |
| Louisa Günther                    | Verkauf             | 25.000 $ |
| Detlef Hembrock                   | Produktion, Verkauf | 40.000 $ |

Der Einfachheit halber basieren diese Szenarien nur auf der Dimension **Abteilungscode** und nur drei Genehmigern in der Genehmigungsgruppe. Allerdings können mehrere Dimensionen und zahlreiche Genehmiger verwendet werden, was sowohl die Flexibilität als auch die Komplexität erhöht.

### Szenario A

Eine Rechnung mit den folgenden Zeilendimensionswerten und -beträgen wird zur Genehmigung gesendet:

<br>

| Zeilennr. | Abteilung  | Betrag                  |
| ------------------------- | ---------- | ----------------------- |
| 1                         | Produktion | 5.000 $ |
| 2                         | Verkauf    | 5.000 $ |

Theoretisch könnte diese Rechnung zur vollständigen Genehmigung an Detlef Hembrock gesendet werden, da er über die Berechtigung und ein ausreichendes Genehmigungslimit verfügt, um beide Dimensionswerte und damit beide Zeilen zu genehmigen. Allerdings ist Detlef Hembrock der höchstrangige Genehmiger und in Document Capture sollen hochrangige Genehmiger so wenig wie möglich belastet werden. Daher wird die Rechnung zuerst an Bernhard Kohler gesendet, dessen Genehmigungsberechtigung mit dem Dimensionswert der ersten Zeile (**Produktion**) übereinstimmt. Wenn Bernhard die erste Zeile genehmigt hat, wird die Rechnung an Louisa Günther weitergeleitet, deren Genehmigungsberechtigung mit der zweiten Zeile (**Verkauf**) übereinstimmt. Wenn Louisa die zweite Zeile genehmigt hat, ist die Rechnung vollständig genehmigt.

### Szenario B

Eine weitere Rechnung mit den folgenden Zeilendimensionswerten und -beträgen wird zur Genehmigung gesendet:

<br>

| Zeilennr. | Abteilung  | Betrag                   |
| ------------------------- | ---------- | ------------------------ |
| 1                         | Produktion | 20.000 $ |
| 2                         | Produktion | 20.000 $ |
| 3                         | Verkauf    | 20.000 $ |

Bei dieser Rechnung kann keiner der drei Genehmiger alle Zeilen genehmigen. Daher muss die Genehmigung unter ihnen aufgeteilt werden. Bernhard Kohler verfügt über die Berechtigung, Rechnungszeilen mit dem Dimensionswert **Produktion** zu genehmigen; sein Genehmigungslimit von 25.000 USD reicht hier jedoch nicht aus, da sich die beiden Zeilen für **Produktion** (Zeilen 1 und 2) auf insgesamt 40.000 USD belaufen. Aus diesem Grund muss der erste Genehmiger stattdessen Detlef Hembrock sein, dessen Genehmigungslimit ausreicht, um die ersten beiden Rechnungszeilen zu genehmigen.

Obwohl Bernhard auch die Berechtigung hat, **Verkauf**-Zeilen zu genehmigen, kann er die letzte Rechnungszeile nicht genehmigen, da der Gesamtbetrag der drei Zeilen dann sein Genehmigungslimit überschreiten würde. Daher muss Zeile 3 stattdessen von einer zweiten Genehmigerin, Louisa Günther, genehmigt werden, die **Verkauf**-Zeilen bis zu 25.000 $ genehmigen kann. Dies reicht aus, um die Genehmigung dieser verbleibenden Zeile abzudecken. Mit Esthers Genehmigung von Zeile 3 ist die Rechnung vollständig genehmigt.

## Beispielszenarien mit Vier-Augen-Genehmigung

Wenn Sie möchten, dass Rechnungen immer von mindestens zwei Genehmigern genehmigt werden, [aktivieren Sie die Einstellung für die Vier-Augen-Genehmigung](@DC-31#so-richten-sie-erweiterte-genehmigungsgruppen-ein). Dies wirkt sich je nach Einrichtung unterschiedlich aus. Im Folgenden wird dieselbe Genehmigungsgruppe wie [oben](#beispielszenarien-fur-die-erweiterte-genehmigung) verwendet, um die unterschiedlichen Szenarien zu veranschaulichen.

### Szenario A

In diesem Szenario wurde **Rechnung** ausgewählt, als die Vier-Augen-Genehmigung aktiviert und eingerichtet war.

Eine Rechnung mit mehreren Zeilen, die mehrere Genehmiger erfordern, wird zur Genehmigung gesendet. Da für die Vier-Augen-Genehmigung bereits mehr als ein Genehmiger erforderlich ist, wird die Vier-Augen-Genehmigung automatisch angewendet und Document Capture muss keine zusätzlichen Genehmiger identifizieren. Dies ist in den oben genannten Szenarien A und B der Fall, in denen beide Rechnungen mehrere Zeilen haben, die mehrere Genehmiger erfordern. Wäre in diesen Szenarien die Vier-Augen-Genehmigung aktiviert gewesen, wäre das Ergebnis dasselbe gewesen.

### Szenario B

In diesem Szenario wurde **Rechnung** ausgewählt, als die Vier-Augen-Genehmigung aktiviert und eingerichtet war.

Eine Rechnung wird zur Genehmigung gesendet, aber diese hat nur eine Zeile:

<br>

| Zeilennr. | Abteilung | Betrag                   |
| ------------------------- | --------- | ------------------------ |
| 1                         | Verkauf   | 21.000 $ |

Zwei der Genehmiger in der Genehmigungsgruppe verfügen über die erforderlichen Berechtigungen und Genehmigungslimits, um diese Zeile zu genehmigen: Louisa Günther (die **Verkauf**-Zeilen bis zu 25.000 US-Dollar genehmigen kann) und Detlef Hembrock (der **Verkauf**- und/oder **Produktion**-Zeilen für bis zu 40.000 US-Dollar genehmigen kann). Da Esther von beiden das niedrigere Genehmigungslimit hat, wird sie als erste Genehmigerin identifiziert. Wenn Esther die Zeile genehmigt hat, wird die Rechnung an Detlef gesendet.

### Szenario C

In diesem Szenario wurde **Rechnungsgesamtbetrag** ausgewählt, als die Vier-Augen-Genehmigung aktiviert und eingerichtet war. Daher müssen mindestens zwei Genehmiger den Gesamtbetrag jeder Rechnung genehmigen.

Eine Rechnung wird zur Genehmigung gesendet; dieses Mal mit den folgenden Zeilendimensionswerten und -beträgen:

<br>

| Zeilennr. | Abteilung  | Betrag                   |
| ------------------------- | ---------- | ------------------------ |
| 1                         | Produktion | 7.000 $  |
| 2                         | Produktion | 16.000 $ |

Bernhard Kohler hat Berechtigungen für die Genehmigung von **Produktion**-Zeilen und sein Genehmigungslimit von 25.000 US-Dollar reicht für beide Zeilen aus, also den gesamten Rechnungsbetrag. Deshalb wird er als erster Genehmiger identifiziert. Nachdem Bernhard die beiden Zeilen genehmigt hat, wird die Rechnung an Detlef Hembrock weitergeleitet, der ebenfalls über die erforderliche Berechtigung und das nötige Genehmigungslimit verfügt, um beide Zeilen zu genehmigen. Sobald Detlef die Zeilen als zweiter Überprüfer im Rahmen der Vier-Augen-Genehmigung genehmigt hat, ist die Rechnung vollständig genehmigt.

> [!NOTE]
> Beim [Einrichten erweiterter Genehmigungsgruppen](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/setting-up-advanced-approval#so-richten-sie-erweiterte-genehmigungsgruppen-ein) können Sie unter **Erster Posten angelegt durch** > **Einkäufer** auswählen, damit immer der Einkäufer als erster Genehmiger zugewiesen wird. Wenn die **Vier-Augen-Genehmigung** jedoch auf **Rechnungsgesamtbetrag und Dimensionen** anstatt auf **Rechnung** eingestellt ist, zählt der Käufer nicht als einer der beiden erforderlichen Genehmiger.

<style>
  .content table tr td:nth-child(1) {
    width: 300px;
  }
  .content table tr td:nth-child(2) {
    width: 300px;
  }  
</style>