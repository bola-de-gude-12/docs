---
title: Enabling the Web Approval Portal for Business Central on premises
date: 16-06-2025
description:  
id: DC-481
lang: en
---

# Enabling the Web Approval Portal for Business Central on premises

If you have an on-premises installation of Microsoft Dynamics 365 Business Central, follow these steps to set up the Continia Web Approval Portal:

1. Search {{search}} for and select **Document Capture Setup**.
1. On the action bar, click **Approval Setup** > **Web Approval** to open the **Document Capture Setup / Continia Web Approval** page.
1. On the **General** FastTab, click the field to the right of **Continia Web Portal** to open the **Continia Company Setup** page. If you haven't yet enabled the Web Approval Portal, the field says **Not configured**.
1. Under **Web Portal Code**, click the down arrow on the right of the field to open the menu, and then click **New** in the lower-left corner of the menu to open the **Continia Web Portal List** page.
1. Under **Code**, enter a free-text code name for the portal environment you're setting up, and then fill out the remaining fields as required.
   > [!NOTE]
   > You can create multiple environments, if necessary. However, you can only use one environment at a time per company.
1. **Optional**: To enable users of the Web Approval Portal to sign in using their Office 365 credentials, follow [this guide](https://continia.zendesk.com/hc/da/articles/360007941420-How-to-setup-Business-Central-On-Prem-with-Continia-Web-Approval) (only available to Continia partners).
1. On the action bar, click **Create Web Services** > **Yes** to update all Continia Document Capture web services. You only have to do this the first time you create an environment.
1. Click **OK** > **OK** to save your changes and close the **Continia Web Portal List** and **Continia Company Setup** pages.
1. On the **Document Capture Setup / Continia Web Approval** page, on the action bar, click **Continia User Setup**, and then follow [this guide](Configuring users for the Web Approval Portal.md) to set up users for the Web Approval Portal.

## Related information

[Requirements for using the Continia Web Approval Portal on premises](@DC-135)  
[How to setup Business Central (On-Prem) with Continia Web Approval (on-Prem) using Office 365 logins](https://continia.zendesk.com/hc/da/articles/360007941420-How-to-setup-Business-Central-On-Prem-with-Continia-Web-Approval) (only available to Continia partners)  
[Configuring users for the Web Approval Portal](@DC-129)  