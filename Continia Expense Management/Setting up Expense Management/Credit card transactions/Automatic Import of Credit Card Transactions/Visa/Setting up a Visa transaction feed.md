---
title: Setting up a Visa Transaction Feed
date: 22-10-2024
description: Details on how to set up a Visa transaction feed to Continia Expense Management
id: EM-282
lang: en
---

# Setting up a Visa Transaction Feed 

This article describes how to set up a transaction feed to Continia Expense Management, so that your Visa transactions can be imported directly into Expense Management.

> [!NOTE]
> The transaction feed must be set up by your bank using the below guide, which describes a process that's external to Continia. The guide may therefore not be entirely up to date at all times, although Continia generally strives to make sure that it is.

## To set up a transaction feed to Expense Management

As a user of Expense Management, you must reach out to your banking relationship manager and request that your VCF feed be sent directly to Continia Software. Refer the banking relationship manager to this guide.

As a banking relationship manager, to set up a Visa transaction feed to Expense Management on behalf of the user's organization, follow these steps:

1. Open Visa Business Solution (VBSE).
1. Select **Manage Companies**.
   
   ![Manage Companies](/images/EM/manage-companies.jpg)
1. Locate the user's organization by searching for it.
   
   ![Locate Organization](/images/EM/locate-organization.jpg)
1. Select **Edit Company**.
   
   ![Edit Company](/images/EM/edit-company.jpg)
1. Select **Services**, and then select **Edit**.
   
   ![Edit Services](/images/EM/edit-services.jpg)
1. In the **Data Delivery** section, select **Continia** as the organization endpoint, and then select **Save**.
   
   ![Data Delivery](/images/EM/data-delivery.png)
   
   > [!NOTE]
   > If you don't see Continia on the list, please reach out to Visa Inc. and request that Continia be enabled for this bank.

Once the subscription has been activated, Visa transaction data will start being delivered to Continia within 2–4 hours.

You're now ready to set up a bank agreement in Expense Management to receive Visa transactions automatically. For information on how to do this, see [Activating Credit Card Agreements](@EM-32).

## See also

[Importing Visa Transactions](@EM-281)  