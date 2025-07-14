---
title: Setting up purchase documents in Payment Management
description: How to set up purchase documents
date: 04-07-2022
id: PM-177
lang: en
---

# Setting up purchase documents

Payment Management uses various payment information on the purchase document to ensure that payments are managed correctly, and critical payment information is available when payments are sent to the bank. Payment Management is set up by default to validate the payment information entered on the purchase documents.

## Preparing payment details

On the vendor card, you can define the payment details needed for Payment Management to automatically fill in the required payment information when creating purchase documents for the given vendor. 

Open the relevant vendor card and fill in the fields as described in the following table.

| Field | Description |
| --- | ----------- |
| **Balance account** | Enter the company bank account from which you want to pay the vendor. |
| **Recipient Bank Account Code** | Select the vendor bank account code that specifies the vendor bank account to which the payments should be transferred for purchases. |
| **Payment Method Code** | Specify how you want to pay the vendor. |
| **Payment Reference Template** | Specify the template that must be used for building automatic payment references for the purchase. The payment reference templates can contain various information constructed from predefined payment fields. |
| **Notification Template** | Choose the payment notification template. The template defines which information about the purchase must be included in the payment notification received by the vendor. |
| **Notification Method** | Specify how you want to notify your vendor about the payment of a given purchase. |
| **Cost Type Code** | Specify who should pay a potential fee for the purchase. When you make a payment that involves a fee, such as SEPA payments, the cost type code can be used to define who should pay the fee. Cost type code can also be defined on the payment method.<br />For information about setting up cost type codes, see [Setting up Cost Types](@PM-44). |
| **Regulatory Reporting Codes** | Select the regulatory reporting codes to be defined for the payment (mainly relevant for cross-border payments). For more information about reporting codes, see [Setting up Regulatory Reporting Codes](@PM-199). |



## Validating payment details

Validation is enabled by default for purchase documents to notify you about any incorrect or missing payment information. The validation runs in the background while you're working on the purchase document, and again when you post it.

The validation is executed when you:

- Reopen the purchase document.
- Reload the purchase document.
- Manually validate the purchase document by selecting **Validate Document** from the action bar.
- Preview the posting of the document or post it.

> [!TIP]
>
> On the purchase document, enable the **Validation** FactBox to see potential validation errors for the document. If you disable the **Use Dynamic Validation** setting, you must manually run the action **Validate Document** to see the validation errors before posting the document.



## To manage purchase document validation

To ensure effective management of purchase document validation, dynamic validation settings for purchase documents are enabled by default. When enabled, approval can only be granted once the validation process is successfully completed.

To view and or edit the validation settings for purchase documents:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Management Setup**, then select the related link. 
2. In the **Purchase and Payments** FastTab, you can change the validation settings.
   - **Validate Purchase Document** - validation occurs when you manually select the action **Validate Document** on the purchase document or when you post the purchase document. This setting is mandatory for Payment Management to perform validation on purchase documents. 
   - **Use Dynamic Validation** - dynamic validation runs in the background while you work on the purchase document, and any validation errors will be displayed in the **Validation** FactBox when you reload or reopen the document. To enable this setting, the **Validate Purchase Document** setting must be enabled. 
   
     > [!NOTE]
     >
     > If you want to disable pre-validation of payment information in Document Capture before document approval, you must deactivate all validation fields.

## Related information

[Setting up validation of purchase journals](@PM-253)
