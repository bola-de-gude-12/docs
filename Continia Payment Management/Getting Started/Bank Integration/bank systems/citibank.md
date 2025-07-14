---
title: Citibank and Payment Management
description: PM integration with the bank system CITI Bank
date: 16-09-2022
id: PM-132
lang: en
---

# Citibank

With Payment Management, you can use manual communication to send bank data between Citibank and Microsoft Dynamics 365 Business Central. 

This article lists the file format requirements for the manual communication method. To learn more about how to set up manual communication for Citibank, refer to the [Setting up bank accounts](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article.



## File formats

This table displays the features supported for Citibank, and the files you must order to use manual communication.

| Bank communication | Send payments| Import status | Update status | Import payments| Reconcile|
| --- | --- | --- | --- | --- | --- |
| Manual | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal") | <p style="text-align: center;">{{cross}}</p> | <p style="text-align: center;">{{cross}}</p> | [CAMT.054C](@PM-123#CAMT.054C "Import customer payments in the cash receipts journal") | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments") |

