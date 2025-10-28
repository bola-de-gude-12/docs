---
title: Automatically split and allocate using amount distribution
date: 10-09-2025
description: Set up automatic split and allocation of expenses into deductible and non-deductible lines
id: EM-216
lang: en
---
# Automatically split and allocate using amount distribution

You can split and allocate expenses using distribution codes in Continia Expense Management. This is useful in countries where, for example, part of the VAT/sales tax on certain types of expenses is deductible.

When an expense user registers an expense to an expense type, this expense will be split and allocated using a distribution code to different expense types: The original one, and the one that's specified when you set up the distribution code. The latter expense type is not visible to expense users, so from the perspective of an expense user, nothing changes when submitting expenses. The split happens when an expense is sent for approval and has the status **Pending Approval**. You can only view the expense split in Business Central.

In most scenarios, users won't see the resulting split Expense Allocation lines until the expense has been submitted. Amount Distribution splitting happens during one of the following processes:

* The expense is being sent for approval.
* An expense user is filling in an expense type for the expense in Business Central.

For more information, refer to the following video, Automatically Split and Allocate with amount distribution in Expense Management.
<br>

<iframe src="https://player.vimeo.com/video/917147014?h=9793ae1a3e&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" title="Automatically Split and Allocate with amount distribution in Expense Management"></iframe>
<br>
## Prerequisites
To set up automatic split and allocation using amount distribution requires the following:

* The **Enable Amount Distribution** setting is enabled in the **Expense Management Setup** under **Expenses**. When enabled, the column **Distribution Code** is visible on the **Expense Types** page.
* A new or existing expense type that expense users will register expenses to, for example **FOOD W. GUESTS**. If you have not set this up already, see [Setting up expense types](@EM-41).
* A new expense type that will only be used for allocation, for example, **ENTERTAIN NON-DEDUCT**.

## To set up amount distribution

You'll need to set up a distribution code on an expense type (such as **FOOD W. GUESTS**). 

To set up a distribution code:

1. Search for {{search}} **Expense Types**.
1. On the action bar, click **Edit List**.
1. Select an expense type (for example, **FOOD W. GUESTS**).
1. In the **Distribution Code** field, select **New** from the dropdown menu, and create a new distribution code by filling in the following fields:
   * **Distribution Code** - The name of the distribution code.
   * **Description** - A short description of the distribution code.
1. Under **Distribution Lines**, define how the expense will be distributed by percentage and to which expense types. This is where you apply the expense types that are mentioned under Prerequisites above.

An example of allocations based on amount distribution:
1st line: 70% | **FOOD W. GUESTS**
2nd line: 30% | **ENTERTAIN NON-DEDUCT**

## Related information

[Setting up expense types](@EM-41)