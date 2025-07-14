---
title: BEC
description: Integration with the bank system BEC
date: 07-06-2021
id: 
lang: en
---

# BEC

BEC provides IT services to smaller and larger financial companies such as Danish banks, foreign banks in Denmark and other institutions in the Danish financial sector. You can find an overview of the banks and institutions using the services of BEC [here](https://www.bec.dk/en/becs-customers/).



{{include "pm-bank-card-introduction"}}

| Bank communication | Bank service | Countries | Bank system code |
| --- | --- | --- | --- |
| Direct communication | BEC | DK | BEC20022 |
| Manual communication | BEC | DK | BEC01 |



{{include "pm-bank-card-file-formats"}}

| Bank communication | Send payments| Import status| Update status| Import payments| Reconcile|
| --- | --- | --- | --- | --- | --- |
| Direct communication | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal") | [PAIN.002](@PM-123#PAIN.002 "Import status in the payment journal") | [CAMT.052](@PM-123#CAMT.052 "Update status in the payment journal") | [CAMT.054](@PM-123#CAMT.054 "Import customer payments in the cash receipts journal") | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments") |
| Manual communication | [ERH](@PM-123#ERH "Send payments to your bank from the payment journal") | Not supported | Not supported | [PBS Sector](@PM-123#PBS "Import NETS PBS FIK DK customer payments in the cash receipts journal.") | [EKP format](@PM-123#EKP "Reconcile bank statements and import payments.")|

## Onboarding BEC with direct communication

To use the functionality of direct communication the service must be enabled from the assisted bank account setup, for more information see [Setting up Direct Communication](@PM-42). For detailed information and guidance about signing up to BEC with direct communication using Bank Connect, see the article [Onboarding Bank Connect Banks](@PM-179).

