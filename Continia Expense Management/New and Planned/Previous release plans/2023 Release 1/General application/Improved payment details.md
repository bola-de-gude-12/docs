---
title: Expense Management Improved Payment Details for Expenses in Payment Management
date: 27-03-2023
description:  
id: EM-129
lang: en
---

# Improved Payment Details for Expenses in Payment Management

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| Improved payment details for expenses in Payment Management | {{checkmark}} Mar 2023 | {{checkmark}} Apr 2023 |

## Business value
More accurate information about expenses will be available to Payment Management users when processing expenses in Payment Management.

## Feature details
Expense Management will send the IDs of all the individual sub-documents (expense reports, expenses, mileage expenses and per diem expenses) that are being processed to Payment Management so that the user can see which expense documents have been reimbursed on their bank account.

When this new feature is enabled, Expense Management identifies expense documents in the Payment Journal and delivers additional information to Payment Management.

The functionality can be enabled in Payment Management by ticking "Enable Payment Management Event" in Notification Setup and is only available for the latest versions of Business Central, starting with Business Central 2020.

With this functionality, a new extension app will be installed: Continia Core Connectivity.

Note that you need to have both Expense Management and Payment Management installed (as well as active subscriptions) for this functionality to work.