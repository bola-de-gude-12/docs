---
title: Using Extended Application Features
date: 04-09-2024
description: Learn how to use dimensions on system entries.
id: CF-32
lang: en
---

# Using Extended Application Features

As you start handling a larger volume of sales and purchase documents, navigating the apply entries pages in Business Central can become challenging. The Extended Applications feature in the Continia Finance Essential module provides a robust set of tools designed to streamline and expedite the process of managing open entries.

## Prerequisites

Enable **Use Extended Application** on the **Continia Finance Setup** page in the **Extended Application** FastTab.

Optional: Enable **Use Ledger Entry Comments** on the **Continia Finance Setup** page in the **General** FastTab.

## Extended application features

With **Use Extended Application** enabled, You get the added functionality of the **Applies-to ID** column, where you can apply-ID with a single click for each line instead of having to select each line and then use the **Set Applies-to ID** action from the **Home** menu.

Additionally, pages for applying entries, such as in the cash receipt journals, gain coloring of details:

   |         Description            | Fields                                                  |
   | ------------------------ | ------------------------------------------------------------ |
| Applied entry lines are displayed with bold green text | <ul><li>Applies-to ID</li><li>Posting Date</li><li>Document Type and Document Number</li><li>Description</li><li>Due date</li></ul> |
| Lines which have been applied to a different ID are displayed in bold italic red text | <ul><li>Applies-to ID</li><li>Posting Date</li><li>Document Type and Document Number</li><li>Description</li><li>Due date</li></ul> |

This is especially useful when multiple Business Central users could be apply entries for the same customer or vendor. It’s possible to overwrite the content of the Applies-to ID field if needed.


## To apply entries with partial payments and residual balances

With Extended Applications, you can enter a partial payment amount in the **Amount to Apply** field, the extra field **Open Amount** displays the remaining amount in bold italic red text.

If you've enabled **Use Ledger Entry Comments**, you can enter a comment in the **Entry Comment** column to explain the reason for the partial payment, if needed.

After posting an applied partial payment, the remaining amount for the entry line is displayed in bold blue coloring in the **Application Remaining Amount** column in future applied entries.

## To handle balance in application

The Extended Application feature includes setup options for **Balance in Application** instead of keeping the payment open for the remaining amount. 

The option at **Action if Balance in Application < > 0** has two choices:

* New line, which always creates an additional line for the balance
* Options, which opens a dialog box whenever the applied payment doesn’t match the remaining amount

If you choose **Options**, you can further select the default option from the choices:

* Create a new line
* Keep payment as open
* Post as payment discount
* Create new G/L line

When you next post a partial payment, a dialog box appears where you can choose between the above-mentioned options.







<style>

 .content table tr td:nth-child(1) {

 width: 200px;

 }

 .content table tr td:nth-child(2) {

 width: 600px;

 }

</style>
