---
title: Extended G/L entries
date: 26-09-2024
description: How to access and use the G/L entries.
id: CF-117
lang: en
---

# Extended G/L Entries

This article describes the **Ext. General Ledger Entries** report in Continia Finance, which builds upon the standard G/L entries report in Microsoft Dynamics 365 Business Central.

To access the **Ext. General Ledger Entries** report, choose the {{search}} icon, enter **Ext. General Ledger Entries**, and then choose the related link.

<a href="/images/CFI/ext-gl-entries-top.png" target="_blank">
  <img src="/images/CFI/ext-gl-entries-top.png" alt="Ext. General Ledger Entries - top section">
</a>

The report provides you with details on each of your G/L accounts, such as the account type, net change, and balance. You can filter this data by selecting one of the filters above the main table, which are described below.

* Balance <> 0: Shows only G/L accounts with a balance other than zero.
* Current Period: Shows only G/L accounts with a net amount other than zero.
* Last Period: Shows only G/L accounts with a net amount other than zero in the last period.
* Current Year: Shows only G/L accounts with a net amount other than zero in the current year.
* Last Year: Shows only G/L accounts with a net amount other than zero in the last year.

In the **Entries** section, you can see a detailed list of entries related to the selected G/L account – provided that the account has values under the **Net Change**, **Balance at Date**, and **Balance** columns.

<a href="/images/CFI/ext-gl-entries-bottom.png" target="_blank">
  <img src="/images/CFI/ext-gl-entries-bottom.png" alt="Ext. General Ledger Entries - bottom section">
</a>

Select **Manage** in the **Entries** section and the actions below are shown.

* Reverse Transaction: Reverses a posted G/L entry.
* Ledge Entry Comments: Shows the entry page, so you can view or add comments, edit the entry description, and update the external document number.
* Calculate Sum: Calculates the sum of the remaining amounts of the selected entries, and shows it in the FactBox.

Select **Application** in the **Entries** section and the actions below are shown.

* Applied Entries: Shows the ledger entries applied to this record.
* Apply Entries: Select one or more entries to apply to this record, so the related posted documents are closed as paid or refunded.
* Unapply Entries: Removes one or more previously applied entries.

Select **Entry** in the **Entries** section and the actions below are shown.

* Find Entries: Finds related entries and documents based on the document number and posting date of the selected entry.
* Show Posted Document: Shows details for the posted payment, invoice, or credit memo.
* Dimensions: View or edit dimensions – such as area, project, or department – that you can assign to sales and purchase document to distribute costs and analyze transaction history.
* G/L Dimensions Overview: Shows an overview of G/L entries and dimensions.
* Correct Dimensions: Corrects dimensions for the selected G/L entries.
* History of Dimension Corrections: Shows a list of corrections that were made to the selected ledger entries.
* Value Entries: Shows all amounts related to an item.
* Print Detail Trial Balance: Prints a detailed trial balance letter of the selected account. For more information on this, see Printing extended financial reports (link to be added).
