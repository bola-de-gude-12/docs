---
title: Editing Payment Approval Workflows Payment Management
date: 14-09-2022
description: Describes how to edit and delete a payment approval workflow.
id: PM-255
lang: en
---

# Editing Payment Approval Workflows

The easiest and safest way to edit a payment approval workflow is to run the assisted **Set up approval workflows** guide again. When you edit a workflow, you'll essentially overwrite it, however, any open approval requests will continue through the existing workflow until they've been approved. When you've finished editing the workflow, all the new approval requests will go through the new workflow. 

> [!IMPORTANT]
>
> You require the CPM365 APPRADMIN or SUPER permission set to create or modify payment approval workflows.

 

## To edit a payment approval workflow

> [!NOTE]
>
> It is recommended that you edit approval workflows at a time when users are unlikely to request new approvals. If a user sends an approval request through to a workflow that is being edited, it may not be completed correctly. 



To create a new approval workflow, you must use the assisted **Set up approval workflows** setup guide. 

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Assisted Setup**, then select the related link. 
1. Scroll to the **Continia Payment Management** section at the bottom of the page, and select **Set up approval workflows**. 
1. Go through each step in the assisted guide and make the relevant changes. For detailed information on the settings, please refer to the article: [Creating Payment Approval Workflows](@PM-254).
1. When you select **Finish**, all new approval requests for the relevant payment journal will use the updated approval workflow. 

> [!TIP]
>
> You can also edit elements of the approval workflow on the **Payment Journal Setup** page, under the **Approval Setup** section. 

## To delete a payment approval workflow

To delete a payment workflow, please refer to the standard [Microsoft Dynamics 365 Business Central documentation](https://docs.microsoft.com/en-us/dynamics365/business-central/across-how-to-delete-workflows).



## Related information

[Creating payment approval workflows](@PM-254)    
[Working with payment approvals](@PM-256)     



