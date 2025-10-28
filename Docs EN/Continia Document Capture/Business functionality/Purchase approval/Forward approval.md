---
title: Forward approval in Document Capture
date: 03-10-2025
description: How to forward approval requests to a different user in Document Capture.
id: DC-404
lang: en
---

# Forward approval

This article describes the forward approval functionality in Continia Document Capture, which allows you to delegate the approval of a document to a different user. Provided that the approval users are configured accordingly, this functionality is available in both Microsoft Dynamics 365 Business Central and in the [Continia Web Approval Portal](@DC-165).

>[!NOTE]
>If the first approver in a flow forwards without approving, the approval hierarchy is recreated. This is based on the presumption that the approval request was sent to the wrong person, requiring a different flow when the right person receives the request.

## Prerequisites for approval forward

Before you can use the approval forward functionality, complete the following steps:

* Enable the Document Approval module. For information on this, see [Using Continia Solution Management](@DC-107#to-enable-or-disable-modules).
* Configure approval users in Document Capture. For information on this, see [Continia User Setup for Approvals](@DC-23).
* **Optional:** add these users to the **Approval Forwarding** list. For information on this, see [Creating User-Specific Lists of Approvers for Approval Forwarding](@DC-138).

## To forward an approval in Business Central

To delegate an approval to another user, complete the following steps in Business Central:

1. In the role center, under the **Continia Document Capture Activities**, click the **PIs for Approval** cue.
1. On the **Purchase Invoices** page, click the purchase invoice whose approval you want to forward.
1. On the **Purchase Invoice** page, click **Approve** > **Forward** on the action bar.
4. Depending on your configuration, you may see up to three forwarding options:
   * **Approve & Forward** - select it to approve the document and have it forwarded to a different user for further approval.
   * **Forward without approval** - select it to forward the document to a different user for approval, without approving it yourself.
   * **Forward and return to me for approval** - select it to forward the document to a different user for approval, and then have the document automatically returned to you for further approval.
1. Select the user you want to forward the approval to, then click **OK**.

## To forward an approval in the Web Approval Portal

To delegate an approval to another user, complete the following steps in the Web Approval Portal:

1. Log in to the Web Approval Portal. If you’re not using the [cross-company dashboard](@DC-165#the-available-views), switch to the company for which you want to forward an approval.
2. Choose the document that requires your approval by selecting it under the {{checkmark}} column, then click **Forward** in the action menu. Alternatively, you can open the document by clicking its **Type**, **Name**, **Description** or other fields.

   > [!TIP]
   > Selecting documents via the {{checkmark}} column allows you to act on multiple documents at once.

3. Select the user you want to forward the approval to.
4. Depending on your setup, there are up to three forwarding options:
   * **Approve & Forward** - select it to approve the document and have it forwarded to a different user for further approval.
   * **Forward without approval** - select it to forward the document to a different user for approval, without approving it yourself.
   * **Forward and return to me for approval** - select it to forward the document to a different user for approval, and then have the document automatically returned to you for further approval.
5. If needed, enter a comment. Then, click **Continue**.