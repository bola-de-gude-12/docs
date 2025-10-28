After expense entries are approved, you can post them to update relevant accounts in Business Central and process reimbursements. Keep in mind that posted expenses are final and cannot be edited. You can post a single expense or batch post. 

## Post an expense

Posting an approved expense finalizes it and records it in Business Central. During the posting process, automatic checks will identify any issues:

- **Warnings** - will prompt a dialog, allowing you to bypass potential concerns.
- **Errors** - must be resolved before the document can be successfully posted.

To post a single expense:

1. Search for {{search}} **Expenses**.
2. Select the approved expense you want to post, then on the action bar, click **Process** > **Post**. The document is posted and moved to **Posted Expenses**.

## Post multiple expenses in a batch

You can also post multiple expenses as a batch. To do this, follow these steps:

1. Search for {{search}} **Expenses**.
2. On the action bar, click **Process** > **Post batch**.
3. A dialog appears, where you can provide additional details::
   * **Group by Expense Report** - select this option to group expenses into a new expense report that will be posted together.
   * **Replace Posting Date** - enable this option to change the posting date for multiple expenses and select the preferred replacement method.
   * **Filter: Expense** - in this section, you can set filters on which expenses should be posted.
4. Click **OK** to post the expenses, and move them to **Posted Expenses**.

> [!NOTE]
> Any entries with warnings or errors will be skipped when posting expenses in a batch until the admin addresses the issues. The admin will receive feedback about the related issues and must process these entries individually before they can be successfully posted.

## Export expense attachments

You can export the expense attachments of posted expenses. For example, this can be convenient when obtaining a Value Added Tax (VAT) refund. In many jurisdictions, businesses can claim a refund on the VAT paid on certain expenses incurred during business operations. Tax authorities often require supporting documentation, such as receipts, invoices, and other expense-related attachments, to support these claims.

To export expense attachments:

1. Search for {{search}} **Posted Expenses**.
2. On the action bar, click **Related** > **Expenses** > **Download expense attachments**.

If you want to include a list of all of the names of the attachments, you'll need to run the **Expense Management Tax Report**.

To run the Expense Management Tax Report:

* Search for {{search}} **Expense Management Tax Report**. You will see a list of all the attachment names.
