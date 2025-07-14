---
title: Managing cash discounts
description: How to manage cash discounts in the payment journal
date: 23-06-2022
id: PM-86
lang: en
---

# Managing Cash Discounts

Some vendors offer cash discounts when paying within a specified period according to the due date. In this case, Payment Management supports making vendor payment suggestions based on the cash discount setup.

Prerequisites for using cash discounts in the payment journal:

* To use cash discounts, you must determine how you wish to manage due dates and payment discounts on the **Payment Terms** setup page. You can read more about [setting up payment terms](https://docs.microsoft.com/en-us/dynamics365/business-central/finance-payment-terms) on Microsoft Docs. When payment terms have been defined, the payment terms codes can be assigned to the vendor card under the FastTab **Payments**.

To use the cash discount when making vendor payment suggestions:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Journals**, then select the related link. This opens a payment journal.
1. On the page header, in the **Batch Name** field, choose the payment journal you want to enable cash discounts for.
1. On the payment journal, navigate to the action bar and select **Prepare** > **Payment Journal Setup**. 
1. On the Payment journal setup page, go to the **Posting Date** section, and enable the **Find Payment Discounts** setting.

>[!NOTE]
>Support for payment discounts has now been enabled for the payment journal. Payment Management will use the cash discount setup to determine the posting date when creating vendor payment suggestions. If a payment discount has been applied to a payment, the **Payment Discount Applied** check box on the payment journal line is selected.
>  


## Related information

[How to set up payment terms](https://docs.microsoft.com/en-us/dynamics365/business-central/finance-payment-terms) (Microsoft Docs)

