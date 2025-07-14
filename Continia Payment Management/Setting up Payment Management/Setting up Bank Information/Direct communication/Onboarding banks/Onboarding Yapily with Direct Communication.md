---
title: Onboarding Yapily with Direct Communication
description: Information about the service provider Yapily and set up direct communication.
date: 15-07-2024
id: PM-268
lang: en
---

# Onboarding Yapily to use Direct Communication

{{include "yapily-fees"}}

To integrate with your United Kingdom-based bank, Payment Management uses Yapily, a secure open banking API infrastructure that provides payment services and enriched financial data. 

Payment Management integrates seamlessly with Yapily, and you can download your bank account statements and initiate payments directly from Microsoft Dynamics 365 Business Central.

> [!IMPORTANT]
>
> To enable users to utilize open banking via Yapily, you'll likely need to grant additional privileges to existing roles or create a new custom role for assignment. Please refer to your bank's articles or contact them for detailed instructions on how to give access to Open Banking providers.

## Yapily Connect

We've partnered with the open banking platform [Yapily](https://www.yapily.com/) to integrate with banks in the United Kingdom. Yapily enables companies to share financial data and access payment infrastructure. 

> [!NOTE]
>
> Connecting banks through Yapily is only supported for Business Central version 24 or higher.

{{include "yapily-payments"}}

Every [payment through Yapily](@PM-268) requires authentication. If you use Yapily Connect with your Payment Management solution, you are informed of making the connection to Yapily Connect, and by proceeding, you agree to the [Yapily terms and conditions](https://www.yapily.com/legal/yapilyconnect-terms-and-conditions).

## To prepare for direct communication through Yapily

Before you can establish direct communication with your bank through Yapily, it is necessary to grant Yapily the required permissions. For more information about granting permissions, please contact your bank or refer to the [Preparing for Direct Communication Through Yapily](@PM-397) article. 

## To set up direct communication with Yapily

To use the services of Yapily, go through the steps of the assisted Assisted Setup guide **Set up Bank Account** in Payment Management. 

1. In Business Central, select the {{search}} icon, enter **Bank Account Setup**, and select the related link.

1. Select **Next** to start the assisted setup.

1. On the **Bank Accounts** page, select an existing bank account or create a new one.

1. In the **Communication** column, ensure that **Direct Communication** is selected for the bank account, and then select **Next**.

1. On the **Choose Bank Account Type** page, select the account type, OK, and **Next**.

1. The fields on the Bank Account Setup page are prefilled with information already available in Business Central. You can change the entries if necessary. Continia uses the **Contact name** and **Contact email** fields to send notifications related to the Know Your Business (KYB) verification process that verifies the ownership of the bank account. 

1. You can enable the **Operating address (if different**) setting to add an alternate address.

1. Select **Next**.

1. On the **Authenticate connection** page, select **Authenticate the connection**. You are now directed to the login page of your bank. 

1. Log in to your bank, select one or multiple accounts, and select **Confirm**. A token is sent to Business Central. Continia uses this token to start the communication with your bank account.

1. Select **Next**. Now, you can download account statements, making payments possible through direct communication from Business Central with the bank. 


## To download the account statements

The bank account reconciliation using Yapily uses standard Payment Management reconciliation functionality. For instructions on how to set up the bank accounts reconciliation, refer to the [Setting up Statement Intelligence](@PM-35) article.

Reconciling bank accounts with Statement Intelligence makes it possible to import bank statements from Yapily directly into the bank accounts reconciliation and automatically match statement lines with posted Bank Account Ledger Entries. For more information, refer to the [Reconciling Bank Accounts](@PM-251) overview.



## To send a payment with Yapily

Yapily lets you do bulk payments, single-line payments, and a mix of these. 

1. In Business Central, select the icon ![Search for page or report](/images/search_small.png), enter **Payment Journal**, and select the related link.

2. Open the relevant journal, and in the action bar, select **Prepare** > **Suggest Vendor Payments**.

3. Select a line, and select **Bank** > **Export Payments**.

4. On the **Payments** page, select a payment, and in the **Action** column, select **Authenticate Payment**. On your first authentication, you are informed of connecting to Yapily Connect. Enable the **Don't show this again** setting to prevent this message from displaying for every payment.

   You can send bulk payments and combine multiple lines or single-line payments.

5. Log in to the bank and select the accounts. 

6. If you select **Ok** to confirm the payment, it disappears from the list, and in the Payment Journal, the status will be set to **Sent**.

## To revoke Yapily Connect consent

At any time, you have the option to withdraw your consent for using Yapily Connect.

 To revoke the Yapily token:

1. Use the {{search}} icon and search for **Banks**, and then select the related link.
2. In the **Banks** overview, choose the bank from which you want to revoke the token.
3. On the action bar, select **Connection** > **Revoke Token**.

   > [!IMPORTANT]
   >
   > When you select Revoke Token, your direct access to the bank will cease immediately. Therefore, you must make sure that there are no pending transactions in the Payment journal awaiting processing. Also, verify that there are no missing statements that you need to retrieve. If you don't follow these steps, these tasks must be done manually.
4. Select **OK** to confirm the deletion of the token.

If, at some point, you decide to reconnect with the bank, refer to the steps outlined in [To set up direct communication with Yapily](#to-set-up-direct-communication-with-yapily).