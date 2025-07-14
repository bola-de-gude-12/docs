---
title: Handelsbanken Netbank Erhverv
description: Integration with the bank system Handelsbanken Netbank Erhverv
date: 07-06-2021
id: 
lang: en
---

# Handelsbanken Netbank Erhverv

{{include "pm-bank-card-introduction"}} 

| Bank communication   | Bank service                           | Countries | Bank system code |
| -------------------- | -------------------------------------- | --------- | ---------------- |
| Direct communication | Netbank Erhverv via Bank Connect (BEC) | DK        | BEC20022         |
| Manual communication | Netbank Erhverv via BEC                | DK        | BEC01            |

{{include "pm-bank-card-file-formats"}}

| Bank communication   | Send payments                                                | Import status                                                | Update status                                                | Import payments                                              | Reconcile                                                    |
| -------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Direct communication | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal") | [PAIN.002](@PM-123#PAIN.002 "Import status in the payment journal") | [CAMT.052](@PM-123#CAMT.052 "Update status in the payment journal") | [CAMT.054C](@PM-123#CAMT.054C "Import customer payments in the cash receipts journal") | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments") |
| Manual communication | [ERH](@PM-123#ERH "Send payments to your bank from the payment journal") | Not supported                                                | Not supported                                                | [PBS Sector](@PM-123#PBS "Import NETS PBS FIK DK customer payments in the cash receipts journal.") | [EKP format](@PM-123#EKP "Reconcile bank statements and import payments.") |

