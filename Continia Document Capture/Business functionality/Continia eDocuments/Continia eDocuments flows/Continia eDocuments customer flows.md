---
title: eDocuments customer flows
date: 15-10-2025
description: How to send purchase orders and invoice responses, register order responses, and receive invoices.
id: DC-220
lang: en
---

# eDocuments customer flows

This article describes the actions you must take as a customer in the Continia eDocuments flows. These actions are parts of different flows, as outlined below.

For information on the corresponding vendor flows, see [eDocuments vendor flows](@DC-221).

## Ordering

### To send a purchase order

To create and send a purchase order:

1. Create a purchase order as described in [Record purchases with purchase invoices and orders](https://learn.microsoft.com/en-US/dynamics365/business-central/purchasing-how-record-purchases?wt.mc_id=d365bc_inproduct_helppane#create-and-post-a-purchase-invoice) (Microsoft article). From the action bar on the **Purchase Orders** page, click **New** to open the **Purchase Order** page, and then enter the necessary details as described.
1. On the action bar, click **Print/Send** > **Send** to open the **Send Document to** dialog box.
1. In the **Electronic Document** dropdown list, select **Through Continia Delivery Network**. Click **OK** to confirm and then **OK** again to return to the **Purchase Order** page.
1. On the **General** FastTab, check [the **eDocument Status** field](@DC-183#the-edocument-status-field):
   * **Sent** - the purchase order has been sent to the vendor.
   * **In Progress** - the purchase order has been sent to the network, but there's no confirmation of receipt or failure.
   * **Failed** - the sending of the purchase order has failed due to a network issue.
   * **Not Valid** - click this to open the **eOrder Document** page, and then do as follows:
      1. On the action bar, click **Validation Log** to open the **eValidation Log** page, which lists a number of validation errors.
      1. Take note of the **Detailed Error Message**, close the log to return to the **eOrder Document** page, and then resolve the listed validation errors.
      1. When done, click **Resend** on the action bar to send the revised purchase order to the vendor.

The purchase order has now been sent to the vendor, who can process it as described in [To import and register a sales order](@DC-221#to-import-and-register-a-sales-order).

### To register an order response

To import and register a vendor's order response:

1. In the Role Center, under **Continia Document Capture Activities**, go to **Actions** and click **Import Files**.
1. The order response is now ready to be registered and available in the **Ready to Register** cue. Click this to open the document journal.
1. On the action bar, click **Document** > **Document Card** to open the document card.
1. If the vendor has made any line changes, these are displayed on the **Lines** FastTab.
   > [!NOTE]
   > Only the actual changes are displayed here – no other line details relating to quantity, price, unit of measure and similar are visible.
   To see the full context of the line changes (before and after), click **Preview Order Changes** on the action bar to open the **Purchase Order Changes Preview** page.
1. The **Purchase Order Lines** section provides an overview of the original lines and their details, whereas the **Changed Lines** section lists the lines as they appear after the vendor changed them. Review the changes, and then close the page to return to the document card.
1. On the action bar, click **Home** > **Register** to register the order response.

The order response is registered, and the purchase order is automatically opened and updated with the changes from the order response.

>[!NOTE]
>Only one change can be submitted per document. If you or the vendor submits a price or quantity change, for example, the other party can't submit any other changes.

>[!TIP]
>For an overview of the changes made by the vendor, click **Home** > **Match Lines** on the action bar from either the document card or the document journal.

### To change a confirmed purchase order
To change an order confirmed by the vendor, after registering the order response:

1. On the **Purchase Order** page, make the required change to the order.
1. On the action bar, click **Actions** > **eDocuments** > **Update**.

### To confirm a changed purchase order
To confirm an order changed by the vendor, after registering the order response:

* On the **Purchase Order** page, click **Actions** > **eDocuments** > **Confirm Changes** on the action bar.

### To cancel a changed purchase order
To cancel an order changed by the vendor, after registering the order response:

1. On the **Purchase Order** page, click **Actions** > **eDocuments** > **Cancel** on the action bar.
2. The **eOrder Document** page opens. On the **General** FastTab, enter a reason in the **Cancellation Note** field.
3. On the action bar, click **Send**.

>[!NOTE]
>Although a cancellation submitted by the vendor is final, cancellations submitted by a customer can be either accepted or rejected by the vendor.

## Billing

### To receive an invoice and send an invoice response

As a customer, you can import a purchase invoice and send back an invoice response by following these steps:

1. In the Role Center, under **Continia Document Capture Activities**, go to **Actions** and click **Import Files**.
1. The purchase invoice is now available in the **Ready to Register** cue. Click this cue to open the document journal.
1. On the action bar, click **Document**.
   1. **Optional**: To view all available information for the purchase invoice, click **eDocument Card** to open the **Incoming eBilling Document** page. Close the page to return to the document journal when you're done.
   1. If the purchase invoice includes invoice lines and you need to set up translations, for example, click **Document Card** to open the document card.
1. The document card allows you to do everything you're used to from Document Capture, including [document matching](@DC-61). To carry out matching, select **Home** > **Match Lines**. Make any necessary adjustments to complete the matching process.
1. When you're done with the purchase invoice and no warnings are displayed, click **Register** on the action bar to register the purchase invoice.
1. The **Purchase Invoice** page opens. From here, you can manually notify the vendor that you've accepted, rejected, or paid the invoice – or that you're processing it or have questions.

   1. On the action bar, click **Invoice** > **Send Electronic Confirmation**.
   1. In the dialog that opens, select the appropriate option – for example, **Accepted** – and then click **OK** to close the dialog.
   1. The **eBilling Response** page opens. On the **Response** FastTab, under **Response Code**, select a response code – if necessary.
   1. On the **Reason** FastTab, select a reason code, and enter your comments for the vendor – if applicable. In some cases, the document won't be sent until you enter a comment here.
   1. On the action bar, click **Send** to send your response to the vendor.
   
   ## To automatically respond to eDocuments
   Instead of manually responding to each order or invoice, you can configure Continia eDocuments to automatically send a response based on an action. Note that not all responses are automatable.
   
   To configure your automatic eDocument responses:
   
   1.	Search ({{search}}) for and select **Continia eDocuments Setup**.
   2.	On the **eDocument Response** FastTab, under **eBilling Response**, configure the settings:
      * **Send In Process** - choose when to notify that the invoice is being processed. For example, when releasing the document.
      * **Send Accepted** - choose when to notify that the invoice has been accepted. For example, when importing the document.
      * **Send Rejected** - choose when to notify that the invoice has been rejected.

## Related information
[eDocuments flows](@DC-183)  
[eDocuments vendor flows](@DC-221)