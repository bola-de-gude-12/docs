---
title: Setting up Exchange Web Services (EWS)
date: 09-10-2025
description: How to configure EWS for on-premises OCR in Document Capture.
id: DC-462
lang: en
---

# Setting up Exchange Web Services (EWS)
For email servers that are configured and used for on-premises OCR, the Continia OCR service supports Exchange Web Services (EWS), which makes it possible to authenticate with [Exchange Online](https://www.microsoft.com/en-ww/microsoft-365/exchange/exchange-online?market=af) using OAuth 2.0.

To set up EWS, you must complete the following guides in the order given. Note that you should follow either [To create and add a certificate](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/setting-up-exchange-web-services-ews#to-create-and-add-a-certificate) or [To create and add a client secret](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/setting-up-exchange-web-services-ews#to-create-and-add-a-client-secret) – but not both.

## To create an app registration in Microsoft Entra ID
To authenticate with Exchange Online, register the Continia OCR service as an application in Microsoft Entra ID (formerly known as Azure Active Directory). This registration establishes a trust relationship between the Continia OCR service and the Microsoft identity platform.

Before you can register the application, you must:
* Have a Microsoft Entra account with an active subscription. For more information, see [Build in the cloud with an Azure account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) (Microsoft article).
* Set up a Microsoft Entra tenant. For more information, see [Set up a new Microsoft Entra tenant](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-create-new-tenant) (Microsoft article).

To register the application:

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com/) with administrator privileges.
1. In the search box at the top, search for and select **App registrations**.
1. On the **App registrations** page, click **New registration**.
1. On the **Register an application** page, under **Name**, enter a name – for example, **Continia Document Capture Service**.
1. Under **Supported account types**, select **Accounts in this organizational directory only** (the default option).
1. Click **Register** to complete the initial app registration.
1. You're returned to the **App registrations** page, where the app registration's **Overview** pane is displayed. In the left menu, under **Manage**, click **API permissions** > **Add a permission**.
1. On the **Request API permissions** page, under **APIs my organization uses**, search for and select the **Office 365 Exchange Online** API and then **Application permissions**.
1. Click **full\_access\_as\_app** > **Add permissions**.
1. You're returned to the **API permissions** page. In the list of API permissions, under **Exchange**, select **full\_access\_as\_app** and then **Grant admin consent for \<domainname\>**.

To finish the app registration, the Document Capture OCR service must authenticate against the registration. For this to happen, you must add credentials in the form of either a client secret (the recommended option) or a certificate. The credentials prove the application's identity when requesting a token during authentication. Both options are described below.

>[!NOTE]
>On 1 October 2026, [Microsoft is retiring Exchange Web Services (EWS)](https://techcommunity.microsoft.com/blog/exchange/retirement-of-exchange-web-services-in-exchange-online/3924440) in favor of Microsoft Graph (MSG) – though EWS remains working until then. Continia plans on allowing Document Capture to export MSG directly to the config file.
>
>To start using MSG immediately:
>
>1. Replace EWS with MSG under \<Email\>, \<Protocol\> in the config file of the DC service. For more information, see [Where does the config.xml file get its data from?](https://continia.zendesk.com/hc/en-us/articles/115005874925-The-Config-xml-file-Where-does-it-get-its-data-from) (PartnerZone article).
>2. In the [Microsoft Entra admin center](https://entra.microsoft.com/), under **App registrations**, select the app you registered using the instructions above (for example, **Continia Document Capture Service**).
>3. Click **API permissions** on the menu and allow the Mail.ReadWrite API, under **Microsoft Graph**, to read and write mail in all mailboxes.

## To create and add a certificate
To use a certificate (also known as a public key) in the app registration process described above:

1. If you don't have an available certificate, you can create and sign your own following [Generate and export certificates for point-to-site using PowerShell](https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-certificates-point-to-site) (Microsoft article).
1. In the [Microsoft Entra admin center](https://entra.microsoft.com/), go to your registered app. On the menu, under **Manage**, click **Certificates & secrets**.
1. On the **Certificates & secrets** page, under **Certificates**, click **Upload certificate**.
1. Select the certificate you want to use. Only the following file types are accepted: .cer, .pem, .crt.
1. Click **Add**.
1. Copy the thumbprint that's displayed below the **Upload certificate** button. You'll need to enter it in Microsoft Dynamics NAV/Business Central later.

> [!IMPORTANT]
> The certificate you use must be installed on the server that's running the Continia Document Capture service.

## To create and add a client secret
To use a client secret (also known as an application password) in the app registration process described above:

1. In the [Microsoft Entra admin center](https://entra.microsoft.com/), go to your registered app. On the menu, under **Manage**, click **Certificates & secrets**.
1. On the **Certificates & secrets** page, under **Client secrets**, click **New client secret**.
1. In the dialog that opens, enter a free-text description for your client secret – for example, **Continia Document Capture Service (EWS)**. 
1. Under **Expires**, select a duration. E.g.: 730 days (24 months).
1. Click **Add**.
1. The client secret is added, and you're returned to the **Certificates & secrets** page. Copy the secret value and store it securely – it won't be displayed again.

## To set up categories in Document Capture
When you've added a certificate or a client secret as described above, the app registration is complete. Before leaving Microsoft Entra, navigate back to the **Overview** pane using the left menu, and then copy the values displayed in the following two fields:

* **Application (client) ID**
* **Directory (tenant) ID**

When configuring categories for document import, you need both of these values – along with your previously copied certificate thumbprint or client secret value (depending on your choice of credentials).

When you've recorded all required values, you're ready to set up categories for document import in Document Capture. To do this, open NAV/Business Central and then follow [Creating and configuring email addresses for document import](@DC-114#configuring-email-addresses-using-ews).

## Security recommendations
As app registration provides access to all mailboxes in the domain, it's recommended that you only associate the registration with the necessary subset of email addresses that function as mail-in accounts for documents to be processed in Document Capture.

For more information, see [Limiting application permissions to specific Exchange Online mailboxes](https://docs.microsoft.com/en-us/graph/auth-limit-mailbox-access) (Microsoft article).

## Related information
[Exchange Online](https://www.microsoft.com/en-ww/microsoft-365/exchange/exchange-online?market=af) (Microsoft article)  
[Configuring email addresses using EWS](@DC-114#configuring-email-addresses-using-ews)  