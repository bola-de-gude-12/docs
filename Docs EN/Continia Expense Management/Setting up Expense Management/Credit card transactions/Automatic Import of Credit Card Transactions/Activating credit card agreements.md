---
title: Activating Credit Card Agreements
date: 21-11-2024
description: Learn how to set up a bank agreement to receive transactions automatically.
id: EM-32
lang: en
---

# Activating Credit Card Agreements

In Expense Management, you can import credit card transactions. This will autogenerate an expense prefilled with all the information from the transaction, such as amount, currency, date, and description.

> [!IMPORTANT]
> Before you attempt to activate a bank agreement in Expense Management, an agreement with the bank must be in place beforehand.

Import of credit card transactions can be done both manually and automatically. In the latter case, you need to set up an agreement with a bank to start receiving transactions automatically.

To set up a bank agreement to receive transactions automatically, follow the steps below:

1. Choose the {{search}} icon, enter **Bank Agreements**, and then choose the related link.
1. On the action bar, select **Request New Agreement**.
1. In the assisted setup guide, select **Next**.
1. On the next page in the assisted setup guide, fill out the fields with transaction details, and then select **Next**.
1. On the confirmation, select **Finish**. 

The request will now be processed by the Continia Support, which will take 1-2 work days. If the provided information matches a transaction, you will start to see transactions coming into the system. If the information does not matches any transactions, the request will be rejected. You can always see the current status of an activation by selecting **Activation Request Log** on the **Bank Agreements** page.

> [!IMPORTANT]
> When a credit card agreement has been activated, you need to synchronize with Continia Online for transactions to begin downloading to Expense Management.
>
> It's recommended to run synchronizations using a job queue. See the article [Setting up Job Queues](@EM-65).

> [!NOTE]
> You can only activate a bank agreement in a production environment. If you want to import transactions in a demo environment, you can do this manually. Read more about this in the article [Manual File Import](Manual file import.md).