---
title: Das Web Approval Portal für Business Central Online aktivieren
date: 04-07-2025
description: So aktivieren Sie das Web Approval Portal in Online-Installationen von Business Central.
id: DC-480
lang: de
---

# Das Web Approval Portal für Business Central Online aktivieren

Wenn Sie über eine Online-Installation von Microsoft Dynamics 365 Business Central verfügen, gehen Sie folgendermaßen vor, um das Continia Web Approval Portal einzurichten:

1. Registrieren Sie das Web Approval Portal als Anwendung in Microsoft Entra ID (vormals Azure Active Directory). Weitere Informationen finden Sie unter [How to setup Continia Web Approval for BC Cloud](https://continia.zendesk.com/hc/en-us/articles/13386916791698) (nur für Continia-Partner verfügbar). Notieren Sie sich unbedingt die ID und den geheimen Clientschlüssel, da Sie diese Informationen später benötigen.
2. Suchen Sie {{search}} nach **Document Capture Einrichtung** und wählen Sie dann den entsprechenden Link aus.
3. Klicken Sie in der Aktionsleiste auf **Einrichtung** > **Web-Genehmigungen**, um die Seite **Document Capture Einrichtung / Continia Web Genehmigungen** zu öffnen.
4. Aktivieren Sie im Inforegister **Allgemein** den Schalter **Continia Web Approval Portal verwenden**.
5. Wählen Sie unter **Begrüßungs-E-Mails** aus, ob Begrüßungs-E-Mails automatisch an Benutzer des Web Approval Portals gesendet werden sollen oder ob dies manuell erfolgen soll.
6. Geben Sie unter **Azure ID-Integration** die Entra ID-Anwendungs-ID und den Schlüssel (geheimer Clientschlüssel) ein, die Sie in Schritt 1 oben erstellt und gespeichert haben. Dadurch können sich Benutzer des Web Approval Portals mit ihren Office 365-Anmeldeinformationen anmelden.
7. Klicken Sie in der Aktionsleiste auf **Benutzer** > **Continia Benutzereinrichtung** und folgen Sie der Anleitung unter [Benutzer für das Web Approval Portal konfigurieren](@DC-129), um Benutzer für das Web Approval Portal einzurichten.

## Informationen zum Thema

[Anforderungen für die Verwendung des Continia Web Approval Portals Online](/continia-document-capture/getting-started/frequently-asked-questions/minimum-requirements/overview#continia-web-approval-portal)