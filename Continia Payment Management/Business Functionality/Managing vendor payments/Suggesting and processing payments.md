---
title: Suggesting and processing payments
description: How to suggest and process payments in the payment journal.
date: 12-02-2025
id: PM-90
lang: en
---

# Suggesting and Processing Payments

With Payment Management, you can take advantage of an extended payment journal that provides enhanced functionality for your payment processes. This includes features like payment validation and direct communication with the bank when creating and sending payments to vendors. 

To use the extended payment journal, Payment Management must be enabled and set up on the payment journal. For more information, see the [Setting up payment journals with Payment Management](@PM-14) article. 

## To create vendor payment suggestions

To create vendor payment suggestions:

1. Use the ![Search for page or report](/images/search_small.png) icon, search for **Payment Journals**, then select the related link. 

1. Go to the **Batch Name** field, select the three dots, and on the **General Journal Batches** page, select a journal that has the Payment Management Journal column checked. 

1. On the action bar, select **Home** > **Suggest Vendor Payments**. 

1. On the **Suggest Vendor Payments** form, to filter payments you can use various criteria such as the **Last Payment Date**, decide whether to summarize payments per vendor, fill in a posting date. Additionally, you can choose to filter on a specific vendor: use the fields in the **Filter: Vendor** section to, for example, filter on a specific payment code. 

1. Select **OK** to generate the vendor payment suggestions. The payment journal will now generate payment lines that align with the settings of the payment journal suggestion.

   After creating payment suggestions in the payment journal, you can rely on the associated **Status** column of each payment line to understand its current stage in the payment process. If you use direct communication, statuses will also be imported from the bank. For more information, see the [Using the payment status](@PM-89) article.

   All payment lines must have status **Valid** before they can be sent/exported to the bank. In case of errors on a payment line, you can use the **Payment File Errors** FactBox in the lower right corner of the payment journal to find a more descriptive error message. Select the error message to learn more about the error. 

## To send or export payments

When the payment lines in the payment journal have the status **Valid**, they can be sent or exported depending on the chosen type of bank communication. 

To send or export payment lines: 

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Journals**, then select **Payment Journals**. 
1. Go to the **Batch Name** field, select the three dots, and on the **General Journal Batches** page, select a journal that has the **Payment Management Journal** column checked. 
1. On the action bar, select **Home** > **Export/Send Payments**. 
1. Select **All Lines** or **Selected Line** and select **OK**. It is possible that you will be asked to confirm your bank account information. To learn more about bank account verification, refer to the [Bank Account Verification](@PM-352) article. If you send payments to various banks, you must choose to which bank you wish to first send payments. After having sent payments to one bank, you can repeat step 3 and select the next bank to send payments.

   The status of the sent/exported payment lines will be updated to **Sent** for exported payments, or **Processing** for payments send by direct communication. For more information, see the [Using the payment status](@PM-89) article.

   > [!NOTE] 
   >
   > It is possible to specify a custom-defined name for payment files manually exported from the payment journal. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Management Setup**, then select the related link. In the action bar, select **Troubleshooting** and navigate to the FastTab **General**. In the field **File Name (Payment File),** define the file name to be used for manually exported payment files.

## To post payments

You can post a payment line when it has the status **Sent** or **Processing**. However, it is recommended not to post any payment lines before they have been paid in the bank. You can define posting criteria to ensure that no payment lines are posted before they have been paid. For more information, see the  [To determine a required status for posting payments](@PM-14#to-define-a-required-status-for-posting-payments) article. 

To post the payment lines:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Journals**, then select the related link. 
1. Go to the **Batch Name** field, select the three dots, and on the **General Journal Batches** page, select a journal that has the **Payment Management Journal** column checked. 
1. On the action bar, select **Home** > **Post/Print** > **Post**. 

## To suggest vendor payments automatically

To enhance the payment suggestion process, Payment Management has implemented a job queue for automation.

To enable the CPM Suggest Vendor Payment (6216230) job queue:

1. On the payment journal, on the action bar, select **Prepare** > **Payment Journal Setup**. 
2. On the Payment Journal Setup page, select **More options** >**Actions** > **Job Queue** > **Enable Suggest Vendor Payments Job Queue**. Once enabled, the system will automatically generate payment suggestions for vendor payments. 

## To post payments automatically

In the Payment Journal Setup, you can now enable the automatic posting of journals based on the status of the payment lines by using a job queue. The posting of the lines can be configured to align with the company's requirements, ensuring that unintended actions, such as posting before payment confirmation in the bank, are avoided. 

To post payments automatically:

1. Open the payment journal that you want to enable automatic posting for and on the Payment Journals page, on the action bar, select **Prepare** > **Payment Journal Setup**.

2. On the **Payment Journal Setup** page, navigate to the **Required Posting Status** field and select the status that you want to trigger the job queue for. 

   > [!IMPORTANT]
   >
   > When using automatic posting, it is highly recommended to set the Required Posting Status to Paid. If set differently, there is a possibility that the journal lines you post may get rejected on the payment date. In case you have already posted them you would need to roll back those payments.

3. Go to the **Posting Method** field, and select **Automatic**.

4. Below the Posting Method field, you can now select **Job Queue Setup** to open the Job Queue Entry Card for the 6216364 CPM Post Payment Journal JQ. To stop the job queue from posting payments automatically, select *Manual* for the **Posting Method**, or navigate to the action bar and select **Actions** > **Job Queue** > **Disable Post Payment Lines Job Queue**. 

6. On the **Job Queue Entry** Card, you can now determine when and how to run the job queue. 

## To view payment details

While working on the payment line, various information about a chosen payment line will be available on the right side of the payment journal. For more detailed information, select the information displayed in *green text*. 

The payment line information includes the following:

| <span style="white-space: nowrap;">FactBox</span> | Description |
| --- | --- |
| Payment Management | All changes to the payment line status are logged for your reference. To view a complete log, select the status displayed in green text. This will open the page **Credit Transfer Log**, from where you can also access the **File Archive** for the payment line. |
| Journal Line Details | This section provides the most basic journal line details, such as **Posting Group**, **Account**, and **Balance Account**. |
| Payment File Errors | If there are errors on the payment line, each error will be described in more detail in this list. When the payment line status is updated, errors that have been resolved will be deleted from the list. |
| Recipient Bank Details | Lists the details of the bank account you are making a payment to. In the **Account Verification** section, you can check the verification status of the bank account. To learn more about bank account verification, refer to the [Bank Account Verification](@PM-352) article. |



## Related information

[Setting up payment journals with Payment Management](@PM-14)  
[Using the payment status](@PM-89)  
[To define a required status for posting payments](@PM-14#to-define-a-required-status-for-posting-payments)