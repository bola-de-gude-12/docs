---
title: Dimension Alignment for Payment Discounts
date: 09-01-2025
description: With this feature, Continia Finance can be set up to align dimensions for payment discounts, enhancing financial tracking
id: CF-136
lang: en
---

# Dimension Alignment for Payment Discounts

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Dimension alignment for payment discounts | - | {{checkmark}} Nov 2024 |



## Business value

This new feature ensures that businesses maintaining compliance with tax regulations, such as those in Germany, can align their financial reporting processes more effectively. By enabling payment discount entries to inherit dimensions from related sales or purchase entries, companies can ensure consistent and accurate financial data. This alignment simplifies reporting, improves data integrity, and enhances decision-making based on precise dimensions in payment discount scenarios.

## Feature details

With this functionality, if a payment discount is granted with tax correction (as, for example, in Germany), the payment discount entries will automatically inherit the same dimensions as the corresponding sales or purchase entries. This alignment ensures that dimension-based financial tracking and reporting remain consistent, even when discounts are applied.

The functionality is controlled by two fields:

1. **Adjust for Payment Disc.** (General Ledger setup): When activated, the system recalculates tax amounts during payment posting if payment discounts are triggered.
2. **Use Invoice Dimensions for Pmt. Discount** (Essentials setup): When enabled, the dimensions of payment discount entries will match the dimensions of the paid invoices.
