---
title: Setting up OAuth for Document Output Service
date: 07-11-2023
description:  
id: DO-22
lang: en
---

# Setting up OAuth for Document Output Service
OAuth is an authentication protocol that provides access to your Microsoft Dynamics 365 Business Central installation from external services, including Document Output Service.

To set up OAuth, you must complete the following guides in the order given.

## Creating an app registration in Azure Active Directory
In order for the Document Output Service to authenticate with your Business Central installation, you must register the service as an application in Azure Active Directory (Azure AD). This registration establishes a trust relationship between the Document Output Service and the Microsoft identity platform.

Before you can register the application, the following prerequisites must be met:
* You must have an Azure account with an active subscription. This can be [created for free here](https://azure.microsoft.com/free/?WT.mc_id=A261C142F).
* An Azure AD tenant must be set up. For more information, see [this Microsoft guide](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-create-new-tenant).

To register the application, follow these steps:

1. Sign in to the [Microsoft Azure portal](https://portal.azure.com/) with administrator privileges.
1. In the search box at the top, search for and select **App registrations**.
1. On the **App registrations** page, select **New registration**.
1. On the **Register an application** page, under **Name**, enter a name – for example, **Continia Document Output Service**.
1. Under **Supported account types**, select **Accounts in this organizational directory only** (the default option).
1. Select **Register** to complete the initial app registration.
1. You're returned to the **App registrations** page, where the app registration's **Overview** pane is displayed. In the left menu, under **Manage**, select **API permissions** > **Add a permission**.
1. On the **Request API permissions** page, under **Microsoft APIs**, select the **Dynamics 365 Business Central** API and then **Application permissions**.
1. Select **app_access**, **API.ReadWrite.All**, **Automation.ReadWrite.All** > **Add permissions**.
1. You're returned to the **API permissions** page. In the list of API permissions, select **Grant admin consent for \<domain name\>** and then **Yes**.

Now, you should copy the generated values from the **Overview** pane to a separate document for later authentication use:

* Application (client) ID
* Directory (tenant) ID

To finish the app registration, the Document Output Service must authenticate against the registration. In order for this to happen, you must add credentials in the form of a client secret. The credentials are used to prove the application's identity when requesting a token, i.e. when authenticating with app registration.

## Creating and adding a client secret
To use a client secret (also known as an *application password*) in the app registration process described above, follow these steps:

1. In the [Microsoft Azure portal](https://portal.azure.com/), go to the left menu. Under **Manage**, select **Certificates & secrets**.
1. On the **Certificates & secrets** page, under **Client secrets**, select **New client secret**.
1. In the dialog that opens, enter a free-text description for your client secret – for example, **Continia Document Output Service**. 
1. Under **Expires**, select a duration. **24 months** is the maximum duration available.
1. Select **Add**.
1. The client secret is added, and you're returned to the **Certificates & secrets** page. Copy the value of the secret and keep it in a safe place, as it will *never be displayed again* once you've navigated away from the page.

> [!NOTE]
> In case you forget to copy the client secret, you can just start the process over from step 1.

## Registering the application in Business Central

To allow requests using the access token that's generated in the OAuth process, the application must be registered in Business Central.

1. Open your Business Central client.
2. Choose the {{search}} icon, enter **Microsoft Entra Applications**  (called **Azure Active Directory Applications** before BC23), and then choose the related link.
3. On **Microsoft Entra Applications**, Click **New**.
4. In the **General** FastTab, under **Client ID**, paste the client ID you wrote down earlier.
5. Under **Description**, enter a description of the application, eg. *CDO Service*. Note that this step will also create a new user with the same name as what's written in the description field.
6. Under **User Groups**, under **Code**, select **D365 Automation**.
7. Under **User Permission Sets**, select **CDO-Super**.

Now that you have completed all of the above steps, you're ready to begin using OAuth for authentication in Document Output Service.

## See also
[Exchange Online](https://www.microsoft.com/en-ww/microsoft-365/exchange/exchange-online?market=af)  
[Microsoft Azure portal](https://portal.azure.com/)  