---
title: Enabling the web approval portal for Business Central online
date: 23-07-2025
description: Set up the web approval portal for your online installation of MS BC
id: EM-52
lang: en
---

# Enabling the Web Approval Portal for Business Central online

Set up the Continia Web Approval Portal in an online installation of Microsoft Dynamics 365 Business Central, then you can sign in to the portal via Microsoft 365 and manage your expense approvals.

## Prerequisite

* You must have an *online* installation of Microsoft Dynamics 365 Business Central

## Configure the app in the Azure Portal

To set up Continia's Web Approval Portal, you must first register the Web Approval Portal as an application in Azure Active Directory (Azure AD). If you need help for this, follow [this guide](https://continia.zendesk.com/hc/da/articles/360005985960-How-to-setup-Dynamics-365-Business-Central-with-Continia-Web-Approval) (only available to Continia partners). Be sure to take note of the ID and client secret, as you'll need these later in the process.

1. Go to the [Microsoft Azure Portal](https://portal.azure.com/) and search for **App registrations**. In the top menu, click **New registration**.
2. Name the app registration (for example, Continia Web Approval), and fill in the following fields as indicated:
   - **Supported account types** - Accounts in this organizational directory only
   - **Redirect URI** - Web, https://www.continiaonline.com
3. Click **Register** to save the app registration. Then on the **App registrations** page, click **Authentication** in the left-hand menu.
4. Add the following redirect URLs then click **Save**. Note URLs are case sensitive.
   - https://www.continiaonline.com/Account/SSOCallback
   - https://demo.continiaonline.com (only if you have a sandbox environment)
   - https://demo.continiaonline.com/Account/SSOCallback (only if you have a sandbox environment)
5. In the left-hand menu, click **Certificates & secrets** > **New client secret**.
6. Enter a description text and select the desired expiry date. Take note of this date, because when it expires you must manually recreate a client secret and copy it to the Web Approval Portal setup in Business Central.
7. Click **Add** to create a client secret, then copy the text under **Value**. 
>[!IMPORTANT]
>Save this value in a safe place, as it's no longer visible after you navigate away from this page.
8. In the left-hand menu, click **API permissions** > **Add a permission**.
9. Click the **Microsoft APIs** tab > **Dynamics 365 Business Central**.
10. Click **Delegated permissions**, then select the **user_impersonation** checkbox and click **Add permissions**.
11. To prevent the consent screen from being displayed to every user during their first login to the Web Approval Portal, click **Grant admin consent for [directory name]**.
12. In the left-hand menu, click **Overview**. Copy the **Application (client) ID**. 
 >[!IMPORTANT]
 >Keep the copied value in a safe place, together with the value copied earlier from the **Client secrets** tab.

## Set up the Web Approval Portal in Business Central

The setup in Business Central is shared between Expense Management and Document Capture. Even if both solutions are activated, only one setup is needed for the Azure AD Integration. However, individual settings for the portal need to be adjusted. 

To set up the Web Approval Portal for Expense Management:

1. In Business Central, search for {{search}} **Expense Management Setup**.
1. On the **Expense Management Setup** page > on the action bar, click **Setup** > **Web Approval** to open the **Edit - Expense Management Setup / Continia Web Approval** page.
1. Under **General**, enable the approval portal by toggling the **Use Continia Web Approval Portal** switch on.
1. Under **Welcome Emails**, select whether you want welcome emails to be sent to users of the Web Approval Portal automatically, or if you prefer to do this manually yourself.
1. Under **Azure ID Integration**, enter the Azure AD application ID and key (client secret) that you created and stored earlier. This will enable users of the Web Approval Portal to sign in using their Office 365 credentials.
 >[!NOTE]
 >The Azure Application Key ( the client secret) expires within the period of time you selected previously. It's crucial that you keep track of this expiry date to avoid any interruptions to the Continia Web Approval Portal service.

6. On the action bar, click **Users** > **Continia User Setup** to open the **Continia User Setup** page. 
7. On the action bar, click **Edit List** and set the **Approval Client** field to Continia Web Approval Portal for your approval users. For more information, see [Configuring users for the Web Approval Portal](@EM-53).
8. On the action bar, click **Export Users**.

The exported approval users can now sign in to https://continiaonline.com and https://demo.continiaonline.com with their Microsoft 365 accounts.

## Related information

[Requirements for using the Continia Web Approval Portal online](/continia-expense-management/getting-started/troubleshooting-and-faqs/minimum-requirements#continia-web-approval-portal)  
[How to setup Dynamics 365 Business Central with Continia Web Approval](https://continia.zendesk.com/hc/da/articles/360005985960-How-to-setup-Dynamics-365-Business-Central-with-Continia-Web-Approval) (only available to Continia partners)  
[Configuring Users for the Web Approval Portal](@EM-53)  