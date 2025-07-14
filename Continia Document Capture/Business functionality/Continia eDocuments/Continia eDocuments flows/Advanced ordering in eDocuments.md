---
title: eDocuments advanced ordering flows
date: 10-07-2025
id: DC-237
lang: en
description: A description of the advanced ordering functionality in eDocuments.
---

# eDocuments advanced ordering flows

This article describes the advanced ordering functionality in eDocuments, which allows for the alteration and cancellation of electronic orders (eOrders) exchanged via the Peppol network in Continia Document Capture.

While the standard eOrdering flow supports orders and order responses, the advanced eOrdering flows add order cancellations and order changes to the process. This provides you with more flexibility when handling orders as a customer (buyer) or as a vendor (seller).

> \[!NOTE] Technically, changes and cancellations are only shown as such when sent by the buyer. When sent by the seller, these are shown as order responses.

The scenarios below illustrate the flows made possible by the advanced ordering functionality.

> \[!IMPORTANT] Only one order change per document is supported, be it on the customer or vendor side.

## Initial order from the buyer

In this scenario, all possible outcomes are shown.

<figure><img src="../../../.gitbook/assets/eDocuments advanced ordering - scenario A.jpg" alt=""><figcaption></figcaption></figure>

## Order changed by the buyer

In this scenario, the buyer requests a change to the initial order. This request can be accepted or rejected by the seller.

<figure><img src="../../../.gitbook/assets/eDocuments advanced ordering - scenario B.JPG" alt=""><figcaption></figcaption></figure>

## Order changed by the seller

In this scenario, the seller requests a change to the initial order. This request can be accepted or rejected by the buyer.

<figure><img src="../../../.gitbook/assets/eDocuments advanced ordering - scenario C.JPG" alt=""><figcaption></figcaption></figure>

## Order cancelled by the buyer

In this scenario, the buyer requests a cancellation. This request can be accepted or rejected by the seller.

<figure><img src="../../../.gitbook/assets/eDocuments advanced ordering - scenario D.JPG" alt=""><figcaption></figcaption></figure>

## Order cancelled by the seller

In this scenario, the vendor submits a cancellation.

<figure><img src="../../../.gitbook/assets/eDocuments advanced ordering - scenario E.JPG" alt=""><figcaption></figcaption></figure>

## Related information

[eDocuments vendor flows](../../../../Continia%20Document%20Capture/Business%20functionality/Continia%20eDocuments/Continia%20eDocuments%20flows/@DC-221/)\
[eDocuments customer flows](../../../../Continia%20Document%20Capture/Business%20functionality/Continia%20eDocuments/Continia%20eDocuments%20flows/@DC-220/)
