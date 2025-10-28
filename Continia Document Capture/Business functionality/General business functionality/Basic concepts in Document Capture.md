---
title: Basic concepts in Document Capture
date: 03-10-2025
description: A description of the essential concepts in Document Capture.
id: DC-83
lang: en
---

# Basic concepts in Document Capture
Working with Continia Document Capture is generally straightforward, but it does involve a number of essential concepts that are important for you to understand. This article explains these concepts.

## What’s a document, and how do I process it?
A document is a scanned paper document, a PDF file, or an XML file that’s imported into Document Capture. It can be any type of document, such as a purchase invoice, a sales order, a contract, an item certificate, a bill of lading, a customer statement, or virtually anything else.

Once a document has been imported into Document Capture, you can capture textual information in it and start working with it. The information you need to capture depends on the specific type of document, but no matter what types of documents you’re dealing with, you handle and process them in the same place – the document journal.

The main purpose of the document journal is to enable you to work with imported documents and capture textual information contained in these documents. Once the information has been captured in the document journal, you must register the document. By registering a document, you convert all captured information into a real business entity in Microsoft Dynamics 365 Business Central. For example, when you register a purchase invoice received from a vendor, you create a Business Central purchase invoice.

The process can be outlined as follows:

1. The document is scanned or sent to Document Capture and OCR-processed.
1. The document is imported into the document journal.
1. Information is captured.
1. The document is registered.
1. A Business Central purchase invoice is created.

## Importing documents into Document Capture 
Before you can start working with documents in Document Capture, the documents must be imported into the system. There are several different ways of doing this.

* **Via email** - import documents by attaching them as PDF or XML files to an email, and then sending that email to a dedicated email address monitored by Document Capture. There’s an email address for each document category within Document Capture, so be sure to send your documents to the right one. You can either forward the documents you receive to the dedicated email address or ask the original senders (e.g.: your vendors) to send them directly to it. To learn more, see [Importing documents](@DC-82).
* **Using a network scanner** - most network scanners can be set up to scan and send documents as PDF files to a predefined email address. You can then send all scanned files in PDF to the email address monitored by Document Capture, as described above. No additional configuration is required, as Document Capture automatically reads all incoming emails and their attachments.
* **Using a desktop scanner** - Document Capture can communicate with a desktop scanner connected directly to each end user’s PC and start the scanning directly from Business Central. To learn more about how to connect desktop scanners, see [Connecting a desktop scanner](@DC-119). For more information about scanners in general, see [Using a desktop scanner](@DC-82#using-a-desktop-scanner).
* **Via the Continia Delivery Network** - the Continia Delivery Network connects you to the global Peppol eDelivery Network and to the Danish NemHandel network, which enables you to import eDocuments directly into Business Central. To learn more, see [Understanding the Continia Delivery Network](@DC-53).

## Working with documents 
When your documents have been imported into Document Capture, you can start working with them. All documents are organized into document categories, and most of them make use of document templates. Both of these concepts are essential for you to understand.

* **Document categories** - document categories serve as a sort of container for all documents of a specific type. For example, all purchase invoices and credit memos belong to the document category **PURCHASE**, whereas all sales orders belong to the **SALES** category. Each document category includes a set of rules and configurations that define how to process documents within that category. To learn more, see [Working with document categories](@DC-78).
* **Templates** - a template is a collection of rules and configurations that determine how documents should be captured and processed. All templates are associated with a document category, and each template is linked to a specific vendor. Templates can be linked to other entities than vendors, but this article focuses exclusively on vendors, for illustrative purposes. In the template, you determine what information and which fields should be captured when you receive a document from a specific vendor. As each vendor has a unique template, you can use templates for capturing different information or for applying different rules and configurations for each vendor. For more information, see [Overview of documents and templates](@DC-120).
* **Documents** - documents are the actual entities processed and stored in Document Capture, such as purchase invoices and credit memos. When you import a document, Document Capture identifies the source of that document (e.g.: the vendor that sent it) and link it to the specific template associated with that source. Once a source has been identified (or manually assigned) and its associated template has been applied, all relevant information in the document is automatically captured – and the document is processed according to the rules and configuration of the applied template. To learn more, see [Overview of documents and templates](@DC-120).
* **Document journal** - the document journal is where you process imported documents and capture the textual information that’s contained within them. What information to capture depends on the type of document you’re dealing with, and you can define the exact rules in templates. Capturing allows you to register the documents and convert them into actual business entities in Business Central. For more information, see [Working with paper and PDF documents](@DC-71).
* **Document card** - the difference between the document journal and the document card is that the document card allows you to capture document lines, which isn’t possible in the document journal. To learn more, see [Working with paper and PDF documents](@DC-71).

## Matching purchase documents 
You may be using Business Central’s functionality for purchase orders and return orders. If so, it’s important that purchase invoices and credit memos are linked to these types of documents when processed. Document Capture has been built with a focus on doing this as efficiently as possible. To learn more, see [Overview of order and receipt matching](@DC-61).

## Approving purchase documents 
The majority of companies prefer having their purchase invoices and credit memos approved before posting them and paying their vendors. Document Capture offers a streamlined workflow that meets the needs of most companies. For more information, see [Overview of purchase approval](@DC-34).

## Document archive 
When a document has been imported and processed, it’s automatically stored in the document archive. Here you can access it – along with all other processed documents – whenever you want, for as long as you want. To learn more, see [Accessing the Document Archive](@DC-390).
