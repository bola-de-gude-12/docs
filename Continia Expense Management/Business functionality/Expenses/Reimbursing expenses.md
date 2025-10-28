---
title: Reimbursing Expenses
date: 25-04-2025
description: Learn how to reimburse expenses.
id: EM-14
lang: en
---
# Reimbursing Expenses

If you’re using an external payroll system for your company to reimburse expense users for example, it's good practice to create a view in the payroll system where you can see how much each expense user is owed. Then, transfer the data to the payroll system, adding information about the users who’ve been reimbursed.

You can filter reimbursement views by date intervals, and have the total shown in terms that make sense, for example: amount, or quantity. All expense types show as columns on the Expense Reimbursement page. The total expenses are provided for each expense type. The amount for each expense type (if used) will also show for each individual expense user.

If your company doesn’t use an external payroll system, these views are not relevant, and the expense will be marked as Reimbursed immediately after posting.

For each document, the Reimbursement Method decides if an external payroll system will be used or not. For more information, see [Setting up reimbursement methods](@EM-177).

In this article you will learn how to:

* [Understand the Expense reimbursement page fields](#understand-the-expense-reimbursement-page-fields) 
* [Reimburse a user's expenses](#reimburse-a-user's-expenses) 

## Understand the Expense reimbursement page fields

| **Field** | **Description** |
| --- | --- |
| **Date filter** | Allows you to filter data by a date interval. For example, when you want to see the reimbursable amounts for only the current month. |
| **View as** | Visualize the total as amounts or quantity. |
| **View by** | You can view different filter options based on the state of the expense: Awaiting posting, Ready to reimburse, Posted and reimbursed, Everything. |
| **User** | The ID of the expense user. |
| **Name** | The name of the expense user. |
| **Balance** | The balance of the current user. This is a total for the specified period for all expenses, independent of their state. The balance presents the amount as it was reported, it does not calculate how much should be refunded to the user. For example, an expense of 100 EUR, that was paid for with a company credit, card will require no refund to the user (since it was paid for by a company credit card). In such a case, the **Balance** will be 100. |
| **Refundable amount** | The refundable balance for the current user. This is the amount that will be reimbursed to the expense user. For example, an expense of 100 EUR that was paid with a company credit card will not be refunded to the user (as it was paid for by a company credit card). In such a scenario, the **Refundable amount** will be 0. |
| **Expense Types** | The total amount or total number of related expenses ready to be reimbursed for a specific user. You can create specific expense types to be in alignment with your company policies. For example, expenses for hotels, motels, and Bed & Breakfasts, can all be grouped by the expense type **Accommodation**. |

## Reimburse a user's expenses

In the following example, you can reimburse expenses for an expense user or an expense user group.

To reimburse a user's expenses:

1. Search {{search}} for **Expense Reimbursement**, then choose the related link.
2. Set a **Date Filter** for the period you want to have an overview of. For example, set filters for the previous month.
3. Ensure **View by** is set to **Ready to Reimburse.**
4. Ensure **View as** is set to **Amount**.
5. In the **Expense Reimbursement** section, check that you agree with the amounts shown.
6. At this stage you can transfer the reimbursable amounts to an external payroll system, either manually or automatically: 
   1. You can do this manually by typing in the external system.
   2. You can automate this on the action bar by selecting **Export to Excel**. You can send the Excel file that's generated to the relevant recipients.
7. When you receive confirmation that the expense user has been reimbursed in the external payroll system, mark the expenses in the current view as Reimbursed. On the action bar, select **Reimburse**. This avoids accidentally reimbursing them again the next time. 

## Related information

For more information about reimbursing expenses and expenses in general, see:

[Overview of expenses](@EM-8)  
[Reimbursing per diem expenses](@EM-16)  
[Reimbursing mileage expenses](@EM-15)    

