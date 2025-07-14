---
title: Setting up a Payment Reference Rule
description: Learn more about how Continia Banking's default rules for reconciling payment references, such as FIK, SCOR, and Swiss QR, automate and ensure accuracy in financial record matching by defining how references are validated and processed.		
date: 27-03-2025	
id: CB-169
lang: en
---

# Setting up a payment reference rule

Continia Banking provides default rules for reconciling various types of payment references, such as FIK, SCOR, and Swiss QR references. These rules are designed to locate references in the document number or payment reference fields.

Creating a payment reference rule automates reconciliation, ensuring accuracy and consistency in financial records. It defines how references are validated, matched, and processed. 

Continia Banking offers the following important guidelines:

- **Mandatory Fields** - fields marked with a red asterisk (*) are mandatory. Make sure these fields are completed to prevent errors.
- **Notifications** - if any settings are missing or incorrect, notifications will appear in the Bank Account Reconciliation or Payment Reconciliation Journal, helping you quickly identify and address issues.

## To access payment reference rules

Continia Banking offers default rules for reconciling payment references like FIK, SCOR, and Swiss QR. These rules identify references in document numbers or payment reference fields.

To access Payment Reference Rules:

1. On the **Banking Import Setup** page, on the action bar, select **Manual Setup** and then select **Payment Reference Rules**. Alternatively, search  ({{search}}) for and select **Payment Reference Rules**. 

2. On the **Payment Reference Rules** page you can view and download predefined rules. Continia Banking provides rules for FIK71, FIK71-PREFIX, QR, and SCOR by default. 

   > [!NOTE]
   >
   >Additional Payment Reference Rules will be introduced in future updates.


3. Selecting a rule displays its detailed configuration. For more information about the different FastTabs and fields, refer to [To set up Payment Reference Rules](#to-set-up-payment-reference-rules) section of this article. 

## To set up payment reference rules

By setting up payment reference rules, you can define how payment references are validated, matched, and processed within your system.

To set up a payment reference rule:

1. Search ({{search}}) for and select **Payment Reference Rules**. 
2. On the **Payment Reference Rules** page, on the action bar, click **New** to create a new Payment Reference Rule or click **Copy Payment Reference Rule** to use a default or previously set rule as a template. 
3. On the **General** FastTab, edit the **Payment Reference Search Field** template to specify the exact location where the reference appears in the payment statement. This helps the system accurately locate and interpret the reference.
4. On the **Validation** FastTab, use a regular expression to define a pattern code that ensures the reference follows the correct format. You can also configure the check digit, specifying its position and calculation method to further guarantee accuracy.
5. On the **Matching** FastTab, you can define the table and field where the system should search for the reference in the ledger table. Use the **Direct Match** field to decide whether the match should be exact or allow some flexibility. You’ll also need to edit the reference information by specifying the start position and length of the reference.
6. On the **Rule Filter** FastTab, set filters to apply specific conditions, to ensure the rule only applies to statement types (e.g., **CAMT.054**) or bank transaction codes. Rules are also configurable per bank or bank account, though default settings are typically sufficient.
7. On the **Test** FastTab, test the rule using the built-in testing functionality to ensure it works as expected, accurately matching references and processing them correctly.

