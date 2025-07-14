---
title: Setting up customer statements
description: How to set up and use customer statements
date: 19-09-2022
id: 
lang: en
---

# Setting up Customer Statements

With Payment Management, you can print customer statements with a payment reference allowing customers to pay multiple invoices using a single payment reference. You can also [include an OCR reference number](#to-set-up-the-payment-reference) to statements.

> [!IMPORTANT]
>
> This feature is primarily developed for the DK localization of Payment Management, as it mainly supports the Danish payment references.



When a customer uses the payment reference number, Payment Management uses it in the following two places:

- **Cash receipt journal**: When you import payments to the cash receipt journal, Payment Management detects the payment reference and automatically applies all the related customer ledger entries in the journal.

- **Bank account reconciliation**: When the payment reference appears in either the description or among the additional information received from the bank, Payment Management identifies the payment reference and creates a reconciliation suggestion. When the line is reconciled, you can access the reconciliation suggestion and see all the related suggestion entries. Additionally, on the bank account reconciliation line, you can open the related customer statement by selecting **Bank Statement Lines** > **Show Customer Statement**. 

## To set up customer statements

To add a payment reference to the customer statement, there are a few things you need to set up:

- [Payment reference type](#to-set-up-the-payment-reference-type)
- [Report layout](#to-set-up-the-word-layout)

> [!NOTE]
>
> A default number series for customer statements is set up with the installation of Continia Payment Management and is ready to go. However, if you want to change the number series, navigate to **Payment Management Setup** > **Payment Receipt Import** > **Customer Statement No.** The number series can only contain numbers.

### To set up the payment reference type

You must select a payment reference type to specify how the payment reference should be structured.

1. Select the ![Search for page or report](/images/search_small.png) icon, enter **Sales & Receivables Setup**, and then the related link.
2. On the **General** FastTab, in the **Payment Reference Type** field, specify the relevant reference type. 

   To include an OCR reference to the bank statement, select the reference type "71".

   If you select the OCR payment reference type and [print the customer statement](#to-print-a-customer-statement), a payment reference displays at the top of the document that customers can use for their payments. 

### To set up the Word layout

To include the payment reference type to the customer statement layout, you should use a Payment Management report layout.

1. Select the ![Search for page or report](/images/search_small.png) icon, enter **Report Layouts**, and select the related link.
2. Search for report ID "1316", and select the word layout "Customer Statement" created by Continia Payment Management (see the **Extension** column).
3. In the action menu, choose **Set Default**. 

> [!NOTE]
>
> You can choose to use a different layout than the one created by Payment Management, but you must be sure the layout includes the payment reference. You can only use a Word layout.

## To print a customer statement

1. Select the ![Search for page or report](/images/search_small.png) icon, enter **Customers**, and select the related link.
2. Select a customer. 
3. On the customer card, in the action menu, select **Reports** > **Statement**.
4. On the **Customer Statement** page, specify the details for the statement you want to print and select **OK**.

The customer statement is now being printed with the payment reference specified. 

>[!NOTE]
>
>If you use the preview functionality, the payment reference is not displayed on the customer statement.



## To view the printed customer statements

When the customer statements are printed, you can view them in Business Central. Here you can see the payment reference and the related customer ledger entries.

1. Select the ![Search for page or report](/images/search_small.png) icon, enter **Customers Statements**, and select the related link.
2. Select the relevant customer statement to view the details and related customer ledger entries.

## To enable the retention policy for the printed customer statements

When using customer statements, data accumulates over time. You can use the retention policy in standard Business Central to make sure tables related to customer statements will be automatically deleted after a specified period. 

There is already a retention policy created for the customer statement data in Payment Management, but to use it, you must enable it. 

To enable the retention policy for customer statements, follow these steps.

1. Select the ![Search for page or report](/images/search_small.png) icon, enter **Retention Policies**, and select the related link.
2. Select the table ID of the "Customer Statement" retention policy. 
3. For the retention policy, specify the retention period and turn on the **Enabled** toggle. 

