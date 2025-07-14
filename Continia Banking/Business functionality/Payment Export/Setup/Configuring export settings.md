---
title: Configuring Export Settings in Continia Banking
description: How to change the export settings in Continia Banking.
date: 11-02-2025	
id: CB-23
lang: en
---

# Configuring export settings

This article provides an overview of Continia Banking's essential export settings and their customization options. On the **Banking Export Setup** page, you can edit general settings, such as adjusting the payment date for [bank closing days](@CB-42), the required posting status for posting a payment, and so on.

To configure export settings:

1. Search ({{search}}) for and select **Banking Export Setup**.

2. On the **Banking Export Setup** page, on the **General** FastTab, you can edit the following settings:

   | Field                                 | Description                                                  |
   | ------------------------------------- | ------------------------------------------------------------ |
   | Advanced Payment Suggestion           | This feature is disabled by default. Enable this option to unlock advanced views and features for payment suggestions. This allows you to manage all your payment entries directly within the payment suggestion interface before sending them to the bank, rather than creating them from the payment journal. <br/>**Warning:** Ensure all entries are posted in the payment journal before using payment suggestions.<br />To switch between standard and advanced mode per journal batch, you can override this setting on the General Journal Batch page. For more information, refer to the [The Advanced Payment Suggestion option](@CB-145) article.<br /> |
   | Last Payment Date Calculation         | Specifies the date formula for calculating the last due date on the Payment Suggestion reports request page. This can be set in the Payment  Journal Setup for each batch. |
   | Suggestion No. Series                 | Indicates the number series that will be used to generate suggestions for advanced payments. |
   | Validate Advanced Payment Suggestions | Specifies whether to validate header suggestions before transferring to Gen. Journal Lines. This setting is disabled by default. When you enabled the Advanced Payment Suggestions mode, you can also configure how validation should work for the payment proposals. For manual validation, enable Validate Suggestion Header. This allows you to review and validate the payment proposals yourself before they are turned into journal lines. |
   | Validate Purchase Documents           | Specifies whether to validate your purchase documents before you post them. This setting is disabled by default. |
   | Validate Sales Documents on Post      | Lets you enable validation for sales documents when using the Direct Debit payment method, preventing sales orders without a mandate ID. |
   | Validate Purchase Order on Approval   | If enabled, payment information will be validated before approving a purchase order. |
   | Validate Purchase Invoice on Approval | Specifies whether payment information is validated before the invoice can be approved. |
   | Use Dynamic Validation                | If you enable this feature, your payment information will be checked and verified on a continuous basis. This will validate the payment proposals automatically as you work on them, ensuring they are ready when transferred to the payment journal. |
3. On the **Payment** FastTab, you can edit the following settings:

   | Field                                    | Description                                                  |
   | ---------------------------------------- | ------------------------------------------------------------ |
   | Use Exchange Rate Adjustment             | When you make payments to foreign vendors, the exchange rate in the file sent from Business Central to the bank may differ from the rate used by the bank for processing. If your bank supports status files for direct communication, you can enable Continia Banking to automatically update the exchange rate on unposted payment lines in the journal based on the actual rate used by the bank for foreign payments. Enabling the Use Exchange Rate Adjustment option allows you to adjust the payment amount to account for the exchange rate used by the bank at the time the payment was completed. However, please note that to use this option, you should not post the payment journal lines until the payment is completed in the bank. Also, not all banks provide the currency exchange rate in their payment information. |
   | Move Payment Date                        | Specifies how the Payment Date or Pmt. Discount Date should be adjusted if it corresponds to a Bank Closing Day (if the due date falls on a non-banking day such as a banking holiday or a Sunday). The options are **Move before**, **Move after**, and **Ask user**. |
   | Allow Updating Postings                  | You can specify how Continia Banking should manage the posting dates in case payments can't be processed on the dates set for the payment lines. In some cases, the bank will not process payments by the posting date stated in the payment journal. If you are communicating with the bank using direct communication, a status file can be imported from the bank with the actual posting date, making it possible for Continia Banking to update the posting dates on the payment journal lines by the status file received from the bank. To use this feature, your bank must support posting dates in status files, and the Allow Updating Posting Date action must be enabled. |
   | Recipient Reference Template             | Specifies the template used for creating recipient references. If a specific Remittance Information Template is employed, the information in the file will adhere to this pattern. |
   | Description Template                     | Defines the template format for the description of journal lines or transactions. |
   | Sender Reference Template                | Specifies the template used for creating sender references in journal lines or transactions. |
   | Description Template Summarized Payments | When making a payment suggestion, you can use template fields to specify how to fill out the description field in the payment journal for summarized payments. You can choose a predefined mask or create your own. This description is visible only in Business Central and is not sent to the bank or vendor. |
   | Description Template Summarized Payments | When making a payment suggestion, you can use template fields to specify how to fill out the description field in the payment journal for summarized payments. You can choose a predefined mask or create your own. This description is visible only in Business Central and is not sent to the bank or vendor. |
4. On the **Direct Debit** FastTab, you can edit the following settings:
   | Field                 | Description                                                  |
   | --------------------- | ------------------------------------------------------------ |
   | Use Direct Debit      | Enable this option to activate the use of Direct Debit for payments. |
   | Default Template Name | Select the templates you want to use for processing Direct Debit payments. This field determines the default template for payment suggestions when processing direct debits, and it is automatically prefilled when activated. |
   | Default Batch Name    | Select the batch name to be used for Direct Debit processing. This field specifies the default batch for payment suggestions, and it is automatically prefilled when activated. |
   | Document No. Series   | Defines the number series that will be used to create direct debit journal lines for advanced payments. |
6. On the **Remittance** FastTab, you can edit the following settings:

   | Field                    | Description                                                  |
   | ------------------------ | ------------------------------------------------------------ |
   | Default Information Type | Specifies the default method for sending Remittance Advice to new vendors. Options include **Bank only** and **Bank and email**. |
   | BCC Email                | Specifies the bcc email address to use for email remittance advices. |
   | Default Language Code    | Specifies the default language code used for remittance advices. |
   | Email Sending Method     | Specifies the trigger condition for sending the Remittance Advice email. Options include: **Manually**, **On post**, **Job queue**, and **On create payment**. For more information on the job queue functionality, refer to the [Using Job Queues to Schedule Tasks](@CB-119) article. |
   | Template                 | Specifies the value of the Remittance Information Template field used for formatting remittance advice content. |
7. On the **Approval** FastTab, you can enable to use bank account verification.

<style>
 .content table tr td:nth-child(1) {
 width: 250px;
 }
 .content table tr td:nth-child(2) {
 width: 550px;
 }
</style>
