---
title: Manual Payments
description: Information on how to pay vendors with the payment method Manual
date: 15-10-2021
id: PM-15
lang: en
---

# Manual Payments

As implied by the name, manual payments are handled manually without involving the bank for the bank transaction. Using the payment method **Manual**, you will still be able to process and post the payments in the system with Payment Management. 

The payment method code **Manual** can be specified either on the vendor card, in case you're dealing with a vendor who is always paid manually, or directly on the purchase document. Once you've made a manual payment and posted the purchase document, you can generate a payment suggestion in the payment journal for the payment to be posted in the system. Manual payments will be created with the status *Manual*, as no validation against the bank's requirements to payment information is needed for these payments.

When you export or send payment lines from the payment journal, payment lines with the payment method code **Manual** will not be exported. This ensures that manual payments are not sent to the bank, while it still allows you to post the payment lines in the payment journal along with all your other payments.

## Confirm posting of manual payments

To ensure that a payment is not registered as a manual payment by mistake, you can enable Payment Management to notify the user about manual payments before posting a payment journal. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Management Setup**, then select the related link. In the FastTab **Purchase and Payments**, enable the action **Confirm Manual Payments**.

