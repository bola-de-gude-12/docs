---
title: Automatic Assignment of Item Charges
date: 30-04-2023
description:  How to have item charges automatically assigned to the lines of incoming documents according to predefined methods
id: DC-137
lang: en
---

# Automatic Assignment of Item Charges

Continia Document Capture can automatically assign item charges to the lines of an incoming document in accordance with a method you define in the relevant document template. In this way, any item charge that appears in an imported document can be split among the lines of that document, as specified by you in the template setup. Item charges can be assigned according to the following four methods:

* **Equally**
* **By amount**
* **By weight**
* **By volume**

These methods will be explained in more detail below, along with a more in-depth account of the functionality in general. The actual charges will be automatically assigned when you register the documents.

> [!NOTE]
> Matching against item charges is only supported when you match against receipt/return shipment lines.

## To set up the assignment of item charges

In order to have item charges automatically split between the lines of incoming documents, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. To open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself), and then choose **Edit** on the action bar.
1. On the **Document Category** page, on the **Templates** FastTab, select the template that you want to configure.
1. On the FastTab title bar, select **Edit** to open the template card.
1. On the **Purchase Documents** FastTab, go to **Item Charge Assignment Method**, and then select the method you want Document Capture to use when assigning item charges. For more details about the assignment methods, see [Understanding the methods](#understanding-the-methods) below.

Your selected method will now be used for every assignment of item charges in documents using this template, once you register the documents. The sections below explain how the [charges are actually distributed among the lines of each document](#understanding-the-methods) when assigned, and how you can [view this distribution](#to-view-assigned-item-charges).

## To view assigned item charges

Once you've registered a document with an item charge, the item charge is automatically assigned to the lines of the document according to your specifications in the setup, and the document page opens (for example, the **Purchase Invoice** page for invoices). To view the item charge assignment and check that this is correct, follow these steps:

1. On the **Lines** FastTab, in the list of document lines, select the one that says **Charge (Item)** under **Type**.
1. On the FastTab title bar, select **Line** > **Related information** > **Item Charge Assignment**.
1. This will open the **Edit - Item Charge Assignment (Purch)** page. In the **Amount to Assign** column, check that the item charge has been distributed among the lines as intended.

## Understanding the methods

To understand the different item charge assignment methods, consider the following example of an incoming document with an item charge:

* Three item lines
* Total amount excluding VAT: €1,000.00
* Total weight of all line items: 100.00 kg
* Total volume of all line items: 10.00 m<sup>3</sup>
* One item charge line with a quantity of 1 and an amount of €200.00

When this document is registered, the distribution of the item charge among the document's item lines will be as follows in the various scenarios:

> [!NOTE]
> Note that this distribution would have been the same if the item charge had been at header level rather than line level. Item charges are assigned to document lines in exactly the same way no matter if they're at line level or header level.

### Equal assignment

If you choose the item charge assignment method **Equally** in [the setup](#to-set-up-the-assignment-of-item-charges), the item charge will be distributed like this: 

<br>

| No. | Qty. to Assign | Amount to Assign |
| --- | :-: | :-: |
| Item 1 | 0.33 | €66.67 |
| Item 2 | 0.33 | €66.67 |
| Item 3 | 0.33 | €66.67 |

The item charge line has an amount of €200.00 and a quantity of 1, and these are both divided by three, as there are three item lines. As a result of this equal distribution, each of the item lines will be assigned an item charge of €66.67.

### Assignment by amount

If you choose the item charge assignment method **By amount** in [the setup](#to-set-up-the-assignment-of-item-charges), the item charge will be distributed like this: 

<br>

| No. | Line Amount Excl. VAT | Qty. to Assign | Amount to Assign |
| --- | :-: | :-: | :-: |
| Item 1 | €500.00 | 0.50 | €100.00 |
| Item 2 | €200.00 | 0.20 | €40.00 |
| Item 3 | €300.00 | 0.30 | €60.00 |

The assigned amount for each item line is calculated based on the line amount's proportion of the total amount. For example, item 1 has a line amount of €500.00, which is exactly half of the total amount of €1,000.00. The item charge line has an amount of €200.00 and a quantity of 1, and because half of 1 is 0.50, the amount to assign will be 0.50 × €200.00 = €100.00.

### Assignment by weight

If you choose the item charge assignment method **By weight** in [the setup](#to-set-up-the-assignment-of-item-charges), the item charge will be distributed like this: 

<br>

| No. | Gross Weight | Qty. to Receive (Base) | Qty. to Assign | Amount to Assign |
| --- | :-: | :-: | :-: | :-: |
| Item 1 | 2.00 | 5 | 0.10 | €20.00 |
| Item 2 | 10.00 | 4 | 0.40 | €80.00 |
| Item 3 | 5.00 | 10 | 0.50 | €100.00 |

The assigned amount for each item line is calculated based on the line item's weight and its proportion of the total weight of all line items. For example, item 1 has a total weight of 2.00 kg × 5 = 10.00 kg (the gross weight of each item unit multiplied by the number of units specified in **Qty. to Receive**), which is exactly one tenth of the total weight of all line items (100.00 kg). The item charge line has an amount of €200.00 and a quantity of 1, and because one tenth of 1 is 0.10, the amount to assign will be 0.10 × €200.00 = €20.00.

### Assignment by volume

If you choose the item charge assignment method **By volume** in [the setup](#to-set-up-the-assignment-of-item-charges), the item charge will be distributed like this:

<br>

| No. | Unit Volume | Qty. to Receive (Base) | Qty. to Assign | Amount to Assign |
| --- | :-: | :-: | :-: | :-: |
| Item 1 | 1.00 | 5 | 5.00 | €100.00 |
| Item 2 | 0.25 | 4 | 1.00 | €20.00 |
| Item 3 | 0.50 | 8 | 4.00 | €80.00 |

The assigned amount for each item line is calculated based on the line item's volume and its proportion of the total volume of all line items. For example, item 1 has a total volume of 1.00 m<sup>3</sup> × 5 = 5.00 m<sup>3</sup> (the volume of each item unit multiplied by the number of units specified in **Qty. to Receive**), which is exactly half of the total volume of all line items (10.00 m<sup>3</sup>). The item charge line has an amount of €200.00 and a quantity of 1, and because half of 1 is 0.50, the amount to assign will be 0.50 × €200.00 = €100.00.

## Related information

[Automatic Document Matching](@DC-70)  