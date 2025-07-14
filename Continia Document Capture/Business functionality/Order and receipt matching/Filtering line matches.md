---
title: Filtering Line Matches
date: 07-07-2022
id: DC-64
lang: en
description: >-
  How to filter the lists of line matches according to different criteria during
  manual document matching
---

# Filtering Line Matches

When you [manually match documents](../../../Continia%20Document%20Capture/Business%20functionality/Order%20and%20receipt%20matching/@DC-62/) and [handle matching discrepancies](../../../Continia%20Document%20Capture/Business%20functionality/Order%20and%20receipt%20matching/@DC-63/), it may be useful to narrow down the list of potential matches to make it easier to identify the correct one, especially if your organization receives large numbers of documents. You can easily do this using a number of predefined filters, as described below.

## To filter the list of matches

The filtering is carried out from either the **Invoice Matching** page or the **Credit Memo Matching** page, depending on what type of document you choose to match against in the document journal.

To open one of these pages and apply filters to the lists of matching document lines, follow these steps:

1. Search (\{{search\}}) for and select **Document Categories**.
2. Select the **PURCHASE** code to open the document journal.
3. In the document list, select the document that you want to match against other documents.
4. On the action bar, click **Process** > **Match Lines**.
5.  In the **Match Overview**, a number of relevant lines from potentially related documents are listed in two overall line sections, depending on what type of document you selected in step 3 above. To filter these lists, select **Process** on the action bar, and then select the filter(s) that you want to apply:

    \


    | Filter                          | Description                                                                                                                                                                                                                                                                                                        |
    | ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
    | **Filter on Order No.**         | Filters the lists to display only lines with the order number that's referenced in the invoice or credit memo and recognized by Document Capture.                                                                                                                                                                  |
    | **Filter on Unmatched Only**    | Filters the lists to display only lines that haven't yet been matched.                                                                                                                                                                                                                                             |
    | **Filter on Match Differences** | Filters the lists to display only lines in which the direct unit costs differ. For example, if you selected an invoice in step 3 above, lines that have different values in the fields **Direct Unit Cost (Order)** and **Direct Unit Cost (Invoice)** will be displayed in the lists when this filter is applied. |

    \

6. To clear a selected filter, simply select **Process** on the action bar, and then select the relevant filter again.

## Related information

[Manual Document Matching](../../../Continia%20Document%20Capture/Business%20functionality/Order%20and%20receipt%20matching/@DC-62/)\
[Handling Discrepancies, Including Partial Matching](../../../Continia%20Document%20Capture/Business%20functionality/Order%20and%20receipt%20matching/@DC-63/)
