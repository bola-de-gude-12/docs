---
title: Managing Balance Accounts for Different Currencies
description: How to set up payment balance account for different currencies.
date: 01-10-2024	
id: CB-41
lang: en
---

# Managing balance accounts for different currencies

Continia Banking lets you verify payment information and select the appropriate balance account for different payments. You can select a bank account or G/L account as a bank account for each currency. Additionally, you can specify a default bank account to use when no specific bank account is entered for a currency code.

To set up the payment bank account for different currency:

1. Search ({{search}}) for **Assisted Setup**.

2. Navigate to the **Continia Banking** section and select **Payment Balance Account Setup**.

3. In the **Bank Account** column, select the bank account you want to use. For example, if you just use one bank account, you select that bank account in the **Bank Account** column, and leave the **Currency Code** column empty. If you have a specific bank account that you want to use for payments in US dollars, in the **Currency Code** field, select **USD**. 

   In the following example, the WWB-Operating bank account handles all payments other than USD payments, while the WWB-USD bank account handles all USD payments.

   ![Payment balance account setup](/images/CB/payment-bank-account.png)  

   > [!NOTE]
   >
   > It is possible to override the general setup for Vendor, Customer, Employee, and G/L accounts. For example, on the **Vendor** card, on the action bar, select **Related** > **Vendor** > **Payment Balance Account Setup**. 

