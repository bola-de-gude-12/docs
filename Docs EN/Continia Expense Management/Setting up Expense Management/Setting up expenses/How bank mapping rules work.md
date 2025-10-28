---
title: How bank mapping rules work
date: 22-09-2025
description: Understand bank mapping rules to create your own
id: EM-330
lang: en
---
# How bank mapping rules work

You can enable bank mapping rules in Business Central to assign an expense type for a bank transaction so it'll automatically assign this expense type to the expense created, based on the bank transaction.

1. Search for {{search}} **Bank Transactions**. 
2. On the action bar, click **Mapping Rules**.
3. On the Bank Mapping Rules page, assign an expense type for a bank transaction in a line in the **Bank Mapping Rules** table. Use the following information about the columns in the table to help:
   * **Continia User ID** - select an ID to use for this rule (for example, "DEMO-NAV\AH")
   * **Rule No.** - to identify the rule, assign it a number (for example, "1" or "2")
   * **Field No.** - the field you will assign for this rule (for example "12" or "14")
   * **Field Name** - the name of the field (for example, "Business Name" or "Business Category")
   * **Value** - this can be a variety of things (for example, it could be the name of the business or category, or the business number, such as "1232")
   * **Expense Type Code** - the code for an expense type (for example, "Food", "Accommodation", "Hardware", or "Transport")

## Reference examples

Refer to the following two examples to create your own mapping rules:

**Example 1**

If User = DEMO-NAV\AH, and if field 14 on the transaction is Food, then the transaction will get the expense type FOOD.

**Example 2**

If User = DEMO-NAV\AH, and if field 12 on the transaction is 1232, then the expense type will be set to ACCOMMODATION.

 >[!NOTE]
 >Mapping Rules are enforced according to the order they are set up (i.e. according to Rule No.)

## Related information

For more information about bank mapping rules, see:

[Mapping bank currency codes](@EM-371)