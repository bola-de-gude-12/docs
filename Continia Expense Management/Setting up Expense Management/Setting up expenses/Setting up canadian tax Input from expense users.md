---
title: Setting up Canadian VAT/Sales Tax Details
date: 04-12-2024
description: Learn how to comply with Canadian tax regulations and handle HST, GST, and PST.
id: EM-291
lang: en
---
# Setting up Canadian VAT/Sales Tax Details

To comply with Canadian tax regulations and handle HST, GST, and PST, you can set up the necessary configurations in Expense Management using **Configured Fields**. HST (Harmonized Sales Tax), GST (Goods and Services Tax), and PST (Provincial Sales Tax) are regional taxes applied in Canada. The rates and application of these taxes vary depending on the province. By using **Configured Fields**, you can ensure that expense users provide the necessary tax details for accurate handling of these taxes in the Expense App and Portal.

To specify the Canadian tax fields:

1. Select the ![Search](https://staging-docs.continia.com/images/search_small.png) icon, enter **Configured Fields**, and then select the related link.
2. On the action bar, select **Expense**.
3. In the **Fields on Header** FastTab, select **New Line** to add a new field.
4. Add the following fields:
   * HST/GST Amount
   * PST Amount
   * Tax Area Code

5. Use the {{search}} icon, enter **Expense Types**, and select the Expense for which you want to add the Tax Group code and then on the action bar, select **Setup**.

6. On the **Expense Posting Setup** page, on the expense type, the **Tax Group Code** specifies the tax group that's used for calculating and posting sales tax.
