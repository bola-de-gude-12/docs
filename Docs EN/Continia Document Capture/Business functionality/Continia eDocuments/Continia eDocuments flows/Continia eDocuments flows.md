---
title: eDocuments flows
date: 10-09-2025
description: A description of the flows supported by Continia eDocuments.
id: DC-183
lang: en
---

# eDocuments flows

Continia eDocuments supports multiple document flows, currently involving the following four types of documents:

* Invoices and invoice responses
* Credit memos
* Orders, order responses, order cancellations, and order changes

More document types will be added in the future, meaning that even more flows and scenarios will be possible with Continia eDocuments at a later stage.

The sections below outline two typical document flows between two parties (customer and vendor) using Continia eDocuments in Microsoft Dynamics 365 Business Central.

> [!NOTE]
> For the sake of example, the outlined flows use the Peppol Network – but many other similar networks can be used instead. Continia eDocuments supports all major networks and digital infrastructures for the exchange of business documents.

For actual user guides on how to carry out the various actions related to these flows, see:
* [eDocuments customer flows](@DC-220)
* [eDocuments vendor flows](@DC-221)

## Ordering flow

A classic Continia eDocuments ordering flow involves a customer (buyer) who places an order with a vendor (seller), who then responds to that order. Such a flow typically looks as follows:

1. The customer [creates a purchase order in Business Central and sends it to the vendor](@DC-220#to-send-a-purchase-order) using Continia eDocuments (via the Peppol Network).

1. The vendor [receives the order and registers it as a Business Central sales order](@DC-221#to-receive-an-order-and-send-an-order-response). One of the following three types of order response is then sent either manually or automatically from the vendor to the customer, indicating if the order can be fulfilled:
   * **Order Acceptance** - the vendor can fulfill the order and accepts it fully. Here, the vendor may also add details that are useful to the customer, for example to assist in item identification.
   * **Order Changes** - the vendor can only partially fulfill the order, because changes must be made to one or more lines (due to price changes, item availability, or similar).
   * **Order Rejection** - the vendor can't fulfill the order at all, and therefore rejects it.

   >[!NOTE]
   >If the vendor rejects the order, the customer has to start the flow again by creating another purchase order and sending it to the vendor.

1. The customer receives the relevant order response in Business Central. If the customer is satisfied with the order, they can accept it and [register it](@DC-220#to-register-an-order-response) – which updates the original purchase order with any changes the vendor has made. Otherwise, the customer can either cancel the order altogether or request changes to it (provided that the vendor didn't submit changes earlier).

1. Depending on the customer's response, the vendor can: accept the updated purchase order and post the sales order, which automatically creates a posted sales invoice; or cancel the sales order.

The posted sales invoice can then be sent to the customer as part of [the billing flow outlined below](#billing-flow).

>[!NOTE]
>Only one order change can be submitted per document.

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src=https://player.vimeo.com/video/1114186087?h=aedccc9114&badge=0&autopause=0&player_id=0&app_id=58479%22 frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="DC_Welcome_to_Document_Capture"></iframe></div><script src=https://player.vimeo.com/api/player.js></script>

## Billing flow

A classic Continia eDocuments billing flow involves a vendor (seller) who sends an invoice to a customer (buyer), who then responds to that invoice. Such a flow will typically look as follows:

1. The vendor creates a sales invoice in Business Central for the items that were ordered by and shipped to the customer, for example by posting a sales order as part of [the ordering flow](#ordering-flow) above.
1. The vendor [sends the sales invoice](@DC-221#to-send-a-sales-invoice) using Continia eDocuments (via the Peppol Network).
1. The customer [receives the invoice](@DC-220#to-receive-an-invoice-and-send-an-invoice-response), and one of the following two types of invoice response is sent either manually or automatically from the customer to the vendor, indicating the status of the invoice:
   * **In Process** - the customer is reviewing the invoice.
   * **Under Query** - the customer needs clarification or has questions about the invoice and may contact the vendor via phone or email.
1. When no more information is needed, the customer matches the invoice against the original order. One of the following three types of invoice response will then be sent either manually or automatically from the customer to the vendor, depending on the result of the matching process:
   * **Rejected** - the invoice and the order don't match, so the customer rejects the invoice.
     
      > [!NOTE]
      > If the customer rejects the invoice, the vendor will have to start the flow again by creating a new sales invoice and sending it to the customer.
   * **Conditional** - the invoice and the order almost match, so the customer accepts under certain conditions – for example, provided that the vendor adjusts the price.
   * **Accepted** - the invoice and the order match, so the customer accepts.
1. Following successful matching, the customer registers the invoice using Document Capture, thereby creating a purchase invoice.
1. The customer pays the invoice, and a **Paid** notification is sent to the vendor.

> [!NOTE]
> On the vendor side, all invoice responses except **Rejected** are purely informational and require no action. When an invoice is rejected, the vendor must take action by sending a credit memo to the customer.

## The eDocument Status field

For all flows, both customers and vendors can monitor the status of a document throughout the process using the **eDocument Status** field. This field is available from a number of key pages, such as the **Sales Order**, **Purchase Invoice**, and **Posted Sales Invoice** pages. For all of these pages, it's located on the **General** FastTab.

If you select the status message in the **eDocument Status** field for a given document, the **eDocument Overview** page opens. This page lists all document statuses and activities that have been automatically logged for the document. It also provides additional useful details like **Change** (if changes have been made) and **Conditionally Accepted** (if a document has been accepted under certain conditions).

## Related information
[Supported electronic document formats](@DC-55)  
[eDocuments advanced ordering flows](@DC-237)