---
title: Signing PDF files
date: 08-04-2024
description:  
id: DO-47
lang: en
---

# Signing PDF files

To add a level of security to your PDF files, it's possible to sign them using a purchased certificate. This ensures that the receiver of the PDF files can trust that the email attachments originate from the sender of the email.

With this feature, the purchased certificate is automatically used when a PDF file is generated and attached to an email.
<br>
<br>
<iframe src="https://player.vimeo.com/video/902199660?h=0574e7500a&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" title="DO Learn_3d PDF passwords and signatures"></iframe>  

This video is part of the course [Get started using Document Output](https://learn.continia.com/get-started-using-document-output) on Continia Learn.

## Set up a PDF signature for an email template

To enable PDF signature for an email template, follow these steps: 

1. Choose the {{search}} icon, enter **Email Templates**, and then choose the related link.
1. Select the email template for which you want to enable PDF signature.
1. In the action bar, select  **Template** > **Import certificate…digital signing PDF**.
1. Select the certificate file.
>  [!NOTE]
>  The certificate type must be a PKCS#12 certificate (.PFX, .P12). Continia can't offer assistance with buying certificates. You need to go through a certificate provider.
5. In the **General** FastTab, in the **PDF Sign Password** field, enter a password for the certificate file.
6. In the **General** FastTab, in the **PDF Sign Location** field, enter a text. This field is only meant as a help for your own administrative purposes and can as such have any value, but it must have a value.
7. In the **General** FastTab, in the **PDF Sign Reason** field, enter a text. This field is only meant as a help for your own administrative purposes and can as such have any value, but it must have a value.

PDF signature is now enabled for all the generated PDFs that are added to this specific email template.