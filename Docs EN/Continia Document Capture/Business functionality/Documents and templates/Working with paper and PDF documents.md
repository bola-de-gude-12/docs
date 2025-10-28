---
title: Working with paper and PDF documents in Document Capture
date: 13-10-2025
description: How to process and register paper and PDF documents using the document journal and viewer.
id: DC-71
lang: en
---

# Working with paper and PDF documents

Once a document has been imported into Continia Document Capture, whether as a PDF file or as a scanned paper document, you can [capture textual information in it](@DC-110) and start working with it. The information you need to capture depends on the specific type of document, but no matter what types of documents you’re dealing with, you handle and process them in the same place – the document journal.

The main purpose of the document journal is to enable you to work with imported documents and capture textual information contained in these documents. Once the information has been captured in the document journal, you must register the document. By registering a document, you convert all captured information into a real business entity in Microsoft Dynamics 365 Business Central. For example, when you register a purchase invoice received from a vendor, you create a Business Central purchase invoice.

> [!IMPORTANT]
> You can configure Document Capture to work with many types of documents that are related to different records or entities in Business Central. Typically, Document Capture is used to process purchase invoices and credit memos, but it can also be used for processing sales orders, contracts, item certificates, and many other types of documents. When you process purchase invoices and credit memos, the documents are linked to vendors. For illustrative purposes, this article focuses exclusively on vendors, but it might as well have been customers, items, fixed assets, or something else. 

## Overview of the document journal
To access the document journal:

1. Search ({{search}}) for and select **Document Categories**.
1. Click the code of the relevant document category – in this case **PURCHASE** – to open the document journal.

The document journal consists of four main sections:

* **Document list (left-hand side)** - lists all documents included in the selected journal. For each document, the table provides you with information such as the document number, the vendor name, the template used, and the number of pages. In addition, the **OK** field indicates if the document is valid and ready to be registered.

* **Document Header (left-hand side)** - lists all fields that have been identified in the currently selected document, along with their corresponding values. The list of fields is determined by the document template, and for each field Document Capture indicates if the value is considered to be valid according to the configuration of each template field.

   > [!NOTE]
   > For a document to be registered, all document header fields must have check marks in the **OK** column. When all document header fields are OK, the document as a whole is also marked as OK in the document list.
   > 
   > Note that **No.** is mandatory for document registration and often has to be entered manually, as it can’t be captured in imported documents. This field is closely related to the **Type** field above, which determines the account type for the document. If you select no account type, **No.** defaults to G/L accounts.

* **Comments (left-hand side)** - displays comments related to the selected document. The three different types of comments are **Information**, **Warning**, and **Error**. To learn more, see [Configuring comment types and importance](@DC-72).

* **Document viewer (right-hand side)** - shows a visual representation of the actual scanned document (a PDF or XML) after it has been OCR-processed. For more information, see [The document viewer](#the-document-viewer) below.

   >[!TIP]
   >If you don't see the document viewer, click the information icon in the top right corner of the action bar.

## The document viewer

The document viewer displays PDF or XML documents that have been scanned, imported, and OCR-processed by Document Capture. For PDF documents, the document image is interactive, meaning that you can manually select text anywhere in the image to capture it as a value associated with a certain field. To learn more, see [Capturing fields in a document](@DC-110).

> [!NOTE]
> During the OCR-processing of a document, a visual representation of the document is created for display purposes, which may result in fewer colors and a lower resolution than the original document. This is done to optimize performance and usability for you when you work with the document in Business Central. What you see in the document viewer is the OCR-processed version of the document – not the original document, which may look slightly different. The actual OCR and recognition process is still performed on the original document at the highest level of detail. To learn more, see [OCR-processing a document](@DC-145).

The upper-left corner of the document viewer features a dropdown menu that allows you to view or download any files that have been attached to the document you're currently processing. The dropdown menu is also available for all other pages that include the document viewer, except for the **Documents (UIC)** page, as no documents displayed on this page have been processed yet.

Most of the attachments listed in the menu can be viewed in the user interface, but some can't (such as .xlsx and .docx files). These can be downloaded straight from the menu, though. The attachments are grouped as follows: 

* **Original** - the main document that was imported into Document Capture
* **Related documents** (OIOUBL/OIOUTS)
* **Attachments** (.bmp, .jpeg, .jpg, .pdf, .png, .tif, and .tiff)
* **XML attachments** (.bmp, .jpeg, .jpg, .pdf, .png, .tif, and .tiff)
* **Downloadable attachments** (all other file types)

If you're viewing an XML document that has an embedded PDF file, you can have this PDF file displayed in the document viewer instead of the original XML. This must first be [configured in the relevant XML master template](@DC-144). If a file in any other format than PDF has been embedded in the imported XML, it's not displayed by default. In such cases, the document viewer displays the original XML instead.

Note that you can resize the document viewer by dragging the vertical handle on the left side of the document viewer FactBox. This also applies to all other pages that include the document viewer (such as **Purchase Invoice**, **Sales Order**, **Vendor Ledger Entries**, **General Journals**, and **General Ledger Entries**).

## Changing a document’s associated vendor
By default, Document Capture links all documents to existing records in Business Central. Purchase documents are linked to vendors, meaning that each purchase document is linked to one specific vendor. In the document journal, some of the first columns of the document list – the columns **Vendor** and **Name** – show the number and the name of the vendor that each document is linked to. When importing documents, Document Capture identifies the vendor automatically based on different parameters. For more information on these parameters, see [Finding the document source and template](@DC-109).

In the event that Document Capture doesn’t manage to identify a vendor, or if you’d like to change the identified vendor, you can assign a new vendor from the document journal. To do this:

1. Search ({{search}}) for and select **Document Categories**.
1. Click the code of the relevant document category – in this case **PURCHASE** – to open the document journal.
1. In the document list, go to the line of the imported document whose vendor you want to change, and select the **Vendor** field. Then click the three dots that appear in order to open the **Vendors** window.
1. Choose the vendor that you want to assign by selecting the relevant number in the **No.** column.

> [!NOTE]
> You can also set up search texts to help Document Capture identify the correct vendor. To learn more, see [Finding the document source and template](@DC-109).

## Assigning document to users

Lorem ipsum dolor sit amet.

### To assign a specific document to a user

1. Search ({{search}}) for and select **Document Categories**.
2. Click the code of the relevant document category – in this case **PURCHASE** – to open the document journal.
3. Select the desired document and, under the **Assigned to User ID** column, select the desired user ID.

### To assign all documents from a specific vendor to a user

1. Search ({{search}}) for and select **Document Categories**.
2. Click the code of the relevant document category – in this case **PURCHASE** – to open the document journal.
3. Select the desired document and click **Template** > **Template Card**.
4. On the **General** FastTab, select the desired user ID in the **Assigned to User ID** field.

>[!NOTE]
>Assignments made via error comments take priority over this setting. For more information, see [To configure comments for all templates in a company](@DC-72).

## Changing a document’s category

To change the category of a document from the document journal:

1. Search ({{search}}) for and select **Document Categories**.
1. Click the code of the relevant document category – in this case **PURCHASE** – to open the document journal.
3. On the action bar, click **Document** > **Change Category** to open the list of categories. You can then move the document(s) to the desired category, which also results in an automatic field recognition.

Note that it's only possible to change the category of documents with the status open – that is, no rejected or registered documents. Additionally, it only works for PDFs.

The alternative to the approach described above is:

1. Search ({{search}}) for and select **Document Categories**.
2. Click the code of the relevant document category – in this case **PURCHASE** – to open the document journal.
3. Click the ({{settings}}) icon > **Personalize**.
4. In the upper-left corner, click **+ Field** to open the **Add Field to Page** pane.
5. Search for the **Document Category Code** field and drag it before or after an existing column in the document journal.
6. Click **Done** in the personalization banner.

You can now select a new value under the **Document Category Code** to change the category of the corresponding document.

## Showing registered and rejected documents
When you open the document journal, it's' filtered to show only open documents. However, you can also filter it to display documents that have been registered or rejected. To do this:

1. Search ({{search}}) for and select **Document Categories**.
1. Click the code of the relevant document category – in this case **PURCHASE** – to open the document journal.
1. In the upper-right corner, above the action bar, go to **Status Filter** and select the box to display the filter options. The default option is **Open**, meaning that only documents with the status "Open" are displayed in the document list. Change this as needed by selecting your preferred filter option.

The document list is updated to display only documents with the status you selected. If you selected **All**, all documents are displayed in the list, regardless of status.

## Related information
[Registering documents](@DC-67)  
[Working with templates](@DC-18)  
[Setting up new template fields](@DC-19)  