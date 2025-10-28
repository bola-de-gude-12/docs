---
title: Finding the document source and template in Document Capture
date: 24-09-2025
description: How sources and templates are identified and linked to documents.
id: DC-109
lang: en
---

# Finding the document source and template
For all incoming documents, Continia Document Capture attempts to identify a source (such as a customer or vendor) and a template, which is then linked to each individual document. As Document Capture is a generic solution, it can basically link incoming documents to any record in Microsoft Dynamics 365 Business Central. Instead of explaining the above process in general terms, this article uses purchase documents and vendors as an illustrative basis – though this process also works with sales documents and customers.

> [!NOTE]
> You can set up Document Capture to link documents to both a vendor and a template, or to link them only to a vendor. If you only link a document to a vendor and not to a template, you're unable to capture the fields of the document – as field recognition is tied to a template. This is fine if you want to link the document to a vendor and don’t need to process any of the data in the document; or if, for example, you want to link a shipment confirmation document to a sales shipment record as proof of delivery. However, for something like purchase invoices and credit memos, you must also assign a template that defines which fields and what information should be extracted and processed in the document.

When you import a purchase document, Document Capture searches for the vendor in the four steps outlined below:

| Step | Description |
| --- | --- |
| Identification templates | Document categories such as the one for purchase documents contain an identification template that searches for one or more business identification fields in each incoming document. <br> <div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Note</span></p><p>A business identification field is a standard application field that's used for identifying the vendor that sent the document. The most commonly used field is the VAT registration number, but additional fields may apply to certain localizations (enterprise number, ABN number, and/or registration number).</p></div> If Document Capture successfully identifies a vendor, the identified vendor is applied to the document, and the vendor's associated default template is then used for capturing information in the document. You can adjust certain parts of the identification templates, such as what captions Document Capture should use when searching for values matching business identification fields. To learn more, see [Understanding identification templates](@DC-471). |
| Identification fields | For each document category, you can specify which fields in the source table (that is, the vendor table for purchase documents) you want to search for in a document in order to find the correct vendor. For example, the default Document Capture configuration sets up the document category for purchase documents to search for vendor name, address, phone number, and a number of other specific fields. When you run field recognition on a document, Document Capture searches the document for these fields and applies the identified vendor and its associated default template to the document. To learn more about setting up identification fields, see [Setting up identification fields](@DC-81). |
| Search texts | For each vendor template, you can use search texts to let Document Capture know that it should assign that specific template and its associated vendor to any document in which the specified search text appears. Normally, you use search texts if Document Capture can’t find a vendor, or if it identifies an incorrect vendor using the identification template or the identification fields search option. As an example, you could tell Document Capture to assign a specific vendor and template whenever it finds a certain bank account number or phone number in a purchase invoice. For more information, see [Setting up search texts for a template](@DC-108). <div class="alarm alarm-important"><p class="alert-title"><i class="icon icon-info"></i><span>Important</span></p><p>For documents with more than one page, note that Document Capture only searches through words on page one.</p></div> |
| AI | For each vendor template, Document Capture can automatically recognize VAT numbers using artificial intelligence (AI) and match them to the corresponding vendors. |

Each of the steps above are carried out by Document Capture in the order shown below. Note that if one of the steps succeeds in finding a vendor and a template, any subsequent steps are skipped:
1. Search texts
1. AI
1. Identification templates
1. Identification fields

> [!NOTE]
> Search texts are optional and not necessarily part of the identification process, but they’re useful when Document Capture fails to identify the correct vendor and template for a document using the other methods. In such cases, use search texts to override any vendor identified using either identification templates or identification fields.

If no matching vendor is found, click **Vendor** > **Vendor Card** to start the **Create Vendor** assisted setup guide. You can follow a similar process to create a customer based on a sales document.

## Excluding certain vendors from recognition
Some organizations set up their own company branches as vendors in Business Central, for various reasons. This may cause Document Capture to assign those vendors to many of the incoming purchase documents, as the branch name, address, VAT number, etc., appear in those documents as the recipient of the purchase documents – but not as the sender/vendor.

If you’re not using such vendors for receiving purchase invoices, you can exclude them completely from identification within a document category. For more information, see [Working with document categories](@DC-78#excluding-identification-sources).