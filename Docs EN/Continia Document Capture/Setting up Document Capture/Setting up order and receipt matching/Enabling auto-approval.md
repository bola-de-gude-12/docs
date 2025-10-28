---
title: Enabling auto-approval
date: 25-04-2025
description: How to enable the automatic approval feature in Document Capture.
id: DC-461
lang: en
---

# Enabling auto-approval

To save time and hassle, you can have all documents that match related documents (within an allowed variance) approved automatically. This goes for both manually and automatically matched documents.

As with matching, automatic approval is configured per template. If you enable it for a specific template, it applies to all documents for which that template is used.

To set up automatic approval:

1. Search ({{search}}) for and select **Document Categories**.
1. To open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself), and then choose **Edit** on the action bar.
1. On the **Document Category** page, on the **Templates** FastTab, select the template that you want to configure.
1. On the FastTab title bar, select **Edit** to open the template card.
1. On the **Purchase Documents** FastTab, under **Approval**, enable the **Auto Approve within Variance** setting.

>[!NOTE]
>The value of the **Invoice Reg. Step 2** field (located on the **Purchase Documents** FastTab, under **Registration**) also affects the auto-approval process. Additionally, the purchase order must have been pre-approved as part of a purchase order approval flow. However, if **Auto Approve Within Variance** is enabled on the template card and all amounts match, registered invoices are automatically approved when later sent for approval – even if **Invoice Reg. Step 2** is left empty.

All documents using the configured template will then be automatically approved if they match their related documents within the defined variance. Each document that's approved this way and subsequently registered is created as an open purchase invoice or credit memo with the status **Released**, and the **Approval Comments** section indicates that it was automatically approved.

## Related information

[Setting up Document Approval](@DC-21)  