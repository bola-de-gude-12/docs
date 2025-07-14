---
title: Expense Management Enabling the Web Approval Portal for Business Central On-Premises
date: 20-1-2022
description:  
id: EM-60
lang: en
---

# Enabling the Web Approval Portal for Business Central On-Premises

If you have an *on-premises* installation of Microsoft Dynamics 365 Business Central, follow these steps to set up the Continia Web Approval Portal:

1. Choose the {{search}} icon, enter **Expense Management Setup**, and then choose the related link.

1. In the action bar, select **Setup**  > **Web Approval** to open the **Expense Management Setup / Web Approval** page.

1. On the **General** FastTab, select the field to the right of **Continia Web Portal** to open the **Continia Company Setup** page. If you haven't yet enabled the Web Approval Portal, the field says **Not configured**.

1. Under **Web Portal Code**, select the down arrow on the right of the field to open the menu, and then select **New** in the lower-left corner of the menu to open the **Continia Web Portal List** page.

1. Under **Code**, enter a free-text code name for the portal environment you're setting up, and then fill in the remaining fields as required.
   > [!NOTE]
   > You can create multiple environments, if necessary. However, you can only use one environment at a time per company.
   
1. **Optional**: If you want to enable users of the Web Approval Portal to sign in using their Office 365 credentials, follow [this guide](https://continia.zendesk.com/hc/da/articles/360007941420-How-to-setup-Business-Central-On-Prem-with-Continia-Web-Approval) (only available to Continia partners).

1. In the action bar, select **Create Web Services** > **Yes** to update all Continia Document Capture web services. You only have to do this the first time you create an environment.

1. Select **OK** > **Close** to save your changes and close the **Continia Web Portal List** and **Continia Company Setup** pages.
1. On the **Expense Management Setup / Web Approval** page, in the action bar, select **Continia User Setup**, and then follow [this guide](@EM-53) to set up users for the Web Approval Portal.

## See also

[Requirements for Using the Continia Web Approval Portal On-Premises](/Continia Expense Management/Development and Administration/On-Premises/Deployment/Web Approval Portal Requirements On-Premises.md)  
[How to setup Business Central (On-Prem) with Continia Web Approval (on-Prem) using Office 365 logins](https://continia.zendesk.com/hc/da/articles/360007941420-How-to-setup-Business-Central-On-Prem-with-Continia-Web-Approval) (only available to Continia partners)  
[Configuring Users for the Web Approval Portal](Configuring users for the Web Approval Portal.md)  