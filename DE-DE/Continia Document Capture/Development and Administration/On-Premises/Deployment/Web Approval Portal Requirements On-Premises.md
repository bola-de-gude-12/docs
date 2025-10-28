---
title: Anforderungen für die Verwendung des Continia Web Approval Portals On-Premises
date: 24-07-2025
description: Eine Liste der Anforderungen für die Verwendung des Web Approval Portals mit Business Central On-Premises.
id: DC-454
lang: de
---

# Anforderungen für die Verwendung des Continia Web Approval Portals On-Premises

Dieser Artikel beschreibt die Anforderungen für die Verwendung des Web Approval Portals mit Microsoft Dynamics 365 Business Central On-Premises. Die Online-Anforderungen finden Sie unter [Mindestanforderungen für die Verwendung von Document Capture](@DC-453#continia-web-approval-portal).

Dokumente können entweder über den Business Central-Webclient oder das Continia Web Approval Portal genehmigt werden. Das Web Approval Portal basiert auf der standardmäßigen Genehmigungsfunktionalität von Business Central. Es handelt sich jedoch um einen separaten Service, auf den lizenzierte Benutzer von allen unterstützten Webbrowsern aus zugreifen können. [Die Webbrowser, die für Continia Document Capture unterstützt werden](/continia-document-capture/getting-started/frequently-asked-questions/minimum-requirements/additional-guidelines#browsers), werden auch für das Web Approval Portal unterstützt.

Das Web Approval Portal wird bis auf wenige Ausnahmen auf Mobilgeräten unterstützt. Eine besondere Ausnahme sind formatierte XML-Dateien, die im Portal im mobilen Modus nicht angezeigt werden. Wenn Sie eine XML-Datei auf einem mobilen Gerät anzeigen möchten, wechseln Sie im Browser auf Ihrem Mobilgerät in den Desktop-Modus.

## Anforderungen für alle Portalinstallationen, unabhängig vom Hostingtyp

Das Web Approval Portal kann entweder von Continia (continiaonline.com) oder auf einem lokalen Server gehostet werden. Der Zugriff erfolgt in beiden Fällen über einen Webbrowser; der Unterschied besteht also nur beim Hosting. Die Informationen in diesem Abschnitt gelten für beide Hostingtypen.

Um das Web Approval Portal On-Premises zu verwenden, müssen Sie Microsoft Dynamics NAV 2009 R2 oder höher ausführen. Bestimmte Microsoft Dynamics NAV/Business Central-Webdienste – SOAP und OData – müssen ebenfalls aktiviert werden, da das Web Approval Portal auf diese Weise mit Dynamics NAV/Business Central kommuniziert.

> [!IMPORTANT]
> Da das Web Approval Portal Webdienste erfordert, funktioniert es nur in Verbindung mit der Runtimeversion von Dynamics NAV 2009 R2 oder höher. Die Runtime-Version ermöglicht Ihnen die Nutzung des Web Approval Portal mit NAV-Versionen älter als 2009 R2.

> [!NOTE]
> Sicherheitsfilter werden im Web Approval Portal nicht unterstützt. Um festzulegen, welcher Inhalt für Benutzer im Portal sichtbar und zugänglich ist, verwenden Sie stattdessen Berechtigungen für Konten und Dimensionen. Diese können entweder für [individuelle Benutzer](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#konten--und-dimensionsberechtigungen-konfigurieren) oder für [Benutzergruppen](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/approval-user-groups#so-konfigurieren-sie-konten--und-dimensionsberechtigungen-fur-eine-gruppe) konfiguriert werden.

Darüber hinaus müssen Sie, abhängig von Ihrer Version von NAV/Business Central, die unten aufgeführten Anforderungen erfüllen. Beachten Sie, dass alle Benutzer gemäß den Lizenzbedingungen von Microsoft lizenziert sein müssen, die von Version zu Version unterschiedlich sein können.

> [!IMPORTANT]
> Konsultieren Sie immer die Microsoft-Lizenzbedingungen, um sich mit den rechtlichen Anforderungen vertraut zu machen, unabhängig davon, wie diese in Continia Docs oder in einer anderen Continia-Dokumentation interpretiert werden. Dabei möchten wir insbesondere auf den Abschnitt **Team Members** im Microsoft Dynamics 365 Business Central Licensing Guide hinweisen, der auf der [Business Central](https://dynamics.microsoft.com/business-central/overview/)-Website zum Download verfügbar ist.

Continias aktuelle Interpretation der Microsoft-Bedingungen lautet wie folgt:

| NAV/BC-Version                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Microsoft Dynamics 365 Business Central     | Jeder Benutzer von Dynamic 365 Business Central muss über eine Named-User-Lizenz verfügen. Eine „Named-User-License“ ist eine separate Abonnementlizenz (Subscription License, SL), die an einen bestimmten Benutzer gebunden ist und nicht mit anderen geteilt werden kann, im Gegensatz zu [Concurrent-User-Lizenzen](https://de.wikipedia.org/wiki/Concurrent_user).<br /><br />Für Genehmigungsbenutzer, die nur Dokumente genehmigen und Einkaufszeilen ändern, sind Team Member-Lizenzen ausreichend, vorbehaltlich der Microsoft-Lizenzbedingungen. In allen anderen Fällen unterstützt Continia nur Benutzer mit Essentials- oder Premium-Lizenzen.<br /><br />Informationen zu Team Member-Lizenzen und wie sich Add-Ons auf deren Nutzung auswirken können, finden Sie im Microsoft Dynamics 365 Business Central Licensing Guide. Sie können dieses Handbuch auf der [Business Central](https://dynamics.microsoft.com/business-central/overview/)-Website herunterladen. |
| Microsoft Dynamics NAV 2013 R2 bis NAV 2018 | Für Microsoft Dynamics NAV 2013 R2 bis NAV 2018 muss jeder Benutzer entweder als Vollbenutzer oder als eingeschränkter Benutzer in der Benutzertabelle vorhanden sein. Wenn ein Benutzer auf die Website zugreift, ist die Benutzersitzung für zwei Stunden (Vollbenutzer) und 15 Minuten (eingeschränkte Benutzer) aktiv.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Microsoft Dynamics NAV 2013                 | Für den Zugriff auf Microsoft Dynamics NAV 2013 ist eine Concurrent-User-Lizenz erforderlich. Datenanforderungen sind stark eingeschränkt und trennen die NAV-Sitzung unmittelbar nach dem Laden der Webseite. In den meisten Fällen führt dies effektiv zu nur einem gleichzeitigen NAV-Benutzer, auch wenn mehrere Webbenutzer gleichzeitig auf die Site zugreifen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Microsoft Dynamics NAV 2009 R2              | Für jeden benannten Webbenutzer wird ein Light User benötigt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |

> [!NOTE]
> Benutzer des Web Approval Portals können auch automatisch auf Business Central zugreifen, sobald ihnen eine Team Member-Lizenz zugewiesen wurde. Das Web Approval Portal ist auf der Standardfunktionalität von Business Central aufgebaut, wodurch sich der Zugriff auf Business Central ergibt.

**Unterstützte Authentifizierungsmethoden**

- Windows-Authentifizierung
- Für Microsoft Dynamics NAV 2009 R2: nur Windows-Authentifizierung
- Für Microsoft Dynamics NAV 2013 und höher: sowohl Windows- als auch NAVUserPassword-Authentifizierung
- For Microsoft Dynamics NAV 2018 und später: Office 365-Authentifizierung

Ab Version 1.16.0 kann das Web Approval Portal gleichzeitig eine Verbindung zu mehreren NAV- und/oder Business Central-Datenbanken herstellen, sodass sich Benutzer aus verschiedenen Datenbanken zur gleichen Zeit anmelden können.

Keine der früheren Versionen des Web Approval Portals unterstützen jedoch die gleichzeitige Anmeldung von Benutzern aus verschiedenen Datenbanken. Wenn Ihr Unternehmen über mehr als eine Datenbank in Business Central verfügt und Benutzer aus einer dieser Datenbanken in das Web Approval Portal exportiert, können sich nur die neu exportierten Benutzer beim Web Approval Portal anmelden; alle bestehenden Benutzer, die zuvor aus einer anderen Datenbank exportiert wurden, werden aus dem Web Approval Portal gelöscht und können sich nicht anmelden.

**Benutzerkündigung**

- Um den Zugriff auf das Web Approval Portal für einen bestimmten Datenbankbenutzer zu verhindern, muss der Webservice-Schlüssel des Benutzers in NAV erneuert werden.
- Um den Zugriff auf das Web Approval Portal für einen Microsoft 365-Benutzer zu verhindern, muss der Benutzer in Microsoft Entra (vormals Azure Active Directory) deaktiviert werden.

## Anforderungen für lokal gehostete Portalinstallationen

Im Gegensatz zum obigen Abschnitt, der für beide Hosting-Typen (continiaonline.com oder lokaler Server) gilt, gelten die folgenden Anforderungen nur für lokal gehostete Web Approval Portal-Installationen.

Sie können die lokal gehostete Version des Web-Genehmigungsportals nur verwenden, wenn Sie Business Central On-Premises verwenden. Auf dem Server, auf dem das Web Approval Portal installiert ist, müssen die folgenden Komponenten installiert sein, um die Mindestanforderungen zu erfüllen:

- Windows Server 2008 R2 Service Pack 1 oder höher
- Internet Information Services 7.5 oder höher
- Microsoft .NET Framework 4.7.2
- Die neuesten Windows Service Packs und Hotfixes

In der folgenden Tabelle können Sie sehen, welche Versionen von NAV/Business Central mit jeder der beiden Versionen des Web Approval Portals (WAP) kompatibel sind:

| Version                   | Älter als NAV 2009 R2-Runtime<a href="#footnote-1"><sup>1</sup></a> | NAV 2009 R2 Runtime | Business Central Cloud | Business Central On-Premises |
| ------------------------- | ------------------------------------------------------------------- | ------------------- | ---------------------- | ---------------------------- |
| WAP gehostet von Continia |                                                                     | {{checkmark}}       | {{checkmark}}          | {{checkmark}}                |
| Lokal gehostetes WAP      |                                                                     | {{checkmark}}       |                        | {{checkmark}}                |

<br>

<small style><div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1">Beachten Sie, dass die Runtime-Version es Ihnen ermöglicht, das Web Approval Portal mit NAV-Versionen älter als 2009 R2 zu verwenden.</li>

  </ol>
</div>
</small>

## Informationen zum Thema

[Mindestanforderungen für die Verwendung von Continia Document Capture On-Premises](Minimum Requirements.md)  
[Business Central-Website](https://dynamics.microsoft.com/business-central/overview/)