---
title: eDocuments vendor flows
date: 15-04-2025
description: How to send sales invoices and order responses, and receive purchase orders. 
id: DC-221
lang: en
---

# eDocuments vendor flows

This article describes the actions you must take as a vendor in the Continia eDocuments flows. The actions are parts of different flows, as outlined below.

For information on the corresponding customer flows, see [eDocuments customer flows](@DC-220).

## Ordering

### To import and register a sales order

To import and register a sales order:

1. In the Role Center, under **Continia Document Capture Activities**, select **Actions** > **Import Files**.

1. The sales order is now available in the **Ready to Register** cue. Select this cue to open the document journal.

1. On the action bar, click **Document**.
   1. **Optional**: To view all available information for the sales order, select **eDocument Card** on the action bar to open the **eOrder Document** page. Close the page to return to the document journal when you're done.
   1. If the sales order includes order lines and you need to set up translations or similar, select **Document Card** on the action bar to open the document card.

1. The document card allows you to do everything you're used to from Document Capture. If you're happy with the sales order and no warnings are displayed, select **Home** > **Register** on the action bar to register the sales order and create a sales order.

### To confirm a sales order

To confirm a sales order, after registering it:

* On the **Sales Order** page, select **Actions > eDocuments > Confirm** on the action bar.

>[!NOTE]
>The action is named **Confirm** even if you change the order, so make sure that no unwanted changes have been applied. For example, the price of an item could be different on your side.

### To reject a sales order

To reject a sales order:

1. In the document journal or on the document card, select **Reject** on the action bar.
2. Select **Actions > Functions > Send eOrder Rejection Response** to communicate the rejection to the customer.

### To cancel a sales order

To cancel a sales order, after registering it:

* On the **Sales Order** page, select **Actions > eDocuments > Cancel** on the action bar.

>[!TIP]
>You can cancel an order at any time, be it before or after confirming it.

### To change a sales order before confirming it

To change a registered sales order before confirming it:

1.	On the **Sales Order** page, make the required change to the order.
2.	On the action bar, click **Actions > eDocuments > Confirm**.
3.	If the customer accepts the changes proposed by you, register the confirmed sales order.

> [!NOTE]
> Only one change can be submitted per document. If you or the customer submits a price or quantity change, for example, the other party can't submit any other changes. Additional changes are shown as errors in the **Comments** section in the document journal or on the document card.

### To confirm a changed sales order

To confirm a sales order changed by the customer:

1.	In the document journal or on the document card, review the changes requested by the customer in the **Comments** section.
2.	**Optional**: For a more detailed overview of the changes requested by the customer, select **Home > Match Lines** on the action bar.
3.	Select **Register** on the action bar.
4.	On the **Sales Order** page, select **Actions > eDocuments > Confirm Changes** on the action bar.

### To update a confirmed sales order

To update a sales order that has been confirmed by both parties:

1.	On the **Sales Order** page, make the required changes to the order.
2.	Select **Actions > eDocuments > Update** on the action bar.
3.	If the customer accepts the changes proposed by you, register the confirmed sales order.

### To confirm the cancellation of a sales order

To confirm the cancellation of a sales order, after registering it:

* On the **Sales Order** page, select **Actions > eDocuments > Confirm cancellation** on the action bar.

### To reject the cancellation of a sales order

To reject the cancellation of a sales order:

1.	In the document journal or on the document card, select **Home > Reject** on the action bar.
2.	On the action bar, click **Actions > Functions > Send eOrder Rejection Response** to communicate the rejection to the customer.

>[!NOTE]
>Only one change can be submitted per document. If you or the customer submits a price or quantity change, for example, the other party can't submit any other changes. Additional changes are shown as errors in the **Comments** section in the document journal or on the document card.

## Billing

### To send a sales invoice

To create and send a sales invoice:

1. Create a sales invoice, for example by posting a sales order that you've received from a customer as part of an ordering flow.
1. From the **Posted Sales Invoice** page, on the action bar, click **Print/Send** > **Send** to open the **Send Document to** dialog.
1. In the **Electronic Document** dropdown menu, select **Through Continia Delivery Network**. Select **OK** to confirm and then **OK** again to return to the **Posted Sales Invoice** page.
1. On the **General** FastTab, check [the **eDocument Status** field](@DC-183#the-edocument-status-field):
   * **Sent** - the sales invoice has been sent to the customer.
   * **In Progress** - the sales invoice has been sent to the network, but there's no confirmation of receipt or failure.
   * **Failed** - the sending of the sales invoice has failed due to a network issue.
   * **Not Valid** - select this text to open either the **eBilling Document** page (if the invoice has no related eOrder) or the **eDocument Overview** page (if a related eOrder exists). If the **eDocument Overview** page opens, locate the eBilling document and select it to open the **eBilling Document** page, and then do as follows:
     1. On the action bar, click **Validation Log** to open the **eValidation Log** page, which lists a number of validation errors.
     1. Take note of the **Detailed Error Message**, close the log to return to the **eBilling Document** page, and then resolve the listed validation errors.
     1. When done, select **Resend** on the action bar to send the revised sales invoice to the customer.

The sales invoice is sent to the customer, who can process it as described in [To receive an invoice and send an invoice response](@DC-220#to-receive-an-invoice-and-send-an-invoice-response).

**To resend an eBilling document**

In certain cases, it might be useful to resend an eBilling document that had already been successfully sent. For example, if a recipient requires a copy of the document. To resend an eBilling document:

>[!NOTE]
>This action is only available in electronic document formats with the **Copy Indicator** field, such as the Danish OIOUBL format.

1. Choose the {{search}} icon, enter **Outgoing Network Documents**, and then choose the related link.
2. Select the document you would like to resend. Note that only documents with the **eDocument Status** 'Successful' can be resent.
3. On the action bar, click **Actions > Resend**. Alternatively, select **eDocument Card** and, on the **eOrder Response** page, select **Resend** on the action bar.

An additional eDocument record is created in the Continia Delivery Network (CDN), and the copy is automatically sent.

>[!TIP]
>To check if a sent eDocument is a copy, go to the **Outgoing Network Documents** page and look up its value under the **Copy** column.

## To automatically respond to eDocuments

Instead of manually responding to each order or invoice, you can configure Continia eDocuments to automatically send a response based on an action.

To configure your automatic eDocument responses:

1. Choose the {{search}} icon, enter **Continia eDocuments Setup**, and then choose the related link.
2. On the **eDocument Response** FastTab, under **eOrder Response**, configure the settings:

   * **Send Updates** - choose when to notify that the order has been updated. For example, when registering the order.
   * **Send Rejected** - choose when to notify that the order has been rejected.

## Related information

[Continia eDocuments flows](@DC-183)  
[Continia eDocuments customer flows](@DC-220)