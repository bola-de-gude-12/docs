---
title: Bankdata and Payment Management
description: PM integration with the bank system Bankdata.
date: 13-03-2025
id: PM-117
lang: en
---

# Bankdata

[Bankdata](https://www.bankdata.dk/) provides IT services to eight Danish banks. Payment Management uses the bank system Bank Connect to send bank data between Bankdata and Microsoft Dynamics 365 Business Central. You can set up your bank accounts using direct or manual communication. 

This article lists the file format requirements for both communication methods. 

To learn more about how to set up communication:

* Direct communication Bankdata - refer to the [Onboarding Bank Connect Banks with Direct Communication](@PM-179) article.
* Manual communication Bankdata- refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article. 



## File formats

How to integrate your bank with Payment Management depends on the bank communication types and files your bank supports. The table below displays what is supported for direct and manual communication with Bankdata.

| Bank communication | Send payments| Import status| Update status| Import payments| Reconcile|
| --- | --- | --- | --- | --- | --- |
| Direct | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal") | [PAIN.002](@PM-123#PAIN.002 "Import status in the payment journal") | [CAMT.052](@PM-123#CAMT.052 "Update status in the payment journal") | [CAMT.054C](@PM-123#CAMT.054C "Import customer payments in the cash receipts journal") | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments") |
| Manual | [BDF](@PM-123#BDF "Send payments to your bank from the payment journal") | <p style="text-align: center;">{{cross}}</p> | <p style="text-align: center;">{{cross}}</p> | [CAMT.054C](@PM-123#CAMT.054C "Import customer payments in the cash receipts journal")<br />[PBS Sector](@PM-123#PBS "Import NETS PBS FIK DK customer payments in the cash receipts journal.") | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments")<br />[BD-V3](@PM-123#BD-V3 "Reconcile bank statements and import payments.") |



## Related information

[About direct and manual bank communication](@PM-158)
