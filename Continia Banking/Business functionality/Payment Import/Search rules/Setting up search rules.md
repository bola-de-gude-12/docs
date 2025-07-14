---
title: Setting up search rules in Continia Banking
description: Learn about adding search rules and the settings involved.
date: 01-10-2024
id: CB-104
lang: en
---

# Setting up Search Rules

During the bank account statement import, the system identifies transactions and attempts to match them with corresponding accounts. If the system does not recognize an account, you can define search rules to assist in identifying accounts based on specific text criteria. These rules are particularly useful for recurring entries such as interests or fees.

To set up search rules:

1. Search ({{search}}) for and select **Search rules**. Alternatively, on the **Bank Account Reconciliation** or **Payment Journal Reconciliation** page, select the bank statement line that needs a search rule, and on the action bar, select **Rules** > **Add Search Rule**. If a search rule with the same search text already exists, the system opens the existing rule.

1. On the **Search Rules** page, navigate to the action bar and select **New** to create a new reconciliation rule.

1. In the **Search Text** field, specify the text to search for when the reconciliation rule is used on the bank account reconciliation lines to identify a match. If you want to use multiple search texts to identify an account, select **Add additional search texts** on the action bar. 

1. In the **Usage Type** field, you can decide how to apply the search rule. The options are:
   * **Always** - select this option if the rule should be applied regardless of the presence or absence of payment application proposals.
   * **With proposal** -  if the rule should be applied only when payment application proposals exist.
   * **Without proposal** - select this option if the rule should be applied only when no payment application proposals exist.

1. In the **Search Field Template** field, you can specify where the system should look for the text. You can include multiple fields in your search. If the text matches any field in the template, the rule is applied to bank statement lines or payment reconciliation journal lines. By default, the most common search field templates are available. To create a new template, select the three dots to open the **Search Field Templates** page, then choose **New**. Enter a Template Code, Template Description, and define the Field Selection Text in this format: `<Table|Field>`. For instance, to search for text in the city field, use `<Bank Acc. Reconciliation Line|Related-Party City>`.

1. In the **Search Method** field, specify how the search is carried out when searching for the specified search text. The options are:

   * **Exact** indicates that the search text must match all the fields from the reconciliation line fields for the rule to be met.

   - **From left** indicates that search text must match the first part of the fields on the reconciliation line (detail) fields for the rule to be met.
   - **From right** indicates that search text must match the last part of the fields on the reconciliation line (detail) fields for the rule to be met.
   - **Within** indicates that search text must just appear some place in the fields on the reconciliation line (detail) fields for the rule to be met.


> [!NOTE]
>
> The fields **Search Text**, **Search Field Template**, **Account Type**, and **Account No.** are mandatory. If any of these fields are missing when a search rule is created, a notification will be displayed on the Bank Account Reconciliation Page and the Payment Reconciliation Journal Page.

On the **Banking Import Setup** page, it is possible to define a template for the default search field.

To create a search rule:

1. In the **Account Type** field, specify to assign to the G/L account, customer, vendor, or employee.
1. In the **Account No.** field, specify the balance account to which the entry will be applied.
1. Use the fields in the **Rule Filter** FastTab to define conditions under which a rule is to be applied. The following fields apply:
   * For the **Amount Filter**, select **Only Negative** to apply the search rule exclusively to lines with negative amounts, or **Only Positive** for lines with positive amounts. Select **All** to apply the rule to every line, regardless of the amount. 
   * Use the **Statement Type Filter** if you want to determine which type the bank account reconciliation is originating from. 
   * Use the **Bank Code** field to specify whether the search rule should be applied to a specific bank. When selecting a specific bank, the search rule applies exclusively to bank statement lines or payment reconciliation journal lines associated with the designated bank account.
   * Use the **Bank Account** field to specify whether the search rule should be applied to a specific bank account. When no account is specified, the rule is applicable to all bank accounts.
1. The fields in the **Posting** FastTab help you how to post the lines. For example, you can add a template for the posting description and assign the VAT business posting group to use. 

> [!TIP]
>
> To disable a rule, go to the **Search Rule** page, and in the **General** FastTab, activate **Disable**. Disabled rules won't be applied during matching.

