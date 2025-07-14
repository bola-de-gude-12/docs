---
title: Moving a document to another company in Document Capture
date: 31-03-2025
description:  
id: DC-74
lang: en
---

# Moving a document to another company
When you have multiple companies set up in Microsoft Dynamics 365 Business Central, you may sometimes want to move a document in Continia Document Capture from one company to another. This could be relevant if you’ve set up Document Capture to import all documents to one particular company, or if somebody by mistake sends a document to the wrong company.

For example, some organizations ask their vendors to send all purchase invoices to the same email address, from which the organizations can then manually distribute the documents to the intended recipient companies. In such cases – and other cases requiring manual transfer – the [manual method described below](/continia-document-capture/business-functionality/documents-and-templates/moving-a-document-to-another-company#moving-documents-to-other-companies-manually) can be used.

As detailed further below, it’s also possible to have [incoming documents moved automatically](/continia-document-capture/business-functionality/documents-and-templates/moving-a-document-to-another-company#moving-documents-to-other-companies-automatically) to another company.

For app versions of Business Central, no matter which of the two methods you use, vendor and field recognition is carried out automatically for every document that's moved from one company to another.

## Moving documents to other companies manually

> [!IMPORTANT]
> For the following guide to work, you must have more than one company set up in Business Central – otherwise the **Move to Company** action isn't available. Also, Document Capture must be installed, activated, and set up correctly in all companies you want to move documents between.

To manually move a document from one company to another:
1. Search ({{search}}) for and select **Document Categories**.
1. Select the code of the relevant document category – for example, **PURCHASE** – to open the document journal.
1. In the document list, select the document you want to move. Select the document line – not the number in the **No.** column, as this opens the document card.
1. On the action bar, click **Actions > Functions > Move to Company**.
1. On the **Move to Company** page, in the **Name** column, select the name of the company you want to move the selected document to.
1. In the **Document Category Code** column, select the category code you want to move the selected document to. If the same document category exists in the destination company, the category code is automatically filled out.
1. If the document transfer is successful, a dialog box confirms that the selected document has been moved to the selected company. Select **OK** to close the dialog box and return to the document journal.

If the document transfer is unsuccessful in step 7 above, a dialog box with an error message appears instead. The reasons for this may be:
* Document Capture wasn't activated or set up correctly in the destination company. To solve this, select **OK** to close the dialog box, and then make sure that Document Capture is activated and fully functional in all relevant companies.
* The configuration of the **Import and Archive Emails** field differs between the origin and destination categories. To solve this, align the configuration of the **Import and Archive Emails** field on the respective **Document Category** pages – under the **Source Table and Fields** section.

## Moving documents to other companies automatically
As an alternative to moving documents manually, you can set up Document Capture to automatically forward incoming documents to the intended recipient companies immediately after import. In order to do so, follow these steps:

To set up automatic forwarding of documents:
1. Follow the guide in [Setting up company identification texts](@DC-443#to-set-up-company-identification-texts) to set up a number of company identification texts, that is, free-text keywords you can map to specific companies.
1. Make sure that Document Capture has been activated and set up in both of the companies you want to move documents between.
1. Search ({{search}}) for and select **Document Categories**.
1. Open the relevant document category. For example, to open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself, as this opens the document journal), and then choose **Edit** on the action bar.
1. On the **OCR Processing** FastTab, enable the **Auto Move to Company** setting.

## Related information
[Installing the Document Capture app](/Continia Document Capture/Development and Administration/Online/Installing the Document Capture app.md)  
[Setting up company identification texts](/Continia Document Capture/Setting up Document Capture/Setting up general business functionality/Setting up company identification texts.md)  