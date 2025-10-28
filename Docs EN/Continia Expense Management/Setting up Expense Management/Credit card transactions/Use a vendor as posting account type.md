---
title: Use a Vendor as Posting Account Type on Credit Card Transactions
date: 04-07-2024
description: Learn how to use a vendor as posting account type on credit card transactions
id: EM-248
lang: en
---

# Use a Vendor as Posting Account Type on Credit Card Transactions

With Expense Management, it's possible to post credit card transactions to a vendor. However, when doing that, you have to keep in mind that there are a few things you then *can't* do:

* You can't use expense reports.
* You can't post to the general journal. All documents (expenses, mileages, per diems) will be posted as purchase invoices instead of to the general journal. The system will create purchase invoices, which will have the status OPEN, and they must be approved and posted afterwards. A purchase invoice will be created for the bank/vendor for all expenses connected to credit card transactions, and all mileages, per diems, and cash/private expenses will create a purchase invoice for each Continia user (their vendor).

## Set a vendor as posting account type on credit card transactions

To set a vendor as posting account type on credit card transactions, follow these steps:

1. Go to **Expense Management Setup**.
1. In the **General** FastTab, disable **Expense Report**.
1. In the **Purchase Document Posting** FastTab, set **Expense Posting** to **Preferable Purchase Invoice**.

This might yield a popup message saying *When enabling "Preferable Purchase Invoice", you are disabling "Post Bank Transactions on Import.". Do you want to continue?*

Select **Yes**. This will disable posting at import.

Now you need to change the posting account type for the payment type for which you want to use a vendor as posting account:

1. Go to **Payment Types**.
1. Select the payment type for which you want to use a vendor as posting account.
1. In the **Posting** FastTab, set **Method** to **Post on a Business Account**.
1. Under **Posting Account**, set **Type** to **Vendor**.
1. In **No.**, select a business vendor via lookup.