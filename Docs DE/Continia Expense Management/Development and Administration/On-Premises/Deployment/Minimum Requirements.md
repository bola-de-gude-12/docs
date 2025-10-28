---
title: Mindestanforderungen für die Verwendung von Continia Expense Management On-Premises
date: 27-09-2024
description: null
id: EM-51
lang: de
---

# Mindestanforderungen für die Verwendung von Continia Expense Management On-Premises

Dieser Artikel beschreibt die Mindestanforderungen und Empfehlungen für die Verwendung von Expense Management in Microsoft Dynamics 365 Business Central _On-Premises_. Beachten Sie, dass sich diese Mindestanforderungen von denen für die _Online_-Version von Business Central unterscheiden, die Sie [hier](@EM-83) finden.

> [!IMPORTANT]
> Da Expense Management in Business Central integriert ist, gelten die Mindestanforderungen für Business Central auch für Expense Management.

## Browser

Wir empfehlen einen der folgenden Webbrowser mit den neuesten Updates:

- Google Chrome
- Mozilla Firefox
- Apple Safari
- Microsoft Edge

Die Verwendung von Internet Explorer kann zu Fehlern und Problemen bei der Darstellung führen. Falls Internet Explorer die einzige Option ist, muss dieser auf die neueste Version aktualisiert werden.

## Bildschirmauflösung

Die Bildschirmauflösung muss mindestens 1440 × 900 betragen, da bei geringeren Auflösungen die Dokumentenvorschau von Expense Management nicht optimal funktioniert. Wir empfehlen eine Bildschirmauflösung von 1680 × 1050 oder höher.

Beachten Sie, dass das Vergrößern in Ihrem Browser oder Ändern der Skalierungs- und Layouteinstellungen Ihres Monitors nicht unterstützt wird und daher die Vorschau beeinträchtigen kann.

## Mobilgeräte

Expense Management wird von [verschiedenen Benutzern unterschiedlich verwendet](/continia-expense-management/getting-started/overview#get-familiar-with-expense-management) und bietet verschiedene Anwendungen, auf die entweder über Webbrowser oder über mobile Apps zugegriffen werden kann:

- Die Continia Expense App (mobile App) – wird von Expense-Benutzern verwendet
- Das Continia Expense Portal (Webportal) – wird von Expense-Benutzern verwendet
- Das Continia Web Approval Portal (Webportal) – wird von Genehmigern verwendet
- Business Central (Web-Client und mobile App) – wird von Genehmigern und Buchhaltern verwendet (siehe Informationen zu Einschränkungen bei der Verwendung der mobilen App weiter unten unter **Business Central**)

**Die Expense App** ist eine separate mobile App, die auf Mobilgeräten vollständig unterstützt wird. Weitere Informationen finden Sie weiter unten unter [Continia Expense App](/continia-expense-management/development-and-administration/on-premises/deployment/minimum-requirements#continia-expense-app).

**Das Expense Portal** ist technisch gesehen auch über Mobilgeräte zugänglich; dies wird jedoch nicht empfohlen, da es _nicht_ für Mobilgeräte optimiert ist. Wenn Sie mobile Geräte zum Einreichen von Spesen verwenden, empfehlen wir Ihnen daher stattdessen die Verwendung der separaten mobilen Expense App.

> [!TIP]
> Verwenden Sie die separate mobile Expense App anstelle des Expense Portals, um Spesen auf Mobilgeräten einzureichen.

**Das Web Approval Portal** wird auf Mobilgeräten vollständig unterstützt. Das Web Approval Portal ist ein separater Continia-Client, der außerhalb von Business Central verwendet wird. Weitere Informationen finden Sie [unten](/continia-expense-management/development-and-administration/on-premises/deployment/minimum-requirements#continia-web-approval-portal).

**Business Central** ist grundsätzlich für die mobile Nutzung optimiert und auf Mobilgeräten leicht zugänglich; das Erscheinungsbild unterscheidet sich jedoch von der Verwendung auf einem Computer. Obwohl die meisten Funktionen zur Spesenverwaltung in Business Central auf Mobilgeräten funktionieren, wird dies nicht offiziell unterstützt. Das bedeutet, dass in der mobilen Version von Business Central nicht alle Funktionen verfügbar sind.

## Anforderungen für den Dynamics NAV-Webclient

Expense Management unterstützt nur den Dynamics NAV-Webclient von Microsoft Dynamics NAV 2016 oder höher.

## Continia Expense App

Die Expense App ist mit jedem Android- oder iOS-Gerät kompatibel, das die folgenden Softwareanforderungen erfüllt:

**Android:**\
Unterstützte Versionen: 9.0 oder spätere Versionen.\
Klicken Sie [hier](https://www.continia.com/continia-expense-app/), um die App auf Ihrem Gerät zu installieren.

**iPhone:**\
Unterstützte Versionen: iOS 14 oder spätere Versionen.\
Klicken Sie [hier](https://www.continia.com/continia-expense-app/), um die App auf Ihrem Gerät zu installieren.

## Continia Web Approval Portal

Die Anforderungen für die Verwendung des Continia Web Approval Portals mit Business Central On-Premises finden Sie [hier](Web Approval Portal Requirements On-Premises.md).

## Firewall-Anforderungen

Die Firewall muss ausgehenden Datenverkehr auf den Ports 80 und 443 (HTTPS) von dem Computer zulassen, der die Continia Expense Management-Aktivierung durchführt und die Expense Management-Konfigurations- und Dokumentdateien herunterlädt. Bei Classic NAV-Clients ist dies der tatsächliche Computer, den Sie verwenden. Bei NAV RTC ist es der Computer, auf dem die NAV-Dienstebene ausgeführt wird.

Um die Vorteile von Expense Management sowohl bei der Einrichtung als auch bei der täglichen Nutzung voll ausschöpfen zu können, müssen Sie Zugriff auf das Internet haben. Möglicherweise müssen Sie auch die folgenden Firewall-Einstellungen konfigurieren, um Expense Management zu aktivieren und die Sicherheit Ihres Setups zu gewährleisten. Beachten Sie jedoch, dass dies häufig nicht erforderlich ist.

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
| cem.continiaonline.com                                            | 443                        | Ausgehend | Produktion |
| democem.continiaonline.com                                        | 443                        | Ausgehend |    Test    |
| notification.continiaonline.com                                   | 443                        | Ausgehend | Produktion |
| demonotification.continiaonline.com                               | 443                        | Ausgehend |    Test    |

<br>

Um E-Mails an Expense-Benutzer und Genehmiger senden zu können, müssen Sie ausgehenden Datenverkehr zum folgenden Server auf dem angegebenen Port zulassen:

| Adresse           | Port(s)                                                        | Richtung  | Umgebung |
| ----------------- | --------------------------------------------------------------------------------- | --------- | :------: |
| Ihr E-Mail-Server | 25 (ungesichertes SMTP) als Standard, Andere sind auch möglich | Ausgehend |    N/A   |

<br>

Wenn Sie das von Continia Software (www.continiaonline.com) gehostete Continia Web Approval Portal verwenden, müssen Sie eingehenden Datenverkehr von den folgenden Adressen und Ports zum NAV/Business Central Web Services-Server zulassen:

| Adresse                                                                                                                                            | Port(s)                                      | Richtung  |  Umgebung  |
| -------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- | --------- | :--------: |
| EUN IP: 23.102.56.117 (Irland, deckt Nordeuropa ab)             | SOAP-Dienst (Standard: 7047) | Eingehend | Produktion |
| USC IP: 13.89.38.96 (Iowa, deckt Central US ab)                 | SOAP-Dienst (Standard: 7047) | Eingehend | Produktion |
| AUE IP: 23.101.213.2 (New South Wales, deckt East Australia ab) | SOAP-Dienst (Standard: 7047) | Eingehend | Produktion |
| DEMO IP: 40.118.71.119                                                             | SOAP-Dienst (Standard: 7047) | Eingehend |    Test    |

<br/>

> [!IMPORTANT]
> Bitte achten Sie bei alledem darauf, dass kein Proxyserver, keine Antivirensoftware oder ähnliches Ihren Internetzugang blockiert. Konsultieren Sie immer die entsprechende IT-Abteilung, um sicherzustellen, dass dies den Unternehmensregeln und -vorschriften entspricht.

## Add-In-Anforderungen

Die mindestens erforderliche Version des .NET Frameworks für Add-Ins ist Version 4.

Die Drag-and-Drop-Funktionalität kann von jedem mit einer eingeschränkten Lizenz oder einer Team Member-Lizenz verwendet werden. Beachten Sie, dass die Drag-and-Drop-Funktion nur funktioniert, wenn Sie eine eingeschränkte/Team Member-Lizenz von Expense Management Version 6.00 Service Pack 2 oder höher verwenden.

## Click Once-Anforderungen

Wenn Click Once zum Verteilen von Microsoft Dynamics NAV oder Business Central an Clients verwendet wird, müssen die Expense Management-Clientkomponenten im Click Once-Basisimage enthalten sein.

## Archivdateiserver

Expense Management speichert alle Dateien, die mit importierten Dokumenten in Zusammenhang stehen, in einem Archivverzeichnis. Dieses Verzeichnis sollte als Windows (NTFS) formatiert sein.

Für dieses Archivverzeichnis müssen Sie die unten aufgeführten Sicherheitsberechtigungen festlegen. Beachten Sie, dass dies für _alle Benutzer_ gilt, wenn Classic-Versionen von Microsoft Dynamics NAV verwendet werden, und für das _Dienstkonto_, wenn eine Dienstebene verwendet wird:

- Ändern
- Lesen und ausführen
- Ordnerinhalt auflisten
- Lesen
- Schreiben

Wenn Sie eine Classic-Version von Microsoft Dynamics NAV verwenden und das ausgewählte Verzeichnis ein im Netzwerk freigegebener Ordner ist, muss dieser Ordner für alle Benutzer zugänglich sein.

> [!NOTE]
> Damit Azure Blob Storage funktioniert, muss die Dynamics NAV/Business Central-Dienstebene für die Verwendung des TLS 1.2-Sicherheitsprotokolls konfiguriert sein.

## Informationen zum Thema

[Mindestanforderungen für die Verwendung von Continia Expense Management (Online)](@EM-83)\
[Überblick über die Geschäftsfunktionen](/Continia Expense Management/Getting Started/Business Functionality.md)\
[Anforderungen für die Verwendung des Continia Web Approval Portals On-Premises](Web Approval Portal Requirements On-Premises.md)\
[Business Central-Website](https://dynamics.microsoft.com/de-de/business-central/overview/)

<style>
  .content table tr td:nth-child(1) {
    width: 500px;
  }
  .content table tr td:nth-child(2) {
    width: 230px;
  }  
</style>
