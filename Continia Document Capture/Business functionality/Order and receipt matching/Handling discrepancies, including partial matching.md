---
title: Handling Discrepancies, Including Partial Matching
date: 31-08-2022
description: How to manage price and quantity discrepancies and partially match documents against each other
id: DC-63
lang: en
---

# Handling Discrepancies, Including Partial Matching

Vendors sometimes ship fewer – or perhaps even more – items to you than you ordered from them, and the invoiced price of the goods you ordered may also occasionally differ from the price given in the purchase order. Such discrepancies can be handled in different ways, depending on the type of discrepancy (relating to [quantity](#partial-matching-quantity-discrepancies) or [price](#price-discrepancies)) and whether your organization matches documents manually or automatically.

> [!NOTE]
> For the sake of simplicity, the handling of all kinds of quantity discrepancies will be referred to as *partial matching* in this article, although the term primarily covers scenarios in which customers are invoiced for fewer items than ordered/received, rather than more.

## Partial matching (quantity discrepancies)

Whenever two documents are matched against each other, Continia Document Capture will by default assume that the full outstanding quantity of each relevant line should be matched against the related document. But if the delivered quantity differs from the quantity that was invoiced, it's necessary to carry out partial matching instead. For example, if you ordered and received 10 laptops but was only invoiced for 7 laptops, the matched quantity should be 7 rather than the full outstanding quantity of 10 laptops.

Partial matching can be carried out either [manually](#manual-partial-matching) or [automatically](#automatic-partial-matching), depending on your overall approach to document matching. The way it's handled differs considerably between these two methods.

### Manual partial matching

If your organization generally matches documents manually, follow these steps to carry out partial matching:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the **PURCHASE** code to open the document journal.
1. In the document list, select the document (invoice or credit memo) that you want to match against other documents.
1. On the action bar, click **Process** > **Match Lines**.
1. In the **Match Overview**, a number of relevant lines from potentially related documents are listed in two overall line sections, depending on what type of document you selected in step 3 above. In one of these sections, select the document line that you want to manually edit.
1. In the **Matched Quantity** field, enter the correct quantity (typically the quantity of the relevant line in the invoice or credit memo that you selected in step 3).
1. Repeat steps 5-6 for any other relevant lines in that line section and/or in the other section.

When you've completed the matching process, you can navigate back to the document journal to register or otherwise process the matched document.

> [!TIP]
> For general information on manual matching, see [Manual Document Matching](@DC-62).

### Automatic partial matching

If your organization generally matches documents automatically, Document Capture will automatically manage quantity discrepancies in one of the following ways, depending on whether or not line matching has been enabled in the setup:

[**If line matching has been enabled**](@DC-69), Document Capture will use the line data recognized in the invoice or credit memo to set the matched quantity on the related document lines. The matched quantity will always equal the recognized quantity of the related invoice/credit memo line. Note that to allow for partial matching, the setup option **Match Quantity** must be set to **No**.

**If header matching is used instead of line matching**, the line details of the invoice or credit memo are unknown, so Document Capture will handle any discrepancy in the total amount (which could be the result of a quantity discrepancy) by creating a new line – a variance line – in the registered invoice/credit memo, ensuring that the imported invoice/credit memo amount equals the registered amount. You can specify the allowed discrepancy by defining a variance [in the setup](@DC-68). The matched quantity of the invoice/credit memo will always equal the quantity of the related document line.

> [!TIP]
> For more information on automatic matching, see [Automatic Document Matching](@DC-70).

## Price discrepancies

Just as with matched quantities, Document Capture by default assumes that the price of delivered goods is the same as the price at which the goods were ordered. However, this isn't always the case, so it may occasionally be necessary to handle price discrepancies one way or the other. This can be done either [manually](#handling-price-discrepancies-manually) or [automatically](#handling-price-discrepancies-automatically), depending on your organization's general approach to document matching. The way it's handled differs considerably between these two methods.

### Handling price discrepancies manually

If your organization generally matches documents manually, follow these steps to manually handle price discrepancies in the matching process:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the **PURCHASE** code to open the document journal.
1. In the document list, select the document (invoice or credit memo) that you want to match against other documents.
1. On the action bar, click **Process** > **Match Lines**.
1. In the **Match Overview**, a number of relevant lines from potentially related documents are listed in two overall line sections, depending on what type of document you selected in step 3 above. In one of these sections, select the document line that you want to manually edit.
1. In the **Direct Unit Cost (Invoice)** field (or, if you selected a credit memo in step 3, in the **Direct Unit Cost (Credit Memo)** field), enter the correct price per delivered item for the selected line. This is typically the price of the relevant line in the invoice or credit memo that you selected in step 3.
1. In the **Line Discount %** field, enter the correct line discount percentage, if necessary.

   > [!NOTE]
   > The **Line Discount %** field may have to be added first in order to be visible. To do this, [personalize the page](https://docs.microsoft.com/en-us/dynamics365/business-central/ui-personalization-user) as follows: Select the {{settings}} icon > **Personalize** > **+ Field** to open the **Add Field to Page** pane, select the relevant line section, and then drag the **Line Discount %** field from the pane to the table in the selected line section. Select **Done** to close the **Personalizing** banner.

1. Repeat steps 5-7 for any other relevant lines in that line section and/or in the other section.

When you've completed the matching process, you can navigate back to the document journal to register or otherwise process the matched document.

> [!TIP]
> For general information on manual matching, see [Manual Document Matching](@DC-62).

### Handling price discrepancies automatically

If your organization generally matches documents automatically, Document Capture will automatically manage price discrepancies in one of the following ways, depending on whether or not line matching has been enabled in the setup:

[**If line matching has been enabled**](@DC-69), Document Capture will use the unit cost from the recognized invoice or credit memo line. If you've set the **Line Matching** setup option **Match Unit Cost** to either **Yes - always** or **Yes - if present**, the unit cost of the invoice/credit memo line and the unit cost of the related document line must equal each other – if not, the document lines can't be matched automatically. However, you can specify a variance amount or percentage in the setup, which allows the two unit costs to differ from each other within the specified variance.

**If header matching is used and a variance has been defined in the setup**, Document Capture will add a newly created variance line to the invoice or credit memo, provided that the discrepancy between the total amount of the invoice/credit memo and that of the matching document is within the defined variance. The variance line will be given an amount that's equivalent to the difference between the total of the invoice/credit memo and the sum of the lines from the document that's been identified as a match. When the variance line is included, the document totals will match exactly as they should. 

> [!NOTE]
> If header matching is used and *no variance has been defined in the setup*, Document Capture will simply be unable to handle the price discrepancy, and the match will therefore be unsuccessful.

> [!TIP]
> For more information on automatic matching, see [Automatic Document Matching](@DC-70).

## Related information

[Filtering Line Matches](@DC-64)  