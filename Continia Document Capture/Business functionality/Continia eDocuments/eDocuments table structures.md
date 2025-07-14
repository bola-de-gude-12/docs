---
title: eDocuments table structures in Document Capture
date: 07-03-2025
description: A brief description of eDocuments table structures.
id: DC-181
lang: en
---

# eDocuments table structures

With Continia eDocuments, document data is saved in a structured way using a set of predefined tables. This enables Continia Document Capture to render and display the documents in the well-known formats of pages and tables, familiar to all users of Microsoft Dynamics 365 Business Central.

This means that when you either receive (i.e.: import) or send (i.e.: export) an XML file using Continia eDocuments, the file is displayed as an ordinary Business Central record with three document card sections:

* A **General** FastTab, with a number of header fields.
* A **Lines** FastTab, with an overview of all document lines displayed as a table.
* Additional document details, including FastTabs like **Order Details**, **Shipping and Payment**, **Delivery**, **Reference**, and **Technical Information**.

Instead of providing an XML file, which is generally difficult to decipher and work with, Continia eDocuments gives you a document card – formatted like any other standard Business Central document page that you can interact with. Such document cards – or records – are available for eBilling documents, eOrder documents, eBilling response documents, and eOrder response documents.

> [!NOTE]
> Every time a record is created, Continia eDocuments names it using the number series that you specified when [setting up Continia eDocuments](@DC-179).

One of the main benefits of this approach is that you can add or correct document details straight in the user interface, if a document fails validation because data is missing or incorrect. There's no need to edit complex XML files or to ask your partner to do this for you if a document fails. Instead, enter the correct or missing data in the relevant field on the document card of the document that failed validation.

Rendering XML files as standard Business Central document pages also enables you (or your partner) to add fields, or filter on specific values to find what you're looking for. In general, it allows you to use and engage with XML files in the same way as you do in Business Central with other documents.