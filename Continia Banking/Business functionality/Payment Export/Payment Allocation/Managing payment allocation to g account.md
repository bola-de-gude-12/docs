---
title: Setting up Payment Allocation for a G account in Continia Banking
description: Learn how to allocate vendor payments to specialized bank accounts, such as G accounts. 
date: 12-06-2025
id: CB-219
lang: en
---
# Setting up payment allocation for a G account

Payment allocations allow payments to be divided into specific categories, such as taxes and social security, to comply with country-specific regulations. For example, in the Netherlands, it's required to separate these components when paying (sub-)contractors.

G accounts are designated bank accounts used to manage tax and social security payments. These accounts ensure that funds intended for tax or social security purposes and kept separate from general vendor payments.

> [!IMPORTANT]
>
> You can enable Payment Allocation from the Continia Feature Management page. Currently, it supports processing G accounts and their associated payment allocations.

This article provides instructions on how to set up payment allocations for G accounts, configure them for specific vendors, and manage the allocations during payment processing. It also covers how to undo an allocation if needed.

## To set up the g account fields

A g account is a specialized bank account used in the Netherlands, specifically designed to hold funds for purposes such as guaranteeing the payment of taxes or social security contributions. Setting up a g account in Continia Banking enables the creation of payment allocations, allowing a single entry to be split into different payments.

To set up the g account fields:

1. If you want to set up payment allocations for a specific vendor, search ({{search}}) for and select **Vendors**.

2. Select the vendor that you want to add the g account to and on the action bar, select **Related** > **Vendor** > **Payment Allocations**

3. On the **Payment Allocations** page, fill in the following fields:

   * **Account Type** - prefilled with the vendor.
   * **Account No.** - specifies the account number associated with the selected account type for payment allocation.
   * **Type** - related to the payment allocation type. You can set up different types on the page. For example, a g account type. 
   * **Description** - provides a brief description of the payment allocation type for reference.
   * **Calculation type** - defines how the payment allocation is calculated. Currently, only percentage-based allocation is available.
   * **Calculation Base Amount** - specifies the base amount used for calculating the payment allocation.
   * **Recipient** - specifies the default bank account the vendor uses for the payment allocation  such as a vendor or financial institution. Currently, because only payment allocations to g accounts are supported, only a g account can be selected as the recipient. Specifies the recipient of the allocated payment. For example, if a vendor must allocate 10% of payments to a g account, the system automatically transfers this portion. In cases where payments go to a financial institution, a dedicated account can be set up to handle these transactions, reducing the need to configure payment allocations for each vendor individually.

   When suggesting vendor payments in the payment journal, the system will allocate the specified percentage to the designated G-account bank account and generate a corresponding allocation entry. For example, if the G account percentage is set to 10, whenever you make a payment to the vendor, 10% of the payment amount will be automatically reserved and transferred to the G account. 

## To undo a payment allocation

If a payment allocation was mistakenly posted, you can reverse it easily.

To undo a payment allocation:

1. Search ({{search}}) for and select **Vendor Ledger Entries**.
2. Locate the relevant entry and clear the checkmark from the **Allocation Payment** column.

This removes the allocation status, allowing for corrections or reposting as needed.

