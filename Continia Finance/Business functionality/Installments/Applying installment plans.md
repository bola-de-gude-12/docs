---
title: Applying installment plans in Continia Finance
date: 17-03-2025
description: Learn how to set up scheduled payment for specific customers/vendors, purchase orders and invoices and open entries.
id: CF-132
lang: en
---

# Applying Installment Plans

If a customer requests to divide the payment of an invoice into installments, the Installment module in Continia Finance can facilitate this process quickly and efficiently. You can also implement [installments using templates](@CF-102) for various document types, including purchase orders and invoices. This article provides step-by-step instructions on setting up installment plans for both customers and vendors, as well as how to apply them to purchase orders and existing ledger entries.

## To set up an installment plan for a customer or vendor

To automatically offer a customer or vendor the option to pay using a specific Installment Template on every invoice, you can assign the template directly to the customer or vendor card. This allows the customer or vendor to pay in split payments for every invoice they receive.

To add an installment plan for a customer or vendor:

1. For example, choose the {{search}} icon, search for **Customers** and select the related link.
2. Open the customer card of the customer you want to assign an installment template to. 
3. On the **Customer Card**, navigate to the **Continia Finance** FastTab, Under the **Installment Payments** section, in the **Installment Template** field, select the desired template. From now on, whenever you send this customer an invoice, the installment template is applied automatically.

## To set up an installment plan on orders or invoices

If you want to offer split payment options in a purchase order or a sales invoice, for example, you can set up an installment plan.

To set up an installment plan on an order:

1. For example, on the **Purchase Order** page, on the action bar, select the **Continia Finance** tab.
1. Select **Installment Plan**.
1. On the **Installment Plan** page, you can either manually enter details for a one-time installment plan or choose a predefined installment template by selecting **Use Template** from the action bar.
1. Once the installment plan is set up, you can preview the installment plan consequences by selecting **Post** > **Preview Posting**.
1. Post the order.

## To set up an installment plan on a journal line

You can set up an installment plan on any journal line. Just make sure that **Document Type** is set to **Invoice** and **Account Type** to **Customer** or **Vendor**. 

To set up an installment plan on a journal line:

1. For example, on the **General Journals** page, select **Daily**.
1. Select the line for which you want to set up an installment plan.
1. In **Installment Template Code**, select a code. Or you can create a new code by selecting **New**.

In the **Installment Plan Lines** FactBox in the right side of the screen, you can view the distribution of the installment plan.

You have the option to adjust your installment plan by selecting **Continia Finance** > **Installment (Lookup)** in the action bar on a journal page.

## To set up an installment plan on an entry directly

In addition to purchase orders and invoices, Continia Finance allows you to create installment plans for any existing vendor or customer ledger entry. This flexibility is useful when you want to apply installment payments after a transaction has been booked.

> [!IMPORTANT]
>
> When setting up an installment plan for a booked transaction, it is crucial to assign an installment account to the vendor or customer posting group. This account is necessary for recording G/L entries when you process and post installment payments related to that entry.

To set up an installment plan on an entry:

1. For example, open the **Vendor Ledger Entries** page, and, in the action bar, select **Continia Finance** > **Installment**.
2. On the **Installment Plan** page, enter information for split payments with a one-time installment plan – or select an installment template by selecting **Use Template** in the action bar.
3. In the action bar, select **Post**.  
4. On the **Installment Plan** page, enter the split payment details for a one-time plan or select an installment template by choosing **Use Template** from the action bar.
5. Once the installment plan is set up, select **Post** in the action bar.
6. A confirmation message appears: *Do you want to create Installment Entries?* Select **Yes**. The system automatically closes the original entry and generates the installment entries.

## To delete an installment plan
To delete an existing installment plan:

1. Choose the {{search}} icon, search for **Installment Plan** and select the related link.
2. On the **Installment Plan** page, select the installment plan you want to delete.
3. In the action bar, select **Delete**.
4. In the popup that appears, select **Yes** to confirm the deletion.

## To view an installment plan

To view the terms of a customer's installment plan:

1. Choose the {{search}} icon, search for **Customer Agreement of Installment** and select the related link.
2. On the **Options** FastTab, select a document type, document number, and, optionally, the reminder terms code related to the installment agreement.
3. You can then share, print, or preview the installment plan.
