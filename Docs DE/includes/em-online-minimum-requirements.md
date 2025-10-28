Es besteht ein erheblicher Unterschied darin, ob Sie Expense Management in der On-Premises-Version von Microsoft Dynamics 365 Business Central oder online in der Cloud-Version nutzen. In diesem Artikel werden die Mindestanforderungen und Aspekte beschrieben, die bei der Nutzung von Expense Management in Business Central _Online_ zu beachten sind. Die On-Premises-Anforderungen finden Sie [hier](/Continia Expense Management/Development and Administration/On-premises/Deployment/Minimum Requirements.md).

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
- Business Central (Webclient und mobile App) – wird von Genehmigern und Administratoren verwendet

**Die Expense App** ist eine separate mobile App, die auf Mobilgeräten vollständig unterstützt wird. Weitere Informationen finden Sie weiter unten unter [Continia Expense App](#continia-expense-app).

**Das Expense Portal** ist technisch gesehen auch über Mobilgeräte zugänglich; dies wird jedoch nicht empfohlen, da es _nicht_ für Mobilgeräte optimiert ist. Wenn Sie mobile Geräte zum Einreichen von Spesen verwenden, empfehlen wir Ihnen daher stattdessen die Verwendung der separaten mobilen Expense App.

> [!TIP]
> Verwenden Sie die separate mobile Expense App anstelle des Expense Portals, um Spesen auf Mobilgeräten einzureichen.

**Das Web Approval Portal** wird auf Mobilgeräten vollständig unterstützt. Das Web Approval Portal ist ein separater Continia-Client, der außerhalb von Business Central verwendet wird. Weitere Informationen finden Sie weiter unten unter [Continia Web Approval Portal](#continia-web-approval-portal).

**Business Central** ist grundsätzlich für die mobile Nutzung optimiert und auf Mobilgeräten leicht zugänglich; das Erscheinungsbild unterscheidet sich jedoch von der Verwendung auf einem Computer. Obwohl die meisten Funktionen zur Spesenverwaltung in Business Central auf Mobilgeräten funktionieren, wird dies nicht offiziell unterstützt. Das bedeutet, dass in der mobilen Version von Business Central nicht alle Funktionen verfügbar sind.

## Continia Expense App

Die Expense App ist mit jedem Android- oder iOS-Gerät kompatibel, das die folgenden Softwareanforderungen erfüllt:

**Android:**  
Unterstützte Versionen: 9.0 oder spätere Versionen.  
Klicken Sie [hier](https://www.continia.com/continia-expense-app/), um die App auf Ihrem Gerät zu installieren.

**iPhone:**  
Unterstützte Versionen: iOS 14 oder spätere Versionen.  
Klicken Sie [hier](https://www.continia.com/continia-expense-app/), um die App auf Ihrem Gerät zu installieren.

## Continia Web Approval Portal

Dokumente können entweder über den Business Central-Webclient oder das Continia Web Approval Portal genehmigt werden. Das Web Approval Portal basiert auf der standardmäßigen Genehmigungsfunktionalität von Business Central. Es handelt sich jedoch um einen separaten Service, auf den lizenzierte Benutzer von allen unterstützten Webbrowsern aus zugreifen können. [Die Webbrowser, die für Continia Expense Management unterstützt werden](/continia-expense-management/getting-started/troubleshooting-and-faqs/minimum-requirements#browser), werden auch für das Web Approval Portal unterstützt.

> [!NOTE]
> Sicherheitsfilter werden derzeit im Web Approval Portal nicht unterstützt.

Das Web Approval Portal kann entweder von Continia (continiaonline.com) oder auf einem lokalen Server gehostet werden. Der Zugriff erfolgt in beiden Fällen über einen Webbrowser; der Unterschied besteht also nur beim Hosting. Sie können die auf einem lokalen Server gehostete Version des Web Approval Portals nicht in Kombination mit Business Central Online verwenden; nur die von Continia gehostete Version des Web Approval Portals kann in Verbindung mit Business Central Online verwendet werden.

Um auf das Web Approval Portal zugreifen zu können, müssen Sie ein authentifizierter Business Central-Benutzer sein und über eine Lizenz für benannte Benutzer für Business Central verfügen.  Eine „Named-User-License“ ist eine separate Abonnementlizenz (Subscription License, SL), die an einen bestimmten Benutzer gebunden ist und nicht mit anderen geteilt werden kann, im Gegensatz zu [_Concurrent-User-Lizenzen_](https://de.wikipedia.org/wiki/Concurrent_user). Benutzer-SLs sind der primäre Lizenztyp für Business Central.

Nur Benutzer mit einer Voll-/Essential-/Premium-Lizenz können Zuordnungen in Dokumenten ändern.

Für Genehmigungsbenutzer, die nur Dokumente genehmigen, sind Team Member-Lizenzen ausreichend, vorbehaltlich der Microsoft-Lizenzbedingungen (siehe unten). In allen anderen Fällen unterstützt Continia nur Benutzer mit Essentials- oder Premium-Lizenzen. Informationen zu Team Member-Lizenzen und wie sich Add-Ons auf deren Nutzung auswirken können, finden Sie im Microsoft Dynamics 365 Business Central Licensing Guide. Sie können dieses Handbuch auf der [Business Central](https://dynamics.microsoft.com/business-central/overview/)-Website herunterladen.

> [!IMPORTANT]
> Bitte konsultieren Sie immer die Microsoft-Lizenzbedingungen, um sich mit den rechtlichen Anforderungen vertraut zu machen, unabhängig davon, wie diese in Continia Docs oder in einer anderen Continia-Dokumentation interpretiert werden. Dabei möchten wir insbesondere auf den Abschnitt **Team Members** im Microsoft Dynamics 365 Business Central Licensing Guide hinweisen, der auf der [Business Central](https://dynamics.microsoft.com/business-central/overview/)-Website zum Download verfügbar ist.

> [!IMPORTANT]
> Ab Version 1.16.0 kann das Web Approval Portal gleichzeitig eine Verbindung zu mehreren NAV- und/oder Business Central-Datenbanken herstellen, sodass sich Benutzer aus verschiedenen Datenbanken zur gleichen Zeit anmelden können.
>
> Keine der früheren Versionen des Web Approval Portals unterstützen jedoch die gleichzeitige Anmeldung von Benutzern aus verschiedenen Datenbanken. Wenn Ihr Unternehmen über mehr als eine Datenbank in Business Central verfügt und Benutzer aus einer dieser Datenbanken in das Web Approval Portal exportiert, können sich nur die neu exportierten Benutzer beim Web Approval Portal anmelden; alle bestehenden Benutzer, die zuvor aus einer anderen Datenbank exportiert wurden, werden aus dem Web Approval Portal gelöscht und können sich nicht anmelden.

## Informationen zum Thema

[Überblick über Geschäftsfunktionen](/Continia Expense Management/Getting Started/Business Functionality.md)  
[Business Central-Website](https://dynamics.microsoft.com/business-central/overview/)