---
title: Das Web Approval Portal für Business Central Online aktivieren
date: 7-1-2022
description: null
id: EM-52
lang: de
---

# Das Web Approval Portal für Business Central Online aktivieren

Wenn Sie über eine _Online_-Installation von Microsoft Dynamics 365 Business Central verfügen, gehen Sie folgendermaßen vor, um das Continia Web Approval Portal einzurichten:

1. Registrieren Sie das Web Approval Portal als Anwendung in Azure Active Directory (Azure AD). Wenn Sie hierbei Unterstützung benötigen, finden Sie Informationen in [dieser Anleitung](https://continia.zendesk.com/hc/da/articles/360005985960-How-to-setup-Dynamics-365-Business-Central-with-Continia-Web-Approval) (nur für Continia-Partner verfügbar). Notieren Sie sich unbedingt die ID und den geheimen Clientschlüssel, da Sie diese Informationen später benötigen.
2. Wählen Sie in Business Central das Symbol {{search}}, geben Sie **Expense Management Einrichtung** ein, und wählen Sie dann den zugehörigen Link.
3. Wählen Sie in der Aktionsleiste **Einrichtung** > **Web Genehmigung** aus, um die Seite **Expense Management Einrichtung / Web-Genehmigung** zu öffnen.
4. Aktivieren Sie im Inforegister **Allgemein** das Genehmigungsportal, indem Sie den Schalter **Continia Web Approval Portal verwenden** umschalten.
5. Wählen Sie unter **Begrüßungs-E-Mails** aus, ob Begrüßungs-E-Mails automatisch an Benutzer des Web Approval Portals gesendet werden sollen oder ob dies manuell erfolgen soll.
6. Geben Sie unter **Azure ID-Integration** die Azure AD-Anwendungs-ID und den Schlüssel (geheimer Clientschlüssel) ein, die Sie in Schritt 1 oben erstellt und gespeichert haben. Dadurch können sich Benutzer des Web Approval Portals mit ihren Office 365-Anmeldeinformationen anmelden.
7. Wählen Sie in der Aktionsleiste **Benutzer** > **Continia Benutzereinrichtung** aus und folgen Sie dann [dieser Anleitung](Configuring users for the Web Approval Portal.md), um Benutzer für das Web Approval Portal einzurichten.

## Informationen zum Thema

[Anforderungen für die Verwendung des Continia Web Approval Portals Online](/continia-expense-management/getting-started/troubleshooting-and-faqs/minimum-requirements#continia-web-approval-portal)\
[Continia Web-Genehmigung mit Dynamics 365 Business Central einrichten](https://continia.zendesk.com/hc/da/articles/360005985960-How-to-setup-Dynamics-365-Business-Central-with-Continia-Web-Approval) (nur für Continia Partner verfügbar)\
[Benutzer für das Web Approval Portal konfigurieren](@EM-53)
