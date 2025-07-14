---
title: Creating and Configuring Email Addresses for Document Import
date: 22-12-2022
description:  
id: DC-114
lang: en
---

# Creating and Configuring Email Addresses for Document Import
When you use on-premises OCR, you must create and configure email addresses for each relevant document category in order to import your documents into Continia Document Capture. Document Capture currently supports the following two protocols:
* Internet Message Access Protocol (IMAP)
* Exchange Web Services (EWS)

The actual configuration of email addresses depends on which of these protocols you use. Both methods are described below.

> [!WARNING]
> It's very important to note that:
> * Only unread emails are processed.
> * You must not use a user-accessible mailbox.
> * You should uninstall or deactivate any other software that processes emails in any way.

## Configuring email addresses using IMAP
To configure an email address for document import using IMAP, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Open the document category that you want to set up with the Document Capture service. For example, to open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself), and then choose **Edit** on the action bar.
1. On the **E-Mail** FastTab, in the **Server Address** field, enter the name or IP address of the mail server you want to use.
1. In **Server Port**, enter the number of the port through which the connection to the mail server should be established. The IMAP port is usually 993 with an SSL connection and 143 without SSL.
1. In **Username**, enter the email address of the account that should be used for the selected document category – for example, invoice@company.com. This will link it to the Document Capture email address for this category.
1. In **Password**, enter the password that's associated with the email address entered under **Username**.
1. Optional: If you want to have incoming documents automatically deleted from the mail server upon download, enable **Delete After Download**.
1. Optional: If you want Document Capture to archive all document-import emails including their attached documents, enable **Import and Archive E-Mails**. In this way, accountants, auditors, and other users of Document Capture have direct access to the emails.
1. Repeat the above steps for any additional categories that you want to set up with the Document Capture service.
1. When you've set up all categories, choose the {{search}} icon, enter **Export OCR Configuration Files**, and then choose the related link. A dialog box confirms that a number of configuration files have been exported. Select **OK** to close it.

## Configuring email addresses using EWS
> [!IMPORTANT]
> Before you can complete the guide below, you must [set up EWS following this guide](Setting up Exchange Web Services, EWS.md). During the EWS setup process, you'll obtain a client ID, a tenant ID, and either a certificate thumbprint or a client secret value, which must be used when you configure EWS email addresses for document import.

To configure an email address for document import using EWS, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Open the document category that you want to set up with the Document Capture service. For example, to open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself), and then choose **Edit** on the action bar.
1. On the **E-Mail** FastTab, under **E-Mail Protocol**, select **EWS**.
1. In **E-Mail Address** or **Shared Email Address**, enter the full address of the mailbox you want the service to scan.
1. In **Client ID** and **Tenant ID**, enter the values you copied from the **Overview** pane in Azure, as described [in this guide](Setting up Exchange Web Services, EWS.md). 
1. Fill out either **Client Secret** or **Certificate Thumbprint**, depending on your choice of credentials.
1. Optional: If you want to have incoming documents automatically deleted from the mail server upon download, enable **Delete After Download**.
1. Optional: If you want Document Capture to archive all document-import emails including their attached documents, enable **Import and Archive E-Mails**. In this way, accountants, auditors, and other users of Document Capture have direct access to the emails.
1. Repeat the above steps for any additional categories that you want to set up with the Document Capture service.
1. When you've set up all categories, choose the {{search}} icon, enter **Export OCR Configuration Files**, and then choose the related link. A dialog box confirms that a number of configuration files have been exported. Select **OK** to close it.

The Document Capture service is now set up to authenticate with EWS using OAuth 2.0. 
If authentication fails, an entry is created in the server application event log with information about the cause of the authentication error.

## Related information
[Setting up Exchange Web Services (EWS)](Setting up Exchange Web Services, EWS.md)  