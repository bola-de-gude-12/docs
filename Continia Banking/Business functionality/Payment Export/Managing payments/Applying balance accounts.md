---
title: Applying balance account to payment lines in Continia Banking
description: How to apply balance account to vendor payment suggestion lines.
date: 28-05-2025
id: CB-110
lang: en
---

# Configuring balance accounts for payment journal lines

To ensure Continia Banking validates and processes payments correctly, you must apply a balance account to the payment journal lines. Once payment suggestions have been initiated in the payment journal, you have two options for defining a balance account on the payment lines:

* **Assign directly** - assign a balance account to each payment line individually.
* **Set Balance Account for multiple lines** - use this feature to update the balance account for multiple payment lines simultaneously.

To update the balance account:

1. Search ({{search}}) and select **Payment Journals**. 

1. To update the balance account in the payment journal, select the specific lines that need adjustment. If you want to update the balance account for all lines, don't select any lines.

1. On the action bar, click **Prepare** > **Set Balance Account No.**

1. On the **Set Balance Account** page, define how to update the balance account on the suggested payment journal lines. By default, the **Balance Account Type** field is set to Bank Account.

1. In the **Balance Account No.** field, select the balance account to set on the suggested payment journal lines.

1. In the **Update** field, select which payment journal lines you want to update with the chosen balance account no. The options are:
   * **Update Blanks**  - this option updates only those suggested payment lines that currently have no value in the Balance Account No. field.
   * **Update Selected** - use this to update only the payment journal lines you have specifically selected.
   * **Update All** - this will apply the chosen balance account to all suggested payment journal lines, regardless of their current state.

1. Select **OK** to update the balance account on the specified payment journal lines.

