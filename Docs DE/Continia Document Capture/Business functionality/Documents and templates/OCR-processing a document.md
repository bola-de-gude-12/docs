---
title: OCR-Verarbeitung von Belegen
date: 17-06-2024
description:
id: DC-145
lang: de
---

# OCR-Verarbeitung von Belegen

OCR steht für Optical Character Recognition (optische Zeichenerkennung) und bezeichnet die automatische Texterkennung, bei der der Textinhalt eines gescannten Bildes oder einer PDF-Datei extrahiert und in Daten umgewandelt wird, die von einem Computer verarbeitet werden können.

Immer wenn Sie ein PDF-Dokument in Continia Document Capture erhalten, wird das Dokument automatisch mit OCR verarbeitet, sodass es zur Registrierung und weiteren Verarbeitung in Document Capture importiert werden kann. Für die OCR-Verarbeitung nutzt Document Capture einige der weltweit führenden Anbieter von OCR- und Dokumentenscan-Diensten. Die jeweilige OCR-Methode hängt von Ihrer Umgebung ab, wie unten beschrieben.

## Die zu Grunde liegende Technologie

Die Technologie, die zur OCR-Verarbeitung eingehender Dokumente in Document Capture verwendet wird, hängt davon ab, ob Sie mit einer Online- oder On-Premises-Installation arbeiten:

**Wenn Sie Microsoft Dynamics 365 Business Central _Online_** verwenden, ist Ihre Standard-OCR-Methode Continia Cloud OCR. Cloud OCR verwendet [Azure AI Dokument Intelligenz](https://learn.microsoft.com/de-de/azure/ai-services/document-intelligence/overview?view=doc-intel-4.0.0), ein vordefiniertes [Rechnungsmodell](https://learn.microsoft.com/de-de/azure/ai-services/document-intelligence/concept-invoice?view=doc-intel-4.0.0).

**Wenn Sie Microsoft Dynamics NAV/Business Central _On-Premises_** verwenden, können Sie entweder On-Premises OCR oder Continia Cloud OCR verwenden. Dieser besteht aus dem Document Capture-Dienst, der E-Mails herunterlädt und eingehende Dateien für die OCR-Verarbeitung überwacht, und der [ABBYY FineReader Engine](https://www.abbyy.com/ocr-sdk/), die die eigentliche OCR-Verarbeitung importierter Dokumente ausführt.

Weitere Informationen zu Continia Cloud OCR und der entsprechenden Einrichtung, finden Sie unter [Cloud OCR für NAV oder Business Central On-Premises konfigurieren](@DC-141).

Weitere Informationen zu On-Premises OCR und dem Continia OCR-Dienst und der entsprechenden Einrichtung finden Sie unter [On-Premises OCR konfigurieren](/Continia Document Capture/Development and Administration/On-Premises/Deployment/Configuring on-premises OCR/Configuring on-premises OCR.md) und [ABBYY und Document Capture-Dienst installieren](/Continia Document Capture/Development and Administration/On-Premises/Deployment/Configuring on-premises OCR/Installing ABBYY and Document Capture services.md). Die jeweiligen Mindestanforderungen finden Sie unter [OCR-Serveranforderungen](/continia-document-capture/development-and-administration/on-premises/deployment/minimum-requirements#ocr-server-anforderungen) und [Firewall-Anforderungen](/continia-document-capture/development-and-administration/on-premises/deployment/minimum-requirements#firewall-anforderungen).

## Der gesamte Prozess

Die OCR-Engine versucht in jedem PDF-Dokument, das in Document Capture importiert wird, alle Zeichen und deren Position zu erfassen. Anhand dieser OCR-Daten kann Document Capture dann alle Wörter und Textzeilen im Dokument ermitteln und so [nach Suchtexten und den entsprechenden Werten suchen](/continia-document-capture/business-functionality/documents-and-templates/working-with-paper-and-pdf-documents#capturing-fields). Um das gescannte PDF-Dokument mit allen identifizierten Suchtexten und Werten optimal in der Benutzeroberfläche anzeigen zu können, wandelt Document Capture es in eine TIFF-Datei um, da diese übersichtlicher und einfacher darzustellen ist. Sie können das Original-PDF-Dokument jedoch jederzeit über die Aktionsleiste abrufen, indem Sie **Dokument** > **PDF-Datei** auswählen.

Für jeden identifizierten Suchtext sucht Document Capture zunächst nach dem Wert rechts neben dem Suchtext. Wenn Document Capture keinen Wert finden kann oder den falschen Wert findet, haben Sie die Möglichkeit, den [richtigen Wert manuell zu identifizieren](/continia-document-capture/business-functionality/documents-and-templates/working-with-paper-and-pdf-documents#working-with-field-captions-and-values). Sobald ein Wert gefunden wurde (von Document Capture oder von Ihnen), speichert Document Capture die relative Position des Suchtextes und des Werts und verwendet diese dann, um die Werte dieses Suchtextes in allen zukünftigen Dokumenten zu identifizieren, die von demselben Kreditor gesendet werden. Die Position des Suchtextes selbst ist unwichtig; es wird nur die relative Position zwischen dem Suchtext und dem Wert verwendet.

## Informationen zum Thema

[Cloud OCR für NAV oder Business Central On-Premises konfigurieren](@DC-141)\
[On-Premises OCR konfigurieren](/Continia Document Capture/Development and Administration/On-Premises/Deployment/Configuring on-premises OCR/Configuring on-premises OCR.md)\
[ABBYY und Document Capture-Dienste installieren](/Continia Document Capture/Development and Administration/On-Premises/Deployment/Configuring on-premises OCR/Installing ABBYY and Document Capture services.md)\
[Mindestanforderungen für die Verwendung von Continia Document Capture On-Premises](/Continia Document Capture/Development and Administration/On-Premises/Deployment/Minimum Requirements.md)\
[Mit Papier- und PDF-Dokumenten arbeiten](/Continia Document Capture/Business functionality/Documents and templates/Working with paper and PDF documents.md)