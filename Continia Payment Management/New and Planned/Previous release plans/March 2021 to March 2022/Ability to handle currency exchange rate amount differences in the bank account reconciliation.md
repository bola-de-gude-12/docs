---
title: Ability to handle currency exchange rate amount differences in the bank account reconciliation
description: Ability to handle currency exchange rate amount differences in the bank account reconciliation
date: 28-02-2021
id: PM-27
lang: en
---

#Ability to handle currency exchange rate amount differences in the bank account reconciliation

| Feature | General availability on-premises | General availability online | Public preview |
| --- | :-: | :-: | :-: |
| Ability to handle currency exchange rate amount differences in the bank account reconciliation | {{checkmark}} Mar 1, 2021 | {{checkmark}} Apr 1, 2021 | {{checkmark}} Oct 1, 2020 |

## Business value

When sending payments to the bank for execution in other currencies than LCY, it will be likely to encounter differences in the currency exchange rate that is used in the system versus the one used by the bank. This will be expressed in the bank account statement line that we receive from the bank. This will only occur on bank accounts that are using “blank currency code” (LCY) as those are the only ones where the payment on the bank account can be in another currency than the one on the bank account itself. Otherwise if it is a USD account there can only be USD entries on the account (Dynamics 365 Business Central limitation).

## Feature details

Differences due to currency exchange rate changes should be handled as seamlessly as possible. Automatic creation of general journal lines “taking care” of the difference in exchange rates, between the time the payment is sent to the bank and the time bank is actually transferring the money, will be created. This is applicable for banks using the Local currency (LCY) of the company.

When the bank account statement is received in the system, Statement Intelligence should be able to find the correct bank account ledger entry using the Transaction ID, and if there is a difference in amounts, then that difference will be an expression of the difference in exchange rates used in the system versus the one used by the bank. The difference will be created in a general journal line and after posting, the new bank ledger entry will be marked for reconciliation as well as the original one thus negating the difference.