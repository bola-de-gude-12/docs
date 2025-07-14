---
title: Reimbursing customers and paying credit memos
description: How to suggest a customer payment.
date: 09-11-2022
id: PM-271
lang: en
---

# Reimbursing customers and paying credit memos

Occasionally, you may need to cancel all or part of an invoice that has already been issued. For example, a customer returned an item, or you made a mistake on the invoice and want to refund the customer the excessive amount. 

With Payment Management, you can directly suggest and validate reimbursement payments and credit memos in the payment journal. By default, the payment journal is intended for managing payments, i.e., to pay your vendors or employees. However, with the added feature of suggesting customer payments, you can create payment lines to reimburse or pay credit memos to customers. 

## To reimburse a customer using the payment journal

In the payment journal, you can create customer payment suggestions based on potential credit memos. This is only possible if the credit memo is higher than the owed balance, meaning a negative balance on the customer.

For example, if a specific customer has $5,000 in outstanding sales invoices, and because of returned goods, the same customer is issued a credit sales memo of $6,000, the payment of $1,000 of document type **Refund** will be created when suggesting a customer payment.

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Journals**, then select the related link. 

1. In the page header, in the field **Batch Name**, choose the payment journal you want to suggest payments for, and select **Prepare** > **Suggest Customer Payment**.

1. On the **Suggest Customer Payment** page, enter information for the relevant fields. For example, set the date filter and select the customer.

1. Select **OK** to create the suggested customer payment lines. Payment lines that comply with the settings of the payment journal suggestion will now be created in the payment journal.  All payment lines must have the status **Valid** before they can be exported to the bank. In case of errors on a payment line, you can use the Payment File Errors, located in the lower right corner of the payment journal, to find a more descriptive error message. 

   In addition, when Payment Management processes the payments, they will be posted with a unique payment ID which will be used to apply the bank account ledger entries in the bank account reconciliation.

> [!NOTE]
>
> Customer reimbursements of customers who still owe you more than you owe them will not display when using the Suggest Customer Payment functionality. To reimburse customers with a negative balance, you must create the payment line and manually reconcile the open credit memo.



## Related information

[Summarizing Payments](@PM-186)

[Suggesting and Processing Payments](@PM-90)

