---
title: Importing documents in Document Capture
date: 09-05-2025
description: How to import documents into Document Capture.
id: DC-82
lang: en
---

# Importing documents
Before you can start working with documents in Continia Document Capture, the documents must be imported into the system. This article describes the many ways in which this can be done.

>[!NOTE]
>When a document is imported, its original filename is kept. A unique identifier is also added to it, ensuring that the original document is kept as is and won't be overwritten – even if the same document is imported multiple times.

## Via email
You can import documents into Document Capture by attaching them as PDF or XML files to an email and then sending that email to a dedicated email address monitored by Document Capture. There are different document categories in Document Capture – such as **Purchase** for purchase documents and **Sales** for sales documents – and each document category has a dedicated email address, so be sure to send your documents to the right document category. You can either forward the documents you receive to the dedicated email address yourself or ask the original senders (often your vendors) to send them directly to that email address.

> [!NOTE]
> A popular choice when importing documents into Document Capture is to set up an email address in your own domain and then have all emails that are sent to this address automatically forwarded to the system-generated email address monitored by Document Capture. 

To import a document via email:
1.	In the Microsoft Dynamics 365 Business Central Role Center, under **Continia Document Capture Activities**, go to **Actions** and select **Submit Document**.
1.	On the **How-to Submit Documents** page, under **Email Address**, your dedicated Document Capture addresses are displayed for each document category. Copy the relevant email address – for example the one from the **Invoices and Credit Memos** category if you want to import an invoice.
1.	Using any external email service, create an email, attach a document (in this case a purchase invoice) in PDF, and send the email to the address you copied in step 2 above. Note that the email must [meet a number of requirements](/continia-document-capture/getting-started/frequently-asked-questions/minimum-requirements/additional-guidelines#technical-email-requirements).
1.	In Business Central, close the **How-to Submit Documents** page to return to the Role Center.
1.	The document you sent is now [OCR-processed automatically by Continia](OCR-processing a document.md), and will appear in the **Continia Document Capture Activities** section of your Role Center in the **Pending OCR** cue.
1.	Once it’s been OCR-processed, the document appears in the **Ready to Import** cue. From here, you can import the document and see how many other files have been OCR-processed and are ready for import. 
1.	To import your document (along with any other OCR-processed documents), go to **Actions** and choose **Import Files**.
1.	When the import is complete, a message shows the number of files that have been imported. Select **OK**.

The document is now ready to be registered and available in the **Ready to Register** cue.

> [!NOTE]
> Files submitted for OCR processing are queued in the order they’re received in Continia Online (Cloud OCR). During peak periods, processing time may be a little longer than usual. You may want to refresh the page to find out if a file has been processed.

## Using a network scanner (multi-function printer, MFP)
Most network scanners can be set up to scan and send documents as PDF files to a predefined email address. You simply set up your scanner to send all scanned files in PDF to the email address that’s monitored by Document Capture, as described above. No additional configuration is required, as Document Capture automatically reads all incoming emails and their attachments as outlined in the above section.

## Using a desktop scanner
Document Capture supports the scanning of documents using a desktop scanner connected directly to each end user’s PC. Document Capture can communicate with the scanner and start the scanning directly from Microsoft Dynamics 365 Business Central. To learn more about how to connect desktop scanners, see [Connecting a Desktop Scanner](/Continia Document Capture/Setting up Document Capture/Setting up general business functionality/Connecting a desktop scanner.md).

Once you’ve connected your desktop scanner, you can scan documents by following these steps:
1. Place the document that you want to scan onto the scanner glass, or load it into the document feeder, depending on your type of scanner. Follow any other relevant instructions provided by your scanner manufacturer.
1. In Business Central, choose the {{search}}  icon, enter **Scanning & OCR**, and then choose the related link.
1. In the **Scanning & OCR** window that opens, go to **Scanner** and select your scanner in the box.
1. On the action bar, click **Scan** to scan the document.

## Via the Continia Delivery Network
The Continia Delivery Network connects you to networks such as the global Peppol eDelivery Network and the Danish NemHandel, which enables you to import electronic documents directly into Business Central. For more information, see [Understanding the Continia Delivery Network](@DC-53).

## Related information
[Technical email requirements](/continia-document-capture/getting-started/frequently-asked-questions/minimum-requirements/additional-guidelines#technical-email-requirements)  
[OCR-processing a document](OCR-processing a document.md)  
[Connecting a desktop scanner](/Continia Document Capture/Setting up Document Capture/Setting up general business functionality/Connecting a desktop scanner.md)  
[Understanding the Continia Delivery Network](@DC-53)  