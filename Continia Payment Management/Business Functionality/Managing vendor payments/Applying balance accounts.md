---
title: Applying balance account to payment lines
description: How to apply balance account to vendor payment suggestion lines
date: 25-10-2021
id: PM-91
lang: en
---

# Applying Balance Account to Payment Lines

A balance account must be applied to the payment journal lines for Payment Management to validate and process the payments. For more information on how to define the settings for balance accounts, see the [Setting up balance accounts](@PM-62) article.

After having initiated payment suggestions in the payment journal, you can define a balance account directly on the payment lines. Alternatively, you can use the **Set Balance Account** feature, to update the balance account on several payment lines at one time. 

To update the balance account:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Journals**, then select the related link. 

1. In the payment journal, select the lines where the balance account must be updated. If you wish to the update balance account for all the lines, you should not make a selection.

1. On the action bar, select **Prepare** > **Set Balance Account No.**

1. On the **Set Balance Account** page, define how to update the balance account on the suggested payment journal lines:

   * **Balance Account Type** - by default set to **Bank Account**.
   * **Balance Account No.** - select the balance account  to set on the suggested payment journal lines.
   * **Update** -  select which payment journal lines you want to update with the chosen balance account no. The following table describes the options:

    | Option | Description |
      | --- | --- |
      | **Update Blanks** | This will update all suggested payment lines that *do not* have a value in **Balance Account No.** |
      | **Update Selected** | This will update the selected suggested payment journal lines. |
      | **Update All** | This will update the balance account on all suggested payment journal lines. |

1. Select **OK** to update the balance account on the specified payment journal lines.

> [!NOTE]
>
> On the **Set Balance Account** request form, you can define criteria for maximum limits on when the request for a balance account is allowed to be executed. The advanced criteria is a default Business Central feature. You can hover over the fields to read a short description of the criteria.

## Related information

 [Setting up balance accounts](@PM-62)  

