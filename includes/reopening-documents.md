In Business Central, you can reopen expense entries that haven't been posted yet. This feature is convenient in numerous scenarios, particularly when you must rectify errors or make necessary adjustments before finalizing the entries. 

To reopen an expense, follow these steps:

1. Select the {{search}} icon, enter **Expenses**, and then choose the related link.
2. In the document list, select the document you want to reopen.
3. On the action bar, select **More Options > Actions > Functions > Reopen**. When reopening an expense document, the document status will change to Open. Below, you can see what happens when reopening a document depending on its status.

| Status before reopening | Effect after reopening                                       |
| ----------------------- | ------------------------------------------------------------ |
| Pending Expense User    | Use this action with caution and use only if absolutely necessary. An expense with the status **Pending Expense User** is a draft document in the expense user's mobile app. The expense user is expected to update the document and submit it. When an expense is in the Pending Expense User status, it represents a draft document in the expense user's mobile app. Reopening an expense in this state displays a message informing the user that an admin in Business Central is processing the document. Any unsaved changes not updated to Continia Online will be discarded. This action may be helpful in situations like an expense user's extended absence and pending month-end bookkeeping. |
| Pending Approval        | When an expense is in the Pending Approval status; it awaits approval from an approver. Reopening an expense in this state cancels the approval entry, making the document invisible to the approver. The document will need to be resent for approval. |
| Released                | If an expense is in the Released status, it means it has been previously approved. Reopening an expense requires the approval process to be carried out again. Depending on the settings, the approval administrator might be able to force approval. This can be useful for minor corrections that won’t have any influence on the approver's decision. |