---
title: eDocuments-Flows
date: 10-09-2025
description: Eine Beschreibung der von Continia eDocuments unterstützten Abläufe.
id: DC-183
lang: de
---

# eDocuments-Flows

Continia eDocuments unterstützt mehrere Dokumentenflows für die folgenden vier Dokumente:

- Rechnungen und Rechnungsantworten
- Gutschriften
- Bestellungen, Bestellbestätigungen, Bestellstornierungen und Bestelländerungen

In Zukunft werden noch weitere Dokumenttypen hinzugefügt, sodass mit Continia eDocuments später noch mehr Flows und Szenarien möglich sein werden.

Die folgenden Abschnitte beschreiben zwei typische Dokumentenflows zwischen zwei Parteien (Debitor und Kreditor) mit Continia eDocuments in Microsoft Dynamics 365 Business Central.

> [!NOTE]
> Die beschriebenen Flows verwenden beispielsweise das Peppol-Netzwerk. Stattdessen können aber auch viele andere ähnliche Netzwerke verwendet werden. Continia eDocuments unterstützt alle wichtigen Netzwerke und digitalen Infrastrukturen für den Austausch von Geschäftsdokumenten.

Anleitungen für die Verwendung dieser Flows finden Sie hier:

- [eDocuments-Debitorflows](@DC-220)
- [eDocuments-Kreditorflows](@DC-221)

## Bestellflow

Ein klassischer Bestellflow für Continia eDocuments umfasst einen Debitor (Einkäufer), der eine Bestellung bei einem Kreditor (Verkäufer) aufgibt, der dann auf diese Bestellung antwortet. Ein solcher Flow sieht typischerweise wie folgt aus:

1. Der Debitor [erstellt eine Einkaufsbestellung in Business Central und sendet sie an den Kreditor](@DC-220#so-senden-sie-eine-einkaufsbestellung) mit Continia eDocuments (über das Peppol-Netzwerk).

2. Der Kreditor [erhält die Bestellung und registriert sie als Business Central-Verkaufsauftrag](@DC-221#so-empfangen-sie-eine-bestellung-und-senden-eine-bestellantwort). Anschließend wird eine der folgenden Bestellbestätigungen entweder manuell oder automatisch vom Kreditor an den Debitor gesendet, die angibt, ob die Bestellung erfüllt werden kann:
   - **Bestellungsannahme**: Der Kreditor kann die Bestellung ausführen und nimmt sie vollständig an. Hier kann der Kreditor auch Angaben hinzufügen, die für den Debitor nützlich sind, um zum Beispiel die Artikelidentifizierung zu erleichtern.

   - **Bestelländerungen**: Der Kreditor kann die Bestellung nur teilweise erfüllen, da an einer oder mehreren Positionen Änderungen vorgenommen werden müssen (aufgrund von Preisänderungen, Artikelverfügbarkeit o.ä.).

   - **Bestellablehnung**: Der Kreditor kann den Auftrag überhaupt nicht ausführen und lehnt ihn deshalb ab.
   > [!NOTE]
   > Wenn der Kreditor die Bestellung ablehnt, muss der Debitor den Ablauf erneut starten, indem er eine neue Bestellung erstellt und an den Kreditor sendet.

3. Der Debitor erhält die entsprechende Bestellbestätigung in Business Central. Wenn der Debitor mit der Bestellung zufrieden ist, kann er sie annehmen und [registrieren](@DC-220#to-register-an-order-response). Dadurch wird die ursprüngliche Bestellung mit allen vom Kreditor vorgenommenen Änderungen aktualisiert. Andernfalls kann der Debitor die Bestellung entweder ganz stornieren oder Änderungen daran verlangen (sofern der Kreditor nicht bereits zuvor Änderungen übermittelt hat).

4. Abhängig von der Antwort des Debitors kann der Kreditor entweder die aktualisierte Bestellung annehmen und den Verkaufsauftrag buchen, wodurch automatisch eine gebuchte Verkaufsrechnung erstellt wird, oder den Verkaufsauftrag stornieren.

Die gebuchte Verkaufsrechnung kann dann im Rahmen [des unten beschriebenen Abrechnungsflows](#abrechnungsflow) an den Debitor gesendet werden.

> [!NOTE]
> Pro Dokument kann nur eine Auftragsänderung übermittelt werden.

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src=https://player.vimeo.com/video/1114186087?h=aedccc9114&badge=0&autopause=0&player_id=0&app_id=58479%22 frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="DC_Welcome_to_Document_Capture"></iframe></div><script src=https://player.vimeo.com/api/player.js></script>

## Abrechnungsflow

Ein klassischer Abrechnungsflow für Continia eDocuments umfasst einen Kreditor (Verkäufer), der eine Rechnung an einen Debitor (Käufer) sendet, der dann auf diese Rechnung antwortet. Ein solcher Flow sieht typischerweise wie folgt aus:

1. Der Kreditor erstellt in Business Central eine Verkaufsrechnung für die Artikel, die vom Debitor bestellt und an ihn versandt wurden, beispielsweise indem er als Teil [des Bestellflows](#bestellflow) oben einen Verkaufsauftrag bucht.
2. Der Kreditor [sendet die Verkaufsrechnung](@DC-221#so-senden-sie-eine-verkaufsrechnung) mithilfe von Continia eDocuments (über das Peppol-Netzwerk).
3. Der Debitor [erhält die Rechnung](@DC-220#so-empfangen-sie-eine-rechnung-und-senden-eine-rechnungsantwort), und eine der folgenden Rechnungsantworten wird entweder manuell oder automatisch vom Debitor an den Kreditor gesendet, wobei der Status der Rechnung angegeben wird:
   - **In Bearbeitung**: Der Debitor prüft die Rechnung.
   - **Unter Abfrage**: Der Debitor hat Klärungsbedarf oder Fragen zur Rechnung und möchte den Kreditor telefonisch oder per E-Mail kontaktieren.
4. Wenn keine weiteren Informationen benötigt werden, gleicht der Debitor die Rechnung mit der ursprünglichen Bestellung ab. Abhängig vom Ergebnis des Abgleichprozesses wird dann eine der folgenden Rechnungsantworten entweder manuell oder automatisch vom Debitor an den Kreditor gesendet:
   - **Abgelehnt**: Rechnung und Bestellung passen nicht zusammen, daher lehnt der Debitor die Rechnung ab.

     > [!NOTE]
     > Wenn der Debitor die Bestellung ablehnt, muss der Kreditor den Flow erneut starten, indem er eine neue Verkaufsrechnung erstellt und an den Debitor sendet.
   - **Unter Vorbehalt**: Die Rechnung und die Bestellung stimmen fast überein. Daher akzeptiert der Debitor sie unter bestimmten Bedingungen, zum Beispiel unter der Bedingung, dass der Kreditor den Preis anpasst.
   - **Akzeptiert**: Rechnung und Bestellung stimmen überein, so dass der Debitor sie akzeptiert.
5. Nach erfolgreichem Abgleich registriert der Debitor die Rechnung mit Document Capture und erstellt so eine Einkaufsrechnung.
6. Der Debitor bezahlt die Rechnung und eine **Bezahlt**-Benachrichtigung wird an den Kreditor gesendet.

> [!NOTE]
> Auf der Kreditorseite dienen alle Rechnungsantworten außer **Abgelehnt** lediglich der Information und erfordern keine Aktion. Bei Ablehnung einer Rechnung muss der Kreditor Maßnahmen ergreifen, indem er dem Debitor eine Gutschrift sendet.

## Das eDokumentenstatus-Feld

Bei allen Flows können sowohl Debitor als auch Kreditor den Status eines Dokuments während des gesamten Prozesses mithilfe des Felds **eDokumentenstatus** überwachen. Dieses Feld ist auf mehreren wichtigen Seiten verfügbar, beispielsweise auf den Seiten **Verkaufsauftrag**, **Einkaufsrechnung** und **Gebuchte Verkaufsrechnung**. Auf allen diesen Seiten befindet es sich im Inforegister **Allgemein**.

Wenn Sie die Statusmeldung im Feld **eDokumentstatus** für ein bestimmtes Dokument auswählen, wird die Seite **eDokument Übersicht** geöffnet. Auf dieser Seite werden alle Dokumentstatus und Aktivitäten aufgelistet, die für das Dokument automatisch protokolliert wurden. Es bietet auch zusätzliche nützliche Details wie **Änderung** (wenn Änderungen vorgenommen wurden) und **Unter Vorbehalt akzeptiert** (wenn ein Dokument unter bestimmten Bedingungen akzeptiert wurde).

## Informationen zum Thema

[Unterstützte ektronische Dokumentformate](@DC-55)  
[eDocuments erweiterte Bestellflows](@DC-237)