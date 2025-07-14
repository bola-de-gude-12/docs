---
title: Setting a Background PDF
date: 25-06-2025
description:  
id: DO-45
lang: en
---

# Setting a Background PDF

Utilizing background PDF files is a straightforward method to personalize the generated PDF attachments within your email templates. This lets you incorporate company-specific information, like logos or watermarks, into the PDF files. When you set a background PDF, the chosen file will be integrated into the generated report's PDF as a layer positioned behind the report text. This allows you to create professional and branded PDF documents that carry your company's unique identity when sent through email templates.
<br>
<br>
<iframe src="https://player.vimeo.com/video/882882315?h=9771cad014&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" title="DO Learn_1c PDF attachments"></iframe>

This video is part of the course [Get started using Document Output](https://learn.continia.com/get-started-using-document-output) on Continia Learn.

## Set a background PDF for an email template line:

To set a background PDF for an email template line, follow these steps:

1. Select the {{search}} icon, enter **Email Templates**, and select the related link.
1. Select the email template to which you want to add a background PDF. The email template card opens.
1. On the **Email Template Lines** FastTab, in the action bar, select one of the following options:

   * **First Page Background PDF** – only applies to the first page of the generated PDF file.

   * **Last Page Background PDF** – only applies to the last page of the generated PDF file.

   * **Background PDF** – applies to all pages of the generated PDF file and the first and last pages if they haven't been specified separately.

     > [!IMPORTANT]
     > To ensure proper integration of the background document, it is crucial to verify that its size matches the dimensions used in the report. 
1. Select a PDF to use as background. To quickly identify which background PDF features are enabled for each email template line, use the checkboxes provided on each line. These checkboxes indicate the specific background PDF options configured for that email template.

   > [!NOTE]
   > For single-page reports, you can specify to use the first-page background PDF or the last-page background PDF. However, note that these options won't take effect until you've uploaded a general background PDF in step 3 above (**Background PDF** > **Set Background PDF**).

## Using the background PDF functionality and other PDF features at the same time

When you use Merge PDF while also using the background PDF functionality, keep in mind that the merged PDF will *not* have its background PDF modified. If you want to maintain a consistent look across both the report PDF and the merged PDF, it's necessary to add that look to the merged PDF prior to uploading it.

Also bear in mind that ”Last-page background PDF” might need to be disabled and that the content of it should be manually added to the last page of the merged PDF.

In the event that the combine functionality is used to create a single PDF file containing multiple documents, the distinction between first-page background, last-page background and default background will not be taken into consideration. Each document will have its background modified as if they were single files.

## See also
[Password Protecting PDF Files](@DO-35)