---
title: Creating approval flows 
date: 04-10-2024
description: How to set up approval flows. 
id: DC-30
lang: en
---

# Creating Approval Flows

As an alternative to [standard purchase approval](@DC-32), you can set up one or more approval flows, which are essentially custom lists of approvers required for document approval. When a document has been assigned an approval flow, it can't be posted until it has been approved either by all approvers in the flow (the default setting) or by the approvers that have been selected according to the specified amount limits. With the default setting, the approvers must approve the document in the order you specify when you set up the flow.

When you create an approval flow, you must provide it with an approval flow code that is suitable for your particular organization's setup. The code can be entered as free text and should be whatever word best describes the approval flow you're setting up, such as **SMALL** (for small purchases) or **GERMANY** (for supplies procured in Germany) – basically anything you prefer. The entered code is to be used when you assign the approval flow to a document.

To be able to add approvers to your approval flow, you must [set them up](@DC-23) first. Once set up, the approvers will be available for selection in the **Continia User List**, as described below.

> [!NOTE]
> Regarding [four-eye approval](@DC-35): When you set up and [assign an approval flow](@DC-33), four-eye approval doesn't apply even if it has been enabled.

## To set up an approval flow

1. Choose the {{search}} icon, enter **Approval Flows**, and then choose the related link.
1. On the action bar, click **New** to add an approval flow.
1. In the list, under **Code**, enter a suitable code for the approval flow.
1. **Optional**: Under **Description**, enter a free-text description of the approval flow.
1. Under **Selection Method**, specify how approvers are to be selected for the approval of documents that have this approval flow code applied. For more information, see [Adding amount limits to an approval flow](#adding-amount-limits-to-an-approval-flow) below.
1. Under **No. of Approvers**, select the number (**0** for new flows) to open the **Approvers** page.
1. On the action bar, click **New** to add an approver.
1. In the list, under **Name**, select the three dots on the right to open the **Continia User List**. Select a user from the list, and then select **OK** to close the page.
1. Under **Approval Amount Limit**, add the amount limit that you want to apply to this approver. This applies specifically to this approval flow and overrules any other approval limits configured elsewhere for this user. Note that any entered amount limits will be disregarded if you select **All** under **Selection Method** in step 5 above.
1. Repeat steps 7-9 for every additional approver you want to add to the flow.

> [!NOTE]
> If you select **All** under **Selection Method** in step 5, the following applies: The order of the approvers on the **Approvers** page reflects the order in which the approvers must approve any document that has this approval flow assigned. The approver at the top will be the first one to approve the document, which will then be passed on to the second approver in the list (followed by the third, fourth, etc., if applicable).

## Adding amount limits to an approval flow

By adding amount limits to an approval flow, you can enable the flow to release documents whenever the specified approval level is met. In this way, each document for approval won't have to be forwarded to all approvers in the flow if it can be released by an approver with the appropriate approval limit early in the process. This ensures that only the necessary number of people are involved in the approval process, thereby enabling documents to be approved faster.

To add amount limits to an approval flow, follow the guide above under [To set up an approval flow](#to-set-up-an-approval-flow). The actual amount limits are added as numerical values for each individual approver in step 9 of the guide, under **Approval Amount Limit**. In step 5 of the guide, you can decide if or how these amount limit values should then be used to select approvers for the approval of documents with this approval flow applied. You can choose between the following selection methods:

<br>

| <span style="white-space: nowrap;">Selection method</span> | Description |
| --- | --- |
| **All** | With this option, an approval entry is created for each approver in the flow. This is the default setting, which corresponds exactly to the functionality of previous versions of Continia Document Capture. Note that any entered amount limits will be disregarded if you select this option. |
| **First qualified** | If you select this option, Document Capture will select the first individual approver with an amount limit value that equals or exceeds the total value of the purchase document submitted for approval. |
| **All to first qualified** | This option will select all approvers in the flow, starting with the approver with the lowest amount limit value and ending with the first qualified approver (for a definition of this, see "**First qualified**" above). |
| **Initial and first qualified** | With this option, Document Capture will select the approver with the lowest amount limit value as well as the first qualified approver (for a definition of this, see "**First qualified**" above). |

## Related information

[Using Approval Flows](@DC-33)  
[Continia User Setup for Approvals](@DC-23)  