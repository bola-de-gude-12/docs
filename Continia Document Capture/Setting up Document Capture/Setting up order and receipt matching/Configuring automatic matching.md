---
title: Configuring Automatic Matching
date: 08-07-2024
description: How to set up automatic matching of incoming invoices and credit memos
id: DC-68
lang: en
---

# Configuring Automatic Matching

Continia Document Capture can automatically match incoming invoices and credit memos against related documents, either as a fully automated process initiated by field recognition (and other actions) or on an ad hoc basis whenever you prefer. If **Autorun Perform Match** has been enabled in the setup as described in [the guide below](#to-set-up-automatic-matching), matching will be a fully automated process that's triggered whenever you perform one of the following actions:

* Update the value of any of the following fields in the **Document Header** section of the document journal:
   * **Amount Excl. VAT**
   * **Our Order No.**
   * **Currency Code**
   * **Vendor Shipment No.** (not visible by default)
   * **Vendor Order No.** (not visible by default)
* Import documents.
* Select **Home > Recognize Fields** in the document journal.

Automatic matching is configured per template, so the matching rules you set up for a specific template will apply to all documents for which that template is used.

## To set up automatic matching

1. Search ({{search}}) for and select **Document Categories**.
1. To open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself), and then choose **Edit** on the action bar.
1. On the **Document Category** page, on the **Templates** FastTab, select the template that you want to configure.
1. On the FastTab title bar, select **Edit** to open the template card.
1. On the **Purchase Documents** FastTab, under **Matching**, enable **Autorun Perform Match** if you want documents to be matched fully automatically on document import, during field recognition, or in any of the other scenarios mentioned above. 
   > [!NOTE]
   > If this feature isn't enabled, you'll have to trigger automatic matching manually yourself for each document. For more information, see [Running automatic matching](/continia-document-capture/business-functionality/order-and-receipt-matching/automatic-document-matching#running-automatic-matching).
1. Fill in the remaining **Matching** fields as needed. Note that in order to activate automatic matching, you must enable **Match Invoice** and/or **Match Credit Memo** by selecting a value other than **No**:
  
   <br>
   
   | Field | Description |
   | --- | --- |
   | **Match Invoice** | Use this field to specify what types of documents you want invoices to be matched against. Invoices can be matched against receipts, orders, or both. Selecting **No** leaves automatic matching of invoices disabled. <div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Note</span></p><p>If you select **Order Only** or **Receipt or Order**, any order that's partially matched with an invoice will be locked until the invoice has been posted, meaning that you can't directly receive or invoice any additional goods or services on that order until the matched invoice has been posted. The same principle applies to credit memos, but with return orders instead of orders – see <b>Match Credit Memo</b> below. <br><br> This limitation was implemented as a security measure, to ensure that the order (or return order) isn't suddenly posted in full, leaving its originally matched invoice (or credit memo) incapable of being posted. </p></div> |
   | **Match Credit Memo** | Use this field to specify what types of documents you want credit memos to be matched against. Credit memos can be matched against return shipments, return orders, or both. Selecting **No** leaves automatic matching of credit memos disabled. <br><br> Regarding the options **Return Order Only** and **Return Shipment or Return Order**, see the note under **Match Invoice** above.  |
   | **Max. Variance Amount Allowed (LCY)** | With this field, you can allow for variance expressed as a fixed amount in the local currency. This means that documents can be matched automatically even if their respective amounts don't match, provided that the discrepancy between them is within the variance amount you define here. |
   | **Max. Variance % Allowed** | With this field, you can allow for variance expressed as a percentage of the invoice/credit memo total. This means that documents can be matched automatically even if their respective amounts don't match, provided that the discrepancy between them is within the variance percentage you define here. |
   | **Variance Posting Account** | This field enables you to select the GL account that variance line amounts will be posted to. A variance line is a line that's created automatically in an invoice or a credit memo when the total amount of the invoice/credit memo differs from the total amount of the matching document. Variance lines are only created if the amount difference is within the variance you've defined in the fields above though (**Max. Variance Amount Allowed (LCY)** and/or **Max. Variance % Allowed**). |
   | **Copy Matched Header Dimensions** | If you enable this setting, Document Capture will copy the header dimensions of a matched document to the invoice or credit memo that it's being matched against. This is done automatically when the invoice or credit memo is registered. |

> [!NOTE]
> As noted in the table above, you can allow for variance in two ways: expressed as a fixed amount or as a percentage of the total. It's actually possible to use both methods at the same time. If you do so, the smaller of the two applies.

## Related information

[Automatic Document Matching](@DC-70)  
[Handling Discrepancies, Including Partial Matching](@DC-63)  