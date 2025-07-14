---
title: Combining Documents
date: 08-04-2024
description:  
id: DO-46
lang: en
---

# Combining Documents

When sending multiple documents of the same category (e.g., sales invoices) to the same customer on the same day, you can merge them into a single PDF. Instead of sending separate emails, each with only one document attached, you can merge multiple documents into a single PDF file. Doing so allows you to send just one email containing all the combined documents. This approach saves time and reduces the clutter in the recipient's inbox, making communication more efficient and user-friendly.
<br>
<br>
<iframe src="https://player.vimeo.com/video/882882315?h=9771cad014&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" title="DO Learn_1c PDF attachments"></iframe>

This video is part of the course [Get started using Document Output](https://learn.continia.com/get-started-using-document-output) on Continia Learn.

## To combine documents into one PDF

To combine documents into one PDF for an email template, follow these steps:

1. Select the {{search}} icon, enter **Email Templates**, and select the related link.
1. Open the template for which you want to combine multiple documents into one.
1. On the **General** FastTab, in the **Combine Documents** field, select **Combine to one document**.
1. In the **Combine documents** FastTab, select the three dots to the right in the field, and then select field from which the documents that will be merged into one PDF file should be found.
1. Select **OK** to close the **Field List**.
1. In the **Email Template Lines** FastTab, enter a file name for the combined PDF file in the **Combined Docs. File Name** field.

   > [!TIP]
   > To identify the document's content for the recipient, utilize merge fields in the Combined File Docs. File Name field. For instance, when sending invoices, you can create a file name such as "%10 invoices.pdf," where "%10" indicates the number of documents combined into one PDF. This naming convention enhances clarity and helps recipients understand the contents of the attached document.

### Other options in the **Combine Documents** field

Instead of combining multiple document into one PDF and attaching it to an email, you have the option of attaching the documents seperately to the same email as well as the option to create one email per attachment.

If you want to attach multiple attachments to one email, select **One email with multiple attachments** in **Combine Documents**, as described in the procedure above.

If you want to create one email per attachment, select **Disable combine** in **Combine Documents**, as described in the procedure above.

## To change the subject field on an email template

After you've gone through the procedure mentioned above of combining documents into one PDF for an email template, you may also find it useful to change the email subject on that email template to highlight that the email covers multiple documents.

1. Select the {{search}} icon, enter **Email Templates**, and select the related link.
1. Open the template for which you want to edit the subject field.
1. On the action bar in the **Email Template Lines** FastTab, select **Email Template** > **Edit HTML Template**.
1. On the **General** FastTab, go to the **Subject** field and enter the text.

   > [!TIP]
   > Using the same name in the subject field as you've used for the PDF file will make the content crystal clear to the recipient, so in the example with the sales invoices above, the subject line would be "%10 invoices".