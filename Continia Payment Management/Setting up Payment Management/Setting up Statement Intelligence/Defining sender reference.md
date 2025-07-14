---
title: Defining sender reference template code
description: Information on how to add sender reference template code with Transaction ID.
date: 24-06-2022
id: PM-194
lang: en
---

# Defining Sender Reference

When sending payments to the bank from the Payment Management payment journal, the payments can be sent with a unique payment sender reference code. This sender reference follows the payments to the bank and the vendors, and, if supported by the bank, it will be applied to the bank account statement lines. When you use a payment reference template that contains a unique transaction ID, Statement Intelligence will use the Transaction ID to automatically match a corresponding bank account ledger entry. 

For information about setting up a sender reference template, see the article [Setting up payment references](@PM-43).

## To define a sender reference template code

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Accounts**, and then select the related link.
1. Open the relevant bank account.
1. On the bank account card navigate to the **Transfer** FastTab.
1. In the **Sender Reference Template Code** field, specify the payment reference template that must be used when creating a payment reference.  

If you import the bank account statement electronically, you should choose a sender reference template code that includes Transaction ID.

> [!NOTE]
>
> It is strongly recommended that you always enter a sender reference on the bank account card to identify a match for the payments in the bank account reconciliation. If the sender reference template code is not specified on the bank account card, the first 16 digits of the transaction ID will be used.
