---
title: Purchase contracts for the United States
date: 04-09-2024
description:  
id: DC-192
lang: en
---

# Purchase Contracts for the United States

The Purchase Contracts module supports tax calculation in the United States. To provide you with more accurate tax calculations, a number of fields have been added to the **Purchase Contract** page.

On the **General** FastTab, the following fields have been added:

| Field | Description |
| --- | --- |
| **Tax Liable** | Specifies at header level if the vendor that's selected for the contract is liable for sales tax. |
| **Tax Area Code** | Specifies at header level what tax area is used for calculating and posting sales tax. |

On the **Lines** FastTab, the following fields have been added:

| Field | Description |
| --- | --- |
| **Tax Liable** | Specifies at line level if the vendor that's selected for the contract is liable for sales tax. |
| **Tax Area Code** | Specifies at line level what tax area is used for calculating and posting sales tax. |
| **Tax Group Code** | Specifies the tax group that's used for calculating and posting sales tax. |

From the **Purchase Contract** page, you can also access the **Purchase Contracts Statistics** page, which provides a tax breakdown of the selected purchase contract by tax area, tax group, and tax jurisdiction. From here, you can even define tax amounts manually – and these are then distributed among the purchase contract lines.

Any taxes defined like this from the Purchase Contracts module are considered when you register documents in the document journal.

## Related information

[Overview of Purchase Contracts](@DC-85)  






<style>
  .content table tr td:nth-child(1) {
    width: 130px;
  }
  .content table tr td:nth-child(2) {
    width: 600px;
  }  
</style>