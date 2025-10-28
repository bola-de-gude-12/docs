---
title: Rejecting documents
date: 27-08-2021
description:
id: EM-4
lang: en
---
# Rejecting documents

When you reject a document, it will get the status **Open** or **Pending Expense User** depending on the setup **Automatically send for approval** in Expense Management Setup.

When an approver rejects a document, the approver is asked to specify a reason of the rejection. Expense Management would like to deliver that message to the expense user, but that functionality is setup conditioned. The rejection comment is only delivered to the expense user if this type of document can be automatically submitted for approval. In that case, the document will change status to **Pending Expense User**, waiting for the user to provide further information or maybe even delete the document if a refund cannot occur.

On the other hand, when documents cannot be automatically submitted for approval, the document will be kept in status **Open**, waiting for the admin to take further action. The admin can decide to delete the document or to send it to the user for further clarification.

To reject a document, follow these steps:

1. Search for {{search}} **Expense Management Approval Entries**.
2. Select the relevant document you want to approve.
3. On the action bar, click **Reject**.
4. A dialog appears asking for a reject comment. This comment is delivered to the expense user, depending on the setup.
5. The document is then rejected and, based on the setup, it is either re-sent to the expense user or to the admin with the status **Open**.