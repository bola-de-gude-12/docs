---
title: Setting up balance accounts
description: A description on how to set up balance accounts on the vendor card, purchase document, payment journal, or based on currency.
date: 05-07-2022
id: PM-62
lang: en
---

# Setting up balance accounts

The balance account specified on a vendor payment defines the company bank account that will be used for the transaction. Payment Management also uses the balance account to validate the payment, as the requirements to the payment information is depending on the bank and the bank account. 

> [!TIP]
>
> We recommend that you apply a balance account to all your vendors. This makes it possible for Payment Management to validate the payments when creating the purchase document. See the guide [To update balance account on several vendors at one time](#to-update-the-balance-account-for-several-vendors-at-the-same-time).



## Overview of balance account setup

Balance accounts can be set up several places in Business Central, and each setup defines when the balance account is applied to the payment. We recommend that the balance account is applied as early in the payment process as possible. 

You can set up the balance account the following places:

- **The vendor card** <br>
  When you specify the balance account on the vendor card, a balance account is automatically applied to all purchase documents for the given vendor. See the guide [To specify a balance account on the vendor card](#to-specify-a-balance-account-on-the-vendor-card).

- **The purchase document** <br>If there's no balance account specified on the vendor card, you can specify it directly on the purchase document. By default, it is mandatory that a balance account is specified on the purchase document. You can change this setting in the [Payment Management Setup](#to-manage-the-balance-account-requirement-on-purchase-documents).
  
- **The payment journal** <br>
  When you specify the balance account on the payment journal, only payments that have the given balance account, or payments without a balance account can be created in the journal. See the guide [To define the balance account on the payment journal](#to-define-the-balance-account-on-the-payment-journal).

- **The balance account setup** <br>
  If there's no balance account specified on a payment or on the payment journal, the balance account will be selected based on the currency of the payment. This is set up in the [Balance Account Setup](#to-set-up-currency-determined-balance-accounts).



## To specify a balance account on the vendor card

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Vendors**, then select the related link. This open the list of vendors.
1. Open the vendor card, for which you want to define balance account.
1. On the vendor card, on the **Payments** FastTab, select **Payment Information**.
1. In the field **Balance Account No.** choose the bank account from which you want to pay the vendor.



## To update the balance account for several vendors at the same time 

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Vendor Payment Information Setup**, then select the related link. This will open the assisted setup of vendor payment information.
1. In step 2 in the guide, in the **Payment Method (New)** column, choose the same payment method as given in the **Payment Method (Current)** column. This will import all vendors to the guide, with the given payment method, without updating the payment method.
1. Select **Next** to go to step 3 in the guide, which will give you a list of all vendors.
1. In the list of vendors, in the **Balance Account No.** column, choose a balance account number on those vendors which balance account must be updated.
1. Choose **Next** to go to step 4 in the guide.
1. On step 4, enable the **Update open Vendor Ledger Entries** function, to apply the balance account to open vendor ledger entries. 
1. Choose **Next** to go to step 5 in the guide, and finish the guide by selecting **Finish**.



## To manage the balance account requirement on purchase documents

The requirement for a balance account on purchase documents is by default enabled. This means that when you post a purchase document without a balance account, you'll be reminded to specify a balance account on the document. 

1. Use the ![Search for page or report](/images/search_small.png) icon to search for **Payment Management Setup**, and then select the related link. 
1. On the **Purchase and Payments** FastTab, enable or disable the **Balance Account Requirement** setting as needed.



## To set up currency determined balance accounts

The Balance Account Setup will be used if the payments don't already have a balance account defined, and if a balance account hasn't already been defined for the given payment journal.

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Balance Account Setup**, then select the related link. This will open the balance account setup page.
1. On the list, select the currency for which you want to define a default balance account.
1. In the **Balance Account No** column, use the dropdown arrow to choose the default bank account for paying vendors in the given currency.
1. Repeat step 2 and 3 to setup more default balance accounts.

When you have finished the setup you can close the page. When generating a payment suggestion in the payment journal, Payment Management will now use the balance account setup to define which balance account to apply to vendor payments that do not have a balance account defined.

> [!TIP]
>
> If you leave the box **Currency** blank and choose a **Balance Account No.** then the given balance account will be used as default balance account for local currency payments.



## To define the balance account on the payment journal

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Journal**, then select the related link. This will open a payment journal.
1. On the payment journal header go to the **Batch name** selection, and select the ![Search for page or report](/images/show-more-options-icon-small.png). This opens the **General Journal Batches**.
1. In the general journal batches list, select the payment journal for which you want to define **Balance Account No.**.
1. On the general journal batch, select the **Payment Management Journal** check box.
1. Fill in the **Bal. Account Type** and the **Bal. Account No.**, if you want a fixed balance account to be used for this journal. Otherwise, leave the **Bal. Account No.** field blank and use the alternative method described below.

Alternatively you can:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Journal**, then select the related link.
1. On the payment journal, in the action bar, select **Prepare** > **Payment Journal Setup**
1. On the **Payment Journal Setup** page, in the **Bal. Account No.** field, choose the balance account number to use for the given payment journal.

>[!NOTE]
>If payments created by a payment suggestion don't have a balance account specified, you can add a balance account manually to the lines. To do that, select **Prepare** > **Set Balance Account No.**, specify the relevant balance account number, and then in the **Update** field, specify for which lines you want to update the balance account number.
