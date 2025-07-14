---
title: Understanding priority and inheritance of dimensions in Expense Management
date: 14-05-2025
description: Learn how dimensions are prioritized and inherited
id: EM-318
lang: en
---
# Understanding priority and inheritance of dimensions in Expense Management

Expense Management uses inheritance and priority of dimensions on different document types. Refer to the following tables to better understand the priority of dimensions and allocations for Expenses, Mileage, and Per diems. The dimension types are listed from the highest priority (P1) to the lowest priority.

## Expenses dimension types and priorities

Expenses have the following dimension types, listed in order of priority from highest (P1) to lowest (P5).

| <span style="white-space: nowrap;">Priority</span> | Description |
| --- | --- |
| P1 | A Job has the highest priority. It is higher than an Expense Type |
| P2 | An Expense Type has priority over a G/L  Account |
| P3 | A G/L Account has priority over a Vendor |
| P4 | A Vendor has priority over a Salesperson/Purchaser |
| P5 | An Account Salesperson/Purchaser has the lowest priority |

## Allocations

An allocation inherits its dimensions from the expense.

## Mileage dimension types and priorities

Mileage has the following dimension types, listed in order of priority from highest (P1) to lowest (P4).

| <span style="white-space: nowrap;">Priority</span> | Description |
| --- | --- |
| P1 | A Job has the highest priority. It is higher than a G/L Account |
| P2 | A G/L Account has priority over a Vendor |
| P3 | A Vendor has priority over a Salesperson/Purchaser |
| P4 | A Salesperson/Purchaser has the lowest priority |

## Per diem dimension types and priorities

Per diems have the following dimension types, listed in order of priority from highest (P1) to lowest (P3). 

> [!NOTE]
 > Per diems do not inherit their dimensions from Accommodation and Meals posting type G/L accounts.

| <span style="white-space: nowrap;">Priority</span> | Description |
| --- | --- |
| P1 | A Job has the highest priority. It is higher than a Vendor |
| P2 | A Vendor has priority over a Salesperson/Purchaser |
| P3 | A Salesperson/Purchaser has the lowest priority |

## Expense report dimension types and priorities

Manually setting a dimension on an Expense report does not affect its underlying documents. Expenses, Mileage, and Per diems on the settlement do not inherit dimensions from the Expense report header.

> [!NOTE]
 > Expense reports are not linked to a posting type and therefore do not inherit from any G/L accounts.

Expense reports have the following dimension types, listed in order of priority from highest (P1) to lowest (P3). 

| <span style="white-space: nowrap;">Priority</span> | Description |
| --- | --- |
| P1 | A Job has the highest priority. It is higher than a G/L Vendor |
| P2 | A Vendor has priority over a Salesperson/Purchaser |
| P3 | A Salesperson/Purchaser has the lowest priority |

## Related information

[Setting up expense types](@EM-41)

[Setting up company policies for expenses](@EM-39)

[Setting up company policies for mileages](@EM-40)

