---
title: Different Approval Clients
date: 18-04-2023
description: 
id: DC-111
lang: en
---

# Different Approval Clients

As an approver, you can approve incoming documents in two ways, depending on your organization's needs and wants:

* [Using Microsoft Dynamics 365 Business Central (or NAV)](#approving-documents-using-business-central)
* [Using the Continia Web Approval Portal](#approving-documents-using-the-web-approval-portal)

Which of these methods you'll use is determined in the setup. For more information, see [To set up users as approvers](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#to-set-up-users-as-approvers).

## Approving documents using Business Central

In Business Central, there are several ways to approve documents. The following are the most important ones:

* From each individual document page, for example from the **Purchase Invoice** page for invoices.
* From the dedicated **Purchase Approval Entries** page provided by Continia.
* Using the **Continia Document Capture Approver** Role Center.

If approvers in your organization already use Business Central in their daily work, it makes sense for them to also use it for the approval of incoming documents. In such cases, the first two options above are typically used, whereas the third one – the **Continia Document Capture Approver** Role Center – is primarily used by approvers who generally don't use Business Central for other purposes.

## Approving documents using the Web Approval Portal

If you prefer using a separate service for the approval of incoming documents, for example if your organization's approvers don't have access to Business Central, Continia's dedicated Web Approval Portal is the ideal choice. Licensed users can access this directly from a web browser and don't need access to Business Central at all.

To set up the Web Approval Portal and configure users for it, see [Setting up Web Approval](@DC-76).

> [!IMPORTANT]
> Although users of the Web Approval Portal need no access to Business Central whatsoever, they will in fact automatically be able to access it once they've been granted a license for the portal (typically a Team Member license). The reason for this is that the Web Approval Portal is built on standard Business Central functionality and was never intended to exclude anyone from accessing Business Central.

## Related information

[Setting up Document Approval](@DC-21)  