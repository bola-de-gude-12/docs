---
title: Approval Sharing
date: 24-03-2024
description: A high-level introduction to approval sharing
id: DC-37
lang: en
---

# Approval Sharing

Approval sharing enables you to have all of your approval tasks automatically forwarded to another approver for a period of time, in case you're unable to approve documents yourself during that period. The other approver will then act as your substitute until you're available again.

There are two types of approval sharing:

* The kind that's done by admins on behalf of other users (for any user and any purpose)
* The kind you do yourself when you're out of office

Both kinds have to be set up every time you're unavailable. For more information and details on how to do this, see [Setting up Approval Sharing](@DC-25).

## Avoiding unnecessary approval requests

If you share your approvals with a higher-ranking approver, that approver could in principle end up having to approve the same document more than once. To avoid this, Continia Document Capture checks the next approval request in the approval chain to determine if the document can be approved by the current approver. If so, it will be automatically approved, so that the approver doesn't have to check the same document twice.

This functionality is enabled for all supported purchase document types:

* Invoices
* Credit memos
* Orders
* Return orders

The feature is supported for Continia standard approval and approval using approval flow codes. It doesn't support advanced approval and approval using account and dimension approval permissions.

> [!NOTE]
> Only approval requests that appear in consecutive order in the approval chain will be automatically approved.

## Related information

[Setting up Approval Sharing](@DC-25)  