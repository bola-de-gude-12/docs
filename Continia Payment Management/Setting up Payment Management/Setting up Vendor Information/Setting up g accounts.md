---
title: Setting up G accounts
description: The fields to use when setting up a G account
date: 15-05-2023
id: PM-335
lang: en
---
# Setting up G Accounts

A G account is a specialized bank account utilized in the Netherlands, specifically created to hold funds for specific purposes, such as guaranteeing the payment of taxes or social security contributions. If you want to set up a G account in Payment Management, there are specific fields that you need to fill out. This article will guide you through those fields and help you set up the G account successfully.

To set up the G account fields:

1. Use the ![Search for a page or report](/images/search_small.png) icon, search for **Vendors**, and select the related link.
2. Select the vendor that you want to add the G account to and on the **Payments** FastTab, enter information for the following fields:
   - **G account %** - specifies the default percentage that should be set aside and paid to the G account.      
   - **G account bank account** - specifies the default bank account the vendor uses for G account deposits.
     

After configuring the G account fields on the vendor card, on the purchase invoice, all the necessary calculations will be performed accordingly, and the following fields are defined:

* **G account %** - specifies the percentage set on the vendor card.
* **G account base amount** - specifies the total amount in the G account bank account.
* **G account amount** - specifies the amount that is allocated and set aside in the G account.

When suggesting vendor payments in the payment journal, the system will allocate the specified percentage to the designated G-account bank account and generate a corresponding ledger entry. For instance, if the G account percentage is set to 10, whenever you make a payment to the vendor, 10 percent of the payment amount will be automatically reserved and transferred to the G account. 

