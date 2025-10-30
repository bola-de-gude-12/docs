---
title: eDocuments Erweiterte Bestellflows
date: 10-07-2025
id: DC-237
lang: de
description: Eine Beschreibung der erweiterten Bestellfunktion in eDocuments.
---

# eDocuments Erweiterte Bestellflows

Dieser Artikel beschreibt die erweiterte Bestellfunktion in eDocuments, die die Änderung und Stornierung elektronischer Bestellungen (eBestellungen) ermöglicht, die über das Peppol-Netzwerk in Continia Document Capture ausgetauscht werden.

Während der standardmäßige eBestellflow Bestellungen und Bestellantworten unterstützt, ermöglicht der erweiterte eBestellflow auch Stornieren und Ändern von Bestellungen. Dies bietet Ihnen mehr Flexibilität bei der Auftragsabwicklung als Debitor (Käufer) oder als Kreditor (Verkäufer).

{% hint style="info" %}
Technisch gesehen werden Änderungen und Stornierungen nur dann als solche angezeigt, wenn sie vom Einkäufer gesendet werden. Bei Versand durch den Verkäufer werden diese als Bestellantworten angezeigt.
{% endhint %}

Die folgenden Szenarien veranschaulichen die Abläufe, die durch die erweiterte Bestellfunktion ermöglicht werden.

{% hint style="warning" %}
Es wird nur eine Auftragsänderung pro Dokument unterstützt, entweder auf Debitoren- oder Kreditorenseite.
{% endhint %}

## Erstbestellung des Käufers

In diesem Szenario werden alle möglichen Ergebnisse angezeigt.

[![eDocuments advanced ordering - scenario A](../../../../images/DC/eDocuments/eDocuments%20advanced%20ordering%20-%20scenario%20A.jpg)](../../../../images/DC/eDocuments/eDocuments%20advanced%20ordering%20-%20scenario%20A.jpg)

## Vom Käufer geänderte Bestellung

In diesem Szenario fordert der Käufer eine Änderung der ursprünglichen Bestellung an. Diese Anfrage kann vom Verkäufer angenommen oder abgelehnt werden.

[![eDocuments advanced ordering - scenario B](../../../../images/DC/eDocuments/eDocuments%20advanced%20ordering%20-%20scenario%20B.jpg)](../../../../images/DC/eDocuments/eDocuments%20advanced%20ordering%20-%20scenario%20B.jpg)

## Vom Verkäufer geänderte Bestellung

In diesem Szenario fordert der Verkäufer eine Änderung der ursprünglichen Bestellung an. Diese Anfrage kann vom Käufer angenommen oder abgelehnt werden.

[![eDocuments advanced ordering - scenario C](../../../../images/DC/eDocuments/eDocuments%20advanced%20ordering%20-%20scenario%20C.jpg)](../../../../images/DC/eDocuments/eDocuments%20advanced%20ordering%20-%20scenario%20C.jpg)

## Vom Käufer stornierte Bestellung

In diesem Szenario verlangt der Käufer eine Stornierung. Diese Anfrage kann vom Verkäufer angenommen oder abgelehnt werden.

[![eDocuments advanced ordering - scenario D](../../../../images/DC/eDocuments/eDocuments%20advanced%20ordering%20-%20scenario%20D.jpg)](../../../../images/DC/eDocuments/eDocuments%20advanced%20ordering%20-%20scenario%20D.jpg)

## Vom Verkäufer stornierte Bestellung

In diesem Szenario reicht der Verkäufer eine Stornierung ein.

[![eDocuments advanced ordering - scenario E](../../../../images/DC/eDocuments/eDocuments%20advanced%20ordering%20-%20scenario%20E.jpg)](../../../../images/DC/eDocuments/eDocuments%20advanced%20ordering%20-%20scenario%20E.jpg)

## Informationen zum Thema

[eDocuments-Kreditorflows](../../../../Docs%20DE/Continia%20Document%20Capture/Business%20functionality/Continia%20eDocuments/@DC-221/)\
[eDocuments-Debitorflows](../../../../Docs%20DE/Continia%20Document%20Capture/Business%20functionality/Continia%20eDocuments/@DC-220/)
