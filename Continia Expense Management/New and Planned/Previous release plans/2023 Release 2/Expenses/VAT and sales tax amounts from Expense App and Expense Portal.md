---
title: VAT and Sales Tax Amounts from Expense App and Expense Portal
date: 02-06-2023
description:  
lang: en
---

# VAT and Sales Tax Amounts from Expense App and Expense Portal

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| VAT and sales tax amounts from Expense App and Expense Portal | - | Oct 2023 |

## Business value

For each expense submitted by a user in an organization, the actual VAT/sales tax amount that's applied to the purchase may differ from the standard VAT/sales tax which has been set up in Microsoft Dynamics 365 Business Central. With this feature, the bookkeeper that receives and processes the submitted expense will receive the actually applied VAT/sales tax amounts from the Continia Expense App or the Continia Expense Portal. The bookkeeper will then be able to use these details to post VAT differences or to double-check and correct the posting setup.

## Feature details

When a user submits an expense using either the Expense App or the Expense Portal, the bookkeeper that receives the expense currently doesn't get any accompanying VAT/sales tax details with the expense. The VAT/sales tax from the posting setup is simply applied to the total expense amount in Business Central by default.

With this new feature, the Expense App and the Expense Portal will be able to provide the actual VAT/sales tax amounts with the submitted expenses, thereby alerting bookkeepers to any potential differences from the posting setup, so they can double-check the setup or even post the differences. The feature will be closely linked to the AI Receipt Scanner recognition functionality, which means that users don’t have to enter any such details manually.