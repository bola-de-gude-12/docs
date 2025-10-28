---
title: Setting up advanced approval in Document Capture
date: 15-10-2025
description: How to enable and configure advanced approval workflows in Document Capture.
id: DC-31
lang: en
---

# Setting up advanced approval

Advanced approval allows you to approve business documents based on document amounts and user-defined [dimensions](https://docs.microsoft.com/en-us/dynamics365/business-central/finance-dimensions). To set it up:

* [Disable standard purchase approval and enable advanced approval.](#to-enable-advanced-approval)
* [Set up advanced approval groups.](#to-set-up-advanced-approval-groups)
* [Add approvers to the advanced approval groups.](#to-add-approvers-to-advanced-approval-groups)

This article uses invoices to illustrate the process, but it works just as well with credit memos.

## To enable advanced approval

To disable the standard purchase approval and enable advanced approval:

1. Search ({{search}}) for and select **Workflows**.
1. Click **Purchase Invoice Approval Workflow** to open its **Workflow** page.
1. Disable the workflow by toggling the **Enabled** switch, then exit the page to get back to the list.
1. On the action bar, click **New Workflow from Template**.
1. Select **Purchase Invoice Advanced Approval Workflow** to add it to the list of workflows. 
1. On the **Workflow** page that opens, enable the workflow by toggling the **Enabled** switch and exit the page to return to the list.

   > [!NOTE]
   > **Purchase Invoice Approval Workflow** and **Purchase Invoice Advanced Approval Workflow** can't both be enabled at the same time.

## To set up advanced approval groups

To set up advanced approval groups with filters and dimensions, follow these steps:

1. Search ({{search}}) for and select **Advanced Approval Groups**.
1. On the action bar, click **New** to open the **Approval Group Card**.
1. On the **General** FastTab, under **Code**, enter the code that you want this approval group to have. Use a code that’s meaningful to your organization.
1. **Optional**: Under **Priority**, enter the priority of the approval group. The first group created is automatically assigned the value **1**. If you have multiple groups, the group with priority equal to **1** is the first to be linked to invoices sent for approval. When creating multiple approval groups, it's obligatory to use filters (see step 5).
1. **Optional**: If you want the approval group to be linked only to invoices that meet certain filtering conditions, you can specify these conditions on the **Filters** FastTab. You can add three kinds of filters, relating to different parts of the invoices that are sent for approval: filters relating to fields in the purchase header, to the purchaser field, or to the vendor field.
   
   > [!NOTE]
   > If you add a field filter under **Purchase Header Filter**, such as **Due Date=01-08-23**, the approval group is only linked to invoices that match this filter – that is, invoices that are due on 1 August, 2023.
1. **Optional**: Fill out the remaining fields on the **General** FastTab as needed:
   
   1. **Description** - a description of the approval group.
   1. **First Entry Created by** - specifies the first approver of invoices linked to the approval group. **Purchaser** refers to the purchaser on invoices sent for approval, while **Approver ID** (the default option) refers to the first approver in the group who has the same dimensions as the first invoice line and who has a sufficient approval limit.
   1. **Four Eyes Approval** - specifies that at least two approvers must approve invoices for these invoices to be considered fully approved (**Invoice**), or if at least two approvers must approve the total amount of the invoices for these invoices to be fully approved (**Invoice Full Amount and Dimensions**).
   
   > [!NOTE]
   > When you [set up advanced approval groups](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/setting-up-advanced-approval#to-set-up-advanced-approval-groups), you can select **Purchaser** under **First Entry Created by** to always have the purchaser assigned as the first approver. However, if **Four Eyes Approval** is set to **Invoice Full Amount and Dimensions**, instead of being set to **Invoice**, the purchaser doesn't count as one of the two approvers required.

1. On the **Dimensions** FastTab, in the list of dimensions, locate the dimension(s) that you want to apply to this approval group, and then select the box(es) under **Active**. If you want to make one or more dimensions mandatory, select the relevant box(es) under **Mandatory**. Note that the only dimensions available to you here are those configured in the **General Ledger Setup**.

   > [!IMPORTANT] If you make a dimension mandatory, its value must be present on all invoice lines during the approval process. Otherwise, the approval flow is halted and an error message is displayed. The **Mandatory** feature is often used when you operate with multiple dimensions.

   > [!TIP]
   > For more information on dimensions, including how to add new ones, see the Microsoft article [Work with Dimensions](https://docs.microsoft.com/en-us/dynamics365/business-central/finance-dimensions).

## To add approvers to advanced approval groups

Once you've created an advanced approval group as [described above](#to-set-up-advanced-approval-groups), you must add users – that is, approvers – to it. To do this, follow these steps:

1. Open the **Approval Group Card** of the relevant group (unless already open): Search ({{search}}) for and select **Advanced Approval Groups**, then select the relevant approval group in the list.
1. On the action bar, click **Users** to open the **Advanced Approval Users** page.
1. In the list, under **Name**, select the three dots on the right to open the **Continia User List**, and then select the user that you want to add to the group as an approver. Click **OK** to close the user list.
1. Under **Approval Amount Limit**, enter the approval limit of the approver.
1. For each of the remaining list columns, do as follows:
   1. Select the field to open the **Edit - Approval User Dimension Selection** page.
      > [!NOTE]
      > The columns of the list represent the dimension(s) that you've applied to the approval group when setting it up, and they vary accordingly (see step 7 in the guide above under [To set up advanced approval groups](#to-set-up-advanced-approval-groups)). For example, if you applied the dimension **Department Code** when you set up the approval group, it will appear as a column on the **Advanced Approval Users** page.
   1. In the list of dimension values, select the value that you want to add to the approver, and then select the box under **Approval Permission** to add it. Select **Close** to close the page and return to the **Advanced Approval Users** page.
1. Repeat steps 3–5 to add more approvers to the group.

Whenever an invoice is sent for approval, Document Capture will then create an approval entry by assigning the approver from the approval group who has the lowest approval limit (but enough to approve as the first approver) and the same combination of dimension values as one or more of the invoice lines. When the first approver has approved all relevant lines but doesn't have sufficient approval limit to approve *all* invoice lines, Document Capture then assigns the next approver in the same approval group who has a higher approval limit, and a new approval entry is created. This process is repeated until all invoice lines have been approved.

## Related information

[Advanced approval](@DC-38)  
[Work with dimensions](https://docs.microsoft.com/en-us/dynamics365/business-central/finance-dimensions) (Microsoft article)  
