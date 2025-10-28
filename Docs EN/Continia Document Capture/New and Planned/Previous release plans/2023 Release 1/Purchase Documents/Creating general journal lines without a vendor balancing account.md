---
title: Creating General Journal Lines Without a Vendor Balancing Account
date: 29-11-2024
description:
id: DC-339
lang: en
---

# Creating General Journal Lines Without a Vendor Balancing Account

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Creating general journal lines without a vendor balancing account | {{checkmark}} Mar 2023 | {{checkmark}} Apr 2023 |

## Business value
This feature provides you with the added flexibility of being able to select other balancing accounts than the default vendor account. This is particularly useful for relatively small purchases and petty cash transactions.

## Feature details
When you register documents whose template has the setting **Create Journal Lines** (under **Invoice Reg. Step 1**), the balancing account that's used for the lines created in the general journal has so far always been the vendor account. With the implementation of this feature, it will now be possible to select either a G/L account or a bank account instead when general journal lines are created upon document registration.

The template header fields **Bal. Account Type** and **Bal. Account No.** will be made avalaible for users to fill out. If these fields are left empty, the vendor account will still be used by default.