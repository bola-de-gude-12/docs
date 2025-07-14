---
title: The split rule fields
description: Learn more about the general fields that apply to all split rules.
date: 14-04-2025
id: CB-234
lang: en
---

# The split rule fields

The following table lists the general fields that apply to all split rules and describes their functionality. Some of these fields are mandatory and are marked with an asterisk (*).

| Field                        | Description                                                  |
| ---------------------------- | ------------------------------------------------------------ |
| Account Type                 | In the **Account Type** field, specify to assign to the G/L account, customer, vendor, or employee. |
| Account No.                  | In the **Account No.** field, specify the balance account to which the entry will be applied. |
| Document Type                | Defines the type of transaction, such as Payment, Invoice, Credit Memo, or Refund. |
| Posting Description Template | The **Posting Description Template** defines the format for transaction descriptions, particularly when handling amount differences in bank reconciliation. These templates ensure consistency in transaction descriptions. Default templates are available, but you can also create a custom template. |
| Department Code              | Specifies the department related to the transaction for cost allocation and reporting. |
| Project Code                 | Assigns the payment to a specific project for tracking expenses and revenues related to that project. |
| Gen. Posting Type            | Select the posting type for the VAT key code. For example, Sales. |
| Gen. Bus. Posting Group      | Categorizes the type of business (e.g., domestic, EU, export) involved in the transaction. |
| Gen. Prod. Posting Group     | Categorizes the type of product or service.                  |
| VAT Bus. Posting Group       | The VAT Business Posting Group determines how VAT is applied based on the business entity involved in a transaction. It allows for proper tax calculation and compliance by mapping captured amounts to specific VAT setups, overriding default values when necessary. |
| VAT Prod. Posting Group      | Here you can choose the VAT Prod. Posting Group to use for posting VAT for a payment. |