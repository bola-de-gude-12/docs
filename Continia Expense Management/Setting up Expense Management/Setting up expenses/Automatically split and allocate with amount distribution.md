---
title: Automatically Split and Allocate using Amount Distribution
date: 15-04-2024
id: EM-216
lang: en
description: >-
  Learn how to set up automatic split and allocation of expenses into deductible
  and non-deductible lines.
---

# Automatically Split and Allocate Using Amount Distribution

This guide explains how to split and allocate expenses using distribution codes in Continia Expense Management. This is useful in countries where, for example, part of the VAT/sales tax on certain types of expenses is deductible.

When an expense user registers an expense to an expense type, this expense will be split and allocated using a distribution code to different expense types: The original one, and the one that's specified when you set up the distribution code. The latter expense type is not visible to expense users, so from the perspective of an expense user, nothing changes when submitting expenses. The expense split can only be viewed in Business Central.\
\


## Prerequisites

The following is required to be able to set up automatic split and allocation using amount distribution:

* The **Enable Amount Distribution** setting is enabled in the **Expense Management Setup** in the **Expenses** FastTab. When enabled, the column **Distribution Code** will be visible on the **Expense Types** page.
* A new or existing expense type that expense users will register expenses to, for example **FOOD W. GUESTS**. Follow the guide [Setting up Expense Types](../../../Continia%20Expense%20Management/Setting%20up%20Expense%20Management/Setting%20up%20expenses/@EM-41/).
* A new expense type that will be used for allocation only, for example **ENTERTAIN NON-DEDUCT**.

## To set up amount distribution

You'll need to set up a distribution code on an expense type (such as **FOOD W. GUESTS**).

1. Choose the \{{search\}} icon, enter **Expense Types**, and then choose the relevant link.
2. In the action bar, select **Edit List**.
3. Select an expense type (for example **FOOD W. GUESTS**).
4. In the **Distribution Code** field, select **New** from the dropdown menu, and create a new distribution code by filling in the following fields:
   * **Distribution Code** - The name of the distribution code.
   * **Description** - A short description of the distribution code.
5. Under **Distribution Lines**, you define how the expense will be distributed by percentage and to which expense types. This is where you apply the expense types that are mentioned under Prerequisites above.

An example of allocations based on amount distribution: 1rst line: 70% | **FOOD W. GUESTS** 2nd line: 30% | **ENTERTAIN NON-DEDUCT**

## See also

[Setting up Expense Types](../../../Continia%20Expense%20Management/Setting%20up%20Expense%20Management/Setting%20up%20expenses/@EM-41/)
