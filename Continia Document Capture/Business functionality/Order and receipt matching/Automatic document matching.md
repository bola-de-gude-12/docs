---
title: Automatic document matching
date: 13-03-2025
description: How purchase invoices and credit memos are automatically matched against related documents
id: DC-70
lang: en
---

# Automatic document matching

If you set up automatic matching, Continia Document Capture automatically matches incoming invoices and credit memos with their related documents based on the matching criteria that you've specified in the setup. This typically saves a lot of valuable time compared to manual matching and is particularly well suited for organizations that receive large volumes of incoming documents.

One of the matching criteria that you can set up is whether lines should be recognized and matched. This setting has a significant impact on the automatic matching process, as line matching differs considerably from header matching. The differences are explained in the sections below.

To set up header matching, see [Configuring automatic matching](@DC-68). To set up line matching, see [Setting up line matching](@DC-69).

>[!TIP]
>Document Capture supports the matching of an incoming invoice to one or more purchase receipts and/or purchase orders, be it on the header level or the line level. Document Capture can also match credit memos to one or more return shipments and/or return orders.

## Overall matching parameters

No matter if line matching has been enabled or not, Document Capture applies a number of overall filters as matching parameters in an attempt to establish a link between an incoming invoice/credit memo and one or more other related documents (orders/receipts for invoices and return orders/return shipments for credit memos). The applied filters are intended to narrow down the number of potential matches before any other matching criteria relating to either header or line matching are applied.

**Mandatory filters (automatically applied)**

* Vendor number
* Currency code
* Open quantity:
   * For order lines, **Outstanding Quantity** must be other than zero.
   * For receipt lines, **Qty. Rcd. Not Invoiced** must be other than zero.
   > [!NOTE]
   > This filter is applied to identify document lines that haven't yet been invoiced.

**Optional filters**

* Order number - relating to the **Our Order No.** field in the document journal
* Vendor order number
* Vendor shipment number

## Header matching

When Document Capture matches an invoice or a credit memo against related documents at header level, it matches the lines of the related documents up with the total amount of the invoice or credit memo – using the quantity and price of each matched document line. Taking an incoming invoice as an example, if the total amount of that invoice is $1,000 and Document Capture identifies a purchase receipt with a line that has a **Quantity** of 10 and a **Direct Unit Cost (Order)** of $100, that purchase receipt line is considered a perfect match (10 × $100 = $1,000).

Note that if, for example, the total invoice amount had been $1,005 and you had set up a variance of $10, the identified purchase receipt line mentioned above would also have been considered an acceptable match. However, seeing that it would have been $5 short of being a perfect match, it wouldn't necessarily have been selected – only if no other better matches were identified.

> [!TIP]
> Usually, the total amounts of incoming invoices and credit memos vary considerably. This means that each total amount is relatively unique, and that matching against a total amount is therefore often enough to ensure a reliable match. However, if there are in fact multiple identical or useful matches for a total amount, Document Capture uses the first match it identifies – which may not be the correct one. To avoid situations like this, it's recommended that you ask your vendors to always include an order reference in documents sent to you. This provides Document Capture with an extra matching parameter (in addition to the total amount, the currency, and the vendor number), which directly links related documents and ensures a much higher degree of accuracy.

### Prioritized list of search methods

When attempting to identify matches for an incoming document at header level, Document Capture searches through document lines using a number of different search methods in the order listed below. The method that provides the most accurate match is the one that's applied.

> [!NOTE]
> For invoices, Document Capture searches for matching order lines and receipt lines, whereas for credit memos it looks for matching return order lines and return shipment lines. The following list of search methods is based on invoices, for descriptive purposes.
> 
> Note that the search methods in the list require different settings on the template card, under **Purchase Documents** > **Matching** > **Match Invoice**. The required template settings are indicated for each method in the list.

<br>

| Priority | Search method | Required&nbsp;template&nbsp;setting |
| --- | --- | --- |
| 1 | Match all orders and/or receipts to the total amount of the incoming invoice. | **Receipt or Order** |
| 2 | Match all receipts to the total amount of the incoming invoice. | **Receipt Only** |
| 3 | Go through each receipt to check if it matches with the total amount of the incoming invoice. | **Receipt Only** |
| 4 | Go through each order to check if it matches with the total amount of the incoming invoice.  | **Order Only** |
| 5 | Attempt to match the total amount of the incoming invoice against one order and all related receipts. | **Receipt or Order** |

If the difference between the invoice/credit memo amount and the sum of the matched document lines is zero for any of the above search methods, Document Capture skips any subsequent search methods.

## Line matching

When Document Capture matches an invoice or a credit memo against related documents with line matching enabled, it checks the lines of the invoice or credit memo one by one and attempts to identify a matching line for each of them in the related documents – based on matching criteria specified by you. For example, if you've set the [line matching setup](@DC-69) option **Match Quantity** to **Yes - always**, any order line or purchase receipt line that's matched against an invoice line must have the same quantity as the invoice line in order to be considered a useful match.

When you set up line matching, there are a number of matching parameters available for you to choose between, and for one of these – **Match Unit Cost** – you can even specify a variance amount or percentage. For example, if you set the [line matching setup](@DC-69) option **Unit Cost - Variance %** to 5 and then match an invoice line that has a unit price of $100, Document Capture identifies order lines and purchase receipt lines with unit costs ranging between $95 and $105 as acceptable matches, provided that any other specified matching parameters are met as well.

The matching of documents at line level rather than header level, combined with the multiple matching parameters available for line matching, enables Document Capture to match in greater detail than with header matching. However, it also adds a level of complexity to the process that may not be necessary for you, so consider what's the right setup for your particular organization.

## Running automatic matching

Both types of automatic matching are carried out as described below, depending on whether you've enabled the **Autorun Perform Match** feature during setup.

If the **Autorun Perform Match** feature is enabled, automatic matching is triggered when you [select **Recognize Fields** in the document journal](/continia-document-capture/business-functionality/documents-and-templates/working-with-paper-and-pdf-documents#capturing-fields). If all document fields are recognized correctly during the [import of the document](@DC-82), matching is even carried out automatically upon import. Either way, the comments section of the document journal confirms that the document has been successfully matched with another document.

If **Autorun Perform Match** is enabled, **Invoice Reg. Step 1** is set to either **Match Order & Create Invoice** or **Match & Update Order**, and there's no match, Document Capture notifies you accordingly in the **Comments** section. However, you can still register the document.

> [!NOTE]
> In the document journal, under **Document Header**, you can retrigger the automatic matching process by manually changing the identified **Order No.** or the **Amount Excl. VAT**, if necessary.

If the **Autorun Perform Match** feature is disabled, automatic matching must be triggered manually by you. To do this:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the **PURCHASE** code to open the document journal.
1. In the list of documents, select the document that you want to automatically match against other documents.
1. If necessary, [assign a vendor](/continia-document-capture/business-functionality/documents-and-templates/working-with-paper-and-pdf-documents#changing-a-documents-associated-vendor) to the document.
1. On the action bar, click **Match Lines** to open the **Invoice Matching** page (or the **Credit Memo Matching** page for credit memos).
1. On the action bar, click **Home** > **Perform Match**.

Document Capture automatically matches the document against other documents. On the **Order Lines** FastTab, the lines for which matches were automatically found turn bold. In the document journal, the **Comments** section confirms that the document has been successfully matched with another document.

## Related information

[Manual document matching](@DC-62)  
[Handling discrepancies, including partial matching](@DC-63)  
