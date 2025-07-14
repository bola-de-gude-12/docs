---
title: Creating an App Registration in Azure Active Directory
date: 04-12-2023
description:  
id: DO-154
lang: en
---

# Creating an App Registration in Azure Active Directory

In order for Document Output to authenticate and send mails using Office 365, you must register an application in your Azure Active Directory (Azure AD).

## Prerequisites

* You must have an Azure account with an active subscription. You can create one for free [here](https://azure.microsoft.com/free/?WT.mc_id=A261C142F).
* An Azure AD tenant must be set up. For more information, see [this Microsoft guide](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-create-new-tenant).

## To create an app registration in Azure Active Directory

To register the application, follow these steps:

1. Sign in to the [Microsoft Azure portal](https://portal.azure.com/) with administrator privileges.
2. In the search box at the top, search for and select **App registrations**.
3. On the **App registrations** page, and then select **New registration**.
4. On the **Register an application** page, under **Name**, enter a name – for example, **Continia Document Output Service**.
5. Under **Supported account types**, select **Accounts in this organizational directory only** (the default option).
6. Select **Register** to complete the initial app registration.
7. You're returned to the **App registrations** page, where the app registration's **Overview** pane is displayed. In the left menu, under **Manage**, select **API permissions** > **Add a permission**.
8. On the **Request API permissions** page, under **Microsoft APIs**, select the **Microsoft Graph** and then **Delegated permissions**.
9. Select **User.Read** (might already be selected).
10. Scroll to the top and select **Application permissions**.
11. Select **Mail.ReadWrite** and **Mail.Send** > **Add permissions**.
12. You're returned to the **API permissions** page. In the list of API permissions, select **Grant admin consent for** <domain name> and then **Yes**.

Now you should copy the generated values from the **Overview** pane to a separate document for later authentication use:

* Application (client) ID
* Directory (tenant) ID

To finish the app registration, Document Output must authenticate against the newly created app. In order for this to happen, you must add credentials in the form of a client secret. The credentials are used to prove the application's identity when requesting a token, i.e. when authenticating with app registration.

## Creating and adding a client secret

To use a client secret (also known as an application password) in the app registration process described above, follow these steps:

1.	In the [Microsoft Azure portal](https://portal.azure.com/), go to the left menu. Under **Manage**, select **Certificates & secrets**.
2.	On the **Certificates & secrets** page, under **Client secrets**, select **New client secret**.
3.	In the dialog that opens, enter a free-text description for your client secret – for example, **Continia Document Output Service**.
4.	Under **Expires**, select a duration. 24 months is the maximum duration available.
5.	Select **Add**.
The client secret is added, and you're returned to the **Certificates & secrets** page. Copy the value of the secret and keep it in a safe place, as it will never be displayed again once you've navigated away from the page.

> [!NOTE]
> In case you forget to copy the client secret, you can just start the process over from step 1.

## To set up Azure Application (Office 365) in Business Central

To send mails from Document Output in Business Central, you must configure Document Output Azure Application (Office 365) in Business Central, and here's how you do it:

1. Open your Business Central client.
2. Choose the {{search}} icon, enter **Azure Application Setup**, and then choose the related link.
3. Give your configuration a name, enter a default from email address and from email name.
4. Fill in the application setup details with the Directory (tenant) ID, Application (tenant) ID and client secret you got from the app registration in the Azure Portal. 

Now you are ready to send emails using your Azure Application (Office 365). You can test by clicking the **Send test E-Mail**.

## See also
[Exchange Online](https://www.microsoft.com/en-ww/microsoft-365/exchange/exchange-online?market=af)  
[Microsoft Azure portal](https://portal.azure.com/)  
[Setting up OAuth for Document Output Service](@DO-22)