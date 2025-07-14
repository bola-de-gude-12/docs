---
title: Setting up Continia eDocuments
date: 13-05-2025
id: DC-179
lang: en
description: How to set up Continia eDocuments in Document Capture.
---

# Setting up Continia eDocuments

This article describes how to set up Continia eDocuments in Continia Document Capture.

## Definitions

During the setup of Continia eDocuments, you'll come across several terms and concepts that need to be defined. Among these are the various document types:

\


| Document type                | Description                                                                                                                                                                                                                                                                                                                        |
| ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| eBilling documents           | Covers both incoming purchase invoices/credit memos and outgoing sales invoices/credit memos.                                                                                                                                                                                                                                      |
| eOrder documents             | Covers both outgoing purchase orders and incoming sales orders.                                                                                                                                                                                                                                                                    |
| eDocument response documents | Can be either a technical response (for example, the received XML file isn't valid, or the rules have been violated) or a business response (for example, the items and/or prices differ from what was agreed). A business response is a document that functions as a response to an invoice or a credit memo (purchase or sales). |
| eOrder response documents    | Covers both incoming purchase order responses and outgoing sales order responses.                                                                                                                                                                                                                                                  |

## XML structures

An XML structure defines the file structure for a certain electronic format (for example, **PEPPOLBIS3** and **OIOUBL**) and for a certain type of business document, such as an invoice, a credit memo, an invoice response, an order, or an order response. Types of XML structures include **Peppol BIS3 Invoice**, **Peppol BIS3 Credit Memo**, and **Peppol BIS3 Order**, but there are many others, covering different types of documents and electronic formats.

Each XML structure is associated with:

* A related identification template that's used for identifying the source of your incoming documents (for example, the customer or vendor who sent the documents).
* A stylesheet, which is a file that's used to transform each XML document into a more readable and user-friendly format to be displayed in the [document viewer](../../../Continia%20Document%20Capture/Business%20functionality/Continia%20eDocuments/@DC-71/#the-document-viewer).

> \[!IMPORTANT] If you're an existing user migrating to Continia eDocuments and you've previously made changes to an XML master template stylesheet, you must export the changed stylesheet and import it into Continia eDocuments using the **XML Structure Setup** page. For more information, see step 5 in the [To set up Continia eDocuments](<Setting up Continia eDocuments.md#to-set-up-continia-edocuments>) section below.

The XML structure operates by linking an XML path with a data type (such as **Text**, **Date**, or **Code**) and then mapping that data to a field in a [record](../../../Continia%20Document%20Capture/Business%20functionality/Continia%20eDocuments/@DC-181/). On the **XML Structure View** page, the name of the table in which a given record appears is displayed in the **Table Name** column, while the name of the related field is found in the **Field Name** column. These two – table name and field name – are essential to the Continia eDocuments framework.

For example, for an incoming Peppol invoice, the XML structure could link the XML path **/ubl:Invoice/cbc:IssueDate** to the data type **Date** – and then map that data to the field **Issue Date** in the table **eBilling Header**. Another invoice with a different electronic format might have an XML path that corresponds to the Peppol one, but look completely different. Nevertheless, the XML structure recognizes that this XML path should be mapped to the same field in the same table for that format too.

Note that format identification takes place within the XML structure – it's no longer part of the identification template. This means that the identification template is only used for party identification (that is, to identify the customer or vendor). For more information about the use of identification templates in Continia eDocuments, see [Capturing data from eDocuments](../../../Continia%20Document%20Capture/Business%20functionality/Continia%20eDocuments/@DC-182/).

### To view and edit an XML structure

To view and edit the structure of an XML:

1. Choose the \{{search\}} icon, enter **XML Structure View**, and then choose the related link. Alternatively, select **XML Structures** on the action bar on the **Continia eDocuments Setup** page, then select the desired structure and, on the action bar, click **Open XML Structure**.
2. On the **XML Structure View** page, select the dropdown list by the **Structure Code** field and choose the desired structure. E.g.: PEPPOLBIS3ORDER.
3. To view the additional information about a specific node in the structure, selecting it in the table and check the **XML Structure Details** FactBox.
4. To edit a value that isn't editable on the **XML Structure View** page, select **Actions > Modify Details** on the action bar to open the **Edit XML Structure Details** page.

> \[!NOTE] It's recommended that you avoid editing XML structures, unless you're absolutely sure you know what you're doing. If necessary, reach out to your partner for assistance.

## To set up Continia eDocuments

To set up Continia eDocuments:

1. Choose the \{{search\}} icon, enter **Continia eDocuments Setup**, and then choose the related link.
2. On the **General** FastTab, specify if you want eDocuments to handle incoming eBilling documents. You can also toggle test mode. For more information, see [To enable test mode](<Setting up Continia eDocuments.md#to-enable-test-mode>).
3. On the **Numbering** FastTab, specify the number series that should be used for automatically assigning numbers to imported electronic documents.
4. On the **eDocument Response** FastTab, specify if you want to send document status updates manually or automatically and – for automatic responses – when these should be sent:
   *   The fields under **eOrder Response** are vendor fields that have to do with the sending of sales order updates to customers who have ordered something from you:

       | Field             | Description                                                                                                                                                                                                                                                                  |
       | ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
       | **Send Updates**  | Notify the customer that you've updated the order (in case of price changes, item replacements, etc.). You can choose to send responses manually yourself or have them sent automatically when the document is released or registered, or when the shipment has been posted. |
       | **Send Rejected** | Notify the customer that you've rejected the sales order. You can choose to send responses manually yourself or have them sent automatically when the order is rejected.                                                                                                     |
   *   The fields under **eBilling Response** are customer fields that relate to the sending of business responses to vendors who have sent invoices or credit memos to you:

       | Field               | Description                                                                                                                                                                                                |
       | ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
       | **Send in Process** | Notify the vendor that you're processing the received document. You can choose to send responses manually yourself or have them sent automatically when the document is imported, registered, or approved. |
       | **Send Accepted**   | Notify the vendor that you've accepted the received document. You can choose to send responses manually yourself or have them sent automatically when the document is registered, released, or posted.     |
       | **Send Rejected**   | Notify the vendor that you've rejected the received document. You can choose to send responses manually yourself or have them sent automatically when the document is rejected.                            |
5. **Optional**: If you've previously made changes to an XML master template stylesheet that you want to import:
   1. To export the stylesheet, search (\{{search\}}) for and select **Document Categories**.
   2. To open the document category whose stylesheet you want to export, select the relevant line (not the code itself), and then select **Edit** on the action bar.
   3. On the **Templates** FastTab, in the list of templates, select the relevant master template, and then select **Edit** to open the template card.
   4. On the action bar, click **Actions** > **XML** > **Export Stylesheet** to export the stylesheet.
   5. To import the exported stylesheet, go to the **XML Structure Setup** page that you opened in step 4.
   6. Select **Actions** > **Stylesheet** > **Import Stylesheet** to import the stylesheet.
   7. If the stylesheet is a ZIP file, go to **Stylesheet Main Filename** and enter the name of the main stylesheet file to be used.

Continia eDocuments has now been set up, and you're ready to set up customers and vendors. This process is described in [Setting up customers and vendors](../../../Continia%20Document%20Capture/Business%20functionality/Continia%20eDocuments/@DC-180/). Note that you must also [set up the Continia Delivery Network](../../../Continia%20Document%20Capture/Business%20functionality/Continia%20eDocuments/@DC-75/), unless this was done at an earlier stage.

### To enable test mode

Enabling test mode allows you to test the Continia eDocuments functionality without actually sending any documents through the Continia Delivery Network (CDN).

To enable test mode:

1. Choose the \{{search\}} icon, enter **Continia eDocuments Setup**, and then choose the related link.
2. On the **General** FastTab, enable **Test Mode**.

When test mode is enabled, the following applies:

* All communication with the CDN is suspended, no documents are sent or received.
* All supported business documents can be resent – regardless of their existing status. Both eDocuments (i.e.: eBilling, eOrder, and eResponse) and related network documents are recreated and marked with the status **Test**.
* When a company is copied, all its existing participations are put in test mode. This goes for companies created within the tenant using the copy functions on the **Companies** page or when SaaS environments from the Admin Center.

### To change the priority of a network profile

The **Network Profiles** page allows you to define the priority of each of your network profiles. Continia eDocuments automatically selects the top registered profile available in the list (i.e.: 1). If this profile isn't registered for the sender, the next profile is used – and so on.

To change the order in which different network profiles are used:

1. Choose the \{{search\}} icon, enter **Continia eDocuments Setup**, and then choose the related link.
2. On the action bar, click **XML Structures**.
3. On the **XML Structures** page, under the **Supported by Network Profiles** column, select the number corresponding to the network profile whose priorities you want to change.
4. On the **Network Profiles** page, select a network profile name and, using the **Move Up** and **Move Down** actions on the action bar, raise or lower the priority of the network profile.
