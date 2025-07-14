---
title: Using the Continia Banking fields on the customer, vendor, and employee card
date: 14-04-2025
description: A guide to CB fields for setting up customers, vendors, and employees.
id: CB-113
lang: en

---

# The Continia Banking fields on the customer, vendor, and employee card

Efficiently managing payments is crucial for effective financial operations. Continia Banking enhances this process with specific fields on the Customer, Vendor, and Employee Cards that help manage payments more effectively. This article serves as a reference for the updates made by Continia Banking to these cards. 

You can find the Continia Banking fields on the **Payments** FastTab of the Customer, Vendor, and Employee Cards.

In this article, you'll find:

* Field descriptions - the table below explains each Continia Banking field on the Customer, Vendor, and Employee Cards that help you manage payment methods, prepayments, and exclusions.
* Action bar features - instructions on how to use the action bar options for tasks such as collecting payments via Direct Debit, printing statements, and setting up balance accounts.

## Continia Banking fields on the Customer, Vendor, and Employee Card
The table below lists the Continia Banking fields, found under the Payments FastTab on the Customer, Vendor, and Employee card, and explains how to use them effectively:

| Field                                      | Description                                                  | Vendor Card   | Customer Card | Employee Card |
| ------------------------------------------ | ------------------------------------------------------------ | ------------- | ------------- | ------------- |
| Skip Payment                               | Indicates whether all payments to this customer should be ignored when generating payment suggestions. | {{checkmark}} | {{checkmark}} | {{checkmark}} |
| Bal. Account No.                           | A balance account must be applied to the payment journal lines for Continia Banking to validate and process the payments. When you specify the balance account on the customer card, a balance account is automatically applied to all purchase documents for the given vendor. | {{checkmark}} | {{checkmark}} | {{checkmark}} |
| Allow Summarizing Payments                 | Indicates if multiple payments can be consolidated into a single payment suggestion. For more information, refer to the [Summarizing payments](@CB-24) article. | {{checkmark}} | {{checkmark}} | {{checkmark}} |
| Exclude Credit Memos                       | Indicates whether credit memos should be excluded when summarizing payments. | {{checkmark}} | {{checkmark}} | {{checkmark}} |
| Exclude Refunds When Summarizing Payments  | Indicates whether refunds should be excluded when summarizing payments. | {{checkmark}} | {{checkmark}} | {{checkmark}} |
| Exclude Payments When Summarizing Payments | Indicates whether individual payments should be excluded when summarizing payments. | {{checkmark}} | {{checkmark}} | {{checkmark}} |
| Employee posting group                     | Specifies the employee's category to link business transactions made for the employee with the appropriate account in the general ledger. The posting group includes details about the payables account, handling of different currencies, and management of rounding differences. |               |               | {{checkmark}} |
| Currency Code                              | This field lets you select the default currency code that is automatically applied when creating entries for the employee. |               |               | {{checkmark}} |
| Payment Reference Template                 | Specifies the template used for generating automatic payment references for this document. | {{checkmark}} | {{checkmark}} |               |
| Cost Type                                  | Specifies the type of cost related to the document.          | {{checkmark}} | {{checkmark}} |               |
| Prepayment %                               | Defines the percentage of the order amount that must be prepaid by the customer, regardless of the items or services on the order. | {{checkmark}} | {{checkmark}} |               |
| Application Method                         | Specifies how payments are applied to entries for this employee, vendor, or customer. The available options are **Manual**, which allows for custom payment allocation, and **Apply to Oldest**, which automatically applies payments to the oldest outstanding entries first. | {{checkmark}} | {{checkmark}} | {{checkmark}} |
| Bank Branch No.                            | Specifies a number of the bank branch.                       |               |               | {{checkmark}} |
| Bank Account No.                           | Specifies the account number assigned by the bank for the bank account. |               |               | {{checkmark}} |
| IBAN                                       | Specifies the International Bank Account Number for the bank account. |               |               | {{checkmark}} |
| Swift                                      | The SWIFT code, also known as a Bank Identifier Code (BIC), consists of 8 to 11 characters and helps ensure that money is sent to the correct bank and branch. |               |               | {{checkmark}} |
| Partner Type                               | Indicates whether the payment is collected from an individual or a company, particularly for direct debit collections. | {{checkmark}} | {{checkmark}} |               |
| Intrastat Partner Type                     | Indicates whether the customer is classified as an individual or a company for Intrastat reporting purposes. |               | {{checkmark}} |               |
| Payment Terms Code                         | Specifies the code for the payment terms, detailing how payments are typically made (e.g., bank transfer or OCR). Continia Banking will alert you if any updates are needed due to changes from the bank. | {{checkmark}} | {{checkmark}} |               |
| Payment Method Code                        | Identifies the specific payment method code used by Continia Banking. | {{checkmark}} | {{checkmark}} |               |
| Priority                                   | Specifies the importance of the vendor when suggesting payments using the Suggest Vendor Payments function. | {{checkmark}} |               |               |
| Block Payment Tolerance                    | Indicates whether the vendor permits payment tolerance. When this option is enabled, payment tolerance is not accepted. | {{checkmark}} |               |               |
| Preferred Bank Account                     | Designates the default vendor bank account to be used on payment journal lines for exporting to a payment bank file. This ensures that all payments processed through the journal will automatically utilize this specified bank account for the vendor. | {{checkmark}} |               |               |
| Reminder Terms Code                        | Specifies how reminders about late payments are handled for this customer. |               | {{checkmark}} |               |
| Fin. Charge Terms Code                     | Specifies the terms under which finance charges are calculated for the customer. |               | {{checkmark}} |               |
| Cash Flow Payment Terms Code               | Indicates the payment term to be used for calculating cash flow, ensuring that due date calculations and cash flow projections are consistently based on the specified payment terms. | {{checkmark}} | {{checkmark}} |               |
| Creditor No.                               | Indicates the vendor's identification number.                | {{checkmark}} |               |               |
| Print Statements                           | Indicates whether this customer should be included when printing the Statement report. |               | {{checkmark}} |               |
| Last Statement No.                         | Shows the number of the last statement printed for this customer. |               | {{checkmark}} |               |
| Block Payment Tolerance                    | Indicates that this customer is or is not allowed any payment tolerance. |               | {{checkmark}} |               |
| Preferred Bank Account Code                | Ensures that the specified preferred bank account is used for this customer when processing journal lines. |               | {{checkmark}} |               |
| Exclude from Payment                       | When enabled, the customer, vendor, or employee is excluded from payment calculations. This means that they will not be included in the system's automatic payment processing and  any invoices or payment entries related to them are not processed in the normal payment cycle. | {{checkmark}} | {{checkmark}} |               |
| Recipient Email                            | Specifies the email address that will be used to notify the customer, vendor, or employee when making payments to this customer. | {{checkmark}} | {{checkmark}} | {{checkmark}} |
| Remittance Advice Information Type         | Lets you choose how remittance details are sent: by bank information only, bank plus email, or bank plus PDF. The **Bank & PDF** option is especially convenient when the recipient’s email address is unknown. | {{checkmark}} | {{checkmark}} | {{checkmark}} |
| Compress Remittance Text                   | Indicates whether remittance advice text should be compressed for this customer, vendor, or employee. | {{checkmark}} | {{checkmark}} | {{checkmark}} |
| Remittance Advice Information Type         | Specifies how remittance advice information is typically sent to this customer, vendor, or employee. | {{checkmark}} | {{checkmark}} | {{checkmark}} |
| Create Remittance Advice After x Entries   | Indicates if remittance advice should be sent after a certain number of payment entries. | {{checkmark}} | {{checkmark}} | {{checkmark}} |
| Name, Address, Address 2, Post Code, City  | On the **Alternative Vendor Information** FastTab, you can add the address if the name or address contains special characters. | {{checkmark}} | {{checkmark}} | {{checkmark}} |

## Action bar features on the Customer card

On the customer card's action bar, Continia Banking offers several functionalities:

### To collect payments via Direct Debit

To streamline collecting payments, you can set up Direct Debit mandates:

1. Navigate to the customer card.
2. Select **Customer** > **Direct Debit Mandates** to group payments based on the mandate ID.

### To print a customer statement

Print customer statements with a payment reference, allowing customers to pay multiple invoices using a single reference.

1. On the customer card, select **Report** > **Statement** from the action menu.
2. In the **Customer Statement** page, specify the required details and click **OK** to print the statement.

### To configure balance accounts

Set up customer-specific balance accounts for more precise payment processing:

1. On the customer card, on the action bar, select **Related** > **Customer** > **Payment Balance Account Setup**.

2. In the **Bank Account** column, choose the bank account you want to use. For general use, select your primary bank account and leave the **Currency Code** column empty. For specific transactions, such as those in US dollars, set the **Currency Code** to **USD**.



<style>

 .content table tr td:nth-child(1) {
 width: 175px;
 }
 .content table tr td:nth-child(2) {
 width: 565px;
 }
  }
 .content table tr td:nth-child(3) {
 width: 20px;
 }
  }
 .content table tr td:nth-child(4) {
 width: 20px;
 }
  }
 .content table tr td:nth-child(5) {
 width: 20px;
 }
</style>

