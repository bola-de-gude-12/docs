---
title: The Payment Management Setup Page
description: The Payment Management Setup Page
date: 16-02-2024
id: PM-385
lang: en
---
# The Payment Management Setup Page

Payment Management offers a wide range of configuration options that allow you to adjust the app to fit your organization's needs. 

> [!NOTE]
>
> If you have completed the [Assisted setup guide for Payment Management](@PM-2), you have already reviewed the most necessary setups of Payment Management. Use the information below if you want to customize the solution or change your setup.

To access the general setup page of Payment Management: 

* Select the ![Search for page or report](/images/search_small.png) icon and search for **Payment Management Setup**, then select the related link. 

## Purchase and Payments fields	

The following table lists the individual fields and functions of the Payment Management Setup page for the **Purchase and Payments** FastTab and what consequences this has for using Payment Management.

| Field                                 | Description                                                  |
| ------------------------------------- | ------------------------------------------------------------ |
| Validate Purchase Document            | If enabled, validation occurs when you manually select the action **Validate Document** on the purchase document or when you post the purchase document. This setting is mandatory for Payment Management to validate purchase documents and is enabled by default. For more information, refer to the [Setting up Purchase documents](@PM-177) article. |
| Use Dynamic Validation                | If enabled, dynamic validation runs in the background, ensuring that payment information is validated whenever something is entered within fields on the page. As you work on the purchase document, any validation errors will be displayed in the **Validation** FactBox when you reload or reopen the document. This setting is enabled by default. Refer to the [Setting up Purchase documents](@PM-177) article for more information. |
| Validate Purchase Journal             | If enabled, validation occurs when you manually select the action **Validate Journal** on the purchase journal or when you post the journal. This setting is enabled by default. For more information, refer to the [Setting up Purchase Journal Validation](@PM-253) article. |
| Use Dynamic Journal                   | If enabled, validation runs in the background dynamically while you work on the purchase journal, and any validation errors will be displayed in the **Validation** FactBox when you reload or reopen the journal. This setting is enabled by default. For more information, refer to the [Setting up Purchase Journal Validation](@PM-253) article. |
| Validate Purchase Order on Approval   | If enabled, payment information for a purchase order should be validated before the order can be approved. |
| Validate Purchase Invoice on Approval | If enabled, the payment information for a purchase invoice should be validated before the invoice can be approved. |
| Balance Account Required              | If enabled, a balance account is mandatory for purchase documents to ensure payment data validation. This setting is enabled by default. |
| Generate Payment Reference            | Specifies if payment reference should be generated from the template on purchase documents and journals. The payment reference serves as a message accompanying the payment, containing payment details. While payment references assist the recipient in identifying transactions, sender references aid in reconciling bank statement lines during account management. This setting is enabled by default. For more information, refer to the [Setting up Payment References](@PM-43) article. |
| Payment Method View                   | Specifies the payment methods to be displayed in the payment method lookup for vendors and purchase documents. Select **Filtered** to show only the relevant payment methods for each vendor or document.<br />To remove the payment method filter and get an overview of all available payment methods, select **All**.<br />For more information, refer to the [Setting up Payment Methods](@PM-4) article. |
| Required Posting Status               | This setting specifies the payment status that needs to be met before payment journal lines can be posted. If you use direct communication, it is recommended that you set this value to **Processing** or **Paid**. For instance, if you select **Paid**, only the lines that have been paid will be posted. However, if you choose **Sent** or **Processing**, all payments in the journal with this status or higher will be posted. If there is no required status specified in the Payment Journal Setup, the value from this field in the Payment Management Setup page will be used. For more information, refer to the [Setting up Payment Journals](@PM-14) article. |
| Confirm Manual Payments               | To avoid mistakenly registering a payment as a manual payment, you can use Payment Management to notify the user before posting a payment journal. This feature specifies whether or not the user should be alerted about manual payments when posting a payment journal. For more information, refer to the [Manual Payments](@PM-15) article. |
| Use Exchange Rate Adjustment          | If enabled, Payment Management will update exchange rates in the payment journal automatically if this is supported by the bank. For more information, refer to the [Manage Exchange Rate Adjustments](@PM-68) article. |
| Allow Updating Posting Date           | This option specifies whether you want to update the posting date for payment if it can't be completed on the specified date. Please note that this option is only applicable if the payment line has not been posted yet. However, it's important to keep in mind that not all banks provide the actual posting date. For more information, refer to the [Managing Posting Dates](@PM-212) article. |
| Use Bank Account Verification         | If enabled, the bank account is verified to ensure it's trustworthy to prevent fraud. For more information, refer to the [Bank Account Verification](@PM-352) article. |
| Update Method                         | Specifies how you want to keep the bank system updated in Business Central. |
| Automatic Update Time                 | Specifies the time of day you want the bank system to update automatically. |
| Handle G-Account base amount          | Specifies whether to add the G-Account base amount to the purchase invoice manually or automatically (adds the total amount, including VAT). Available in Dutch localization. |

## Payment Receipt Import fields

The following table lists the individual fields and functions of the Payment Management Setup page for the **Payment Receipt Import** FastTab and what consequences this has for the use of Payment Management.

| Field                                        | Description                                                  |
| -------------------------------------------- | ------------------------------------------------------------ |
| Default Payment Reference Mask               | Specifies the default payment reference mask used for matching OCR references when matching payment receipts. For more information, refer to the [Defining the Payment ID mask](@PM-92) article. |
| Customer Statement Nos.                      | Specifies the number series code for generating unique payment references on customer statements. |
| Update External Payment Reference            | Select the field that should be automatically copied to the sales documents as the reference number value. For more information, refer to the [Adding a Payment Service Provider](@PM-298) article. |
| Custom External Payment Reference Field Name | If you selected **Using Custom Field** in the **Update External Payment Reference** field, select the appropriate field from the **Sales Header** table. For more information, refer to the [Adding a Payment Service Provider](@PM-298) article. |

## Usage Areas

After Payment Management is installed and activated, it automatically enables usage areas that allow you to use it in the payment journal, cash receipt journal, and bank account reconciliation. If you turn off a usage area such as **Payments**, you won't be able to use the Payment Management Payment Journal to process payments.

For more information, refer to the [Manage Usage Areas](@PM-207) article.

## Related information

[Assisted Setups for the Payment Management Configuration](@PM-2)  
[Setting up bank holidays](@PM-7)  
[Setting up currency exchange rates](@PM-41)  

