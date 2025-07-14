---
title: Using the advanced payment suggestions mode in Continia Banking
description: Learn more about the functionality that is enabled when using the Advanced Payment Suggestions mode.
date: 11-02-2025
id: CB-145
lang: en

---

# The Advanced Payment Suggestion option

The Advanced Payment Suggestion option in Continia Banking offers a more detailed way to create and manage payment suggestions. While keeping tasks simple and fast in the standard setup for payment processes that don't require considering many details and control, the Advanced Payment Suggestion mode supports more complex payment scenarios, such as partial payment, payment discount and due date handling, flexible summarizing of payments, keeping a structured overview on all payments in a payment suggestion. You can enable the Advanced Payment Suggestion option, in the [Banking Export Setup](@CB-23).

## Key features

Choose the Advanced Payment Suggestion option if there is the need for a more granular control over payments. This option will enable you to manage and monitor payments individually, providing enhanced visibility on the payment related data.

The key features of the Advanced Payment Suggestion mode:

* Summarized information on overall payment suggestion, including details on payment method, currency, or bank level.
* Payment overview with summarized amounts per payment, payment methods, details on recipient bank accounts as well as sender bank accounts.
* Fast access to all vendor and customer related information on the payment level.
* Direct access to ledger entries and their details from within the payments.
* Easy handling of partial payments and payment discounts for each individual payment.
* Payments for Associations - integrating Continia Banking with Continia Finance allows you to efficiently manage payments to vendor or customer associations while maintaining standard checks on due dates, payment discounts, and other details.
* Payment Suggestion Templates with predefined filter settings to simplify and speed up recurring payment processes.

## Key differences

In the standard setup, the user is working from the payment journal. With Advanced Payment Suggestions, the user can choose to work directly from the Payment Suggestions taking advantage of the detailed information offered here.

### Standard setup

Working with payments using Continia Banking's standard setup is a straightforward, efficient process. The system manages payments in a straightforward way, ideal for users who require a quick, streamlined workflow without the need for extensive customization or additional steps. Once the payment suggestion is generated, it is automatically transferred to the Payment Journal, enabling fast processing with minimal effort and fewer steps involved.

The procedure using the standard setup:

* The user runs the Payment Suggestion process, generating the suggestion and transferring it to the Payment Journal, where they can review the payments, send them to the bank, update statuses, and post the transactions.

### Advanced Payment Suggestion setup

The Advance Payment suggestion setup is designed for users who want more flexibility and control over the payment process before the payments are finalized. Initially, the payment suggestion remains in the advanced Payment Overview on the Payment Suggestions page, where all payments and direct debits are displayed along with recipient information and a detailed view of the applied entries. This allows users to review, adjust, and fine-tune payment details as needed before transferring them to the Payment Journal for final processing.

The procedure using the advanced setup:

1. The user runs the Payment Suggestion, and the system creates the suggestion similar to the Standard Setup. Instead of immediately moving the data to the Payment Journal, the system presents the user with an advanced view. The user can edit, validate, or manipulate the payment lines in this advanced view. This allows for a more thorough review and handling of payments before finalizing them. Once the user is satisfied with the suggestions, the payment lines are transferred to the Payment Journal.
2. Final steps in the Payment Journal - after the transfer, the user completes the process in the Payment Journal, where they can send the payments to the bank, update payment statuses, and post the transactions, following a workflow similar to the standard setup.

## To switch between Standard and Advanced mode on journal batch level

To offer even more flexibility over payment processes, you have the possibility to set a different mode per journal batch. For example, companies can set the default mode to **Standard** in the Banking Export Setup for efficiency but enable **Advanced Mode** for specific journal batches that require more detailed handling. This is especially useful when managing vendors differently - such as enabling Advanced Mode for vendors with large volumes of payments, complex discount structures, or special due date considerations - while keeping a simpler setup for others.

To change the Banking Suggestion mode for a journal batch:
* On the General Journal **Batches** page, navigate to the journal and in the Banking Suggestion Mode column, select one of the following options:
  * **Empty** - uses the default setup.
  * **Advanced Mode** - enables advanced payment suggestions. First make sure all entries are posted in the payment journal before using payment suggestions. 
  * **Standard Mode** - uses standard payment suggestions.

> [!IMPORTANT]
>
> If a journal batch has a different mode than the **Banking Export Setup**, the batch setting takes precedence.



