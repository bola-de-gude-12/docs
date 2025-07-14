---
title: Using Approval Flows
date: 01-10-2024
description: How to assign an approval flow to a purchase document, including assignment using templates
id: DC-33
lang: en
---

# Using Approval Flows

An approval flow is a custom list of approvers that are required for the approval of applicable purchase documents. This article uses purchase invoices to illustrate how to use approval flows, but the functionality works equally well with credit memos.

Once you've [set up an approval flow](@DC-30), you can assign it to a document to determine exactly who should approve the document and in what order. When you assign an approval flow to a document, it overrides the standard purchase approval process, which is based on purchaser codes.

All approvers in the approval flow must approve the document before it can be posted, and they must do it in the order specified by you during setup.

> [!IMPORTANT]
> The **Approval Flow Code** field that is required when you assign approval flows to documents is only visible if [purchase approval has been enabled](@DC-22) in the **Document Capture Setup**.

## To assign an approval flow to an invoice

1. In the Role Center, under **Continia Document Capture Activities**, go to **Purchase Approval - Invoices** and select **Open PIs** to open the list of open purchase invoices.
1. From the list, open the invoice to which you want to assign an approval flow.
1. On the **General** FastTab, go to **Approval Flow Code** and select the three dots on the right to open the **Approval Flows** page.
1. Select the approval flow code you want to apply to the purchase invoice, and then select **OK** to close the page.

The code is now added under **Approval Flow Code**, and the selected approval flow is assigned to the invoice. When you submit the invoice for approval, it will be sent to the approvers specified in the approval flow, in the order given.

>[!NOTE]
>Approval flow codes can also be used with advanced approvals, provided that the document belongs to the Purchase category, such as credit memos, orders, purchase invoices, or return orders.

## To assign approval flows using templates

If you want to always use approval flows to determine the identity and order of document approvers, you can apply the relevant approval flow code to a document template, which will then automatically assign the code to all documents that use this template.

To apply an approval flow code to a template, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the **PURCHASE** code to open the document journal.
1. In the list of documents, select the one whose template you want to edit.
1. On the action bar, click **Template** > **Template Card**.
1. On the **Purchase Documents** FastTab, under **Approval**, select the **Approval Flow Code** field, and then select the code you want to apply to the template.

The selected approval flow code will now be added to the template and, by extension, assigned to all documents using this template.

## Related information

[Creating Approval Flows](@DC-30)  
[Document Capture Setup](@DC-22)  