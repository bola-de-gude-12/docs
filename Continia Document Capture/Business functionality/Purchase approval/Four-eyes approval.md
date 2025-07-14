---
title: Four-eye approval
date: 04-10-2024
description: Details on four-eye approval and approver identification (manual or automatic).
id: DC-35
lang: en
---

# Four-Eye Approval

The purpose of four-eye approval is to ensure that every document submitted for approval is approved by at least two approvers (four eyes). Once enabled, four-eye approval applies universally to all documents – it can't be enabled or disabled for individual documents. However, there are two exceptions in which four-eyes approval doesn't apply even if it has been enabled:

*  If document approval is initiated by an [approval flow code](@DC-33), four-eye approval won't apply.
*  If you [configure a **4-eyes Threshold Amount (LCY)**](@DC-22#to-set-up-purchase-approval) that triggers four-eye approval for all invoices exceeding that threshold, four-eye approval doesn't apply to invoices with lower values.

Four-eye approval can be used as an added feature for both standard and advanced approval, so the identification of the first approver depends on your choice of overall approval method. As for the identification of the second approver, you can set this up to be done either automatically by Continia Document Capture or manually by the first approver. 

> [!NOTE]
> To enable and set up four-eye approval in the Document Capture Setup, see [Enabling Purchase Approval](@DC-22). However, note that four-eye approval for advanced approval must be set up using the **Approval Group Card**. For more information, see [To set up advanced approval groups](@DC-31#to-set-up-advanced-approval-groups) and [Advanced Approval](@DC-38#four-eyes-approval).

## Manual or automatic approver identification 

If a document that has been submitted for approval only has one approver assigned, a second approver must be added when four-eye approval has been enabled. The second approver can be identified and added either manually or automatically, depending on your configuration:

* If **Automatic selection** was chosen in the setup, Document Capture identifies the second approver based on the settings of the first approver (specifically the **4-eyes Approval, 2nd Approver Name** field in the first approver's **Continia User Setup**). In this scenario, Document Capture adds the second approver automatically – and no manual action is required.
* If **Manual selection** was chosen in the setup, the first approver must manually select the second approver when approving the document. A dialog box prompts the first approver to forward the document to another approver using the **Forward and Approve** action.

## Related information

[Document Capture Setup](@DC-22)  