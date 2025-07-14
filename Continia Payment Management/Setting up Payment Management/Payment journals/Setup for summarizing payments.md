---
title: Setup for Summarizing payments
description: Information on how to define the settings for summarizing payments in the payment journal
date: 22-05-2025
id: PM-186
lang: en
---

# Setup for summarizing payments

You can summarize payment lines in the payment journal, thereby sending one payment line to the bank. This can be advantage if for example the bank charges a fee per payment line. Depending on how you want to summarize payments lines, see the different setup guides below. 

For more information on how to manually summarize payment lines after the setup has been completed, see [Summarizing Payments](@PM-201).



## To allow for vendor payments to be summarized

1. Search ({{search}}) for and select **Vendors**.
1. Open the vendor card for the vendor who must receive summarized payments.
1. On the vendor card under the FastTab **Payments** activate **Allow Summarizing Payments** to allow for payments to be summarized in the payment journal.

## To allow for payments to be summarized in the payment journal

1. Search ({{search}}) for and select **Payment Journals**.
2. On the payment journal in the action bar select **Prepare** > **Payment Journal Setup**.
3. Under the menu item **Summarize Payments Setup** activate the setting **Summarize Per Vendor**.

> [!NOTE]
>
> The settings defined under the menu item **Summarize Payment Setup** do not apply when manually summarizing payments.

## To allow for payments with different dimensions to be summarized in the payment journal

1. Search ({{search}}) for and select **Payment Journals**. 
2. On the payment journal in the action bar select **Prepare** > **Payment Journal Setup**.
1. For manual summarization settings, go to the **Manual Summarization Payment Setup** section to see the following options:
   * **Delete Dimensions** - when enabled, this option will clear all dimension values from the summarized payment lines, regardless of what dimensions were set on the original lines.
   * **Summarize Across Dimensions** -  when enabled, this allows payment lines with different dimension values to be summarized together. The dimensions from the vendor ledger entry are used, and combined with the logic used when summarizing in the payment suggestion.
4. For automatic summarization settings, go to the **Automatic Summarization Payment Setup** section to enable:
   * **Summarize per Vendor** - when enabled, payment lines are grouped and summarized per vendor.


## To allow summarizing lines differing in value (only manual summation)

1. Search ({{search}}) for and select **Payment Journals**, then select the related link. 
1. On the payment journal in the action bar select **Prepare** > **Payment Journal Setup**.
1. On the payment journal setup go to the menu item **Manual Summarize Payments Setup**. In the section **Vendor defaults**, choose if you want to allow journal lines that differ in various values to be summarized. If you enable one of the settings allowing values to differ between payment lines, then the value defined in the vendor card will be used on the summarized line. <br> An example could be two lines that you want to summarize that have different **Payment Method Codes**: 
   - Payment line 1: Payment Method is *Domestic Bank Transfer*
   - Payment line 2: Payment Method Code is *FIK 71 card payment*
   If the payment method defined on the vendor card is *FIK 71 card payment*, then the two lines will be summarized with the payment method defined on the vendor card (*FIK 71 card payment*).
1. In the section **Allowed differences**, choose if you want to allow journal lines that differ in **Regulatory Reporting Codes** to be summarized. If this setting is enabled, then all the given regulatory reporting codes will be summarized on the summarized line.
> [!NOTE]
>
> The settings allowing for different values are only applicable for manual summarization. This means that payment lines can't automatically be summarized if they differ in one of the following values: **Bal. Account No.**, **Creditor No.**, **Payment Method Code**, **Recipient Bank Account**, or **Regulatory Reporting Code**.



## To avoid summarizing credit memos

If you do not want credit memos to be summarized in the payment journal, this can be defined on the vendor card and on the payment journal setup. See the two guides below for defining if credit memos must be excluded when summarizing payments.

Exclude summation of credit memos for a specific vendor:

1. Search ({{search}}) for and select **Vendors**.
1. On the vendor card under the FastTab **Payments** in the box **Exclude Credit Memo When Summarizing Payments** activate the setting if credit memos are *not* allowed to be summarized in the payment journal for the given vendor.

Exclude summation of credit memos for a payment journal:

1. Search ({{search}}) for and select **Payment Journals**.
1. On the payment journal in the action bar select **Prepare** > **Payment Journal Setup**.
1. Under the menu item **Summarize Payments Setup**, in the dropdown menu **Exclude Credit Memo**, choose if credit memos must be excluded for the payment journal when summarizing payment journal lines. You can choose between the following three options: 
   - **Vendor Specific**: The setting on the vendor will define if credit memos can be summarized.
   - **No**: Credit memos will not be excluded when summarizing payment journal lines.
   - **All**: Credit memos will not be summarized regardless of the setting on the vendor card. 



## To allow for date deviation

1. Search ({{search}}) for and select **Payment Journals**. 
1. On the payment journal in the action bar select **Prepare** > **Prepare Journal Setup**.
1. Under the menu item **Summarize Payments Setup** in the field **Date Deviation** specify the allowed date deviation between posting dates, when summarizing payments. The earliest posting date will then be used on the summarized payment line.



## Related information

[Summarizing Payments](@PM-201)
