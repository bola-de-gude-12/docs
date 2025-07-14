---
title: Output Profiles
date: 27-06-2025
description:  
id: DO-74
lang: en
---

# Output Profiles

An Output Profile defines how Document Output sends documents to a specific customer or vendor. In the Document Output FactBox, which is attached to all customers and vendors, you can see how Document Output will distribute documents for that customer/vendor. Each customer/vendor can only have one Output Profile.

As default it's possible to select **Print**, **Email**, or **Peppol** as distribution method. If this field has no value, Document Output will ignore documents intended for this vendor or customer
<br>
<br>
<iframe src="https://player.vimeo.com/video/888005565?h=d939a24702&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" title="DO Learn_2b Output Profiles"></iframe>

This video is part of the course [Get started using Document Output](https://learn.continia.com/get-started-using-document-output) on Continia Learn.

> [!NOTE]
> From Document Output version 2024 R2, the Output Profile has been added directly to the posted Business Central document. The process of using the actual posted value began with the introduction of the Handled(DO) monitoring field, but until December 2024 it was still possible to override the posted Output Profile value by changing the Output Profile on the Document Output customer card. This is no longer possible.
> 
> The value configured on the Document Output customer card is automatically retrieved and inserted into the draft documents that’s created but only before posting. If a document is posted with a empty value in an Output Profile, and a value is configured on the customer, there is now a fallback solution where the configured Output Profile is used.

## To create an Output Profile

You can create your own Output Profiles, or edit existing ones of course, to suit the needs of your organization, and this process is described below. You could, for example, create an Output Profile that won't send emails or electronic invoices but will send PDF files directly to a printer in addition to the existing Output Profiles.

To create a new Output Profile, follow these steps:

1. Choose the {{search}} icon, enter **Output Profile**, and then choose the related link.
1. In the action bar, select **New**.
1. Fill out the fields as necessary. **Profile Code** is mandatory, but the rest are optional. Below you'll find an explanation of the most important fields.

### Important fields in Output Profiles

There are a number of important fields when you create or edit an Output Profile, and below  you'll find a description of them so you can set up profiles in the exact manner you want to. 

* **Profile Code**: Defines the **Send Code**. It is possible to have identical profile codes if they are combined with different setup options in the **Template** field.

* **Template**: If this field is left empty, it means that this profile code defaults all enabled Templates. If the only value in the field is **Statement**, it will only apply when statements are sent.

* **Email**: If this field has a value other than **Skip**, the email template will be used and emails will be generated and sent. **PDF** means that emails will be generated, and a PDF, based on the report selection in the designated email template, will be attached to the email. **XML(e-doc)**, will generate an XML file and attach this as well. This requires that another field (**E-Document Setup Code**) is defined to determine the XML format that will be generated. If **Email** is configured with **PDF** and **XML(e-doc)**, two files will be attached to the email: A PDF file based on the report selection in the email template and an XML file based on the format that's been selected in **E-Document Setup Code**.

* **E-Document Setup Code**: This field defines the type of XML file that will be generated for electronic invoicing. The available format types may vary depending on the country the XML is intended for. **E-Document Setup Code** refers to another setup page, **E-Document Setup**, which is configured with the Codeunits for generating the XML files and also configuration of export file folders or link to the Continia Delivery Network through which electronic document are sent.

The rest of the setup fields are configuration fields that are used in connection with special setups required for supporting the ZUGFeRD/Factur-x formats.

## To exclude recipients with no Output Profile from being serviced by Document Output

Instead of having to create and apply an Output Profile with *Skip* as the only setting, the option to exclude recipients with no Output Profile from being serviced by Document Output can be found in the **Document Output Setup** in the form of a toggle.

If you wish to exclude recipients with no Output Profile from being serviced by Document Output, here's how you do it:

1. Choose the {{search}} icon, enter **Document Output Setup**, and then choose the related link.
1. In the **General** FastTab, toggle the switch **Skip Email if no Output Profile** to enable/disable the feature as desired.

## To embed files in XML documents
You have the option of embedding the PDF version of a document – such as an invoice or a credit note – and/or files attached to such documents in an XML file. This way the receiver may extract the PDF version for easy viewing and archiving or extract any other file embedded in the XML. In Document Output, you can do this using output profiles and email templates.

To embed a report PDF and/or file attachments in an XML file, follow these steps:

1. Choose the {{search}} icon, enter **Output Profiles**, and then choose the related link.
1. In the **Embed Documents in eDocument** column, select one of the following:
   * **Report** (for PDF reports)
   * **Attachments** (for any of the files filtered from the Business Central document record)
   * **Both** (for a combination of the two options above)
   
   You must make this selection for each individual output profile line.

> [!NOTE]
> If **Attachments** or **Both** is selected, you must activate **Include Document Attachments** and/or **Include Document Line Attachments** in the corresponding template. If **Report** is selected, the corresponding template must be set up to generate the correct PDF file.