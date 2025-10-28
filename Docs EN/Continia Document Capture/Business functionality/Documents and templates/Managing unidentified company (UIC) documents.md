---
title: Manage unidentified company (UIC) documents in Document Capture
date: 03-10-2025
description: How to enable and manage unidentified company documents in Document Capture.
id: DC-492
lang: en
---

# Manage unidentified company (UIC) documents

If your Microsoft Dynamics 365 Business Central environment is comprised of more than one company, Continia Document Capture can [automatically move imported documents to the right company](@DC-74). If the right company can't be identified, you have the option to automatically move the related document to the **Documents (UIC)** journal.

>[!NOTE]
>The **Documents (UIC)** journal can only be used by users with full access to all companies.

## To enable unidentified company documents

1. Search ({{search}}) for and select **Document Capture Setup**.
2. On the **General** FastTab, enable the **Use Unidentified Company Documents** setting.

## To manage unidentified company documents

1. Search ({{search}}) for and select **Documents (UIC)**.
2. If needed, use the **Document Category** and **Status Filter** to narrow down the list of unidentified company documents.
3. Select the desired document and, under the **Move to Company** column, select the target company. Repeat this step for each unidentified document you want to move.
4. On the action bar, click **Home** > **Move to Company**. Alternatively, press <kbd>F9</kbd>.

