---
title: Manual Document Matching
date: 07-07-2022
id: DC-62
lang: en
description: >-
  How to manually match incoming purchase invoices and credit memos against
  related documents
---

# Manual Document Matching

Manual document matching enables you to manually select exactly what documents to match against each other. For example, for an incoming purchase invoice, you can freely select the purchase order you want to match it with from a list of relevant open purchase orders, thereby gaining full personal control of the matching process. This approach is particularly useful for organizations that generally receive fairly small volumes of documents.

Note that matching is only available in the **PURCHASE** category and that you perform it from either the **Invoice Matching** page or the **Credit Memo Matching** page, depending on what type of document you choose to match against in the document journal.

## To manually match documents

If you want to match an incoming document – whether an invoice or a credit memo – with related documents, follow these steps:

1. Search (\{{search\}}) for and select **Document Categories**.
2. Select the **PURCHASE** code to open the document journal.
3.  In the document list, select the document that you want to match against other documents.

    > \[!NOTE] The document you select determines where to perform the matching, what types of documents you can match against, and what line sections will be displayed in the **Match Overview** in step 5 below:
    >
    > * If you select an invoice, you can match against _orders_ and _purchase receipts_ on the **Invoice Matching** page, and this will be reflected in the sections shown.
    > * If you select a credit memo, you can match against _return orders_ and _return shipments_ on the **Credit Memo Matching** page, as reflected in the displayed sections.
4. On the action bar, click **Process** > **Match Lines**.
5.  In the **Match Overview**, a number of relevant lines from potentially related documents are listed in two overall line sections, depending on what type of document you selected in step 3 above. Select the relevant document line(s) in one of the sections, and then select **Line** > **Toggle Match**.

    > \[!NOTE] **Toggle Match** populates the **Matched Quantity** field of the selected line(s) with the outstanding quantity. If this field already has a value, selecting **Toggle Match** will reset the value to zero.
6. If you need to make adjustments to some of the values, for example due to [quantity or price discrepancies](../../../Continia%20Document%20Capture/Business%20functionality/Order%20and%20receipt%20matching/@DC-63/), you can manually edit the following fields:
   * **Matched Quantity**
   * **Direct Unit Cost (Invoice)** or **Direct Unit Cost (Credit Memo)**
   * **Line Discount % (Invoice)** or **Line Discount % (Credit Memo)**
7.  Repeat steps 5-6 for the other line section, if relevant – that is, if you need to match against both line types, and if both sections have lines available to choose from.

    > \[!TIP] If you need more information about a document line in order to be sure if it's the right match, select the line in the relevant line section, and then select **Line** > **Card** to open the document card for that line.

Each of the lines for which you select **Toggle Match** or manually enter a value will be made bold to indicate that it's been matched to the document. Also, the matched line amount will be added to the calculations displayed at the top of the **Match Overview** section, which indicate the progress of the matching process:

\


| Field               | Description                                                                                                                                                                                                                                                        |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Amount to Match** | The amount displayed in this field is the same as the total invoice amount, unless the invoice includes freight charges, environmental fees, or similar. Any such fees and charges are typically deducted from the invoice total in the **Amount to Match** field. |
| **Matched Amount**  | **Matched Amount** will initially be zero and then increase as lines are matched. **Matched Amount** should be equal to **Amount to Match** once the matching is complete.                                                                                         |
| **Difference**      | This field shows the difference between **Amount to Match** and **Matched Amount**. The difference should be zero once the matching is complete.                                                                                                                   |

When the **Difference** is zero (or within any variance you may have set up), you've completed the matching process. You can now navigate back to the document journal, where the comments section at the bottom will display a new **Manual Match** record to indicate that the invoice has been matched manually.

The document is now ready to be [registered](../../../Continia%20Document%20Capture/Business%20functionality/Order%20and%20receipt%20matching/@DC-67/) for further processing.

## Related information

[Filtering Line Matches](../../../Continia%20Document%20Capture/Business%20functionality/Order%20and%20receipt%20matching/@DC-64/)\
[Handling Discrepancies, Including Partial Matching](../../../Continia%20Document%20Capture/Business%20functionality/Order%20and%20receipt%20matching/@DC-63/)
