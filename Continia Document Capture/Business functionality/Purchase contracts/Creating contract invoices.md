---
title: Creating Contract Invoices
date: 01-10-2024
description: How to create invoices linked to purchase contracts in Document Capture.
id: DC-88
lang: en
---

# Creating Contract Invoices

A contract invoice is an invoice that has been linked with a purchase contract. When the invoice is registered, the lines of the purchase contract are automatically inserted into the invoice.

The first step in the process is to [link an incoming invoice with a contract](#to-link-a-purchase-contract-with-an-invoice), and the second step is to [register the invoice as a contract invoice](#to-register-an-invoice-as-a-contract-invoice). Upon registration, the contract invoice is created as a real business entity in Microsoft Dynamics 365 Business Central. Using the posting setup, you can also enable Continia Document Capture to automatically create the link between the invoice and the contract during the actual registration of the invoice, as described under [To create a contract invoice using the posting setup](#to-create-a-contract-invoice-using-the-posting-setup).

For ease of understanding, this article deals exclusively with invoices as a representative example – as this is by far the most common scenario. However, the exact same principle applies to *contract credit memos*.

> [!IMPORTANT]
> For the lines of the contract to be automatically inserted into the invoice, line recognition must be disabled in the relevant template.

## To link a purchase contract with an invoice

A purchase contract can be linked to an incoming invoice either manually by you or automatically by Document Capture when the invoice is created from a document. Both methods are described below:

### Automatic linking

To link the contract with the invoice automatically, you must create the contract based on a purchase invoice – as described under [To create a purchase contract from a document](@DC-86#to-create-a-purchase-contract-from-a-document). This automatically links the contract with the invoice, and adds the following two values to the **Document Header** section of the document journal for the selected invoice:

* In the **Type** field, the value **Purchase Contract** is added.
* In the **No.** field, the contract number is added.

### Manual linking

To manually link the contract with the invoice, you must add the same two values by following these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the **PURCHASE** code to open the document journal.
1. In the list of documents, select the invoice that you want to link with the contract.
1. On the action bar, click **Purchase Contract** > **Select Purchase Contract**.
1. On the **Purchase Contract Selection** page, select a contract. On the **Match Overview** FastTab, the **Amount to Match**, **Matched Amount**, and **Difference** fields help you select the right contract – whether the document lines are recognized or not.

This links the contract with the invoice, which can then be registered as a contract invoice.

## To register an invoice as a contract invoice

Once you've linked a contract with an invoice as described above, you can register the invoice as a contract invoice in Business Central. To do this, simply [register the invoice](@DC-67) as any other invoice. This automatically inserts the lines of the contract into the invoice. The lines are displayed on the **Lines** FastTab of the **Purchase Invoice** page, under a top line that indicates the number of the purchase contract from which the lines originated.

> [!NOTE]
> The lines inserted into the invoice are exact copies of the lines in the linked contract, with the amounts calculated based on the state of the **Distribute Document Amount** setting on the **Purchase Contract Setup** page. If the amounts of the invoice and the contract differ, a dialog notifies you of this, and you have to perform any subsequent steps manually to confirm that everything is in order.

## To create a contract invoice using the posting setup

You can automate the linking process using the posting setup, which enables you to decide how amounts are posted for incoming invoices when they're registered. By specifying that the amounts must be transferred from a specific purchase contract for all invoices using the selected template, you enable Document Capture to automatically create a link between the invoices and the specified contract during invoice registration. To do this, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the **PURCHASE** code to open the document journal.
1. In the list of documents, select the invoice that you want to register as a contract invoice.
1. On the action bar, click **Template** > **Accounts for Amounts**.
1. On the **Amount Excl. VAT** field line, under **Type**, select **Purchase Contract**.
1. Under **No.**, select the contract that you want to link with the selected invoice and with all other invoices using the same template.
1. Close the **Accounts for Amounts** page to return to the document journal.
1. On the action bar, click **Process** > **Register** to register the invoice.

This automatically links the invoice with the selected contract and inserts the lines of the contract into the invoice. The lines are displayed on the **Lines** FastTab of the **Purchase Invoice** page, under a top line that indicates the number of the purchase contract from which the lines originated.

> [!NOTE]
> The lines that are inserted into the invoice are exact copies of the lines in the linked contract, with the amounts calculated based on the state of the **Distribute Document Amount** setting on the **Purchase Contract Setup** page. If the amounts of the invoice and the contract differ, a dialog notifies you of this, and you have to perform any subsequent steps manually to confirm that everything is in order.

## Related information

[Creating Purchase Contracts](@DC-86)  
[Purchase Contract Approvals](@DC-87)  
[Approving Contract Invoices](@DC-89)  
[Viewing the Purchase Contract Archive](@DC-90)  