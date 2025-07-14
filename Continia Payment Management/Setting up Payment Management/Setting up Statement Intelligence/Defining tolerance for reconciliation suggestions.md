---
title: Defining allowed tolerances for reconciliation
description: How to set up allowed tolerances for reconciliation suggestions
date: 13-09-2021
id: PM-273
lang: en
---

# Defining Tolerance for Reconciliation Suggestions

You can use reconciliation amount tolerances in matching scenarios for reconciliation. Statement Intelligence assists you by searching for matches in open payments and creating reconciliation suggestions. Suggestions are made based on parameters such as total balance amount, document no., and date. Sometimes, reconciliation suggestions can't be made due to amount differences caused by, for example, currency differences or additional fees. By setting up a tolerance for reconciliation suggestions, you can widen the search for ledger entries and improve matching and suggestion possibilities. 

If you add a Reconciliation Suggestion Tolerance amount to the bank account, customer card, or vendor card, Statement Intelligence adds the tolerance to the statement amount when reconciling for any open ledger entry. If the reconciliation suggestion is based on this tolerance, the **Found by** field value is **Tolerance Amount**.

You can set up the tolerance amount on the Customer Card, the Vendor Card, and the Bank Account Card page. Tolerance amounts set on the Customer Card or Vendor Card take precedence over the tolerance amount specified on the Bank Account Card.

> [!IMPORTANT]
> The tolerance setup is applied to the reconciliation suggestions only if the customer or vendor is identified on a specific bank statement line in the bank account reconciliation.


## To define Tolerance on the Customer or Vendor Card

To create reconciliation suggestions for a tolerance range, you can specify the maximum and minimum amount a payment line can deviate from a customer or vendor ledger entry. 

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Customer** or **Vendor**.
1. Select a customer or vendor.
1. On the customer or vendor card, on the **Payments** FastTab, navigate to the **Reconciliation Suggestion Tolerance** section.
1. Select the **Tolerance Type** drop-down and select **Percentage** or **Amount**.
1. In the **Tolerance Value** field, enter the value for the tolerance. 

> [!NOTE]
> The tolerance value amount is always in LCY and can't be negative. 

The tolerance setup on the Customer or Vendor Card is used if the **Tolerance Value** field contains an amount and if a customer or vendor is identified during the reconciliation. If the **Tolerance Value** field on the Customer of Vendor Card is empty, the **Tolerance Value** field on the Bank Account is used.



## To define Tolerance on the Bank Account

If you want to add a general tolerance range, you can also set the tolerance type and amount on a bank account. 

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Account**.

1. Select a bank account.

1. On the bank account card, on the **Statement Intelligence** FastTab, navigate to the **Reconciliation Suggestion Tolerance** section.

1. Select the **Tolerance Type** drop-down and select **Percentage** or **Amount**.

1. In the **Tolerance Value** field, enter the value for the tolerance. 

> [!NOTE]
> The tolerance value amount is always in LCY and can't be negative. 

   

