---
title: Enabling the Web Approval Portal for Business Central (online)
date: 23-07-2025
description: How to enable the Web Approval Portal in online installations of Business Central.
id: DC-480
lang: en
---

# Enabling the Web Approval Portal for Business Central (online)

Set up the Continia Web Approval Portal in an online installation of Microsoft Dynamics 365 Business Central, then you can sign in to the portal via Microsoft 365 and manage your approvals.

## Configure the application in the Azure portal

1. Go to the [Microsoft Azure Portal](https://portal.azure.com) and search for **App registrations**. In the top menu, click **New registration**.
1. Name the app registration (e.g.: Continia Web Approval), and fill out the remaining fields as indicated below.
   * **Supported account types** - Accounts in this organizational directory only
   * **Redirect URI** - Web, https://www.continiaonline.com
1. Click **Register** to save the app registration. On the **App registrations** page, click **Authentication** in the left-hand menu.
1. Add the following redirect URIs and click **Save** when you're done. Note that URIs are case sensitive.
   * https://www.continiaonline.com/Account/SSOCallback
   * https://demo.continiaonline.com (only if you have a sandbox environment)
   * https://demo.continiaonline.com/Account/SSOCallback (only if you have a sandbox environment)
1. In the left-hand menu, click **Certificates & secrets** and click **New client secret**.
1. Enter a description text and select the desired expiry date. Take note of the date you set in here. When it expires, you have to manually recreate a client secret and copy it to the Web Approval Portal setup in Business Central.
1. Click **Add** to create a client secret, then copy the text under **Value**. Make sure to save this value in a safe place, as it's no longer visible after you navigate away from this page.
1. In the left-hand menu, click **API permissions**. Then, click **Add a permission**.
1. Click the **Microsoft APIs** tab, then click **Dynamics 365 Business Central**.
1. Click **Delegated permissions**, then select the **user_impersonation** box and click **Add permissions**.
1. To prevent the consent screen from being displayed to every user during their first login to the Web Approval Portal, click **Grant admin consent for [directory name]**.
1. In the left-hand menu, click **Overview**. Copy the **Application (client) ID**. Keep the copied value in a safe place, together with the value copied earlier from the **Client secrets** tab.

## Set up the Web Approval Portal in Business Central

The setup in Business Central is shared between Expense Management and Document Capture. Even if both solutions are activated, only one setup is needed for the Azure AD Integration. However, individual settings for the portal need to be adjusted.

### Document Capture

1. Search ({{search}}) for and select **Document Capture Setup**.
1. On the **Document Capture Setup** page, on the action bar, click **Setup** > **Web Approval** to open the **Document Capture Setup / Continia Web Approval** page.
1. On the **General** FastTab, enable **Use Continia Web Approval Portal**.
1. Under **Welcome Emails**, select whether you want welcome emails to be sent to users of the Web Approval Portal automatically or if you prefer doing this manually yourself.
1. Fill out the fields under the **Azure AD Integration** section using the application ID and the client secret value created earlier. Note that the **Azure Application Key** (i.e.: client secret) expires within the period of time you selected previously. It's crucial that you keep track of this expiry date to avoid any interruptions to the Continia Web Approval Portal service.
1. On the action bar, click **Users** > **Continia User Setup** to open the **Continia User Setup** page.
1. On the action bar, click **Edit List** and set the **Approval Client** field to Continia Web Approval Portal for your approval users. For more information, see [Configuring users for the Web Approval Portal](@DC-129).
1. On the action bar, click **Export Users**.

The exported approval users can now sign in to https://continiaonline.com and https://demo.continiaonline.com with their Microsoft 365 accounts.

## Related information

[Requirements for using the Continia Web Approval Portal online](/continia-document-capture/getting-started/frequently-asked-questions/minimum-requirements/overview#continia-web-approval-portal)