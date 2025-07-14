---
title: Using Templates in Banking Export
date: 08-02-2025
description: Learn how to create a custom Continia Banking template.
id: CB-165
lang: en
---

# Using Field Templates in Banking Export

Field templates in Banking Export help standardize and automate key processes, improving consistency across payment and notification workflows. For example, **Payment Reference Templates** allow you to generate automatic payment references for documents, ensuring accurate information is applied to purchase invoices and other records. You can also define direct debit templates and format payment details. 

## Payment Reference Templates

Payment reference templates ensure that the payment references are automatically formatted correctly based on the purchase invoice details, such as the vendor invoice number and control number. 

### Default templates

Here are two examples of default Payment Reference Templates used in Continia Banking:

FIK71

* **Description** - Continia Banking FIK71 Payment Reference
* **Payment Reference Pattern**:
    *  `<Purchase Header | Vendor Invoice No.>`
    *  `<Template Method | Modulus 10 Control No.>`

FIK75

* **Description** - Continia Banking FIK75 Payment Reference
* **Payment Reference Pattern**:
  * `<Purchase Header | Vendor Invoice No.>`


These templates ensure that the payment references are automatically formatted correctly based on the purchase invoice details, such as the vendor invoice number and control number. 

## Direct Debit Templates

Direct Debit Templates allow you to manage collections and automate the processing of direct debit payments. They use specific formats to distinguish direct debit payments from other payment types.

GJ01

* **Description** - General Journal Template for Direct Debits
* **Direct Debit Template Pattern**: 
  * `DirectDebit|<Vendor Invoice No.><Control Code|Batch No.>`

This template is used when setting up the **General Journal Template** for direct debit transactions, automatically categorizing and processing the payments in the correct format.

## Remittance Information Templates

Remittance Information Templates define how payment details such as invoice numbers, payment amounts, and payment dates are formatted when sending payment notifications to vendors.

REM01

* **Description** - Remittance Information Template for Vendor Payments
* **Remittance Pattern**:
  *  `<Document Type|Invoice No.><Payment Date|Amount>`

This template ensures that remittance details are clearly presented when processing payments to vendors, helping streamline reconciliation.

