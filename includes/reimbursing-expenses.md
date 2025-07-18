The reimbursement pages provide helpful information when you’re using an external payroll system, for example, when your company uses an external payroll system to reimburse expense users. In this case, it's good practice to create a view in the payroll system where you can see how much each expense user is owed. Then, transfer the data to the payroll system, adding information about the users who’ve now been reimbursed.

You can filter reimbursement views by date intervals, and have the total shown in **Amounts**, **Quantity**, or **Distance**, among others. The total is also distributed over a dynamic range of columns for each document type. On the Expense reimbursement page, for example, the totals are displayed over each expense type. On the Mileage reimbursement page, the totals are displayed for each mileage rate, while the totals are shown over each for each per diem group on the Per Diem reimbursement page.

All expense types show as columns on the Expense Reimbursement page. The amount for each expense type (if used) will also show for each individual Expense user.

When your company doesn’t use an external payroll system, these views are not relevant. The expense will be marked as **Reimbursed** immediately after posting.

The **Reimbursement Method** decides for each document if an external payroll system will be used or not, see [Setting up Reimbursement Method](/Continia Expense Management/Setting up Expense Management/Setting up General Business Functionality/Setting up Reimbursement Method.md).

## Reimbursement page fields

| **Field** | **Description** |
| --- | --- |
| **Date Filter** | Allows you to filter data by a date interval. For example, when you want to see the reimbursable amounts for only the current month. |
| **View By** | You can view different filter options based on the state of the expense: Awaiting Posting, Ready to reimburse, Posted and reimbursed, Everything. |
| **View As** | Visualize the total as amounts or quantity. |
| **User** | The ID of the expense user. |
| **Name** | The name of the expense user. |
| **Balance** | The balance of the current user. This is a total for the specified period for all expenses, independent of their state. The balance presents the amount as it was reported, it does not calculate how much should be refunded to the user. For example, an expense with 100 EUR paid with company credit card will give no refund to the user (since it is paid by a company credit card). In such a case, the **Balance** will be 100. |
| **Reimbursable Amount** | The reimbursable balance on the current user. This is the amount which should be reimbursed to the expense user. For example, an expense of 100 EUR that was paid with a company credit card will give no refund to the user (as it was paid by company credit card). In such a scenario, the **Reimbursable Amount** will be 0. |

## Reimbursing a user's expenses

In the following example, you can reimburse expenses for an expense user or an expense user group.

To reimburse a user's expenses:

1. Search {{search}} for **Expense Reimbursement**, then choose the related link.
2. Set a **Date Filter** for the period you want to have an overview of. For example, set filters for the previous month.
3. Ensure **View by** is set to **Ready to be Reimbursed.**
4. Ensure **View as** is set to **Amount**.
5. On the **Expense Reimbursement** section, check you agree with the amounts.
6. At this stage you can transfer the reimbursable amounts to an external payroll system. You can do this manually by typing in the external system, or by selecting **Export to Excel** on the action bar. You can send the Excel file that's generated to the relevant recipients.
7. When you receive confirmation that the expense user has been reimbursed in the external payroll system, mark the expenses in the current view as **Reimbursed** by selecting **Reimburse** on the action bar. This avoids reimbursing them again the next time. 
