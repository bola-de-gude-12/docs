---
title: Setting up matching checks before registration in Document Capture
date: 06-10-2025
description: How to enable Document Capture to check if documents have been matched before they're registered.
id: DC-84
lang: en
---

# Setting up matching checks before registration

To prevent users from registering unmatched documents – or to notify them before doing so –, you can configure Continia Document Capture to check for matches during registration. If no matches are found, Document Capture does one of the following, depending on your setup:

* **If line recognition is enabled** - Document Capture displays an error message in the **Comments** section of the document journal, preventing you from registering the document.
* **If line recognition is disabled** - Document Capture displays a dialog in the first step of the registration, notifying you that no matches exist and asking if you want to continue registering the document anyway.

> [!NOTE]
> With line recognition disabled, the check doesn't prevent you from registering unmatched documents – but the resulting dialog makes you actively confirm the registration before it's carried out.

Such matching checks are configured per template, so if you enable them for a specific template, they'll apply to all documents for which that template is used.

To set up matching checks:

1. Search ({{search}}) for and select **Document Categories**.
1. To open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself), and click **Edit** on the action bar.
1. On the **Document Category** page, on the **Templates** FastTab, select the template you want to configure.
1. On the FastTab title bar, click **Edit** to open the template card.
1. On the **Purchase Documents** FastTab, under **Registration**, make the following changes:
   * For the **Invoice Reg. Step 1** field, select **Match Order & Create Invoice**.
   * For the **Credit Memo Reg. Step 1** field, select **Match Return Order & Create Credit Memo**.

## Related information

[Automatic document matching](@DC-70)  