---
title: Capturing Data from eDocuments
date: 23-09-2025
description:  
id: DC-182
lang: en
---

# Capturing data from eDocuments

With Continia eDocuments, more data than before is captured and made available to you for the setup and use of templates. This ensures improved source identification and extended usability of the document journal.

Previously, Continia Document Capture handled incoming XML documents through the use of XML paths. For both identification templates and source templates, XML paths have been used to specify where the various fields or lines are to be found in each incoming XML document. With Continia eDocuments, these XML paths have been replaced by eDocument tables, which provide greater flexibility across electronic formats.

For XML identification template cards, the **Fields** FastTab and its list of fields with corresponding XML paths has been replaced with a FastTab named **eDocument Source Identification**, listing a number of eDocument tables instead. And for XML source template cards, the **Invoice** and **Credit Memo** sections of the **General** FastTab have been replaced with a single **eDocuments** section, which uses header and line eDocument tables instead of XML paths to identify and capture data.

> [!NOTE]
> To understand how identification templates work for Continia eDocuments, see [Source identification](#source-identification) and [To view or edit an XML identification template](#to-view-or-edit-an-xml-identification-template) below.
> 
> To learn about source templates and how to customize them, see [Field mapping and detail pages for source template header fields](#field-mapping-and-detail-pages-for-source-template-header-fields) and [To map fields and set up detail pages](#to-map-fields-and-set-up-detail-pages) below.

## Source identification

XML identification templates are used for party identification, also known as source identification – that is, to identify the customer or vendor. To optimize their ability to do so, Continia eDocuments has equipped these templates with a new feature, accessible from the template card of each identification template, on the **eDocument Source Identification** FastTab.

This allows you to use more identification parameters and to customize these to fit your needs and wants. For each identification parameter, you can choose between a large number of different eDocument tables, between various fields from each table, and between all fields relating to the vendor/customer. This means that you can specify how you want Continia eDocuments to identify the vendor/customer and exactly what fields it should search for in incoming documents to do so.

A number of typical eDocument table field locations for global location numbers (GLNs) and VAT registration numbers have been set up by default. You can view or edit these by following the guide under [To view or edit an XML identification template](#to-view-or-edit-an-xml-identification-template).

## To view or edit an XML identification template

To view or edit an XML identification template:

1. Search ({{search}}) for and select **Document Categories**.
1. Open the relevant document category – such as **PURCHASE** – by selecting the category line (not the code itself) and then clicking **Edit** on the action bar.
1. On the **Templates** FastTab, in the list of templates, select the XML identification template you want to view or edit (such as **EBILLING-ID**), and then click **Edit** to open the template card.
1. On the **eDocument Source Identification** FastTab, you can see the default identification parameter setup. You can edit this as follows:
   * To add an identification parameter, click **New Line** on the FastTab title bar, or select the empty line at the bottom of the list, and then fill out the table fields in each column as needed.
   * To delete an identification parameter, click **Delete Line** on the FastTab title bar.
   * To edit an existing identification parameter, select the table field that you want to edit, and then click the three dots on the right side of the field to open an **Objects**/**Fields Lookup** page. From this page, select the eDocument table or field that you want Continia eDocuments to use to identify the vendor/customer, and then click **OK**.

## Field mapping and detail pages for source template header fields

Source templates are tied to a certain source (e.g.: a vendor) and used by Document Capture to capture, validate, and register documents. With Continia eDocuments, you can customize source templates to your liking by setting each template header field up to capture specific data from an incoming XML document and by linking from each header field to a certain page with more details.

To configure template header fields to capture specific data, use the **Capture from eDocument** feature – which lists all the fields that the XML structure has mapped between a given document and the various tables. For example, you may have the following tables available for you to choose from:

* **eBilling Header**
* **Party Information** – **Accounting supplier**
* **Party Information** – **Accounting customer**
* **Party Identification** – **Accounting supplier**
* **Party Identification** – **Accounting customer**
* **Payment Means**
* **VAT Sub Total**
* **Document Note**

You can choose freely between the fields of all these tables when deciding what specific table field to map a given template header field to. For example, you can map the template header field **Line Posting Description** to the **Payment Terms Note** field from the **eBilling Header** table. This will ensure that **Line Posting Description** always captures the document data that's in this particular table field.

To link from a header field to a specific page with more details, use the **eDocuments Details Page** feature. This enables you to:

* Provide the user with more information that's relevant for the given header field.
* Allow the user to choose between a number of provided options in order to specify something for a given field.

For example, you can use the feature to link the **VAT Amount** header field to a page that provides details about VAT percentage, VAT scheme ID and similar, so that the user gets access to much more information about VAT than just the amount. Another example could be to use the feature to present the user with a number of options to choose from in order to specify payment means.

> [!TIP]
> No matter how you use the feature, your specified details or options will be available to the user in the **Document Header** section of the document journal, in the **Details** column of the table of fields.

The following section, [To map fields and set up detail pages](#to-map-fields-and-set-up-detail-pages), guides you through the two overall processes described above. 

## To map fields and set up detail pages

In order to map template header fields to specific table fields and/or to set up detail pages for specific header fields, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Open the relevant document category – such as **PURCHASE** – by selecting the category line (not the code itself) and then clicking **Edit** on the action bar.
1. On the **Templates** FastTab, in the list of templates, select the XML template that you want to configure, and then click **Edit** to open the template card.
1. On the **Fields** FastTab, select the header field that you want to configure. This opens the template field card.
1. On the **General** FastTab, go to the **eDocument** section.
1. To map the selected header field to a specific table field, click the **Capture from eDocument** field to open the corresponding page. In the list of eDocument tables, locate the relevant one, and then select the table field that you want to map the header field to.
   > [!NOTE]
   > The selected field will be added to the **Capture from eDocument** field as a link (the name of the selected eDocument table followed by the name of the selected table field). You can click this link to edit your selection later, if necessary.
   > 
   > If you've selected a table field from an eDocument table that's duplicate, the **No. of Filters** field below will be autofilled to specify the exact location of the selected field. For example, there are two **Party Information** tables – one for **Accounting supplier** and one for **Accounting customer** – and if you select a field from one of these, the **No. of Filters** field will indicate which one. 
1. To apply a filter, click the **No. of Filters** field to open the **Table Filters** page, which lists all fields for the table you selected in **Capture from eDocument** above. Locate the field you want to filter on, and then type in or select the filter you want to use, in the **Filter** column.
1. If the field's value is the result of an operation performed using other document data, specify the kind of operation in **Value Operation**. You can choose between three options:
   | Option | Description |
   | --- | --- |
   | **Sum** | Adds up the values of the selected field and its corresponding fields for all records in the table that you selected in step 6 above. |
   | **Count** | Counts the number of records in the table that you selected in step 6 above. |
   | **Exists** | Specifies if the record exists in the table that you selected in step 6 above. |
1. In **eDocuments Details Page**, specify what details, if any, you want to display to users in the **Document Header** section of the document journal:
   * If the selected field is the type of field that allows users to select from a number of options (such as **Payment Means**), click the field to open a list of options, and then select the options that users are to be presented with.
   * If the selected field is any other type of field, click the field to open a list of pages, and then select the page that you want to link to in order to provide users with more relevant information about the field.
