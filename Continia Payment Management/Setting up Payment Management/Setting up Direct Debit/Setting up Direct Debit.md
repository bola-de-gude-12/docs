---
title: Setting up Direct Debit
date: 20-11-2024
description: How to set up and work with direct debit and direct debit reversal rules.
id: PM-223
lang: en
---

# Setting up Direct Debit

Payment Management Direct Debit enables you to perform a direct debit collection from a customer's bank account to your bank account and to set up rules to handle reversal transactions automatically.

> [!NOTE]
>
> If you use the on-premises version of Business Central, ask your Continia partner to add the [relevant license granule](@PM-18) to your license file.



## Requirements

The minimum requirements for setting up Direct Debit are:

* Rabobank, ING Bank, or ABN Amro. 

  > [!NOTE]
  >
  > You can use PM Direct Debit with direct communication for Rabobank. For ING and ABN AMRO, you can only use PM Direct Debit with manual communication. If you want to add support for a different bank, please contact Continia to learn more about the possibilities.

* Manual communication - direct debit only allows manual file upload (Pain.008).

* Mandate ID - before you can collect payment by Direct Debit, your customer must issue you with a mandate that authorizes you to collect future payments.

* Transactions must be in euros.

  

## To set up Direct Debit

>  [!IMPORTANT]
>
> For Payment Management versions lower than 5.0, you must enable Direct Debit on the Continia Feature Management page in Microsoft Dynamics 365 Business Central.

In recent versions of Payment Management, Direct Debit is automatically activated in the Payment Management Setup. If you use Payment Management version 4.4.0.2 or lower, you must activate the feature in the Payment Management Setup:

1. Select the ![Search for page or report](/images/search_small.png) icon, enter **Payment Management Setup** and select the related link. 
2. Navigate to the FastTab **Usage Areas** and enable **Direct Debit**.



Before you start using the Direct Debit module, follow these steps to set it up:

1. Select the ![Search for page or report](/images/search_small.png) icon, enter **Direct Debit Setup** and select the related link.

2. On the **Direct Debit Setup** page, enter information into the following fields:
   - **Separate by Sequence Type** – if enabled, on a new mandate ID, all the collection entries of the sequence type *First* are exported before you export the collection entries of the type *Recurring*. This applies to the collection entries on the same mandate ID. For more information about direct debit collection entries, see the article [Working with Direct Debit Collections](@PM-246).
   - **Process On Export** – determine if you want to process the direct debit files after they are posted automatically. The options are: *Move and post entries* and *Move entries to the journal*.
   - **General Journal Template** - specify the general journal template to which the direct debit entries will be moved if you choose to automatically process the entries after the direct debit file is exported.
   - **General Journal Batch** - specify the general journal batch to which the direct debit entries will be moved if you choose to automatically process the entries after the direct debit file is exported.
   - **Show Reversals in Role Center** – change the date range in which reversals must have been created for the related invoice to appear in the **New Reversals** Cues on the Role Center. By default, the **New Reversals** Cues lists invoices whose payment has been reversed in the last week from today’s date (-1W).
   - **Post Complete Group** - if enabled, all general journal lines belonging to the same direct debit group are posted simultaneously.
   - **Number of Direct Debit Entries per Collection** - by default, the system can handle a large volume of entries. If processing becomes slow, you can improve efficiency by reducing the number of entries per collection.


## To set up Direct Debit on the customer card

To use direct debit on the customer card:

1. On the customer card,  select **Customer** > **Direct Debit Mandates**.
2. On the **SEPA Direct Debit Mandates** page, in the ID field, enter the Mandate ID you received from the customer.
3. Navigate to the FastTab **Payments**, and in the **Partner Type** field, select *Company* if you received the Mandate ID from the customer.
4. To specify the mandate ID, you want to add to invoices automatically, go to the **Preferred Mandate ID** field and select the ID.


## To set up Direct Debit on the bank card

To use direct debit on the bank card:

1. On the bank card, go to **General** > **Bank System** and add the bank to the **Manual** field.

2. On the bank card, go to **Import/Export** and set the **Direct Debit Export** field to *Manual*.

## To set up Direct Debit reversal rules

A direct debit reversal occurs when customers reject a recurring payment and return the money to their account. In Payment Management, you can set up rules for how to react to reversals for a specific customer or all your customers. For example, if the same customer has reversed a payment multiple times, you can set up Payment Management to put the relevant invoice on hold. 

To create a reversal rule:

1. Select the ![Search for a page or report](/images/search_small.png) icon, enter **Direct Debit Setup** and select the related link.

2. On the action bar, select **Reversal Rules**.

3. On the **Reversal Rules** page, select **New** to create a new rule, and fill in the following fields: 
   
   | Field                     | Description                                                  |
   | ------------------------- | ------------------------------------------------------------ |
   | Reversal Code             | Select the reversal code to specify the reason for the direct debit reversal. For example, an invalid file format or a wrong account number. Required field. |
   | Reversal Description      | Description of the reason for the reversal. For example, an invalid file format, a wrong account number, or incorrect currency. |
   | Customer No.              | Specify the customer the reversal applies to.                |
   | Customer Name             | Specify the customer name.                                   |
   | Type                      | Specify if the rule applies to a single customer or all customers. Required field. If you select **Customer Specific**, you must select a customer in the **Customer No**. field. |
   | Action                    | Specify the action that follows after the reversal rule is triggered. The options are: **Invoice on hold** and **Block the customer**. If you select **Block the Customer**, it will block the specific customer, and you can't create new invoices. The **Invoice on Hold** option will put the related invoice on hold until you resolve the situation manually and clear the **Invoice on Hold** field on the corresponding customer ledger entry. Required field. |
   | Required No. of Reversals | Specifies after how many reversals the rule must be triggered. |
   
   If a reversal rule is applied, the invoices that can't be handled are displayed in the Reconciliation.

To post a reversal, see the [Working with Direct Debit Collections article](@PM-246)

## Related information

[Working with Direct Debit Collections](@PM-246)  
[About Direct Debit – Dynamics 365 Business Central](https://docs.microsoft.com/en-us/dynamics365/business-central/finance-collect-payments-with-sepa-direct-debit)

