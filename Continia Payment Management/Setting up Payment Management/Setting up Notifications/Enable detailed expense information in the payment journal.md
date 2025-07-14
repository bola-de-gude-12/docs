---
title: Adding detailed expense information in the payment journal
description: View Expense Management documents in Payment Management
date: 10-04-2025
id: PM-332
lang: en
---

# Adding detailed expense information to the Payment Journal

With the integration between Payment Management and Expense Management, you can easily access data from expense documents in the payment journal. If you enable the Payment Notification setting, Expense Management sends the IDs of all the sub-documents (e.g., expense reports, travel expenses, mileage expenses, etc.) that are being processed to Payment Management so that the user can see which expense documents have been reimbursed to their bank account.

Before using this feature, ensure the following: 

- Verify subscriptions – make sure both Expense Management and Payment Management are installed and have active subscriptions. 

- Business Central versions and the Continia Core Connectivity app - make sure you're using Business Central 2020 or a later version, as this feature is only available in these versions. The integration between Expense Management and Payment Management also requires the Continia Core Connectivity extension app, which is automatically installed with the update to Business Central 2020 and later versions. 

To enable expense details in the payment journal:

1. Use the ![Search for page or report](https://docs.continia.com/images/search_small.png) icon and search for **Payment Notification Setup**, then select the related link.
2. On the **General** FastTab, enable the **Enable Payment Notification Event** setting. The system will now send the IDs of all expense reports, individual expenses, mileage expenses, and per diem expenses from Expense Management to Payment Management for better tracking. 

