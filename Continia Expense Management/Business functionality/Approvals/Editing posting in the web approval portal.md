---
title: Editing posting in the web approval portal
date: 09-09-2025
description: Learn how to edit posting in the web approval portal
id: EM-321
lang: en
---
# Editing posting in the Web Approval Portal

Having access to edit a posting is crucial if you want to ensure clear and accurate financial processing and compliance. Being able to edit a posting means you can:

* Correct accounting errors
* Ensure compliance with your company's policies
* Adjust VAT/GST tax codes accordingly
* Add or update dimensions
* Adjust the posting date to match the correct accounting period (especially around closings)
* Prevent rejections or delays if approvers are allowed to make minor corrections directly
* Improve data quality for reporting to ensure better financial and management reporting

## Enable editing

Refer to the following table to check if you have the required permissions to enable editing and change the posting on documents. 

| License type | Can/Cannot change the posting on documents |
| --- | --- |
| Approvers with a Full license | Yes |
| Approvers with a Premium license    | Yes                                        |
| Approvers with an Essential license | Yes |
| Users with a Team member license    | No |
| Users with a Limited license        | No |

To enable editing:

1.	Search for {{search}} **Expense Management Setup**.
1.	On the action bar, click **Setup** > **Web Approval**.
1.	In **Edit - Expense Management Setup / Web Approval**, under **General**, toggle the switch for **Enable Allocations**, to enable the functionality.

Approvers can now modify the expense type (posting account) and dimensions directly. For instance, if the original expense type (Software, for example) was initially misclassified, you can correct it by adding an allocation line (such as Hardware).

In this scenario, the expense entry remains unchanged in Business Central. Whereas, the posting is updated in the background. This is similar to how line-level edits work in Document Capture Purchase Invoices, where the PI header is fixed but the lines are editable. 

In Business Central it will still show Software as the expense type. However, a comment added to the allocation line description (such as "The expense has been allocated to one or more expenses") indicates that it has been reallocated to reflect the new expense type.

## Related information

For more information about posting expenses and expenses in general, see:

[Overview of expenses](@EM-8)  
[Posting expenses](@EM-11)  

