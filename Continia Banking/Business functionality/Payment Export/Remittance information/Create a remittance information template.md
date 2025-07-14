---
title: Create a Remittance Information Template in Continia Banking
description: Learn how to add a custom remittance information template.
date: 12-06-2025	
id: CB-117
lang: en
---

# Adding a remittance information template

Remittance information helps payees reconcile incoming payments by detailing which invoices or accounts the payments relate to. To streamline this process and ensure clarity, you can use **Remittance Information Templates** in Continia Banking. These templates define how payment-related data - such as invoice numbers and amounts - should appear in the remittance text.

This article explains how to create and customize a template. To learn how to apply a template to vendor payments, see [Selecting a Remittance Information Template](@CB-116).

## To add a remittance information template

To create a template:

1. Search ({{search}}) for and select **Remittance Templates**.
2. On the **Remittance Templates** page, to add or change a template, enter information for the **Template Code** and **Template Description**. Enter a descriptive template description that clarifies the purpose and functionality of this template.

   > [!IMPORTANT]
   >
   > Do not change the default DEFREMMITANCEINFORM. It will be automatically updated by the setup server during system updates.

3. The **Remittance Information Pattern** field controls how payment information is formatted in the communication to vendors. This pattern is applied across all transaction lines when the [template is selected for the journal](@CB-116). Click the three dots on the far right to access the **Field Selection** page.
4. Select the data fields you want to include, such as document type, document no., and amount.
5. Click **OK** to insert them into the pattern.
   ![Remittance fields](/images/CB/remittance-fields.png)

   > [!NOTE]
   >
   > To apply a remittance template when suggesting payments, click **Show More** on the **Suggest Vendor Payments** page and locate the **Remittance Information Template** field.
6. Additionally options are:

   * **Sorting Field** – defines the order in which payment lines are presented.
   * **Template Method: Line Break** – adds a line break between data entries for better structure.
   * **Template Field Properties** – customizes how each selected field is displayed. Click the three dots beside the pattern to open this page and refine your formatting.

## Examples

You can use the Remittance Information Pattern field to create customized formats for presenting remittance details in communication.

Imagine a company is ABC Corporation with the following vendor ledger entries to be paid:

* Invoice 4711
* Invoice 4712

### Pattern setup example 1

#### Pattern

`<Company Information|Name><Template Method|Line Break><Payment Suggestion Line|Applies-to Doc. Type> <Payment Suggestion Line|External Document No.>`

#### Generated remittance information example 1

ABC Corporation,Invoice 4711, Invoice 4712


#### Pattern setup example 2

`<Company Information|Name><Payment Suggestion Line|Applies-to Doc. Type> <Payment Suggestion Line|External Document No.>`

#### Generated remittance information example 2

ABC Corporation Invoice 4711, ABC Corporation Invoice 4712

Here, the company name is included with each invoice detail, resulting in a more detailed line-by-line format.

When preparing remittance information, especially for formats with strict character limits like SEPA (which allows one line with 140 characters), it's crucial to optimize space. The goal is to include as much relevant information as possible without redundant repetition of the company's name. The company name should ideally appear just once to maximize the space available for other important details.
