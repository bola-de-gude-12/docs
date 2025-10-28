---
title: Setting up document categories and templates in Document Capture
date: 25-09-2025
description: An overview of document category and template functionality.
id: DC-473
lang: en
---

# Setting up document categories and templates
All documents belong to a document category, which serves as a sort of container for all documents of a specific type. For example, all purchase invoices and credit memos belong to the document category **PURCHASE**, whereas all sales orders belong to the **SALES** category.

Within each document category you can have one or more templates, and each template includes a number of rules and configurations that determine how documents should be captured and processed. There are different types of templates used for different purposes, including templates for identifying document sources (for example, vendor) and templates specifying how to capture and process documents.

Continia Document Capture comes with a default configuration that sets up a number of document categories, including categories for handling purchase and sales documents. These categories are ready to use, but you can adjust them to your liking if you have specific needs or requirements. You can also create categories if you want to process certain types of documents.

| To | See |
| --- | --- |
| Learn about working with document categories and using settings to match your needs | [Working with document categories](@DC-78) |
| Configure which fields should be used when finding the document source (e.g.: vendor) | [Setting up identification fields](@DC-81) |
| Understand identification templates and how they’re used to identify the document source (e.g.: vendor) | [Understanding identification templates](@DC-471) |
| Customize the way incoming documents are OCR-processed | [Configuring advanced OCR options](@DC-472) |
| Register incoming documents as lines in a general journal | [Setting up the registration of documents as general journal lines](@DC-112) |
| View embedded PDF attachments rather than original XML files in the document journal | [Enabling the document viewer to display embedded PDF files (XML)](@DC-144) |
| Check if the captured data in incoming documents matches the data from the vendors who sent the documents | [Setting up fraud checks](@DC-213) |