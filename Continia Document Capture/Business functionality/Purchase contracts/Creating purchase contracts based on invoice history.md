---
title: Creating purchase contracts based on invoice history in Document Capture
date: 23-07-2025
description: How to create purchase contracts based on invoice history.
id: DC-163
lang: en
---

# Creating purchase contracts based on invoice history

Using artificial intelligence (AI), the Purchase Contracts module can detect patterns in your incoming invoices and determine if any of them are recurring and suitable for automatic handling by a purchase contract. If this is the case, a message at the top of your document journal notifies you that it might be a good idea to let the Purchase Contracts module handle this and similar future invoices automatically.

To provide a personalized experience, the notification differs depending on whether you've already enabled the Purchase Contracts module – and so do the various user flows that the notification invites you to initiate:

* [The flow when the Purchase Contracts module has been enabled](#with-the-purchase-contracts-module-enabled)
* [The flow when the Purchase Contracts module has not been enabled](#with-the-purchase-contracts-module-disabled)

If you select any of the actions suggested by the notification, you're guided through the process – as described in the sections below.

The module automatically suggests one or more purchase contracts based on the historical data of the identified recurring invoices. You can then choose to create a purchase contract right away based on the module's suggestion and prefilled data (provided that you've already enabled the module), or you can open an overview of all possible purchase contracts identified by the module to see if everything checks out.

> [!NOTE]
> This feature is currently only available for online versions of Continia Document Capture.

## With the Purchase Contracts module enabled

If you've enabled the Purchase Contracts module when potentially recurring invoices are detected, the following notification appears at the top of the document journal:

![Module activated](/images/DC/PurchaseContracts/module-activated.png)

From this notification, you can carry out the following actions:

<br>

| Action | Description |
| --- | --- |
| **Create purchase contract** | Opens [the **Create Purchase Contract** page](#the-create-purchase-contract-page), which enables you to create a purchase contract. |
| **View similar invoices** | Opens [the **Suggested Purchase Contracts** list](#the-suggested-purchase-contracts-list). |
| **Don’t show this again** | Shows a message that allows you to choose how to disable the notification: <ul><li>**Don’t ask about this invoice again** - disables this notification for the user and for this particular document template.</li><li>**Don’t show this notification again** - disables this notification for the user and for all document templates.</li></ul> |

### The Create Purchase Contract page

The **Create Purchase Contract** page allows you to create a purchase contract. If you open the page from the notification at the top of the document journal or from [the **Suggested Purchase Contract** page](#the-suggested-purchase-contract-page), the Purchase Contracts module attempts to fill out as many fields as possible – including **Description**, **Purchaser Code**, and **Invoicing Period Code** – based on data from the invoices that have been [identified as recurring and related and grouped together as such](#the-technology-and-criteria-behind).

To create a purchase contract, update the text/values of the prefilled fields (if necessary), fill out any remaining fields as needed, and select **OK** when you're done. This creates the contract and add it to the list of contracts on the **Purchase Contracts** page. If you enabled **Open Purchase Contract** on the **Create Purchase Contract** page, the new contract opens once you select **OK**.

## With the Purchase Contracts module disabled

If you haven't enabled the Purchase Contracts module when potentially recurring invoices are detected, the following notification appears at the top of the document journal:

![Module not activated](/images/DC/PurchaseContracts/module-not-activated.png)

From this notification, you can carry out the following actions:

<br>

| Action | Description |
| --- | --- |
| **Learn more** | Opens [the **Try Purchase Contracts** assisted setup guide](#the-try-purchase-contracts-assisted-setup-guide), which provides an overview and guides you through the process of starting a Purchase Contracts trial. |
| **View similar invoices** | Opens [the **Suggested Purchase Contracts** list](#the-suggested-purchase-contracts-list). |
| **Don’t show this again** | Disables the notification for the user and for all document templates. |

> [!NOTE]
> When the Purchase Contracts module is not enabled, you can also open **Try Purchase Contracts** from the **Continia Solution Management** page:
> 
> 1. Search ({{search}}) for and select **Continia Solution Management**.
> 1. In the **Subscription Details** FactBox on the right, under **Subscription Modules**, click **Try it out** to open [the **Try Purchase Contracts** assisted setup guide](#the-try-purchase-contracts-assisted-setup-guide).

### The Try Purchase Contracts assisted setup guide

The **Try Purchase Contracts** assisted setup guide provides an overview of the benefits that you may enjoy with the Purchase Contracts module.

The first step of the guide includes a **\{number} of your vendors are perfect for trying out the module** link, notifying you of the total number of vendors that have been identified to have sent you potentially recurring invoices suitable for contract handling. If you click this link, [the **Suggested Purchase Contracts** list](#the-suggested-purchase-contracts-list) opens. This either provides an overview of all potential purchase contracts or allows you to create one from scratch, depending on whether you have enabled the Purchase Contracts module.

Selecting **Next** brings you to the second step of the assisted setup guide. Here, you can select **Start Trial** to start a free 30-day trial of the Purchase Contracts module. This activates the trial and does one of the following:

* If you opened the guide from the notification at the top of the document journal, you're returned to the document journal – where you can carry on as usual.
* If you opened the guide from **Continia Solution Management**, a dialog is displayed, asking if you would like to create a purchase contract right away. Click **Yes** to open [the **Suggested Purchase Contracts** list](#the-suggested-purchase-contracts-list).

##  The Suggested Purchase Contracts list

The **Suggested Purchase Contracts** list is a page that lists all possible purchase contracts [based on job queue analysis](#the-technology-and-criteria-behind).

On the action bar, you can select **View Details** to open [the Suggested Purchase Contract page](#the-suggested-purchase-contract-page) for the contract you've selected in the list of possible contracts. This page provides a more detailed view of the suggested contract and allows you to create a new contract based on this, provided that you've enabled the Purchase Contracts module.

If you've enabled the Purchase Contracts module, the following actions are also available on the action bar:

* **Create Purchase Contract** - opens [the **Create Purchase Contract** page](#the-create-purchase-contract-page), from where you can then create a purchase contract based on the contract suggestion.
* **Open Purchase Contract** - opens the **Purchase Contract** card of any pre-existing contract that's similar to the selected invoice. The action is only available if such a contract has already been created in the Purchase Contracts module.

> [!NOTE]
> These two actions are only selectable if the Purchase Contracts module has been enabled. If it hasn't been enabled, the actions aren't visible at all on the action bar.

The list includes the following columns:

<br>

| Column header | Description |
| --- | --- |
| **Buy-from Vendor No.** | The number of the vendor who sent the recurring invoices that the suggested contract is based on. This number is used for the grouping together of the invoices. |
| **Buy-from Vendor Name** | The name of the vendor who sent the recurring invoices that the suggested contract is based on. This name is used for the grouping together of the invoices. | 
| **Invoicing Period** | The invoicing period that the system has predicted based on the document dates of the grouped invoices. |
| **Currency Code** | The currency of the suggested contract. The invoices that the suggested contract is based on are also grouped using this value. |
| **Latest Invoice Amount** | The amount of the latest invoice in the group of invoices that the suggested contract is based on. This amount is excluding VAT. | 
| **Latest Invoice Date** | The date of the latest invoice in the group of invoices that the suggested contract is based on. |
| **Existing Contract** | An indication of whether a similar purchase contract already exists in the system. This column isn't visible if the Purchase Contracts module hasn't been enabled. If the checkbox has been checked, the **Open Purchase Contract** action on the action bar is enabled. |
| **No. of Invoices** | The number of invoices that have been grouped together to form a possible purchase contract. |

## The Suggested Purchase Contract page

The **Suggested Purchase Contract** page provides an overview of the purchase contract that's been suggested as a possibility, based on the recurring invoices that have been detected. This includes a document viewer on the right, which displays the document that you've selected in the list under **Recurring Invoices** (see below).

On the action bar, click **Create Purchase Contract** to open [the **Create Purchase Contract** page](#the-create-purchase-contract-page), from where you can then create a purchase contract based on the contract suggestion.

> [!NOTE]
> This is only possible if the Purchase Contracts module has been enabled. If it hasn't been enabled, the **Suggested Purchase Contract** page only provides an overview, and no actions are available on the action bar.

On the **General** FastTab, you find the basic details of the suggested contract, including the following fields:

<br>

| Field | Description |
| --- | --- |
| **Buy-from Vendor Name** | The name of the vendor who sent the recurring invoices that the suggested contract is based on. This name is used for the grouping together of the invoices. | 
| **Buy-from Vendor No.** | The number of the vendor who sent the recurring invoices that the suggested contract is based on. This number is used for the grouping together of the invoices. |
| **Currency Code** | The currency of the suggested contract. The invoices that the suggested contract is based on are also grouped using this value. |
| **Invoicing Period** | The invoicing period that the system has predicted based on the document dates of the grouped invoices. |

The **Recurring Invoices** FastTab lists the posted purchase invoices that have been [identified as recurring and related](#the-technology-and-criteria-behind). The list only includes the three most recent of these invoices, but to view all invoices that have been grouped together, you can go to the FastTab title bar and select **All Invoices**. From the FastTab title bar, you can also select **Open Invoice** to open any of the invoices in the list as a **Posted Purchase Invoice**.

The list includes the following columns:

<br>

| Column header | Description |
| --- | --- |
| **No.** | The number of the posted purchase invoice as registered in Document Capture. |
| **Vendor Invoice No.** | The invoice number as registered internally by the vendor (typically stated in the purchase invoice itself). |
| **Purchaser Code** | The purchaser code as stated in the invoice. |
| **Document Date** | The date when the invoice was issued, as stated in the invoice itself. |
| **Amount** | The total amount of the invoice, excluding VAT. |
| **Amount Including VAT** | The total amount of the invoice, including VAT. |

## The technology and criteria behind

The feature suggests possible purchase contracts based on recurring invoices that it has identified in the system. Recurring invoices are invoices that you receive at a fixed frequency (for example, on a monthly basis) and which are essentially identical or at least very similar. To identify any such recurring invoices, job queues are run every 24 hours. These job queues are executed at midnight and only run for 30 minutes to minimize system interruptions. If a job queue is unable to perform a full analysis within the 30-minute window, it'll continue where it left off next time, ensuring that all invoices are analyzed.

Regarding scope, the job queues:

* Analyze all invoices received within a period of three years.
* Include posted invoices but not canceled invoices.
* Exclude invoices from blocked vendors.
* Factor in inflation and other changes by allowing for a maximum price difference of:
    * 3% for monthly contracts.
    * 14% for annual contracts.

When analyzing your received invoices within this scope, job queues group related invoices together using the following criteria:

* Vendors must match.
* Currency codes must match.
* Amounts must match (within the acceptable variance percentages mentioned above).
* Document dates must match, meaning that they must follow a sequential pattern within the identified invoicing period.
* Lines must match (regarding the fields **Type**, **No.**, **Quantity**, **Unit Cost**, and **Amount**).
* It must be possible to determine the invoicing period based on invoice dates.
* The number of invoices grouped together for the identified invoicing period must be sufficient:
    * For annual, biannual, and quarterly contracts, two invoices are required.
    * For monthly contracts, three invoices are required.
* The last invoicing period must have an invoice. <br> <div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Note</span></p><p>For example, if related invoices are identified for June, July, and August but no similar invoice exists for September, the system determines that these invoices are no longer recurring – and no contract will then be suggested based on these. </p></div>

If these criteria are met by a number of invoices, these invoices are grouped together and identified as recurring and related, and this invoice group will then form the basis of a possible contract.

## Related information

[Creating purchase contracts](@DC-86)  
[Purchase contract approvals](@DC-87)  
[Creating contract invoices](@DC-88)  
[Approving contract invoices](@DC-89)  
[Viewing the Purchase Contract Archive](@DC-90)  