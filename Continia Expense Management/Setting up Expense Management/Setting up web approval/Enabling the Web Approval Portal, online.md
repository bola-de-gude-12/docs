---
title: Enabling the Web Approval Portal for Business Central Online
date: 7-1-2022
description: 
id: EM-52
lang: en
---

# Enabling the Web Approval Portal for Business Central Online

If you have an *online* installation of Microsoft Dynamics 365 Business Central, follow these steps to set up the Continia Web Approval Portal:

1. Register the Web Approval Portal as an application in Azure Active Directory (Azure AD). If you need help for this, follow [this guide](https://continia.zendesk.com/hc/da/articles/360005985960-How-to-setup-Dynamics-365-Business-Central-with-Continia-Web-Approval) (only available to Continia partners). Be sure to take note of the ID and client secret, as you'll need these later in the process.
1. In Business Central, choose the {{search}} icon, enter **Expense Management Setup**, and then choose the related link.
1. In the action bar, select **Setup** > **Web Approval** to open the **Edit - Expense Management Setup / Continia Web Approval** page.
1. On the **General** FastTab, enable the approval portal by toggling the **Use Continia Web Approval Portal** switch.
1. Under **Welcome Emails**, select whether you want welcome emails to be sent to users of the Web Approval Portal automatically, or if you prefer doing this manually yourself.
1. Under **Azure ID Integration**, enter the Azure AD application ID and key (client secret) that you created and stored in step 1 above. This will enable users of the Web Approval Portal to sign in using their Office 365 credentials.
1. In the action bar, select **Users** > **Continia User Setup**, and then follow [this guide](Configuring users for the Web Approval Portal.md) to set up users for the Web Approval Portal.

## See also

[Requirements for using the Continia Web Approval Portal online](/continia-expense-management/getting-started/troubleshooting-and-faqs/minimum-requirements#continia-web-approval-portal)  
[How to setup Dynamics 365 Business Central with Continia Web Approval](https://continia.zendesk.com/hc/da/articles/360005985960-How-to-setup-Dynamics-365-Business-Central-with-Continia-Web-Approval) (only available to Continia partners)  
[Configuring Users for the Web Approval Portal](@EM-53)  