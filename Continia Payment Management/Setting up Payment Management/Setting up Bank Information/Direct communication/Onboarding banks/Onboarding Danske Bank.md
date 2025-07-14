---
title: Onboarding Danske Bank
date: 08-08-2022
description: Onboarding Danske Bank with direct communication
id: PM-178
lang: en
---

# Onboarding Danske Bank with Direct Communication

As a customer of Danske Bank, you can use the Danske Bank District service to send and receive bank files automatically between Danske Bank and Microsoft Dynamics 365 Business Central using the Payment Management Direct Communication service. 

This article covers the steps to set up direct communication between Danske Bank District and Payment Management. 

## To request access to Danske Bank District

Before you begin setting up direct communication in Payment Management, please contact your bank Cash Management adviser and request access to Danske Bank District with the following modules:

- Cash Management - Account Information
- Cash Management - Payments
- Cash Management - File Transfer
- EDI Web Services 

> [!IMPORTANT]
>
> When the agreement with Danske Bank has been approved, you'll receive a letter with a user number and pin code. You must use this login information to order the bank files and set up direct communication.

## To order bank files in Danske Bank District

When the subscription to Danske Bank District has been approved, log in to Danske Bank District using the login information you received from Danske Bank and order the files you want to use. It can take up to a day before you receive the files as they are generated during the night or early morning and not by request. 

For an overview of the files you need to order, see the article about [Danske Bank](@PM-118).

## To set up bank accounts to use direct communication

When you have received the user number and pin code in a letter from Danske Bank, you can run the assisted Bank Account Setup guide to set up your bank account to use direct communication.

1. In Business Central, select the icon ![Search for page or report](/images/search_small.png), enter **Bank Account Setup**, and select the related link.

1. Select **Next** to begin the assisted setup.

1. On the **Bank Accounts** page, select an existing bank account, or create a new one by selecting **New Bank Account**.

1. In the **Communication** column, ensure that **Direct Communication** is selected for the bank account, and then select **Next**.

   > [!NOTE]
   >
   > If any bank account information is missing, you may be prompted to verify or update the information.

1. On the **Create certificate for direct communication** page, enter the user number and pin code you received from the bank and select **Next**.

1. You have now set up the bank account to use direct communication. Select **Next**, and you'll see the bank account status has changed to *Ready*. 

When you receive the bank files from Danske Bank District, you are ready to start using Payment Management Direct Communication.  



## Recommended next steps

When you have set up your bank accounts to use direct communication, you can continue the setup of Payment Management by following the recommended steps as specified in the [Quick guide to setting up Payment Management](@PM-226). 

