---
title: Setting up the registration of documents as general journal lines
date: 07-04-2025
description: How to register incoming documents as lines in a general journal in Document Capture.
id: DC-112
lang: en
---

# Setting up the registration of documents as general journal lines

This article describes how to register incoming documents as lines in a general journal using Continia Document Capture.

To set up documents to be registered directly as general journal lines:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the **PURCHASE** line (not the **PURCHASE** code itself), and then choose **Edit** on the action bar to open the **Document Category** page.
1. On the **General** FastTab, under **Journal Template**, make the following changes:
   1. Under **Journal Template Name**, select the journal template to be used when documents are registered as general journal lines.
   1. Under **Journal Batch Name**, select the journal batch to be used when documents are registered as general journal lines.
1. On the **Templates** FastTab, select the relevant template in the list, and then select **Edit** to open the **Template Card**.
1. On the **Purchase Documents** FastTab, set **Invoice Reg. Step 1** and/or **Credit Memo Reg. Step 1** to **Create Journal Lines**, depending on what documents you want to register as general journal lines (i.e.: invoices and/or credit memos).
1. **Optional**: To have general journal lines posted upon registration, you can set **Invoice Reg. Step 2** and/or **Credit Memo Reg. Step 2** to **Post** depending on the type of documents you want to register.

This changes the way documents are registered, so that general journal lines are created instead of documents in Microsoft Dynamics 365 Business Central. For more information, see [Registering documents as general journal lines](@DC-67#registering-documents-as-general-journal-lines).

## Related information

[Registering documents](@DC-67)