---
title: Defining Merge Rules
description: How to define merge rules for the Bank account reconciliation
date: 03-03-2021
id: PM-40
lang: en
---

# Defining Merge Rules

Continia Statement Intelligence includes a function for creating rules that merge specific account statement lines when you import an account statement. You can define merge rules that combine several account statement lines into one or more entries, e.g. one entry per day, or, one entry per. credit card terminal per day.

Merging of bank account entries is typically used where several credit card transfers are merged into one total per day because that is the amount posted in the general ledger. 

## To define merge rules

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Merge Rules**, then select the related link.
2. On the **Merge Rules** page, select **New** to create a new merge rule.
3. In the **Bank Account No.** field, choose the bank account for which you want to create a merge rule.
4. In the **Text** field, enter a text that Payment Management must search for in the payment line description in order to merge lines. Use filter expressions (*, ', ", @) to obtain a more accurate search result. Read more about [Sorting, Searching, and Filtering](https://docs.microsoft.com/en-us/dynamics365/business-central/ui-enter-criteria-filters) on Microsoft Docs.
   The payments that are identified by the search text are considered for merge, however, they will not be merged unless the criteria specified by **Merge by Date** or **Merge by Positions** is met.
5. Specify to merge either by  **Merge by Date** or **Merge by Positions**. You can only choose one of the two.
   - In the **Merge by Date** field, specify whether to merge by **Transaction Date** or **Value Date**. 
   - In the **Merge by Positions** field, specify which characters in the description on the payment you want to use to merge entries. If you for example specify 7-10, the function will merge all entries where these 4 characters are the same. You must specify from position (inclusive) to position (inclusive). 
6. Select **New** if you want to set up more merge rules.

The merge rule has now been defined and will be used the next time an account statement is imported for the given bank account. To see which account statement lines are part of the merged line select the action **Notifications** on the line.

> [!NOTE]
>
> Several merge rules can be set up per bank account. The rules are created in a list, and the prioritization of which rule is used will take place from top to bottom. If the first rule defined for the bank account does not comply with then Statement Intelligence will proceed to the next rule, and so on.

## Example of defining a merge rule

This is an example of how to use the search text in a merge rule. 

In this example, an account statement is imported into the reconciliation journal. The description from a payment in the file is ”DKFLCS0102 4015711830300”. In the description the date is placed in position 7-10 (0102), the credit card terminal number is 4015711, and the rest is a slip number.

In the example below the **Text** includes a wildcard (*), and the rule will **Merge by Positions**.

By inserting wildcards at these positions, as well as by specifying in the field **Merge by Position** which characters to merge by, you can use the merge rule to create one account statement line per day per terminal.

**Text**: `DKFLSC*4015711*`

**Merge by Positions**: 7-10

The following account statement lines thus become one line:

”DKFLCS**0102** **4015711**830300” </br>
”DKFLCS**0102** **4015711**830301” </br>
”DKFLCS**0102** **4015711**830302”

The rule in the example above will also be applied to the reconciliation lines posting text and will in the example look like this:

![merge line posting text](/images/PM365/merge-lines-posting-text.png)

