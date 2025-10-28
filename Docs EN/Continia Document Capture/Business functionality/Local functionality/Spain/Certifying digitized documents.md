---
title: Certifying digitized documents in Document Capture
date: 15-10-2025
description: How to digitally certify purchase invoices in compliance with Spanish regulations.
id: DC-441
lang: en
---

# Certifying digitized documents

This article describes how Continia Document Capture helps you comply with the Order EHA/962/2007 by the Spanish Ministry of Economy and Finance, which establishes regulations for electronic invoicing and the electronic storage of invoices.

Digital documents must meet specific standards to be considered valid for tax purposes in Spain. When you import a PDF file using Document Capture, the file automatically receives a hash value (that is, a digital fingerprint) that can be used to verify its integrity.

A similar certification process applies when exporting purchase invoices from Document Capture using the **Export Purchase Invoices** functionality, which is described below.

## To digitally certify purchase invoices

To export purchase invoices into a digitally certified XML file:

1. Search ({{search}}) for and select **Export Purchase Invoices**.
1. Enter the desired filename for the exported invoices in **Export File Path**. By default, the filename is Invoices.xml. 
1. Fill out the **Posting Date** filter, along with any other desired filters, to narrow down the scope of the exported invoices.
1. Click **OK** to export immediately, or click **Schedule** to define a later time.
1. The exported XML file is generated and automatically downloaded.
