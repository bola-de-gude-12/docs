---
title: Enabling the Web Approval Portal for Business Central online
date: 04-07-2025
description: How to enable the Web Approval Portal in online installations of Business Central.
id: DC-480
lang: en
---

# Enabling the Web Approval Portal for Business Central online

If you have an online installation of Microsoft Dynamics 365 Business Central, follow these steps to set up the Continia Web Approval Portal:

1. Register the Web Approval Portal as an application in Microsoft Entra ID (formerly known as Azure Active Directory). For more information, follow [How to setup Continia Web Approval for BC Cloud](https://continia.zendesk.com/hc/en-us/articles/13386916791698) (only available to Continia partners). Be sure to take note of the ID and client secret, as you'll need these later in the process.
1. Search {{search}} for and select **Document Capture Setup**.
1. On the action bar, click **Setup** > **Web Approval** to open the **Document Capture Setup / Continia Web Approval** page.
1. On the **General** FastTab, enable the **Use Continia Web Approval Portal** toggle.
1. Under **Welcome Emails**, select whether you want welcome emails to be sent to users of the Web Approval Portal automatically or if you prefer doing this manually yourself.
1. Under **Azure ID Integration**, enter the Entra ID application ID and key (client secret) that you created and stored in step 1 above. This enables users of the Web Approval Portal to sign in using their Office 365 credentials.
1. On the action bar, click **Users** > **Continia User Setup** and follow [Configuring users for the Web Approval Portal](@DC-129) to set up users for the Web Approval Portal.

## Related information

[Requirements for using the Continia Web Approval Portal online](/continia-document-capture/getting-started/frequently-asked-questions/minimum-requirements/overview#continia-web-approval-portal)