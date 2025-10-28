---
title: Using payment means in eDocuments
date: 15-10-2025
description: How to configure payment means on the bank account, company, and customer levels.
id: DC-450
lang: en
---

# Using payment means in eDocuments

The Payment Means feature enables you to define payment methods when sending eDocuments, such as invoices or credit memos, from Microsoft Dynamics 365 Business Central.

This article guides you through the process of configuring payment means on the bank account, company, and customer levels.

## Using the default configuration

By default, the Payment Means configuration is taken from the **Company Information** page. That is, unless changes are made to the **eDocuments Payment Means Setup** (and applied on the desired level, such as customer or bank account), the payment means section in your electronic documents contains the following values:

- **Payment Means Code** - 42, that is, payment to bank account.
- **Payment Type** - Bank.

In this case, two values must be specified: **Bank Account No.** and **Bank Branch No.** If the **Company Bank Account Code** field on the invoice or credit memo is empty, those values are taken from the Company Information – otherwise, they’re taken from the specified bank account (e.g.: CHECKING).

Additionally, the default payment means doesn’t generate a payment ID. To do this, or to use values other than the values from the **Company Information** page, configure Payment Means as described in [Configuring custom payment means setups](#configuring-custom-payment-means-setups).

> [!IMPORTANT]
> If a payment means has the **Payment Type** set to **Bank**, the **Bank Account No.** and **Bank Branch No.** can’t be customized in the **Payment Means Setup**.

## Configuring custom payment means setups

It’s possible to configure custom payment means on the bank account, company, and customer levels. To do so, start by creating a default setup.

1. Search ({{search}}) for and select **eDocuments Payment Means Setup**.
2. On the **eDocuments Payment Means Setup** page, click **New** on the action bar.
3. On the **General** FastTab, enter the following details:
   * **Code** - the code that identifies the payment means setup. E.g.: FIK73.
   * **Description** - the text that describes the payment means setup. E.g.: FIK 73.
   * **Payment Means** - the desired payment means, selected from the **eDocuments Payment Means** table. Depending on the payment means selected, you may have to fill out additional fields. For more information, see [Managing and creating payment means](#managing-and-creating-payment-means).

This creates a configuration in the **eDocuments Payment Means Setup**. Like the default configuration, new configurations also use the **Bank Account No.** and **Bank Branch No.** from the **Company Information** page.

## Applying custom payment means setups

Custom payment means setups can be applied on the company, bank account, or customer levels.

> [!NOTE]
> If your company, bank account, and customer have a payment means setup configured, the most specific setup is used. That is, the payment means on the customer level overrides the payment means on the bank account level – which overrides the payment means on the company level.

### Company

To apply a custom payment means setup to a company:

1. Search ({{search}}) for and select **Company Information**.

1. On the **Company Information** page, on the **Payments** FastTab, click the three dots by the **Payment Means Setup** field.
2. Select the desired payment means setup.

The selected payment means becomes the new default, which is used if the **Company Bank Account Code** field on the invoice or credit memo is empty.

> [!NOTE]
> Only one configuration can be created per company.

### Bank account

To apply a custom payment means setup to a bank account:

1. Search ({{search}}) for and select **Bank Accounts**.
2. On the **Bank Accounts** page, select the desired bank account.
3. On the **Bank Account Card**, on the **General** FastTab, click the three dots by the **Payment Means Setup** field.
4. Select the desired payment means setup.

When you then set the **Company Bank Account Code** field of an electronic invoice or credit memo to this bank account, the payment means associated with it is used.

> [!NOTE]
> Only one configuration can be created per bank account.

### Customer

To apply a custom payment means setup to a customer:

1. Search ({{search}}) for and select **Customers**.
2. On the **Customers** page, select the desired customer. Note that this customer must be able to receive eDocuments.
3. On the **Customer Card**, on the eDocuments FastTab, click the three dots by the **Payment Means Setup** field.
4. Select the desired payment means setup.

When invoices and credit memos are sent to this customer, the payment means associated with it is used.

> [!NOTE]
> Only one configuration can be created per customer.

## Managing and creating payment means

When you import configuration files from Continia Online, several payment means become available. These payment means are pre-configured and ready to use, covering the most common options.

However, it’s also possible to create a payment means. To do so:

1. Search ({{search}}) for and select **eDocuments Payment Means**.
2. On the **eDocuments Payment Means** page, click **New** on the action bar.
3. Enter the following details:
   * **Code** - the code that identifies the payment means. 
   * **Description** - the text that describes the payment means.
   * **Type** - the type of payment means, selected from the dropdown list.
   * **Payment Means Code** - the payment means code, compliant with the UNCL4461 standards. For more information, see [Payment means code (UNCL4461)](https://docs.peppol.eu/poacc/billing/3.0/codelist/UNCL4461/) (Peppol list).