---
title: Splitting and merging documents in Document Capture
date: 15-10-2025
description: How to split and merge documents, be it automatically or manually.
id: DC-80
lang: en
---

# Splitting and merging documents

Some of the files you scan or receive may consist of multiple documents combined into a single file. For example, a vendor may send you one PDF file containing multiple purchase invoices. In such cases, you can split the PDF file into multiple separate documents in Continia Document Capture.

Likewise, you can merge two or more separate PDF files into one single document. This is necessary when you receive an invoice with sales conditions or other attachments that belong to the invoice, for example. Document Capture can merge these attachments with the invoice, so no loose documents are left in the document journal.

> [!NOTE]
> By splitting and merging PDF documents, you manipulate the original documents. If an original document contains a vendor certificate, this is invalidated the moment the original document is either split into multiple smaller documents or merged with other documents.

## Splitting documents manually
To split a document manually:
1. Search ({{search}}) for and select **Document Categories**.
1. Click the code of the relevant document category – for example, **PURCHASE** – to open the document journal.
1. On the action bar, click **Document** and then **Split and Merge**.
1. In the list of documents, select the document that you want to split and the page from where you would like to split the document. Note that you can’t select the first page of the document as the splitting page.
1. On the action bar, click **Split**. The document will now be split into two, and the page you selected in step 3 above will become the first page of the new document.

Note that the new document is provided with a new document number, which is displayed under **Document No.** in the list.

> [!NOTE]
> Only documents with multiple pages can be split. You can’t split up single pages.

## Splitting documents automatically
You can also have documents split automatically by changing the settings of the purchase document category. To do this:
1. Search ({{search}}) for and select **Document Categories**.
1. Open the relevant document category. For example, to open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself, as this opens the document journal), then click **Edit** on the action bar.
1. On the **OCR Processing** FastTab, go to the **Split PDF Documents** section and enable the **Automatically** setting. Several additional options appear, as detailed in the table below.

The following additional options allow you to specify how you want your documents to be split.

<table>
  <thead>
    <tr>
      <th>Option</th>
      <th>Definition</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Blank Page</strong></td>
      <td>Splits any incoming document when a blank page is identified in the document. A blank page is defined as a page with fewer than 40 characters.</td>
    </tr>
    <tr>
      <td><strong>Source ID</strong></td>
      <td>Splits incoming documents when a source ID is identified in a document. The source ID is whatever you select under <strong>Source Table and Fields</strong> on the <strong>Document Category</strong> page, in the fields <strong>Table</strong> and <strong>Primary Key Field</strong>. For purchase invoices, the default source ID is the vendor number, meaning that Document Capture splits incoming documents when a new vendor is identified.</td>
    </tr>
    <tr>
      <td><strong>Separator Fields</strong></td>
      <td>Splits incoming documents when a separator field is identified. You can define your own separator fields as follows:
        <ol>
          <li>On the <strong>Document Category</strong> page, under <strong>Templates</strong>, select the relevant template line, click the three dots (...), and select <strong>Edit</strong>.</li>
          <li>Under <strong>Fields</strong>, select the field that you want to use as a separator field.</li>
          <li>On the <strong>Template Field Card</strong>, under <strong>General</strong>, select <strong>Use as Document Separator</strong>.</li>
        </ol>
        <p>Note that a default separator field may have been assigned already. For purchase invoices, the default separator field is the invoice number, meaning that Document Capture will split incoming documents whenever the value in the invoice number field changes. Also, note that the <strong>Source ID</strong> option is mandatory and automatically enabled when you enable <strong>Separator Fields</strong>.</p>
      </td>
    </tr>
    <tr>
      <td><strong>Barcode</strong></td>
      <td>Splits incoming documents when a barcode or a QR code is identified. Note that this option is closely related to the optional <strong>Barcode Text</strong> field immediately below it in the user interface, provided that you fill out the <strong>Barcode Text</strong> field (see below).</td>
    </tr>
    <tr>
      <td><strong>Barcode Text</strong></td>
      <td>Splits incoming documents when a barcode or QR code containing this particular text is identified, provided that the <strong>Barcode</strong> option is enabled and that you've entered a specific text in the <strong>Barcode Text</strong> field.
        <p>You can also use special symbols/characters known as <em>operators</em> to specify the splitting value, for example as follows:</p>
        <ul>
          <li><strong>DK\*</strong> splits incoming documents when a barcode/QR code starts with DK.</li>
          <li><strong>SHIP\*&\*2020</strong> splits incoming documents when a barcode/QR code starts with SHIP and ends with 2020.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>



## Merging documents manually
To merge a document manually:
1. Search ({{search}}) for and select **Document Categories**.
1. Click the code of the relevant document category – for example, **PURCHASE** – to open the document journal.
1. On the action bar, click **Document** > **Split and Merge**.
1. In the list of documents, select the documents that you want to merge. On a computer, you can select multiple documents by pressing Shift+Click.<a href="#footnote-1"><sup>1</sup></a>
1. Once you’ve selected the documents that should be merged, click **Merge** on the action bar. The documents are merged into one, and the constituent documents are renamed as follows in the **Name** column: The first page of the merged document is either renamed Page 1 or named after the vendor, while all following pages are named by page number, such as Page 2, Page 3, and so on.
1. **Optional**: You can reorder the pages of the merged document using the **Move Up** and **Move Down** options on the action bar.<a href="#footnote-2"><sup>2</sup></a>

## Merging documents automatically
You can also have documents merge automatically by changing the settings of the template card. To do this:
1. Search ({{search}}) for and select **Document Categories**.
1. Click the code of the relevant document category – for example, **PURCHASE** – to open the document journal.
1. On the action bar, click **Template** > **Template Card** to open the template card.
1. On the **General** FastTab, enable the setting **Merge from same Email**.

   >[!NOTE]
   >As it's possible to attach invoices from multiple vendors to a single email, Document Capture must be able to identify the vendor in each document in order to merge them effectively.

   >[!IMPORTANT]
   >**Merge from same Email** only works when you import all files at once via the **Import files** action on the Role Center. If you attempt to merge multiple files by clicking the **Ready to Import** cue and picking the desired files on the **Scanning & OCR** page, the import results in multiple documents.

<small style>

<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1">The documents to be merged must be arranged in sequence. For example, documents 1, 2, 3, and 4 on the list can be merged, but documents 1 and 4 can’t.</li>
    <li id="footnote-2">The <b>Move Up</b> and <b>Move Down</b> options can only be used to move pages within a document. Separate documents can’t be moved up and down the list using this feature.</li>    
  </ol>
</div>
</small>