---
title: Using the Payment Management fields on the customer card
date: 01-03-2024
description: A guide to PM fields for setting up a customer.
id: PM-386
lang: en

---

# The Payment Management fields on the Customer Card

This article describes the Payment Management-specific fields on the customer card and how to benefit from them. On the Customer card, navigate to the FastTab **Payments** to find the following fields:

| Field                                     | Description                                                  |
| ----------------------------------------- | ------------------------------------------------------------ |
| Balance Account No.                       | A balance account must be applied to the payment journal lines for Payment Management to validate and process the payments. When you specify the balance account on the customer card, a balance account is automatically applied to all purchase documents for the given vendor. For more information, see the [Setting up Balance Accounts](@PM-62) article. |
| Payment Method Code                       | The Payment Management Payment Method Code specifies how the payments are usually submitted, for example, via a bank transfer or OCR. If the bank changes something, Payment Management will notify you to update your settings. |
| Payment Method Description                | A description of the Payment Management Payment Method code. |
| Partner Type                              | Specifies whether the payment is collected from a person or a company for direct debit collections. For more information, see [Working with Direct Debit Collections](@PM-246). |
| Preferred Mandate ID                      | Specifies the ID of the preferred mandate that you would like to automatically add to your invoices. For more information, see [Working with Direct Debit Collections](@PM-246). |
| Skip Direct Debit                         | When switched on, all payments to this customer are excluded from direct debit when creating payment suggestions. This could be convenient if you made payments not sent directly from Business Central, for example, a direct withdrawal from a credit card. |
| Recipient Email                           | Specifies the email address that will be used to notify the vendor when making payments to this vendor. |
| Limit Notification Size                   | Specifies whether to set limitations when summarizing payments. Summarized payments exceeding the allowed notification size for the payment method will be split into multiple payments. |
| Notification Template                     | Specifies the payment notification template that should be used as the default for this vendor. |
| Notification Method                       | Specifies the payment notification method that should be used as the default for this vendor. The options are *Bank only* and *Bank and Email*. |
| Name, Address, Address 2, Post Code, City | On the **Alternative Vendor Information** FastTab, you can add the address if the name or address contains special characters. See the [Defining Alternate Payment Addresses](@PM-87) article for more information. |
| Tolerance Type                            | By setting up a tolerance for reconciliation suggestions, you can widen the search for ledger entries and improve matching and suggestion possibilities. You can select to set up the tolerance in percentage or amount. See the [Defining Allowed Tolerances for Reconciliation Suggestions](@PM-273) article for more information. |
| Tolerance Value                           | Specifies if the automatic bank account reconciliation function will suggest ledger entries with the amount incl. tolerance suggested by percentage or amount. See the [Defining Allowed Tolerances for Reconciliation Suggestions](@PM-273) article for more information. |
| Preferred Bank Account Code               | This ensures that when processing journal lines, the system will use the specified preferred bank account for the customer. |

On the action bar of the customer card, Payment Management offers the following possibilities:

* **Collect payments via Direct Debit** - to streamline the process of collecting mandates, to authorize future payments, Payment Management offers setting up Direct Debit grouping based on the mandate ID. Follow these steps to enable automatic grouping:
  * Navigate to the customer card and select **Customer** > **Direct Debit Mandates**.
    To read more, refer to the [Working with Direct Debit Collections](@PM-246) article. 
* **Print a customer statement** - you can print customer statements with a payment reference allowing customers to pay multiple invoices using a single payment reference. 
  1. On the customer card, in the action menu, select **Reports** > **Statement**.
  2. On the **Customer Statement** page, specify the details for the statement you want to print and select **OK**.
     To learn more, refer to the [Setting up Customer Statements](@PM-258) article.
