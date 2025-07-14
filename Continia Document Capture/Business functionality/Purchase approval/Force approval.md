---
title: Force Approval
date: 06-08-2024
description: How to force the approval of a document
id: DC-36
lang: en
---

# Force Approval

The **Force Approval** feature allows approval administrators to force the approval of a specific document through, thereby bypassing the usual approval workflow. As evident in the below, this article uses purchase invoices as an illustrative basis to explain how this is done, but the functionality also works with credit memos.

Note that the feature must be [enabled in the **Document Capture Setup**](@DC-22) first, and that it can only be used by approval administrators. To set up a user as an approval administrator, see [To set up users as approvers](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#to-set-up-users-as-approvers).

> [!IMPORTANT]
> If the feature hasn't been enabled or you don't have the necessary approval administrator privileges, the **Force Approval** button will not be displayed at all on the **Purchase Invoice** page, as described [below](#to-force-the-approval-of-an-invoice).

## To force the approval of an invoice

As an approval administrator, you can force the approval of a purchase invoice by following these steps:

1. Open the purchase invoice whose approval you want to force through.
1. On the **Purchase Invoice** page, on the action bar, click **Actions** > **Approval Administration** > **Force Approval**.
1. A dialog box asks if you want to force the approval of the invoice. Select **Yes**.

The invoice will now be instantly approved and moved to the **Released PIs** tile in the Role Center.

> [!NOTE]
> For any invoice whose approval has been forced, the forced approval will be logged in the **Approval Entry** table. Also, on the **Purchase Invoice** page of the relevant invoice, on the **General** FastTab, the **Approval Comments** field will read **Approval forced by [user ID]**.

## Considerations

While **Force Approval** is an invaluable tool when an exception needs to be made, it must be used carefully and responsibly. As well as compromising the integrity of the established approval flow, it:

* Skips the amount check on approval, which verifies that the recognized amount is equal to the configured amount.
* Skips the [approval permission check](@DC-24), if this is enabled.
* Increases the risk of fraud.
* May result in compliance issues and/or increased scrutiny during audits.
* May cause errors that otherwise wouldn't be made, including incorrect or duplicate payments.

To mitigate these issues, it's crucial to:

* Activate [amount validation on post](@DC-139).
* Restrict the use of the **Force Approval** feature to a small number of trusted individuals.
* Set clear guidelines and boundaries when training individuals with access to the feature.
* Ensure compliance by tracking the usage of the feature and conducting regular audits.

## Related information

[Document Capture Setup](@DC-22)  
[Continia User Setup for Approvals](@DC-23)  