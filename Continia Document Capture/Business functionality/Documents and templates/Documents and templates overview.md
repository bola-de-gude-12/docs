---
title: Overview of Documents and Templates
date: 24-03-2024
description:  
id: DC-120
lang: en
---

# Overview of Documents and Templates
When your documents have been imported into Continia Document Capture, you can start working with them. All documents are organized into *document categories*, and most of them make use of document *templates*. Both of these concepts – as well as the way they interact with your documents – are essential for you to understand, which is why they’re explained in the sections below, along with a few other crucial concepts.

## Document categories
All documents belong to a document category, which serves as a sort of container for all documents of a specific type. For example, all purchase invoices and credit memos belong to the document category **PURCHASE**, whereas all sales orders belong to the **SALES** category. Each document category includes a set of rules and configurations that define how to process documents within that category. This may be less relevant to you if, for example, you generally only process purchase documents – but you could still occasionally benefit from knowing that there are different types of documents and that they’re grouped into document categories.

## Templates
A template is a collection of rules and configurations that determine how documents should be captured and processed. All templates are associated with a document category, and each template is linked to a specific vendor. Templates can be linked to other entities than vendors, but this article will focus exclusively on vendors, for illustrative purposes. In the template, you determine what information and which fields should be captured whenever you receive a document from a specific vendor. As each vendor has a unique template, you can use templates for capturing different information or for applying different rules and configurations for each vendor.

Templates usually have one or more template fields, which are the fields that you want to capture in a document. For example, purchase-related templates typically include template fields such as **Invoice No.**, **Posting Date**, **Due Date**, **Currency**, and **Amount**. For each template field, you can set up different rules and checks to be implemented whenever information is captured for that specific field. For example, you may want to set up a rule to ensure that all invoices contain an order number, or that you only receive invoices in a particular currency from a particular vendor.

Document Capture includes a configuration that sets up all base templates, meaning that you don’t have to configure everything from scratch. You only need to make changes to a template or to any of the template fields if you want to change how information is captured in documents from specific vendors, or if you’d like to capture additional information in documents.

## Documents
Documents are the actual entities that are processed and stored in Document Capture, such as purchase invoices and credit memos. When you import a document, Document Capture will identify the source of that document (for example, the vendor that sent it) and link it to the specific template associated with that source. Once a source has been identified (or manually assigned) and its associated template has been applied, all relevant information in the document is automatically captured, and the document is processed according to the rules and configuration of the applied template. 

| To | See |
| --- | --- |
| Import documents into Document Capture and get an overview of the various methods | [Importing Documents](Importing documents.md) |
| Learn how to OCR-process documents and gain insights into the OCR process | [OCR-Processing a Document](OCR-processing a document.md) |
| Understand the ins and outs of the document journal, assign new vendors to documents, or view only specific types of documents | [Working with Paper and PDF Documents](Working with paper and PDF documents.md) |
| Identify or change header field captions, capture header field values, and add or remove template fields | [Capturing Header Fields in a Document](@DC-110) |
| Identify or change line field captions and capture line field values (line recognition) | [Capturing Line Fields in a Document (Line Recognition)](@DC-147) |
| Learn about and use enhanced line recognition, including advanced AI capabilities | [Enhanced Line Recognition](@DC-191) |
| Translate captured **Our Contact** values into purchaser codes for correct registration | [Purchaser Code Translation](@DC-128) |
| Register documents in order to make them available as real business entities in Microsoft Dynamics 365 Business Central | [Registering Documents](Registering documents.md) |
| Have item charges automatically assigned to the lines of incoming documents according to predefined methods | [Automatic Assignment of Item Charges](@DC-137) |
| Reopen documents, for instance to match them again, to correct errors, or if they were mistakenly rejected | [Reopening Documents](Reopening documents.md) |
| Reject documents, thereby dismissing them but retaining them in the database (as opposed to deleting them entirely) | [Rejecting Documents](Rejecting documents.md) |
| Split files into multiple separate documents (either manually or automatically) or manually merge separate files into one single document | [Splitting and Merging Documents](Splitting and merging documents.md) |
| Move documents to other companies, either manually or automatically | [Moving a Document to Another Company](Moving a document to another company.md) |
| Familiarize yourself with the process of template identification | [Finding the Document Source and Template](Finding the document source and template.md) |
| Create and set up new template fields | [Setting up New Template Fields](Setting up new template fields.md) |
| Add captions suggested by Document Capture to PDF master templates | [Adding Captions to PDF Master Templates](@DC-117) |
| Learn the various ways of accessing the document archive | [Accessing the Document Archive](Accessing the document archive.md) |
| Configure comments and learn about comment types | [Configuring Comment Types and Importance](@DC-72) |


## Related information
[Importing Documents](Importing documents.md)  
[Working with Paper and PDF Documents](Working with paper and PDF documents.md)  
[Registering Documents](Registering documents.md)  
[Reopening Documents](Reopening documents.md)  
[Rejecting Documents](Rejecting documents.md)  
[Splitting and Merging Documents](Splitting and merging documents.md)  
[Moving a Document to Another Company](Moving a document to another company.md)  
[Finding the Document Source and Template](Finding the document source and template.md)  
[Setting up New Template Fields](Setting up new template fields.md)  
[OCR-Processing a Document](OCR-processing a document.md)  