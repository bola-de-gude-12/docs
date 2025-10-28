---
title: Configuring users for the Web Approval Portal
date: 15-10-2025
description: How to configure users for access to the Continia Web Approval Portal.
id: DC-129
lang: en
---

# Configuring users for the Web Approval Portal

The process of configuring users for the Continia Web Approval Portal is the same for online and on-premises installations of Microsoft Dynamics 365 Business Central. This is done using the Continia user setup, which includes a number of fields that are specific and relevant to the Web Approval Portal. To edit these fields:

1. Search ({{search}}) for and select **Continia User Setup**.
1. Select the user whose properties you want to edit.
1. On the action bar, click **Edit List** to make the user entries in the list editable.
1. In the **Approval Client** column, select **Continia Web Approval Portal** to grant the selected user access to the portal.
1. If you want the user to be able to edit purchase lines in the portal, select the checkbox under **Can Edit Posting Lines**.
1. To determine what documents the user can search for in the portal's document archive (either all documents or only the user's own), make your selection under the **Document Search** column.
1. Repeat steps 2–6 for any additional users whose properties you want to edit.
1. When you're done, click **Export Users** on the action bar to export the Continia user setup to the Web Approval Portal.

Document Capture checks whether any relevant changes have been made. If this is the case, it performs the user export. If no such changes have been made, Document Capture skips the user export to avoid any unnecessary system downtime resulting from an export.

> [!IMPORTANT]
> The following applies to Continia-hosted versions of the Web Approval Portal (continiaonline.com): If your organization uses one of the two Business Central user login types **Windows** or **Database** (NavUserPassword), the email domains of the configured users must be registered as valid by Continia for you to be able to export users. This doesn't apply to the **Office 365** login type, though.
> 
> Only verified domain names – such as company domains like microsoft.com – can be registered. The domains of a number of well-known third-party email services like gmail.com, yahoo.com, and hotmail.com aren't allowed for this purpose, as such domains can't be verified as belonging to an organization.

## Using multiple databases

As of version 1.16.0, it's possible for users to be set up across multiple databases in the Web Approval Portal. The unique ID that groups users is their email address, and this is also true for partners who work with multiple customers.

If you have access to more than one database, the database selector is visible next to the company selector in the Web Approval Portal. Note that the company selector only works within the currently selected database, and only if you've selected the classic view on the **Settings** page of the Web Approval Portal. For example, if you have access to five companies in one database and three in another, you don't see eight companies altogether in the company selector.

## Available login types

All three login types are available in the Web Approval Portal, that is: **Database**, **Microsoft 365**, and **Windows**. You can also log in to different databases via different login types. For example, you can log in via Microsoft 365 to one database, via Windows to another, and via NavUserPassword to yet another – and also switch between them. Note that if you switch between login types, you're prompted for your password.

## Related information

[Setting up Web Approval](@DC-76)