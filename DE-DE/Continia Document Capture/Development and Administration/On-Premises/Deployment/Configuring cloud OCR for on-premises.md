---
title: |
  Cloud OCR für NAV oder Business Central On-Premises konfigurieren
date: 22-04-2024
description:
id: DC-141
lang: de
---

# Cloud OCR für NAV oder Business Central On-Premises konfigurieren

OCR steht für Optical Character Recognition (optische Zeichenerkennung) und bezeichnet die automatische Texterkennung, bei der der Textinhalt eines gescannten Bildes oder einer PDF-Datei extrahiert und in Daten umgewandelt wird, die von einem Computer verarbeitet werden können.

Wenn Sie Microsoft Dynamics 365 Business Central Online verwenden, ist Ihre Standard-OCR-Methode Continia Cloud OCR, wofür keine zusätzliche Konfiguration erforderlich ist.

Wenn Sie jedoch Microsoft Dynamics NAV/Business Central On-Premises verwenden, können Sie entweder On-Premises OCR oder Continia Cloud OCR verwenden. Continia Cloud OCR wird weiter unten ausführlich beschrieben, während Sie eine detaillierte Beschreibung der On-Premises-Methode im Artikel [On-Premises OCR konfigurieren](Configuring on-premises OCR/Configuring on-premises OCR.md) finden.

\##Setting up Continia Cloud OCR for NAV/Business Central on-premises
When you use Continia Cloud OCR, Continia will provide you with a system-generated dedicated email address that you must send or scan documents to in order to import them into Continia Document Capture. Diese Adresse sieht ungefähr so aus: <xyz.2342341@continiaonline.com>.

Dies ist keine E-Mail-Adresse, die man sich leicht merken kann, und auch keine, die Sie wahrscheinlich an Ihre Kreditoren weitergeben würden, damit diese Dokumente direkt an Document Capture senden können. Wir empfehlen Ihnen daher, stattdessen bei Ihrem eigenen E-Mail-Dienst eine weitere E-Mail-Adresse zu erstellen und alle E-Mails, die an diese Adresse gesendet werden, an die Continia-E-Mail-Adresse weiterleiten zu lassen. Beispielsweise sollten alle an <invoice@company.com> gesendeten E-Mails an <xyz.2342341@continiaonline.com>weitergeleitet werden. Auf diese Weise haben Sie eine leicht zu merkende E-Mail-Adresse, die Sie auch Ihren Kreditoren zur Übermittlung von Einkaufsrechnungen und Gutschriften zur Verfügung stellen können.

> [!NOTE]
> Bevor Sie mit dem folgenden Einrichtungsprozess beginnen, überprüfen Sie, ob Sie sich für Continia Cloud OCR angemeldet haben. Stellen Sie außerdem sicher, dass Sie den **Document Capture Konfigurationsassistenten** ausgeführt haben.

Um Continia Cloud OCR für NAV/Business Central On-Premises einzurichten, führen Sie diese Schritte aus:

1. Suchen Sie ({{search}}) nach **Document Capture Einrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Aktivieren Sie auf der Seite **Document Capture Einrichtung** auf dem Inforegister **Allgemein** die Option **Cloud OCR verwenden**, indem Sie das Kontrollkästchen aktivieren.<a href="#footnote-1"><sup>1</sup></a>
3. Es wird ein Dialogfeld angezeigt, in dem Sie gefragt werden, ob Sie alle Belegkategorien zu Cloud OCR exportieren möchten. Wählen Sie **Ja**.
4. Optional (empfohlen): Richten Sie mit Ihrem eigenen E-Mail-Dienst eine lokale E-Mail-Adresse mit Ihrer eigenen Domäne ein und lassen Sie alle eingehenden E-Mails an die speziell eingerichtete Continia Cloud OCR-E-Mail-Adresse weiterleiten. Geben Sie die neue lokale E-Mail-Adresse an die Unternehmen weiter, die Ihnen Dokumente zur OCR-Verarbeitung in Document Capture senden.

<small style>
<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1">Wenn Sie Continia Cloud OCR verwenden, müssen Sie den Document Capture-Dienst oder den ABBYY-Dienst nicht installieren.</li>

  </ol>
</div>
</small>

> [!NOTE]
> Um Ihre spezielle Continia Cloud OCR-E-Mail-Adresse zu finden, suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Link aus. Unter **E-Mail (Continia Cloud OCR)** werden Ihre speziellen Cloud OCR-Adressen für die einzelnen Belegkategorien angezeigt. Sie sollten für jede relevante Belegkategorie eine lokale E-Mail-Adresse erstellen.

## Informationen zum Thema

[On-Premises OCR konfigigurieren](Configuring on-premises OCR/Configuring on-premises OCR.md)  
[Document Capture einrichten](/Continia Document Capture/Setting up Document Capture/Setting up Document Capture.md)