---
title: Attaching Files to Email Templates
date: 19-04-2024
description:  
id: DO-58
lang: en
---

# Attaching Files to Email Templates

You can attach any type of document, such as welcome letters, terms and conditions, etc., and any file type to email templates using the Attach File feature. When you attach one or more files using this method, the email will contain the PDF file created from the Report Selection in the template as well as all files attached separately. The composition of the attached files can be different for each email template line, so you can vary them to the specific requirements of the situation.
<br>
<br>
<iframe src="https://player.vimeo.com/video/882882315?h=9771cad014&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" title="DO Learn_1c PDF attachments"></iframe>

This video is part of the course [Get started using Document Output](https://learn.continia.com/get-started-using-document-output) on Continia Learn.

## Including attachments from source documents

If you want to include attachments from source documents from Business Central in an email template, you need to enable the appropriate attachment options for that email template, and here's how you do that:

1. Choose the {{search}} icon, enter **Email Templates**, and then choose the related link.
1. Select the email template for which you want to include attachments from source documents.
1. In the **Email Template Lines** FastTab, under **Mail Attachments**, enable the needed options.

Repeat steps 2 and 3 for each template for which you want to include attachments from source documents.

## Attaching files to email templates

To attach one or more files to an email template, follow these steps:

1. Choose the {{search}} icon, enter **Email Templates**, and then choose the related link.
1. Select the email template to which you want to attach a file.
1. In the action bar in the **Email Template Lines** FastTab, select **Email Template** > **Edit HTML Template**.
1. In the **Attachment** FactBox, select the **Attachment** dropdown menu and then **New**.
1. Select a file to attach it to this specific email template. You can only attach one file at a time, but you can repeat the process as many times as needed.

You can also view the full list of attachments, remove files, or download a list of the attached files.

Though you as such can attach any file type and files of any size, you're recommended to keep in mind that attaching very large files (because exchange servers have a limitation on file size) or certain file types (such as .exe files, as they are caught by firewalls) can result in rejected emails.

## Disabling reports as email attachments

You have the option to disable sending reports as email attachments as well. This can be practical in cases where you've opted to include report information in the email body using the [Merge Tables](@DO-167) feature. This way the receiver only gets the information in one place and doesn't have to process an email attachment.

To disable sending reports as email attachments for an email template, follow these steps:

1. Choose the {{search}} icon, enter **Email Templates**, and then choose the related link.
1. Select the email template for which you want to disable sending reports as email attachments.
1. In the **Email attachments** FastTab, disable **Use reports for email attachments**.