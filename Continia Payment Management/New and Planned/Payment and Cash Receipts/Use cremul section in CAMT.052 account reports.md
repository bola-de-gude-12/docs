---
title: Use Cremul section in CAMT.052 account reports
description: Improving the use of CAMT files in the Payment Management solution
date: 30-09-2022
id: PM-264
lang: en
---

# Use Cremul Section in CAMT.052 Account Reports

| Feature | General availability online | Public preview |
| --- | :-: | :-: |
| Use Cremul section in CAMT.052 account reports | - | - |

> [!IMPORTANT]
>
> The development of this feature is postponed. We are currently investigating whether the development of this feature will be rescheduled for a future version of Payment Management.

## Business value

Improving the use of CAMT files is an ongoing process in the Payment Management solution. As banks provide more information, and at an increasing frequency, it's vital that companies have updated financial data in Business Central. Continia aims to improve and supporting these banks and give our customers updated data as soon as possible.

## Feature details

Many banks offer the CAMT.052 account report – a type of bank statement that can be retrieved one or several times a day. Today, this file is processed by Payment Management solely for updating the status of lines in the payout journal (debits), although this file also contains detailed information on deposits (credits) to the account. With this feature update, we'll make use of the Cremul (credits) section as well, utilizing the possibility of much earlier and frequent updates of, for example, customer payments in the cash receipt journal.