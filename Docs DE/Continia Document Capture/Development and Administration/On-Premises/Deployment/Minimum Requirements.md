---
title: Mindestanforderungen für die Verwendung von Continia Document Capture (On-Premises)
date: 18-09-2025
description: Die Mindestanforderungen und Empfehlungen für die Verwendung von Document Capture in Business Central On-Premises.
id: DC-135
lang: de
---

# Mindestanforderungen für die Verwendung von Continia Document Capture (On-Premises)

Dieser Artikel beschreibt die Mindestanforderungen und Empfehlungen für die Verwendung von Document Capture in Microsoft Dynamics 365 Business Central On-Premises. Beachten Sie, dass sich diese Mindestanforderungen von denen für die Onlineversion von Business Central unterscheiden, die unter [Mindestanforderungen für die Verwendung von Continia Document Capture](/Continia Document Capture/Getting Started/Frequently Asked Questions/Minimum Requirements/Overview.md) zu finden sind.

> [!IMPORTANT]
> Da Document Capture in Business Central integriert ist, gelten die Mindestanforderungen für Business Central auch für Document Capture.

## Anforderungen für den Dynamics NAV-Webclient

Document Capture unterstützt nur den Dynamics NAV-Webclient von Microsoft Dynamics NAV 2016 oder höher.

## Anforderungen für lokale Scanner

Document Capture unterstützt das Scannen von Dokumenten mit einem lokalen Desktopscanner, der an einen Computer angeschlossen ist. Wenn Sie eine Classic- oder RTC-Version von NAV/Business Central verwenden, das heißt eine Version, die älter als Business Central 2019 Release Wave 2 (BC v15) ist, scannen Sie Dokumente mit dem eigentlichen NAV/Business Central-Client.

> [!IMPORTANT]
> Wenn Sie den RTC-Client verwenden, müssen Sie eine Version des Scannertreibers installieren, die der Microsoft Dynamics NAV-Version entspricht. Wenn Sie beispielsweise die 32-Bit-Version von Microsoft Dynamics NAV installiert haben, müssen Sie die 32-Bit-Version des Scannertreibers installieren.

Bei BC v15 und höher scannen Sie Dokumente mit dem Webclient, wofür die Installation einer separaten Continia-Anwendung sowie eines TWAIN-kompatiblen Scanners erforderlich ist. Wenn Sie den Business Central-Webclient verwenden, werden sowohl 32- als auch 64-Bit-Versionen des TWAIN-Scannertreibers unterstützt. Beachten Sie jedoch, dass 32-Bit-TWAIN-Scannertreiber nur in Document Capture 2021 R1 Service Pack 2 und spätere Versionen unterstützt werden. Weitere Informationen, wie Sie den Document Capture Scanner Service als eine 32-Bit-Anwendung ausführen können, finden Sie unter [How to alter the Document Capture Scanner Service to run as 32-bit application](https://continia.zendesk.com/hc/en-us/articles/360022114180-How-to-alter-the-Document-Capture-Scanner-Service-to-run-as-32-bit-application).

> [!NOTE]
> Wenn Sie mehrere Dokumente auf einmal scannen, müssen Sie jedes Dokument durch eine leere Seite trennen.

## OCR-Server-Anforderungen

Um Dokumente per OCR zu verarbeiten, benötigen Sie Zugriff auf die OCR-Engine, die entweder auf einem Continia-Server oder Ihrem eigenen lokalen Server gehostet werden kann. Wenn Sie über Ihren eigenen Server auf die Engine zugreifen möchten, müssen Sie sowohl den Document Capture OCR-Dienst als auch die Drittanbieteranwendung ABBYY FineReader auf diesem Server installieren. Darüber hinaus müssen die unten aufgeführten zusätzlichen Serveranforderungen erfüllt sein.

> [!NOTE]
> Die OCR-Verarbeitung von Dokumenten dauert 4–6 Sekunden pro Seite und ist sehr CPU-intensiv. Dies sollten Sie berücksichtigen, wenn die oben genannten OCR-Anwendungen auf einem vorhandenen Server installiert sind, da der OCR-Prozess andere Anwendungen verlangsamen kann. Diese mögliche Leistungsbeeinträchtigung hängt jedoch von der Anzahl der zu verarbeitenden Dokumente ab; meist gibt es überhaupt kein Problem.

Mindestanforderungen an die Hardware:

- Betriebssystem: Windows 2008 R2 Service Pack 1 oder höher
- CPU: 2 GHz; zwei oder mehr Kerne empfohlen
- Speicher: mindestens 8 GB, 16 GB oder mehr empfohlen
- Verfügbarer Speicherplatz: 2 GB
- Microsoft Internet Explorer 8.0 oder höher

Beachten Sie: Damit die ABBYY-Engine während der OCR-Erkennung die richtigen Schriftarten erkennt, müssen zuerst die in den verarbeiteten Dokumenten verwendeten Schriftarten installiert werden.

> [!NOTE]
> ABBYY und der Document Capture Service unterstützen keine Hochverfügbarkeit/Lastverteilung. Wenn Ihnen dies wichtig ist, sollten Sie stattdessen Continia Cloud OCR verwenden, da dieses auf hohe Verfügbarkeit ausgelegt ist.

## Internetanforderungen

Obwohl es möglich ist, Document Capture ohne Verbindung zum Internet zu verwenden, sind die folgenden Funktionen nicht verfügbar, wenn Sie Business Central v22 und höher offline verwenden:

- [Teilen und Zusammenführen](@DC-80)
- Dokumentendrehung
- Dokumentenvorschau im Belegjournal und auf der Dokumentenkarte\*

\* Abhängig von der Version von Document Capture, von der Sie eine Migration durchgeführt haben.

## E-Mail-Anforderungen

Sie importieren Dokumente (bzw. Belege) in Document Capture, indem Sie sie einfach per E-Mail an eine von Continia vorgegebene E-Mail-Adresse senden. Informationen zu den technischen Anforderungen und wichtige Hinweise finden Sie unter [Zusätzliche Richtlinien für die Verwendung von Continia Document Capture](@DC-224#technische-e-mail-anforderungen).

## PDF-Anforderungen

Wenn Sie PDF-Dokumente in Document Capture importieren, wird empfohlen, jedes Dokument als separate PDF-Datei zu senden. Es ist jedoch möglich, eine aus mehreren Dokumenten bestehende [PDF-Datei automatisch aufzuteilen](/Continia Document Capture/Business functionality/Documents and templates/Splitting and merging documents.md), basierend auf verschiedenen Kriterien, wie zum Beispiel Barcode oder Rechnungsnummer.

Die PDF-Datei muss der Version PDF 1.7 oder früher sowie dem PDF/A-Standard entsprechen. Beachten Sie, dass handschriftlicher Text nicht unterstützt und wahrscheinlich nicht gut erkannt wird.

Darüber hinaus gelten folgende Einschränkungen:

- Verschlüsselte/passwortgeschützte PDF-Dateien werden nicht unterstützt.
- PDF-Dateien mit elektronischen Signaturen werden möglicherweise erfolgreich verarbeitet, werden jedoch im Allgemeinen nicht unterstützt.
- PDF-Dateien im XFA-Format von Adobe (XML Forms Architecture) werden nicht unterstützt.
- Ab Document Capture Service 8.00 beträgt die maximale Seitenzahl, die für PDF-Dateien verarbeitet werden kann, 500.

Um Dateien mit den obigen Eigenschaften verarbeiten zu können, müssen Sie sie als neue PDF-Dateien erstellen. Dies ist beispielsweise mit der Option **Microsoft Print to PDF** möglich, die in Windows 10 kostenlos verfügbar ist. Wenn Sie neue PDFs erstellen, werden zusätzliche Funktionen entfernt und „einfache“ PDF-Dateien ohne interaktive Elemente erstellt.

## E-Mail-Server-Anforderungen

Wenn ein E-Mail-Server für On-Premises OCR konfiguriert und verwendet wird, muss der E-Mail-Server IMAP oder EWS unterstützen.

> [!NOTE]
> Die IMAP-Unterstützung für Exchange Online wird eingestellt. Weitere Informationen finden Sie unter [Erweiterung des OCR-Dienstes zur Unterstützung von Exchange Web Services (EWS) anstelle von IMAP](@DC-373).

## Continia Web Approval Portal

Weitere Informationen finden Sie unter [Anforderungen für die Verwendung des Continia Web Approval Portals On-Premises](@DC-454).

## Firewall-Anforderungen

Die Firewall muss ausgehenden Datenverkehr auf den Ports 80 und 443 (HTTPS) von dem Computer zulassen, der die Continia Document Capture-Aktivierung durchführt und die Document Capture-Konfigurations- und Dokumentdateien herunterlädt. Bei Classic NAV-Clients ist dies der tatsächliche Computer, den Sie verwenden. Bei NAV RTC ist es der Computer, auf dem die NAV-Dienstebene ausgeführt wird.

Um die Vorteile von Document Capture sowohl bei der Einrichtung als auch bei der täglichen Nutzung voll ausschöpfen zu können, müssen Sie Zugriff auf das Internet haben. Möglicherweise müssen Sie auch die folgenden Firewall-Einstellungen konfigurieren, um Document Capture zu aktivieren und die Sicherheit Ihres Setups zu gewährleisten.

> [!IMPORTANT]
> Wenn Sie wie die meisten Unternehmen den gesamten ausgehenden Datenverkehr Ihrer Clients und Server zulassen, müssen Sie keine Firewall-Einstellungen für den ausgehenden Datenverkehr konfigurieren. Wenn Ihre Richtlinien für ausgehenden Netzwerkverkehr jedoch in irgendeiner Weise eingeschränkt sind, müssen Sie Ihre Firewall so konfigurieren, dass der folgende Datenverkehr zugelassen wird.

> [!NOTE]
> Alle Continia-Ressourcen werden in einer Microsoft Azure-Umgebung gehostet. Dies bedeutet, dass die mit jedem der unten aufgeführten Domänennamen verknüpften IP-Adressen nach Ermessen von Microsoft geändert werden können. Wenn sich die IP-Adressen ändern, können Sie einen plötzlichen Stopp aller internetbezogenen Funktionen verhindern, indem Sie die URL-Filterung anstelle der IP-Filterung zulassen.

<br>

Von allen NAV/Business Central-Client- und Servercomputern müssen Sie ausgehenden Datenverkehr zu den folgenden Adressen auf den angegebenen Ports zulassen:

| Adresse                                                                                           | Port(s) | Richtung  |  Umgebung  |
| ------------------------------------------------------------------------------------------------- | -------------------------- | --------- | :--------: |
| auth.continiaonline.com                                           | 443                        | Ausgehend | Produktion |
| demoauth.continiaonline.com                                       | 443                        | Ausgehend |    Test    |
| license.continiaonline.com                                        | 443                        | Ausgehend | Produktion |
| demolicense.continiaonline.com                                    | 443                        | Ausgehend |    Test    |
| codownloads.blob.core.windows.net | 80, 443                    | Ausgehend |   Beides   |
| notification.continiaonline.com                                   | 443                        | Ausgehend | Produktion |
| demonotification.continiaonline.com                               | 443                        | Ausgehend |    Test    |
| eun-cdc.continiaonline.com                                        | 443                        | Ausgehend | Produktion |
| democontiniaonline.com                                                            | 443                        | Ausgehend |    Test    |
| ocsp.sectigo.com                                                  | 443                        | Ausgehend |   Beides   |

<br>

Wenn Sie On-Premises OCR verwenden, müssen Sie ausgehenden Datenverkehr vom ABBYY FineReader/Document Capture-Dienstcomputer zu den folgenden Adressen auf den angegebenen Ports zulassen:

| Adresse                                                                                       | Port(s)                                                                                                    | Richtung  | Umgebung |
| --------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | --------- | :------: |
| registration2.abbyy.com<a href="#footnote-1"><sup>1</sup></a> | 80, 443                                                                                                                       | Ausgehend |    N/A   |
| Ihr E-Mail-Server                                                                             | 143 (ungesichertes IMAP) oder 993 (sicheres IMAP)<a href="#footnote-2"><sup>2</sup></a> | Ausgehend |    N/A   |

<br>

<small style>
<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1">Der ABBYY-Aktivierungsserver befindet sich in Microsoft Azure (Niederlande).</li>
    <li id="footnote-2">Bitte beachten Sie hierzu unsere allgemeine Dokumentation. Sie finden diese im Continia Document Capture-Softwarepaket im Ordner <b>Documentation</b>.</li>
  </ol>
</div>
</small>

<br>

Wenn Sie Cloud OCR verwenden, müssen Sie den ausgehenden Datenverkehr von allen NAV/Business Central-Client- und Servercomputern zu den Adressen auf den angegebenen Ports zulassen:

| Adresse                                                                                              | Port(s) | Richtung  |  Umgebung  |
| ---------------------------------------------------------------------------------------------------- | -------------------------- | --------- | :--------: |
| cdc.continiaonline.com                                               | 443                        | Ausgehend | Produktion |
| democdc.continiaonline.com                                           | 443                        | Ausgehend |    Test    |
| cocloudocr.blob.core.windows.net     | 443                        | Ausgehend | Produktion |
| cocloudocrdemo.blob.core.windows.net | 443                        | Ausgehend |    Test    |

<br>

Wenn Sie das von Continia Software (www.continiaonline.com) gehostete Continia Web Approval Portal verwenden, müssen Sie eingehenden Datenverkehr von den folgenden Adressen und Ports zum NAV/Business Central Web Services-Server zulassen:

| Adresse                                                                                                                                            | Port(s)                                      | Richtung  |  Umgebung  |
| -------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- | --------- | :--------: |
| EUN IP: 23.102.56.117 (Irland, deckt Nordeuropa ab)             | SOAP-Dienst (Standard: 7047) | Eingehend | Produktion |
| USC IP: 13.89.38.96 (Iowa, deckt Central US ab)                 | SOAP-Dienst (Standard: 7047) | Eingehend | Produktion |
| AUE IP: 23.101.213.2 (New South Wales, deckt East Australia ab) | SOAP-Dienst (Standard: 7047) | Eingehend | Produktion |
| DEMO IP: 40.118.71.119                                                             | SOAP-Dienst (Standard: 7047) | Eingehend |    Test    |

<br>

Wenn Sie das Continia Delivery Network verwenden, müssen Sie den ausgehenden Datenverkehr von allen NAV/Business Central-Client- und Servercomputern zu den Adressen auf den angegebenen Ports zulassen:

| Adresse                                                                                                     | Port(s) | Richtung  |  Umgebung  |
| ----------------------------------------------------------------------------------------------------------- | -------------------------- | --------- | :--------: |
| cdnapi.continiaonline.com                                                   | 443                        | Ausgehend | Produktion |
| codeliverynetworkprod.blob.core.windows.net | 80, 443                    | Ausgehend |   Beides   |

<br/>

**Wenn Sie Continia Expense Management verwenden**, sollte auch der Datenverkehr zu den folgenden beiden URLs zugelassen werden:

- cem.continiaonline.com – Port 443 (Produktion)
- democem.continiaonline.com – Port 443 (Test)

> [!IMPORTANT]
> Bitte achten Sie bei alledem darauf, dass kein Proxyserver, keine Antivirensoftware oder ähnliches Ihren Internetzugang blockiert. Konsultieren Sie immer die entsprechende IT-Abteilung, um sicherzustellen, dass dies den Unternehmensregeln und -vorschriften entspricht.

## Add-In-Anforderungen

Die mindestens erforderliche Version des .NET Frameworks für Add-Ins ist Version 4.

Die Drag-and-Drop-Funktionalität kann von jedem mit einer eingeschränkten Lizenz oder einer Team Member-Lizenz verwendet werden. Beachten Sie, dass die Drag-and-Drop-Funktion nur funktioniert, wenn Sie eine eingeschränkte/Team Member-Lizenz von Document Capture Version 6.00 Service Pack 2 oder höher verwenden.

## Citrix- und Terminalserver-Anforderungen

Lokales Scannen ist nicht möglich, wenn Microsoft Dynamics NAV oder Business Central von einem Citrix- oder Terminalserver ausgeführt wird. Außerdem können bei der Verwendung von Citrix bestimmte Leistungsprobleme auftreten, wenn die Clientkomponenten von Document Capture nicht ordnungsgemäß installiert wurden, z. B. wenn die Clientkomponenten nicht in das Citrix-Image integriert wurden.

## Click Once-Anforderungen

Wenn Click Once zum Verteilen von Microsoft Dynamics NAV oder Business Central an Clients verwendet wird, müssen die Document Capture-Clientkomponenten im Click Once-Basisimage enthalten sein.

## Archivdateiserver

Document Capture speichert alle Dateien, die mit importierten Dokumenten in Zusammenhang stehen, in einem Archivverzeichnis. Dieses Verzeichnis sollte als Windows (NTFS) formatiert sein.

Für dieses Archivverzeichnis müssen Sie die unten aufgeführten Sicherheitsberechtigungen festlegen. Beachten Sie, dass dies für _alle Benutzer_ gilt, wenn Classic-Versionen von Microsoft Dynamics NAV verwendet werden, und für das Dienstkonto, wenn eine Dienstebene verwendet wird:

- Ändern
- Lesen und ausführen
- Ordnerinhalt auflisten
- Lesen
- Schreiben

Wenn Sie eine Classic-Version von Microsoft Dynamics NAV verwenden und das ausgewählte Verzeichnis ein im Netzwerk freigegebener Ordner ist, muss dieser Ordner für alle Benutzer zugänglich sein.

## Azure Blob Storage

Für neuere Versionen von Microsoft Dynamics NAV/Business Central (NAV 2013 oder später) unterstützt Document Capture die Archivierung von Dokumentdateien mit Azure Blob Storage. Weitere Informationen zu Azure Blob Storage, einschließlich Informationen zu Preisen und Konfiguration, finden Sie unter [Azure Blob Storage](https://azure.microsoft.com/de-de/services/storage/blobs/) (Microsoft-Artikel).

Damit Azure Blob Storage funktioniert, muss die Dynamics NAV/Business Central-Dienstebene für die Verwendung des TLS 1.2-Sicherheitsprotokolls konfiguriert sein. Weitere Informationen finden Sie unter [Azure Blob Storage einrichten](/Continia Document Capture/Development and Administration/Setting up Azure Blob storage.md).

> [!IMPORTANT]
> Es wird dringend empfohlen, dass Sie für Ihre Azure Blob Storage-Konten [vorläufiges Löschen für Blobs](https://docs.microsoft.com/de-de/azure/storage/blobs/soft-delete-blob-overview) aktivieren, da Sie so alle Dokumente oder Dateien wiederherstellen können, die versehentlich gelöscht oder überschrieben wurden.

> [!CAUTION]
> Es ist wichtig, dass Document Capture vollständigen Lese-/Schreib-/Löschzugriff auf den entsprechenden Blob-Container hat. So wird zum Beispiel die Konfiguration von Zugriffsrichtlinien mit zeitbasierter Aufbewahrung nicht unterstützt, ebenso wenig wie Unveränderlichkeit und die Aufbewahrung für juristische Zwecke.

Continia hat keine weiteren Mindestanforderungen für die Verwendung von Azure Blob Storage zum Speichern von Document Capture-Dateien. Wenn Sie Fragen oder Anforderungen hinsichtlich Azure haben, zum Beispiel in Bezug auf Einrichtung, Abonnementtypen und die allgemeine Architektur, wenden Sie sich bitte an Microsoft.

## Continia File Service

Der Continia File Service basiert auf .NET Core 8, das auf Windows Server Core 2012 oder höher unterstützt wird. Wenn Sie eine frühere Version von .NET Core haben, müssen Sie diese auf .NET Core 8 aktualisieren.

## Zusätzliche Richtlinien

Es gibt noch eine Reihe weiterer Anforderungen und Empfehlungen, die sich auf die Leistung von Document Capture und die Verwendung der App auswirken. Weitere Informationen finden Sie unter [Zusätzliche Richtlinien für die Verwendung von Continia Document Capture](@DC-224).

## Informationen zum Thema

[Mindestanforderungen für die Verwendung von Document Capture (Online)](/Continia Document Capture/Getting Started/Frequently Asked Questions/Minimum Requirements/Overview.md)  
[Zusätzliche Richtlinien für die Verwendung von Continia Document Capture](/Continia Document Capture/Getting Started/Frequently Asked Questions/Minimum Requirements/Additional guidelines.md)  
[Überblick über die Geschäftsfunktionen](/Continia Document Capture/Getting Started/Business Functionality.md)  
[Anforderungen für die Verwendung des Continia Web Approval Portals On-Premises](Web Approval Portal Requirements On-Premises.md)  
[Nicht unterstützte Standardfunktionen](@DC-134)  
[Business Central-Website](https://dynamics.microsoft.com/business-central/overview/)  
[Microsoft-Seite über Azure Blob Storage](https://azure.microsoft.com/en-us/services/storage/blobs/)  
[Azure Blob Storage einrichten](/Continia Document Capture/Development and Administration/Setting up Azure Blob storage.md)

<style>
  .content table tr td:nth-child(1) {
    width: 500px;
  }
  .content table tr td:nth-child(2) {
    width: 230px;
  }  
</style>