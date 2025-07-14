---
title: Expense Management Rejecting Documents
date: 16-03-2021
description:
id: EM-4
lang: en
---
# Rejecting Documents

When you reject a document, it will get the status **Open** or **Pending Expense User** depending on the setup **Automatically send for approval** in Expense Management Setup.

When an approver rejects a document, the approver is asked to specify a reason of the rejection. Expense Management would like to deliver that message to the expense user, but that functionality is setup conditioned. The rejection comment is only delivered to the expense user if this type of document can be automatically submitted for approval. In that case, the document will change status to **Pending Expense User**, waiting for the user to provide further information or maybe even delete the document if a refund cannot occur.

On the other hand, when documents cannot be automatically submitted for approval, the document will be kept in status **Open**, waiting for the admin to take further action. The admin can decide to delete the document or to send it to the user for further clarification.

To reject a document, follow these steps:

1. Choose the {{search}} icon, enter  **Expense Management Approval Entries**, and then choose the related link.
2. Select the relevant document to be approved.
3. In the action bar, select **Reject**.
4. A dialog appears asking for a reject comment. This comment will be delivered to the expense user, depending on the setup.
5. The document is then rejected, and based on the setup it would be either re-sent to the expense user or will be ready for the admin with the status Open.