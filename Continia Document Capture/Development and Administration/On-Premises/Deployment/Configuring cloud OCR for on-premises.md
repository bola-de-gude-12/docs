---
title: Configuring Cloud OCR for NAV or Business Central on-premises
date: 22-04-2024
description:  
id: DC-141
lang: en
---

# Configuring Cloud OCR for NAV or Business Central on-premises
Optical character recognition (OCR) is the process of extracting the textual content of a scanned image or PDF file and converting it into something that can be processed by a computer.

If you’re using Microsoft Dynamics 365 Business Central online, your default OCR method is Continia Cloud OCR, which means that no additional configuration is required.

However, if you’re using Microsoft Dynamics NAV/Business Central on-premises, you can choose to use either on-premises OCR or Continia Cloud OCR. Continia Cloud OCR is described in detail below, whereas you can find an in-depth description of the on-premises method in the article [Configuring On-Premises OCR](Configuring on-premises OCR/Configuring on-premises OCR.md).

##Setting up Continia Cloud OCR for NAV/Business Central on-premises
When you use Continia Cloud OCR, Continia will provide you with a system-generated dedicated email address that you must send or scan documents to in order to import them into Continia Document Capture. That address will look something like this: <xyz.2342341@continiaonline.com>.

Obviously, this is not an email address that’s easy to remember, or one that you’re likely to share with your vendors to enable them to send documents directly into Document Capture. We therefore recommend that you use your own email service to create another email address instead, and then have all emails that are sent to this address forwarded to the Continia email address. For example, all emails sent to <invoice@company.com> should be forwarded to <xyz.2342341@continiaonline.com>. In this way, you get an easy-to-remember email address that you can also ask your vendors to use for submitting purchase invoices and credit memos.

> [!NOTE]
> Before you get started on the setup process below, check that you’ve signed up for Continia Cloud OCR. Also, please ensure that you’ve run the **Document Capture Setup Wizard**.

To set up Continia Cloud OCR for NAV/Business Central on-premises, follow these steps:

1. Search ({{search}}) for and select **Document Capture Setup**.
1. On the **Document Capture Setup** page, on the **General** FastTab, enable **Use Cloud OCR** by checking the box.<a href="#footnote-1"><sup>1</sup></a>
1. A dialog box appears, asking you if you want to export all document categories to Cloud OCR. Choose **Yes**.
1. Optional (recommended): Using your own email service, set up a local email address with your own domain and have all incoming emails forwarded to the dedicated Continia Cloud OCR email address. Share the new local email address with the companies that send you documents for OCR processing in Document Capture.

<small style>
<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1">When using Continia Cloud OCR, you don’t have to install the Document Capture service or the ABBYY service.</li>
  </ol>
</div>
</small>

> [!NOTE]
> To find your dedicated Continia Cloud OCR email address, search ({{search}}) for and select **Document Categories**. Under **Email (Continia Cloud OCR)**, your dedicated Cloud OCR addresses are displayed for each document category. You should create one local email address for each relevant document category.

## Related information
[Configuring On-Premises OCR](Configuring on-premises OCR/Configuring on-premises OCR.md)  
[Setting up Document Capture](/Continia Document Capture/Setting up Document Capture/Setting up Document Capture.md)  