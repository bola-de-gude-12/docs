---
title: Integration der QR-Bill Management App
date: 30-01-2025
description:
id: DC-217
lang: de
---

# Integration der QR-Bill Management App

> [!IMPORTANT]
> Dieser Artikel gilt nur für Microsoft Dynamics 365 Business Central 2023 Release Wave 1 (BC v22) und höher.

Wenn Sie die von Microsoft für den Schweizer Markt entwickelte QR-Bill Management App installiert haben, kann diese mit Continia Document Capture integriert werden, indem der Inhalt jedes identifizierten QR-Codes direkt in die App kopiert wird. Wenn ein Einkaufsbeleg mit einem gültigen QR-Code in Document Capture importiert wird, wird der QR-Code von Document Capture automatisch identifiziert und gelesen und die erfassten QR-Daten werden dann bei der Registrierung des Belegs an die QR-Bill Management App übertragen.

Die folgenden Felder im Inforegister **QR-Rechnung** werden bei der Belegregistrierung automatisch mit den erfassten Daten ausgefüllt:

- **IBAN/QR-IBAN**
- **Währung**
- **Abrechnungsinformationen**
- **Betrag**
- **Unstrukturierte Meldung**

Auch in erfassten QR-Codes enthaltene Zahlungsreferenzen werden automatisch in das entsprechende Feld in Microsoft Dynamics 365 Business Central übertragen. In registrierten Rechnungen finden Sie diese, wenn Sie die Rechnung öffnen. Gehen Sie dann zum Inforegister **Rechnungsdetails** und dann zum Feld **Zahlungsreferenz**.

Darüber hinaus führt Document Capture auch andere QR-bezogene Aktionen aus, wenn Sie einen Beleg mit einem QR-Code registrieren:

- Die im QR-Code erkannte IBAN wird zur Identifizierung des Kreditors verwendet, der den Beleg gesendet hat.
- Es wird überprüft, ob der erfasste Belegbetrag dem Betrag des QR-Codes entspricht.
- Beim Anlegen eines Kreditoren-Bankkontos aus einem QR-Code werden die folgenden Felder automatisch aus dem Bankenstamm ausgefüllt:
  - **Name**
  - **Adresse**
  - **Adresse 2**
  - **Ort**
  - **PLZ**
  - **SWIFT-Code**

> [!IMPORTANT]
> Das automatische Ausfüllen der Kreditorfelder erfordert einen aktualisierten Bankenstamm. So erhalten Sie die aktuellsten Clearing-Nummern:
>
> 1. Laden Sie die TXT-Datei von der Seite [Download Bankenstamm](https://www.six-group.com/de/products-services/banking-services/interbank-clearing/online-services/download-bank-master.html) der SIX-Website herunter. Gehen Sie als Nächstes zu Business Central.
> 2. Wählen Sie das Symbol {{search}}, geben Sie **Bankenstamm** ein, und wählen Sie dann den zugehörigen Link.
> 3. Wählen Sie auf der Seite **Bankenstamm** die Option **Bankenstamm einlesen** aus. Wählen Sie dann die in Schritt 1 heruntergeladene TXT-Datei aus.