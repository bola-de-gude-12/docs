---
title: Creating and configuring email addresses for document import in Document Capture
date: 09-10-2025
description: How to configure email addresses for document import using IMAP or EWS.
id: DC-114
lang: en
---

# Creating and configuring email addresses for document import
When you use on-premises OCR, you must create and configure email addresses for each relevant document category to import your documents into Continia Document Capture. The following protocols are supported:
* Internet message access protocol (IMAP)
* Exchange Web Services (EWS)

The actual configuration of email addresses depends on which of these protocols you use. Both methods are described below.

> [!IMPORTANT]
>
> * Only unread emails are processed.
> * You must not use a user-accessible inbox.
> * You should uninstall or deactivate any other software that processes emails in any way.

## Configuring email addresses using IMAP
To configure an email address for document import using IMAP, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Open the document category that you want to set up with the Document Capture service. For example, to open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself) and click **Edit** on the action bar.
1. On the **Email** FastTab, in the **Server Address** field, enter the name or IP address of the email server you want to use.
1. In **Server Port**, enter the number of the port through which the connection to the mail server should be established. The IMAP port is usually 993 with an SSL connection and 143 without SSL.
1. In **Username**, enter the email address of the account that should be used for the selected document category (e.g.: invoice@company.com). This links it to the Document Capture email address for this category.
1. In **Password**, enter the password associated with the email address entered under **Username**.
1. **Optional**: to have incoming documents automatically deleted from the mail server upon download, enable **Delete After Download**.
1. **Optional**: to archive all document-import emails including their attached documents, enable **Import and Archive EMails**. This way, accountants, auditors, and other users of Document Capture have direct access to the emails.
1. Repeat the above steps for any additional categories that you want to set up with the Document Capture service.
1. When you've set up all categories, search ({{search}}) for and select **Export OCR Configuration Files**. A dialog box confirms that a number of configuration files have been exported. Click **OK** to close it.

## Configuring email addresses using EWS
> [!IMPORTANT]
> Before you can complete the guide below, you must set up EWS following the guide in [Setting up Exchange Web Services (EWS)](@DC-462). During the EWS setup process, you'll obtain a client ID, a tenant ID, and either a certificate thumbprint or a client secret value, which must be used when you configure EWS email addresses for document import.

To configure an email address for document import using EWS, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Open the document category that you want to set up with the Document Capture service. For example, to open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself) and click **Edit** on the action bar.
1. On the **Email** FastTab, under **Email Protocol**, select **EWS**.
1. In **Email Address** or **Shared Email Address**, enter the full address of the inbox you want the service to scan.
1. In **Client ID** and **Tenant ID**, enter the values you copied from the **Overview** pane in Azure, as described in [Setting up Exchange Web Services (EWS)](@DC-462). 
1. Fill out either **Client Secret** or **Certificate Thumbprint**, depending on your choice of credentials.
1. **Optional**: to have incoming documents automatically deleted from the mail server upon download, enable **Delete After Download**.
1. **Optional**: to archive all document-import emails including their attached documents, enable **Import and Archive Emails**. This gives accountants, auditors, and other users direct access to the original emails.
1. Repeat the above steps for any additional categories that you want to set up with the Document Capture service.
1. When you've set up all categories, search ({{search}}) for and select **Export OCR Configuration Files**. A dialog box confirms that a number of configuration files have been exported. Click **OK** to close it.

Document Capture is now configured to authenticate with EWS using OAuth 2.0. If authentication fails, an entry is created in the server application event log with information about the cause of the authentication error.