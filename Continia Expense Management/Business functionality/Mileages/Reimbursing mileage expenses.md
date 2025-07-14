---
title: Reimbursing Mileage Expenses
date: 25-04-2025
description: Learn how to reimburse mileage expenses.
id: EM-15
lang: en
---
# Reimbursing Mileage Expenses

If you’re using an external payroll system for your company to reimburse expense users for example, it's good practice to create a view in the payroll system where you can see how much each expense user is owed. Then, transfer the data to the payroll system, adding information about the users who’ve been reimbursed.

You can filter reimbursement views by date intervals, and have the total shown in terms that make sense, for example: amount, quantity, or distance. All expense types show as columns on the Mileage Reimbursement page. The total amounts and distances are displayed for each mileage rate. The amount for each mileage expense type (if used) will also show for each individual expense user.

If your company doesn’t use an external payroll system, these views are not relevant, and the expense will be marked as Reimbursed immediately after posting.

For each document, the Reimbursement Method decides if an external payroll system will be used or not. For more information, see [Setting up reimbursement methods](@EM-177).

In this article you will learn how to:

* [Understand the Mileage reimbursement page fields](#understand-the-mileage-reimbursement-page-fields) 
* [Reimburse a user's mileage expenses](#reimburse-a-user's-mileage-expenses) 

## Understand the Mileage reimbursement page fields

| **Field** | **Description** |
| --- | --- |
| **Date filter** | Allows you to filter data by a date interval. For example, when you want to see the reimbursable amounts for only the current month. |
| **View as** | Visualize the total as distances or amounts. |
| **Vehicle filter** | Select a vehicle code from the list, for example a company car or a private car. You can also add to this list. |
| **View by** | You can view different filter options based on the state of the expense: Awaiting posting, Ready to reimburse, Posted and reimbursed, Everything. |
| **User** | The ID of the expense user. |
| **Name** | The name of the expense user. |
| **Balance** (Miles/Kilometers) | The balance of the current user. This is a total for the specified period for all mileage expenses, independent of their state. The balance presents the amount as it was reported, it does not calculate how much should be refunded to the user. For example, an expense with 100 EUR paid with company credit card will give no refund to the user (since it is paid by a company credit card). In such a case, the **Balance** will be 100. |
| **Refundable** (Miles/Kilometers) | The refundable balance for the current user. This is the amount that will be refunded to the expense user. For example, an expense of 100 EUR that was paid for with a company credit card will not be refunded to the user (as it was paid for by a company credit card). In such a scenario, the **Refundable amount** will be 0. |
| **High** | The total amount or the distance of mileage ready to be reimbursed for a specific user, grouped on **Vehicle code**. |

## Reimburse a user's mileage expenses

In the following example, you can reimburse expenses for an expense user or an expense user group.

To reimburse a user's expenses:

1. Search {{search}} for **Mileage Reimbursement**, then choose the related link.
2. Set a **Date Filter** for the period you want to have an overview of. For example, set filters for the previous month.
3. Ensure **View by** is set to **Ready to be Reimbursed.**
4. Ensure **View as** is set to **Amount**.
5. In the **Mileage Reimbursement** section, check you agree with the amounts and distances.
6. At this stage you can transfer the reimbursable amounts to an external payroll system, either manually or automatically:
   1. You can do this manually by typing in the external system.
   2. You can automate this on the action bar by selecting **Export to Excel**. You can send the Excel file that's generated to the relevant recipients.
7. When you receive confirmation that the expense user has been reimbursed in the external payroll system, mark the mileage expenses in the current view as Reimbursed. On the action bar, select **Reimburse**. This avoids accidentally reimbursing them again the next time. 

## See also

For more information about reimbursing expense and mileages, see:

[Overview of mileage expenses](@EM-9)  
[Reimbursing expenses](@EM-14)  
[Reimbursing per diem expenses](@EM-16)  

