---
title: Using Extended Lists for General Ledger Entries in Continia Finance
date: 23-05-2024
description: Learn more about differences in the display of G/L entries when using Extended Lists and Reports.
id: CF-88
lang: en
---

# Using Extended Lists for General Ledger Entries

This article describes how the Extended Lists and Reports module enhances the display and functionality of G/L entries in Continia Finance. It describes the additional fields and functionalities provided by this module, how to filter entries for specific periods, and how to add comments to G/L entries.

## To use the footer fields

When you activate the Extended Lists and Reports module, additional fields appear in the footer of the G/L entries page. The page layout consists of a header with the account number and description, and the individual entries displayed below. The enhanced footer fields include Balance, Net Change, Balancing Account Number, and Balancing Account Name, among others. Key functionalities available from the Continia Finance menu include Calculate Sum and Show Posted Document.

Key footer fields:

- **Bal. Account Number** - displays the associated balancing account numbers.
- **Bal. Account Name** - shows the names of corresponding balancing accounts.
- **Number** - appears when you select **Calculate Sum** in the **Entry** menu. It computes the total of chosen entries, displaying it in the footer within the **Balance** field.

> [!NOTE] 
>
> The visibility of the balancing account number and name relies on activating the **Show Bal Account** field in the **Extended Lists and Reports Setup** window.



## To filter G/L entries for a specific period

To view G/L entries for a specific period, use the date filter in the Filter totals by field. This will limit the displayed entries to those within the specified period. Press Enter to confirm, and the filtered entries will appear. The Net Change field will show the value for the filtered period. You can browse through entries for other G/L accounts that fall under the same date filter by selecting them.

> [!NOTE]
>
> Once you close the window, the system will not save the applied filter. If you need to use the filter again, you must reapply it.

## To add G/L entry comments

The Extended Lists and Reports module allows you to enhance ledger entries by adding comments. This feature is useful for attaching detailed notes or specific remarks to individual ledger entries, improving documentation and enabling easy tracking or referencing of transaction details.

To add comments:

1. On the Ext. General Ledger Entries page, navigate to the Entries section and select **Ledger Entry Comments**.
2. On the G/L Entry card, in the General section, you can view the header details:
   * **Document No.** - reflects the ledger entry's document number. The content of this field cannot be modified.
   * **External. Doc. No.** Depending on the configuration, you can display and edit the entry's external document number. Any changes made will only apply to the corresponding G/L entry.
   * **Amount** - represents the ledger entry amount. This field's content is not editable.
   * **Description** - illustrates the entry's description. The content of this field can be modified.
   * **Document Date** - shows the ledger entry document date. The content of this field cannot be modified.

3. In the **Entry Comment Line** section, you can add comments. Adding a comment marks the **Entry Comment** field of the G/L entry as **Yes**.

4. Click **Print Comments** to generate a report for the G/L entry that includes comments.

