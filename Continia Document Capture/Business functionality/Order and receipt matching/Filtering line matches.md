---
title: Filtering line matches in Document Capture
date: 31-07-2025
description: How to filter the lists of line matches according to different criteria during manual document matching.
id: DC-64
lang: en
---

# Filtering line matches

When you [manually match documents](@DC-62) and [handle matching discrepancies](@DC-63), it may be useful to narrow down the list of potential matches to make it easier to identify the correct one – especially if your organization receives large numbers of documents. You can do this using a number of predefined filters.

## To filter the list of matches

The filtering is carried out from either the **Invoice Matching** page or the **Credit Memo Matching** page, depending on what type of document you choose to match against in the document journal.

To open one of these pages and apply filters to the lists of matching document lines, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Click the **PURCHASE** code to open the document journal.
1. In the document list, select the document that you want to match against other documents.
1. On the action bar, click **Home** > **Match Lines**.
1. In the **Match Overview**, a number of relevant lines from potentially related documents are listed in two overall line sections, depending on what type of document you selected in step 3 above. To filter these lists, click **Home** on the action bar and then select the filters you want to apply:

   <br>

   | Filter | Description |
   | --- | --- |
   | **Filter on Order No.** | Displays only lines with the order number referenced in the invoice or credit memo and recognized by Document Capture. |
   | **Filter on Unmatched Only** | Displays only lines that haven't yet been matched. |
   | **Filter on Match Differences** | Displays only lines in which the direct unit costs differ. For example, if you selected an invoice in step 3 above, lines that have different values in the fields **Direct Unit Cost (Order)** and **Direct Unit Cost (Invoice)** are displayed in the lists when this filter is applied. |

   <br>

1. To clear a selected filter, click **Home** on the action bar and then select the relevant filter again.
