---
title: eDocuments advanced ordering flows
date: 10-07-2025
description: A description of the advanced ordering functionality in eDocuments.
id: DC-237
lang: en
---

# eDocuments advanced ordering flows

This article describes the advanced ordering functionality in eDocuments, which allows for the alteration and cancellation of electronic orders (eOrders) exchanged via the Peppol network in Continia Document Capture.

While the standard eOrdering flow supports orders and order responses, the advanced eOrdering flows add order cancellations and order changes to the process. This provides you with more flexibility when handling orders as a customer (buyer) or as a vendor (seller).

>[!NOTE]
>Technically, changes and cancellations are only shown as such when sent by the buyer. When sent by the seller, these are shown as order responses.

The scenarios below illustrate the flows made possible by the advanced ordering functionality.

>[!IMPORTANT]
>Only one order change per document is supported, be it on the customer or vendor side.

## Initial order from the buyer

In this scenario, all possible outcomes are shown.

<a href="/images/DC/eDocuments/eDocuments advanced ordering - scenario A.jpg" target="_blank">
<img src="/images/DC/eDocuments/eDocuments advanced ordering - scenario A.jpg" alt="eDocuments advanced ordering - scenario A">
</a>

## Order changed by the buyer

In this scenario, the buyer requests a change to the initial order. This request can be accepted or rejected by the seller.

<a href="/images/DC/eDocuments/eDocuments advanced ordering - scenario B.jpg" target="_blank">
<img src="/images/DC/eDocuments/eDocuments advanced ordering - scenario B.jpg" alt="eDocuments advanced ordering - scenario B">
</a>

## Order changed by the seller

In this scenario, the seller requests a change to the initial order. This request can be accepted or rejected by the buyer.

<a href="/images/DC/eDocuments/eDocuments advanced ordering - scenario C.jpg" target="_blank">
<img src="/images/DC/eDocuments/eDocuments advanced ordering - scenario C.jpg" alt="eDocuments advanced ordering - scenario C">
</a>

## Order cancelled by the buyer

In this scenario, the buyer requests a cancellation. This request can be accepted or rejected by the seller.

<a href="/images/DC/eDocuments/eDocuments advanced ordering - scenario D.jpg" target="_blank">
<img src="/images/DC/eDocuments/eDocuments advanced ordering - scenario D.jpg" alt="eDocuments advanced ordering - scenario D">
</a>

## Order cancelled by the seller

In this scenario, the vendor submits a cancellation.

<a href="/images/DC/eDocuments/eDocuments advanced ordering - scenario E.jpg" target="_blank">
<img src="/images/DC/eDocuments/eDocuments advanced ordering - scenario E.jpg" alt="eDocuments advanced ordering - scenario E">
</a>

## Related information
[eDocuments vendor flows](@DC-221)   
[eDocuments customer flows](@DC-220)