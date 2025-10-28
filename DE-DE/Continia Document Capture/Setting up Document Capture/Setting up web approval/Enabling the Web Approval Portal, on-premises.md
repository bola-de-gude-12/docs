---
title: Das Web Approval Portal für Business Central On-Premises aktivieren
date: 16-06-2025
description:
id: DC-481
lang: de
---

# Das Web Approval Portal für Business Central On-Premises aktivieren

Wenn Sie über eine On-Premises-Installation von Microsoft Dynamics 365 Business Central verfügen, gehen Sie folgendermaßen vor, um das Continia Web Approval Portal einzurichten:

1. Suchen Sie ({{search}}) nach **Document Capture Einrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie in der Aktionsleiste auf **Genehmigungseinrichtung** > **Web-Genehmigungen**, um die Seite **Document Capture Einrichtung / Continia Web Genehmigungen** zu öffnen.
3. Klicken Sie im Inforegister **Allgemein** auf das Feld rechts neben **Continia Web Portal** aus, um die Seite **Continia Mandant Einrichtung** zu öffnen. Wenn Sie das Web Approval Portal noch nicht aktiviert haben, wird im Feld **Nicht konfiguriert** angezeigt.
4. Klicken Sie unter **Webportal** auf den nach unten zeigenden Pfeil rechts neben dem Feld aus, um das Menü zu öffnen, und klicken Sie dann auf **Neu** in der unteren linken Ecke des Menüs aus, um die Seite **Continia Webportalübersicht** zu öffnen.
5. Geben Sie unter **Code** eine Beschreibung für die Portalumgebung ein, die Sie einrichten, und füllen Sie dann die restlichen Felder nach Bedarf aus.
   > [!NOTE]
   > Sie können bei Bedarf mehrere Umgebungen erstellen. Allerdings können Sie jeweils nur eine Umgebung pro Mandant nutzen.
6. **Optional**: Wenn Sie Benutzern des Web Approval Portals ermöglichen möchten, sich mit ihren Office 365-Anmeldeinformationen anzumelden, können Sie dies mit [dieser Anleitung](https://continia.zendesk.com/hc/da/articles/360007941420-How-to-setup-Business-Central-On-Prem-with-Continia-Web-Approval) einrichten (nur für Continia-Partner verfügbar).
7. Klicken Sie in der Aktionsleiste auf **Erzeuge Web Service** > **Ja**, um alle Continia Document Capture-Webdienste zu aktualisieren. Dies ist nur erforderlich, wenn Sie eine Umgebung zum ersten Mal  erstellen.
8. Klicken Sie auf **OK** > **OK**, um Ihre Änderungen zu speichern und um die Seiten **Continia Webportalübersicht** und **Continia Mandant Einrichtung** zu schließen.
9. Klicken Sie auf der Seite **Document Capture Einrichtung / Continia Web Genehmigungen** in der Aktionsleiste auf **Continia Benutzereinrichtung**, und folgen Sie dann [dieser Anleitung](Configuring users for the Web Approval Portal.md), um Benutzer für das Web Approval Portal einzurichten.

## Informationen zum Thema

[Anforderungen für die Verwendung des Continia Web Approval Portals On-Premises](@DC-135)  
[So richten Sie Business Central (On-Premises) für die Continia Web-Genehmigung (On-Premises) mit Office 365-Anmeldeinformationen ein](https://continia.zendesk.com/hc/da/articles/360007941420-How-to-setup-Business-Central-On-Prem-with-Continia-Web-Approval) (nur für Continia-Partner verfügbar)  
[Benutzer für das Web Approval Portal konfigurieren](@DC-129)