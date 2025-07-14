---
title: Suggesting and processing payments in Continia Banking
description: How to suggest and process payments in the payment journal.
date: 11-02-2025
id: CB-109
lang: en
---

# Suggesting and processing payments

With Continia Banking, you can take advantage of an extended payment journal that provides enhanced functionality for your payment processes. This includes features like payment validation and direct communication with the bank when creating and sending payments. 

To use the extended payment journal, you need to enable and set up Continia Banking on the payment journal. 

## To create payment suggestions

Once you create a payment journal, you can establish parameters and rules for how to execute the Create Payment Suggestion function for this specific journal. The setup lets you specify whether the function should find and trigger discounts or only payments with a particular payment method. Additionally, you can switch between Standard and Advanced Payment Suggestion mode at the journal batch level, allowing for more flexibility in payment processing. For more details on Advanced Mode and its benefits, see [The advanced payment suggestion option](@CB-145) article.

To create payment suggestions:

1. Search ({{search}}) for and select **Payment Journals**.

1. Go to the **Batch Name** field, select the three dots, and on the **General Journal Batches** page, select a journal. For payment journals to work with Continia Banking functionality, the **Banking Export Journal** column must be selected. 

1. On the action bar, select **Home** > **Suggest Vendor/Customer/Employee Payments**. 

1. On the **Suggest Payments** form, to filter payments, you can use various criteria such as the **Last Payment Date**, decide whether to summarize payments per vendor, and fill in a posting date. Additionally, you can choose to filter on a specific vendor: use the fields in the **Filter** section to, for example, filter on a specific payment method. With Continia Banking it is also possible to setup up Templates for your Payment Suggestions. For more information on using templates to suggest payments and the filter settings, refer to the [Payment suggestion templates](@CB-89) article. 

1. Select **OK** to generate the payment suggestions. The payment suggestion will now generate payment lines that align with the settings of the payment journal suggestion.

   After creating payment suggestions in the payment journal, you can rely on the **Payment Status** field in the **Line Information** FactBox on the right to understand its current stage in the payment process. If you use direct communication, statuses will also be imported from the bank. For more information on statuses, read the [Payment statuses](@CB-111) article. 

   You can only send/export payment lines to the bank if they have status Valid or Approved (in case Payment Approval is used). In case of errors on a payment line, you can use the **Payment Journal Errors** FactBox in the right panel of the payment journal to find a more descriptive error message. Select the error message to learn more about the error. 

## To send or export payments

When the payment lines in the payment journal have the status Valid, you can send or export them depending on the chosen type of bank communication. 

To send or export payment lines: 

1. Search ({{search}}) for and select **Payment Journals**. 
1. Go to the **Batch Name** field, select the three dots, and on the **General Journal Batches** page, select a journal that has the **Banking Export Journal** column checked. 
1. On the action bar, select **Home** > **Export/Send Payments**. 
1. Select **All Lines** or **Selected Line** and select **OK**. It is possible that you will be asked to verify your bank account information. To learn more about bank account verification, refer to the [Bank account verification](@CB-30) article. 

   The status of the sent/exported payment lines will be updated to **Sent** for exported payments, or **Processing** for payments send by direct communication. 


## To post payments

You can post a payment line when it has the status **Sent**,  **Processing**, or **Exported to File**. However, it is recommended not to post any payment lines before they have been paid in the bank. You can define posting criteria to ensure that no payment lines are posted before they have been paid. 

To post the payment lines:

1. Search ({{search}}) for and select **Payment Journals**, then select the related link. 
1. Go to the **Batch Name** field, select the three dots, and on the **General Journal Batches** page, select a journal that has the **Banking Export Journal** column checked. 
1. On the action bar, select **Home** > **Post** > **Post**. 

## To suggest payments automatically

To enhance the payment suggestion process, Continia Banking has implemented a job queue for automation. For more information on how to set this up, refer to the [Setting up payment suggestion templates](@CB-89) article. 

## To view payment details

While working on the payment line, various information about a chosen payment line will be available on the right side of the payment journal. For more detailed information you can use the links to open the relevant page whether it is the bank account, status log for the payment line, or the verification status of the recipient bank accounts. Links are displayed in green texts. 

The payment line information includes the following fields:

| <span style="white-space: nowrap;">FactBox</span> | Description |
| --- | --- |
| Line Information | This section provides the most basic journal line details, such as **Posting Group**, **Account**, and **Balance Account**. |
| Payment Journal Errors | If there are errors on the payment line, each error will be described in more detail in this list. When the payment line status is updated, errors that have been resolved will be deleted from the list. |
| Recipient Bank Details | Lists the details of the bank account you are making a payment to. In the **Account Verification** section, you can check the verification status of the bank account. To learn more about bank account verification, refer to the [Bank Account Verification](@CB-30) article. |

