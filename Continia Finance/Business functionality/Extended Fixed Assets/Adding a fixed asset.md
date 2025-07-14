---
title: Using Continia Finance fields on Fixed Assets
date: 27-05-2024
description: Learn how to create and use Fixed Assets.
id: CF-110
lang: en
---

# Adding a Fixed Asset

Continia Finance allows you to use [asset templates](@CF-86) within the Fixed Assets Template Card to speed up the creation of new assets. These templates streamline asset creation and management by standardizing fields, depreciation books, and inventory settings. They offer a consistent framework, saving time and ensuring uniformity when handling assets.

To use the Continia Finance fields on a Fixed Asset card:

1. Use the {{search}} icon, enter Fixed Assets, and select the related link. 
2. On the action bar, select **New**.
3. On the **Fixed Asset card**, fill in the fields on the **General** FastTab as necessary and find the following Continia Finance fields:
   * **Maintain Quantity** - lets you specify quantities for your assets. When enabled, the FA Depreciation Book will display the remaining quantity for the respective depreciation book.
   * **Quantity** - this field indicates the quantity associated with the asset, if applicable.
   * **Inserted by FA Template** - indicates whether the asset was created using an asset template. 
   * **Last Date Modified** - specifies the date when the fixed asset card was last modified.

To enter acquisitions with quantities, you can use the following pages:

* FA Journals
* Purchase Invoices

The result is shown in the FA Depreciation Books as well as in the FA entries.

The quantity is printed in the following reports:

* Inventory Sheet Report
* Assets – History
