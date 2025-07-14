---
title: Setting up payment journals
description: Information on how to set up the payment journal and prepare it for making vendor payment suggestions with Payment Management
date: 18-05-2021
id: PM-14
lang: en
---

# Setting up Payment Journals

Payment Management has extended the standard payment journal with additional functionality to improve the payment flow. In addition, payment lines will be validated by Payment Management before they are sent to the bank, and the status on the payment line will let you know if further actions are needed for the payment. 

> [!NOTE] 
>
> During the general setup of Payment Management, a payment journal will automatically be generated with Payment Management enabled. However, if you create a new payment journal or use an existing payment journal, you must manually activate Payment Management on the journal. 

The first time you use a payment journal with Payment Management enabled, you will be asked to set up the payment journal. The payment journal setup forms the basis of the vendor payment suggestions in the given payment journal. 



## To activate Payment Management on a payment journal

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Journal**, then select the related link. This will open a **Payment Journal**.
1. On the payment journal header, go to **Batch name** and select ![Search for page or report](/images/show-more-options-icon-small.png). This opens the **General Journal Batches**.
1. In the **General Journal Batches** list, in the **Payment Management journal** column, select the checkbox for the payment journal you want to activate Payment Management for. 

Payment Management has now been activated on the payment journal.

## To set up the payment journal

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Journal**, then select the related link. This will open a payment journal.
1. In the action bar, select **Prepare** > **Payment Journal Setup**.
1. On the **Payment Journal Setup** page, you can update the settings for the specific payment journal. For example:
   * **Required Posting Status** - specifies the payment status required for posting. For example, it is a good idea to select the status *Paid* to only post the lines that are actually paid. If you select *Sent* or *Processing*, all payments in the journal with this status or higher will be posted. If no required status is defined in the journal, the value from the general Payment Management setup page will be used.
   * **Find Payment Discounts** - specifies if the suggestion should look for possible payment discount dates. For example, some vendors offer discounts of 1%-2% off the total invoice amount if paid within 10-15 days. If you switch this option on, Payment Management automatically finds these payment discounts for you.
   * **Handle Bank Holidays on Payments** - select how to handle Bank Holidays when suggesting payments for this journal. Payment Management has added all bank holidays to the system. If you send a payment on a bank holiday, you can select to handle a payment *before* or *after* the bank holiday instead.


After you have defined the settings in the payment journal setup, the settings form the basis of the **Suggest Vendor Payments** setup, and you are ready to create vendor payment suggestions.

## Managing required status for posting payments

When payments have been processed and paid in the bank, you post the related payment lines on the **Payment Journal** page. To control when payments can be posted, you can choose a posting criterion based on the status of the payment line.
You can manage the required payment line status for posting payments from the following two places:

- On the **Payment Management Setup** page, under the FastTab **Purchase and Payments** > **Required Posting Status**.

- On the **Payment Journal** page in the **Payment Journal Setup** > **Required Posting Status**. 
  

In both setups, use the dropdown to choose between the following three required payment line statuses:
  -  **Sent**
  -  **Processing**
  -  **Paid**

> [!WARNING]
> If you use direct communication, we strongly advise against setting the required posting status to Sent. If, for example, your bank rejects a payment, the payment line will then not be updated accordingly in Business Central with the status Rejected. The result can be that a payment is registered as completed in Business Central, while in fact, it has been rejected by the bank.

> [!NOTE]
> 
> If you use manual communication, the only available status is **Sent**. 

