---
title: Exchange Web Services (EWS) einrichten
date: 08-05-2025
description:
id: DC-462
lang: de
---

# Exchange Web Services (EWS) einrichten

Für E-Mail-Server, die für On-Premises OCR konfiguriert und verwendet werden, unterstützt der Continia OCR-Dienst Exchange Web Services (EWS), wodurch die Authentifizierung bei [Exchange Online](https://www.microsoft.com/en-ww/microsoft-365/exchange/exchange-online?market=af) mit OAuth 2.0 möglich ist.

Um EWS einzurichten, müssen Sie eine der folgenden Anleitungen in der angegebenen Reihenfolge ausführen. Befolgen Sie entweder die Anleitung [So erstellen ein Zertifikat und fügen es hinzu](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/setting-up-exchange-web-services-ews#so-erstellen-ein-zertifikat-und-fugen-es-hinzu) oder [So erstellen Sie einen geheimen Clientschlüssel und fügen ihn hinzu](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/setting-up-exchange-web-services-ews#so-erstellen-sie-einen-geheimen-clientschlussel-und-fugen-ihn-hinzu), jedoch nicht beide.

## So erstellen Sie eine App-Registrierung in Microsoft Entra ID

Um sich bei Exchange Online zu authentifizieren, müssen Sie den Continia OCR-Dienst als Anwendung in Microsoft Entra ID (vormals Azure Active Directory) registrieren. Durch diese Registrierung wird eine Vertrauensbeziehung zwischen dem Continia OCR-Dienst und der Microsoft-Identitätsplattform hergestellt.

Bevor Sie die Anwendung registrieren können, müssen folgende Voraussetzungen erfüllt sein:

- Sie müssen über ein Microsoft Entra-Konto mit einem aktiven Abonnement verfügen. Weitere Informationen finden Sie unter [Erstellen in der Cloud mit einem Azure-Konto](https://azure.microsoft.com/de-de/pricing/purchase-options/azure-account?icid=azurefreeaccount&WT.mc_id=A261C142F) (Microsoft-Artikel).
- Ein Microsoft Entra-Mandant muss eingerichtet sein. Weitere Informationen finden Sie unter [Einrichten eines neuen Microsoft Entra-Mandanten](https://docs.microsoft.com/de-de/azure/active-directory/develop/quickstart-create-new-tenant) (Microsoft-Artikel).

So registrieren Sie die Anwendung:

1. Melden Sie sich mit Administratorrechten beim [Microsoft Entra Admin Center](https://entra.microsoft.com/) an.
2. Suchen und wählen Sie im Suchfeld oben **App-Registrierungen** aus.
3. Wählen Sie auf der Seite **App-Registrierungen** die Option **Neue Registrierung** aus.
4. Geben Sie auf der Seite **Anwendung registrieren** unter **Name** einen Namen ein, zum Beispiel **Continia Document Capture Service** ein.
5. Wählen Sie unter **Unterstützte Kontotypen** die Option **Nur Konten in diesem Organisationsverzeichnis** aus (die Standardoption).
6. Wählen Sie **Registrieren** aus, um die erstmalige App-Registrierung abzuschließen.
7. Sie werden zur Seite **App-Registrierungen** zurückgeleitet, auf der der Bereich **Übersicht** der App-Registrierung angezeigt wird. Wählen Sie im linken Menü unter **Verwalten** die Option **API-Berechtigungen** > **Berechtigung hinzufügen**.
8. Suchen und wählen Sie auf der Seite **API-Berechtigungen anfordern** unter **Von meiner Organisation verwendete APIs** die **Office 365 Exchange Online**-API und dann **Anwendungsberechtigungen** aus.
9. Wählen Sie **full\_access\_as\_app** > **Berechtigungen hinzufügen**.
10. Sie werden zur Seite **API-Berechtigungen** zurückgeleitet. Wählen Sie in der Liste der API-Berechtigungen unter **Exchange** > **full\_access\_as\_app** und dann **Adminstratorzustimmung für \<domainname\> erteilen**.

Um die App-Registrierung abzuschließen, muss sich der Document Capture OCR-Dienst gegenüber der Registrierung authentifizieren. Dazu müssen Sie Anmeldeinformationen entweder in Form eines geheimen Clientschlüssels (die empfohlene Option) oder eines Zertifikats hinzufügen. Die Anmeldeinformationen werden verwendet, um die Identität der Anwendung beim Anfordern eines Tokens nachzuweisen, d. h. bei der Authentifizierung bei der App-Registrierung. Beide Optionen werden nachfolgend beschrieben.

> [!NOTE]
> Am 1. Oktober 2026 [stellt Microsoft Exchange Web Services (EWS) ein](https://techcommunity.microsoft.com/blog/exchange/retirement-of-exchange-web-services-in-exchange-online/3924440) zugunsten von Microsoft Graph (MSG); EWS funktioniert bis dahin jedoch weiterhin. Continia plant, Document Capture den direkten Export von MSG in die Konfigurationsdatei zu ermöglichen.
>
> So können Sie MSG sofort verwenden:
>
> 1. Ersetzen Sie EWS durch MSG unter \<Email\>, \<Protocol\> in der Konfigurationsdatei des DC-Dienstes. Weitere Informationen finden Sie unter [The Config.xml file - Where does it get its data from?](https://continia.zendesk.com/hc/en-us/articles/115005874925-The-Config-xml-file-Where-does-it-get-its-data-from) (PartnerZone-Artikel).
> 2. Wählen Sie im [Microsoft Entra Admin Center(https://entra.microsoft.com/) unter **App-Registrierungen** die App aus, die Sie anhand der obigen Anweisungen registriert haben (z. B. **Continia Document Capture Service**).
> 3. Wählen Sie im Menü **API-Berechtigungen** aus und erlauben Sie der Mail.ReadWrite-API unter **Microsoft Graph**, E-Mails in allen Postfächern zu lesen und zu schreiben.

## So erstellen ein Zertifikat und fügen es hinzu

Um ein Zertifikat (auch öffentlicher Schlüssel genannt) im oben beschriebenen App-Registrierungsprozess zu verwenden, gehen Sie folgendermaßen vor:

1. Wenn Sie über kein verfügbares Zertifikat verfügen, können Sie es mit dieser Anleitung erstellen und signieren: [Generieren und Exportieren von Zertifikaten für Point-to-Site-Verbindungen mithilfe von PowerShell](https://docs.microsoft.com/de-de/azure/vpn-gateway/vpn-gateway-certificates-point-to-site) (Microsoft-Artikel).
2. Gehen Sie im [Microsoft Entra Admin Center](https://entra.microsoft.com/) zu Ihrer registrierten App. Wählen Sie im Menü unter **Verwalten** die Option **Zertifikate & Geheimnisse** aus.
3. Wählen Sie auf der Seite **Zertifikate & Geheimnisse** unter **Zertifikate** die Option **Zertifikat hochladen** aus.
4. Wählen Sie das Zertifikat aus, das Sie verwenden möchten. Es werden nur die folgenden Dateitypen akzeptiert: .cer, .pem, .crt.
5. Wählen Sie **Hinzufügen** aus.
6. Kopieren Sie den Fingerabdruck, der unter der Schaltfläche **Zertifikat hochladen** angezeigt wird. Sie müssen ihn später in Microsoft Dynamics NAV/Business Central eingeben.

> [!IMPORTANT]
> Das von Ihnen verwendete Zertifikat muss auf dem Server installiert sein, auf dem der Continia Document Capture-Dienst ausgeführt wird.

## So erstellen Sie einen geheimen Clientschlüssel und fügen ihn hinzu

So verwenden Sie einen geheimen Clientschlüssel (auch Anwendungskennwort genannt) im oben beschriebenen App-Registrierungsprozess:

1. Gehen Sie im [Microsoft Entra Admin Center](https://entra.microsoft.com/) zu Ihrer registrierten App. Wählen Sie im Menü unter **Verwalten** die Option **Zertifikate & Geheimnisse** aus.
2. Wählen Sie auf der Seite **Zertifikate & Geheimnisse** unter **Geheime Clientschlüssel** die Option **Neuer geheimer Clientschlüssel** aus.
3. Geben Sie im sich öffnenden Dialogfeld eine Freitextbeschreibung für Ihren geheimen Clientschlüssel ein, zum Beispiel **Continia Document Capture Service (EWS)**.
4. Wählen Sie unter **Gültig bis** eine entsprechende Option aus. Es wird empfohlen, die Gültigkeit auf unendlich zu setzen.
5. Wählen Sie **Hinzufügen** aus.
6. Der geheime Clientschlüssel wird hinzugefügt und Sie werden zur Seite **Zertifikate & Geheimnisse** zurückgeleitet. Kopieren Sie den Wert des geheimen Schlüssels und bewahren Sie ihn an einem sicheren Ort auf, da er nie wieder angezeigt wird, sobald Sie die Seite verlassen.

## So richten Sie Kategorien in Document Capture ein

Wenn Sie wie oben beschrieben ein Zertifikat oder ein Clientgeheimnis hinzugefügt haben, ist die App-Registrierung abgeschlossen. Bevor Sie Microsoft Entra verlassen, navigieren Sie jedoch über das linke Menü zurück zum Bereich **Übersicht** und kopieren Sie dann die in den folgenden beiden Feldern angezeigten Werte:

- **Anwendungs-ID (Client)**
- **Verzeichnis-ID (Mandant)**

Beim Konfigurieren von Kategorien für den Dokumentimport benötigen Sie beide Werte – zusammen mit Ihrem zuvor kopierten Zertifikatfingerabdruck oder Client-Geheimniswert (je nach den von Ihnen gewählten Anmeldeinformationen).

Wenn Sie alle erforderlichen Werte erfasst haben, können Sie Kategorien für den Dokumentimport in Document Capture einrichten. Öffnen Sie hierzu NAV/Business Central und folgen Sie dann der Anleitung [E-Mail-Adressen für den Dokumentenimport erstellen und konfigurieren](@DC-114#configuring-email-addresses-using-ews).

## Sicherheitsempfehlungen

Da die App-Registrierung Zugriff auf alle Postfächer in der Domäne bietet, wird empfohlen, die Registrierung nur mit der erforderlichen Teilmenge an E-Mail-Adressen zu verknüpfen, die als Mail-In-Konten für in Document Capture zu verarbeitende Dokumente verwendet werden. Weitere Informationen finden Sie unter [Anwendungsberechtigungen für bestimmte Exchange Online-Postfächer einschränken](https://docs.microsoft.com/de-de/graph/auth-limit-mailbox-access) (Microsoft-Artikel).

## Informationen zum Thema

[Exchange Online](https://www.microsoft.com/en-ww/microsoft-365/exchange/exchange-online?market=af)  
[E-Mail-Adressen mit EWS konfigurieren](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/creating-and-configuring-email-addresses-for-document-import#configuring-email-addresses-using-ews)