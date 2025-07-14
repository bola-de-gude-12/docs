---
title: Frequently Asked Questions About Emails
date: 25-06-2024
description: Frequently asked questions about emails
id: DO-105
lang: en
---

# Email FAQ
In this section, you can find answers to some of the most frequently asked questions about the use of emails in Document Output. The answers provide information on subjects such as handling error codes and the use of external fonts.

## Can I use fonts from external sources in Document Output?
The fonts implemented in the Document Output editor are all considered websafe, meaning they are standard on most computers/browsers/mail clients. As an example, Calibri is a Microsoft font and not one you can just assume is on all clients.
In addition, there are some technical limitations to what the editor can do.

If your client wants to use a specific font, you or your developer should be able to modify the HTML code to use the font manually. Continia doesn't provide support for this, though, or take any kind of responsibility.

## I get a popup window in the email editor saying "CDOa46Editor control add-in might not run as you expect it to". What should I do about it?
This is a Microsoft message and will not change or affect the functionality of Document Output. It's small conflict in the way our HTML mail editor works versus Microsoft's way of handling it.

The only thing you need to do is clicking it away.

## System.Net.Mail.SmtpClient.Send failed with an error message. What do I do?

System.Net.Mail.SmtpClient.Send failed with the following message:

*A call to System.Net.Mail.SmtpClient.Send failed with the following message. A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond [IP address and port number]*

The error occurred because the mail server connection timed out, likely due to a restriction on the number of emails you can send per minute.

To solve the issue in a *cloud* installation, follow these steps:

1. Open **Document Output Setup**.
2. Look for **Max no. of mails per minute** in the **General** FastTab.
3. Enter **29** in this field.

To solve the issue in a *on-premises* installation, follow these steps:

1. Open **Document Output SMTP Setup**.
2. Look for **Max no. of mails per minute** in the **General** FastTab.
3. Enter **29** in this field.

This adjustment will help prevent the error in the future. By setting the connection timeout to 29, you ensure a smoother email sending process.

## How can I check if my email arrived?

If you are uncertain whether your email has reached the recipient, consider the following steps to diagnose the issue: 

* **Check the Document Output Log** - look for an entry in the Document Output log indicating that the email was sent. If the log contains a record of the email, it confirms that it has left Document Output successfully. To view the log, go to the customer card, and in the right panel, in the **Mail** section, select **Log**. 
* **Check whether there's an issue with the exchange server** - if the log shows that the email was sent, but the recipient claims it did not arrive, it's possible that there might be an issue with the exchange server or some other factors outside of Document Output. The exchange server may have a hard time handling a large volume of emails simultaneously, or it could block certain emails, considering them as potential spam. You should contact your email administrator so they can look into the status of the emails and resolve the issue. Administrators can assess the performance of the exchange, identify potential blocks, and address email delivery problems.

## Why is my PDF locked?

Sending emails with unprotected PDF file attachments poses a significant security risk. To address this issue, you can enhance security by protecting PDF files with a password shared exclusively with the intended recipient. This can be achieved by [assigning PDF passwords for specific templates and individual customers](@DO-35).

If you prefer not to encrypt your PDF files, or if you just want to check if a PDF password is assigned, check the following:

1. Firstly, check if the email template or customer card has a password protection feature enabled:

   * Go to **Email Templates**, and select the email template. In the **General** FastTab, under **Advanced**, see whether a password has been added to the **PDF Password** field. If a password has been added, the PDF can only be opened using this password after the PDF has been sent out.
   * Open the customer card, navigate to the **Document Output** FactBox, and select the three dots next to the **Output Profile** field. In the **General** FastTab, see whether a password has been added to the **PDF Password** field. If it is, this password will be used for documents sent to this customer.

2. Additionally, ensure that your email browser (e.g., Chrome, Edge, Firefox) doesn't automatically fill in password fields.

## How do I export and import email templates?

You can export templates from an old account and import them into a new one, and here's how you do it:

1. Open the **Email Templates**  menu.
2. Select the templates you want to export.
3. Click on the **Import/Export** menu and select **Export Template**.
4. Change to a different account.
5. Open the **Email Templates** page, navigate to the **Import/Export** submenu, and select **Import Template**.

## How can I exclude specific document types from being sent?

There are two ways to exclude specific document types:
* Build an Output Profile with the same profile code that is generally used on the customer, but define a *Skip* profile for certain templates. On the customer card, select the new profile code.
* Alternatively, you can disable the email template.  

For more information, refer to the [Output Profiles](@DO-74) article.