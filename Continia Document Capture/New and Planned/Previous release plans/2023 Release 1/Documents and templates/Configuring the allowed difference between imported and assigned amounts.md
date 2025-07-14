---
title: Configuring the Allowed Difference Between Imported and Assigned Amounts
date: 28-11-2024
description:
id: DC-295
lang: en
---

# Configuring the Allowed Difference Between Imported and Assigned Amounts

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Configuring the allowed difference between imported and assigned amounts | {{checkmark}} Mar 2023 | {{checkmark}} Apr 2023 |

## Business value

Until now, it's only been possible to specify the allowed difference between imported and assigned amounts using the standard Microsoft Dynamics 365 Business Central fields **Invoice Rounding Precision**, **Inv. Rounding Precision (LCY)**, and **Max. VAT Difference Allowed**. However, seeing that these fields may occasionally conflict with each other when used for this purpose, this feature will introduce two dedicated Continia Document Capture fields that enable you to specify the allowed difference between imported and assigned amounts without the risk of conflict.

## Feature details

For various reasons, minor differences between imported and assigned amounts in purchase documents are often acceptable and sometimes even necessary. You'll now be able to have such differences validated by Document Capture using the following two new fields that will be added to the **General Ledger Setup** and **Currencies** pages:

* **Max. Allowed Diff. Excl. VAT**
* **Max. Allowed Diff. Incl. VAT**

Values specified in the **General Ledger Setup** will apply to amounts registered in LCY (empty currency code), while values specified in the **Currencies** table will apply to amounts in various foreign currencies.

> [!NOTE]
> The feature will only be available in app-based versions of Document Capture.
