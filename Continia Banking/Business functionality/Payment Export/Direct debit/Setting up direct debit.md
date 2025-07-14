---
title: Setting up direct debit in Continia Banking
description: Learn how to configure and manage direct debit in Continia Banking.
date: 12-06-2025	
id: CB-130
lang: en
---

# Setting up direct debit

Continia Banking enhances the standard direct debit functionality in Business Central by enabling users to view and manage customer direct debit suggestions. This allows you to track collections transferred from the customer’s bank account to yours.

## To configure direct debit

Before you can process direct debits, you must enable and configure the relevant settings.

To configure direct debit:

1. Search ({{search}}) for and select **Banking Export Setup**.
2. On the **Direct Debit** FastTab, enable **Use Direct Debit**.
3. From the **Default Template Name** and **Default Batch Name** fields, select the templates you want to use for direct debit. These fields specify the default template and batch names for payment suggestions when processing direct debits. Once enabled, the system will prefill related fields during payment processing.

## To view mandate usage history

You can track how and where a SEPA mandate has been used. This includes identifying if a mandate was voided and reviewing all related transactions for auditing or troubleshooting purposes.

To view mandate usage:

1. Search ({{search}}) for and select **SEPA Direct Debit Mandates**. 

2. On the **Direct Debit Mandate Usages** page, you can review the list of the different payment registers. For example, you could see that a direct debit mandate was used but subsequently voided. This helps identify discrepancies, such as why a mandate appears to have been used only five times instead of six.

   

## To process direct debit payment suggestions

Continia Banking provides an enhanced journal for processing direct debit payments. You can automate this with templates that generate daily suggestions and optionally integrate with an approval workflow. 

To create direct debit payment suggestions:

1. Search ({{search}}) for and select **Payment Suggestions**. 
2. On the action bar, click **Suggest Customer Direct Debits**.
3. Follow the same steps as described in the [Suggesting and Processing Payment](@CB-109) article. The journal information gets prefilled by the settings from the Banking Export Setup. 
4. On the **Payment Suggestion Card** page, verify fields such as **SEPA Mandate ID**, **SEPA Mandate Sequence Type**, and **SEPA Mandate Date of Signature**. 
5. On the action bar, click **Create Journal Lines**. You can access the direct debit journal directly from this page. Alternatively, you can navigate to the direct debit journal from the payment suggestion page. You can now proceed like you would in any other journal. 

You can also [create a payment suggestion template](@CB-89) or [set up an approval workflow](@CB-27) to automate this further. 
