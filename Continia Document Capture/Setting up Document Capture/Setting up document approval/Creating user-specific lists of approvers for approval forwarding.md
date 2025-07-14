---
title: Creating User-Specific Lists of Approvers for Approval Forwarding 
date: 27-04-2023
description:  How to set up a list of available approvers for each user to choose between when forwarding documents for approval
id: DC-138
lang: en
---

# Creating User-Specific Lists of Approvers for Approval Forwarding

Approvers in your organization may occasionally receive approval requests that are more relevant to other approvers or which were simply sent to them by mistake. In such cases, they have to forward the approval requests to the right approvers, and you can make this process easier for them by setting up a list of available approvers for each of them to choose between. In this way, instead of having to go through all approvers in the entire organization to find the right one when forwarding documents for approval, they'll be presented with a limited and more useful list of approvers to choose between, customized specifically for them.

## To set up a list of approvers for approval forwarding

In order to set up a list that narrows down the number of available approvers per user, follow these steps:

1. Choose the {{search}} icon, enter **Approval Forwarding**, and then choose the related link.
1. In the **Owner User ID** column of the table, enter or select the ID of the user whose approval forwarding permissions you want to edit.
1. In the **Forward to User ID** column, enter or select the ID of the approver that you want the selected user to be able to forward approval requests to.
   > [!NOTE]
   > The relationship between **Owner User ID** and **Forward to User ID** is one-to-one rather than one-to-many, so if you want the user to be able to forward approval requests to more than one approver, you'll have to add more lines to the table for this user (as described in step 4 below).
1. **Optional**: To enable the user to forward approval requests to additional approvers, repeat steps 2-3 above.

The **Owner User ID** user will now only be able to forward approval requests to the approvers you've specified under **Forward to User ID**. This can be done in both Microsoft Dynamics 365 Business Central and the Continia Web Approval Portal.

## Related information

[Editing Approval Requests](@DC-39)  