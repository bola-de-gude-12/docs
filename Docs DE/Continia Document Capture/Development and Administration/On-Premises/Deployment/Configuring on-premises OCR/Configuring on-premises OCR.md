---
title: On-Premises OCR in Document Capture konfigurieren
date: 10-01-2025
description: So konfigurieren Sie OCR in On-Premises-Einrichtungen von Document Capture.
id: DC-150
lang: de
---

# On-Premises OCR konfigurieren

OCR steht für Optical Character Recognition (optische Zeichenerkennung) und bezeichnet die automatische Texterkennung, bei der der Textinhalt eines gescannten Bildes oder einer PDF-Datei extrahiert und in Daten umgewandelt wird, die von einem Computer verarbeitet werden können.

Wenn Sie Microsoft Dynamics 365 Business Central Online verwenden, ist Ihre Standard-OCR-Methode Continia Cloud OCR, wofür keine zusätzliche Konfiguration erforderlich ist.

Wenn Sie jedoch Microsoft Dynamics NAV/Business Central On-Premises verwenden, können Sie entweder On-Premises OCR oder Continia Cloud OCR verwenden. Die On-Premises-Methode wird weiter unten ausführlich beschrieben, während Sie eine umfassende Beschreibung von Continia Cloud OCR im Artikel [Cloud OCR für NAV oder Business Central On-Premises](@DC-141) finden.

> [!NOTE]
> Wenn Sie On-Premises OCR verwenden, müssen Sie als Speichertyp „Dateisystem“ verwenden. Weitere Informationen finden Sie unter  [Dokumentenspeicher einrichten](@DC-3).

## On-Premises OCR einrichten

Wenn Sie On-Premises OCR verwenden, wird Ihnen für den Dokumentimport keine systemgenerierte E-Mail-Adresse bereitgestellt, wie dies bei Continia Cloud OCR der Fall ist. Stattdessen müssen Sie für jede relevante Belegkategorie E-Mail-Adressen erstellen und konfigurieren, um Ihre Dokumente in Document Capture zu importieren. Sie müssen außerdem den OCR-Dienst und Document Capture einrichten, damit die importierten Dokumente per OCR verarbeitet und gespeichert werden können.

So richten Sie On-Premises OCR ein:

1. Stellen Sie sicher, dass Sie die Document Capture-Standardkonfiguration importiert haben.
2. Erstellen und konfigurieren Sie E-Mail-Adressen für jede relevante Belegkategorie. Weitere Informationen finden Sie unter [E-Mail-Adressen für den Dokumentimport erstellen und konfigurieren](Creating and configuring email addresses for document import.md).
3. Installieren Sie ABBYY und die Document Capture-Dienste. Weitere Informationen finden Sie unter [ABBYY und Document Capture-Dienste installieren](Installing ABBYY and Document Capture services.md).
4. Suchen Sie ({{search}}) nach **Document Capture Einrichtung** und wählen Sie dann den entsprechenden Link aus.
5. Gehen Sie auf der Seite **Document Capture Einrichtung** im Inforegister **Allgemein** zum Abschnitt **On-Premise OCR Datei Speicher**.
6. Geben Sie im Feld **Dateipfad für gescannte PDF** einen Pfad zu dem Ordner an, in dem Sie alle gescannten PDF-Dokumente speichern möchten. Dieser Ordner entspricht dem Stapel **Warten auf OCR** im Abschnitt **Continia Document Capture-Aktivitäten** des Rollencenters.
   > [!IMPORTANT]
   > Beachten Sie, dass der eingegebene Pfad mit dem Pfad identisch sein muss, der während der [Installation des Document Capture-Dienstes](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/installing-abbyy-and-document-capture-services#der-document-capture-dienst) in **Dateipfad für gescannte PDF** eingegeben wurde.
7. Geben Sie im Feld **Dateipfad für OCR-verarbeitete Dateien** einen Pfad zu dem Ordner an, in dem Sie alle gescannten PDF-Dokumente speichern möchten. Dieser Ordner entspricht dem Stapel **Bereit zum Import** im Abschnitt **Continia Document Capture-Aktivitäten** des Rollencenters.
   > [!IMPORTANT]
   > Beachten Sie, dass der eingegebene Pfad mit dem Pfad identisch sein muss, der während der [Installation des Document Capture-Dienstes](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/installing-abbyy-and-document-capture-services#der-document-capture-dienst) in **OCR-verarbeitete Dateien für NAV** eingegeben wurde.
8. Geben Sie im Feld **Dateipfad für XML** einen Pfad zu dem Ordner an, in dem Sie alle eingehenden XML-Dokumente (sofern vorhanden) speichern möchten.
9. Wählen Sie das Symbol {{search}}, geben Sie **OCR Konfigurationsdateien exportieren** ein, und wählen Sie dann den zugehörigen Link. Ein Dialogfeld bestätigt, dass eine Reihe von Konfigurationsdateien exportiert wurde. Wählen Sie **OK**, um es zu schließen.

> [!NOTE]
> Es wird empfohlen, dass Sie [UNC-Pfade](https://docs.microsoft.com/de-de/dotnet/standard/io/file-path-formats#unc-paths) verwenden, wenn Sie Ordnerpfade wie oben beschrieben angeben – zum Beispiel \\\\servername\share\DC\PDF\. Beachten Sie außerdem, dass das Dienstkonto, unter dem der Business Central-Dienst ausgeführt wird, über Lese-, Schreib- und Löschberechtigungen für die entsprechenden Ordner verfügen muss.

## Informationen zum Thema

[Cloud OCR für NAV oder Business Central On-Premises konfigurieren](@DC-141)  
[E-Mail-Adressen für den Dokumentenimport erstellen und konfigurieren](Creating and configuring email addresses for document import.md)  
[ABBYY und Document Capture-Dienste installieren](Installing ABBYY and Document Capture services.md)  
[Microsoft-Artikel über UNC-Pfade](https://docs.microsoft.com/de-de/dotnet/standard/io/file-path-formats#unc-paths)