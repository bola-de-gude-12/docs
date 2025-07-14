---
title: Overview of order and receipt matching in Document Capture
date: 29-10-2024
description: An outline of the basics of document matching, including a number of links to other matching articles.
id: DC-61
lang: en
---

# Overview of Order and Receipt Matching

By comparing documents and ensuring consistency between them, document matching enables you to control that you, for example, don't pay for more than you received or that you don't ship more goods than agreed. With Continia Document Capture, you can match incoming invoices and credit memos against related documents such as purchase orders and receipts, and you can either do this manually yourself or let Document Capture handle it automatically.

While the manual procedure requires no setup at all, automatic matching must be enabled and configured according to your specific needs and wants. To do this, see [Setting up Order and Receipt Matching](@DC-60).

> [!NOTE]
> Matching is available in the **PURCHASE** category, which allows the following types of documents to be matched against each other:
> * Purchase invoices can be matched against purchase orders, purchase receipts, or both.
> * Purchase credit memos can be matched against return orders, return shipments, or both.
> 
> Additionally, it's possible to match against purchase receipts and return shipments with tracking – though order lines and return order lines with tracking aren't supported.

For a match to be successful, the documents that are matched against each other must generally have the **same currency**, and the **vendor numbers must be identical**. However, there are two notable exceptions to this general rule:

* If the currency code of an incoming document is the same as the company currency code (**LCY**) and the matching document has no currency code at all, it will be accepted as a match despite the currency mismatch. For example, if an invoice is in euros and its corresponding order has no currency specified, the two documents can be successfully matched if the company currency is also euros.
* If, for example, you're invoiced by a branch with a vendor number that's different from the number of the branch you placed the order with, the invoice and the order can be successfully matched despite this mismatch, provided that you've entered both vendor numbers on the vendor card. The number of the vendor that you buy from is specified on the **General** FastTab, under **No.**, whereas you can enter the number of the vendor that you pay to on the **Invoicing** FastTab, under **Pay-to Vendor No.**

Note that any order that's partially matched with an invoice will be locked until the invoice has been posted, meaning that you can't directly receive or invoice any additional goods or services on that order until the matched invoice has been posted. The same principle applies to credit memos, but with return orders instead of orders. This limitation was implemented as a security measure, to ensure that the order (or return order) isn't suddenly posted in full, leaving its originally matched invoice (or credit memo) incapable of being posted.

For more information on various practical aspects of document matching, check out the useful links provided in the table below:

<br>

| To | See |
| --- | --- |
| Match documents manually | [Manual Document Matching](@DC-62) |
| Have documents matched automatically, including line matching | [Automatic Document Matching](@DC-70) |
| Partially match documents and manage price and quantity discrepancies in general | [Handling Discrepancies, Including Partial Matching](@DC-63) |
| Filter the lists of line matches according to different criteria | [Filtering Line Matches](@DC-64) |

## Related information

[Setting up Order and Receipt Matching](@DC-60)  